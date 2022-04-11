---
category: Publications
type: Blog
icon: fas fa-blog fa-2x
description: Using apickli to contract test
order: 10000
---

# Consumer based contract testing

With the advent of micro services and containerisation (with kubernetes) services are becoming simpler and easier for developers to understand. There are several advantages to a micro-service infrastructure

- Simpler and easier to understand services
- Service outage doesn't necessarily bring down a whole system
- Easier to build, test and deploy

Having these disconnected services performing a system wide requirement creates more challenges for building and deploying.

### A monolithic applicaton

There are pros to a monolithic application

1. Deployed code is usually compiled and functionality within is deployed as a full stack application
2. Simpler to manage in some cases, one app, one deploy

But there are many down sides

1. Complexity and inability for developers to understand the code, and possibly the need to understand everything when changes specific areas of the code
2. Long test and regression cycles
3. Downtime for the whole system under deployment cycles

### Separating the monolith

The figure below shows a simple monolithic application and a representation of separating a specific function into a micro service

![Monolithic application](/assets/publications/consumer based contract testing.drawio.png)

We see that there exists a specific contract between `class A` and `class B` ie one is using the other. In most cases any issue with the contract will be found at compile time, thus a build failure will be rasied and fixed before test and deployment.

When we split this functionality out into `service B` we see that we have now decoupled the contract that was previously made at compile time in the monolith. This presents a problem when deploying `service B`

How do we know that deploying `service B` will not break the contract on `service A`. For example a developer on service B decides to return a 201 instead of a 200 when something is POSTED. All the tests pass so lets deploy?

_**What happens if the consumers code is checking for a status that is no longer returned?**_

> The result will probably be a consumer service that breaks, and many teams running around looking at dashboards trying to see what broke the system.

_**So how can this be mitigated?**_

## Testing the contract

Consumer based contract testing is defined as follows:

_**"Consumer driven contract testing is a type of contract testing that ensures that a provider is compatible with the expectations that the consumer has of it."**_

`If you can replace your whole service for example by changing the language and you do not need to change the contract tests then they are true outside in contract tests`

Examples of other tests that are outside in like

1. Using TestServer on a C# service
2. Node tests (where the service is hosted)

## Advantages

There are many advantages to writing consumer contract tests

1. You are testing the network aspects of the service as well as the code
2. You will reduce the number of unit tests you need to write as the contract tests will cover many aspects end to end
3. The tests are easily understandable by non-technical stakeholders
4. You can change literally anything about the service, e.g. the language. The tests will still pass if the contract is adhered to 

## Requirements

1. It is much easier to run consumer based contract tests using containerisation, e.g. docker. you can use docker-compose or bash scripts to run the service to be tested in a container and then run another container to perform the contract tests
2. Always run the tests against the current branch, NOT that deployed to production as this will not find bugs that are not deployed
3. Set up a standard for any consumer teams to PR their BDD style tests into
4. The BDD style tests should be run as part of the 

## apickli

[Apickli](https://github.com/apickli/apickli) is a REST API integration testing framework based on cucumber.js. It provides a gherkin framework and a collection of utility functions to make API testing easy and less time consuming.

Why is apickli so good?

- You can write BDD style tests against a suit of in build library methods
- No code needed
- Extensions can be built on top of the existing extensions

The main call out here is

> IF you can replace your service with a completely different language without changing your Consumer based contract tests then its an outside in test

The following extensions are supported in apickli

``` 
GIVEN:
    I set (.*) header to (.*)
    	I set cookie to (.*)
	I set body to (.*)
	I pipe contents of file (.*) to body
	I have basic authentication credentials (.*) and (.*)
	I set bearer token
	I have (.+) client TLS configuration
	I set query parameters to (data table with headers |parameter|value|)
	I set headers to (data table with headers |name|value|)
    	I set form parameters to (data table with headers |parameter|value|)

WHEN:
	I GET $resource
	I POST to $resource
	I PUT $resource
	I DELETE $resource
	I PATCH $resource
	I request OPTIONS for $resource

THEN:
	response code should be (\d+)
	response code should not be (\d+)
	response header (.*) should exist
	response header (.*) should not exist
	response header (.*) should be (.*)
	response header (.*) should not be (.*)
	response body should be valid (xml|json)
	response body should contain (.*)
	response body should not contain (.*)
	response body path (.*) should be (.*)
	response body path (.*) should not be (.*)
   	response body path (.*) should be of type array
   	response body path (.*) should be of type array with length (\d+)
   	response body should be valid according to schema file (.*)
   	response body should be valid according to openapi description (.*) in file (.*)
	I store the value of body path (.*) as access token
	I store the value of response header (.*) as (.*) in scenario scope
	I store the value of body path (.*) as (.*) in scenario scope
	value of scenario variable (.*) should be (.*)
	I store the value of response header (.*) as (.*) in global scope
	I store the value of body path (.*) as (.*) in global scope
```

## Implementation

