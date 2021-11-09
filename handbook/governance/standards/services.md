# Service standards

Service standards encompass a lot of areas, but we shall concentrate on the following
1. Continuous Integration
2. Continuous Deployment
3. Naming
4. Source control templates 
5. Default REST endpoints

# Continuous Integration

Continuous integration is the process of building, testing and packaging the code
and artefacts needed to deploy the service.

![CI process](../../../assets/CI.png)

The CI process can have as many steps as you need, but generally there are 4
main steps, Build, Test, Scan, Create in that order and you will need a source code versioing
platform like github or bitbucket

Each step is run in turn and if the step succeeds the next us run, until the pipeline
is completed. Errors stop the process and stakeholders are alerted to this fact and
can investigate as to why the error occurred.

There are several CI platforms that can be used, in no specific order:
- Azure devops
- Github Actions
- Teamcity
- Jenkins

## The build stage

The build process should run via a standard script called `build.sh` and a non-zero exit code
will mean a failed build. See TBD for the standard file structure for a service.

The build stage is fired via the check-in of code (via either a poll on the code
repository or a webhook). In either event the `build.sh` script will be run.

This stage may actually not do an awful lot for service written in node, as these are compiled 
at runtime, however for netcore the code needs to be compiled (built) before being run specifically

## The test stage

The test process should run via a standard script called `test.sh` and a non-zero exit code
will mean a failed test stage. See TBD for the standard file structure for a service.

The test stage is automatically fired by a successful build stage

This stage will effectively run any tests, be it unit, outside-in, functional or regression tests

# The scan stage

This stage is important for the security of the code you write and the images or artefacts you produce
and there are plenty of tools out in the wild to test and check your code.
Again its good to have a common entry point so this stage should be run by a `scan.sh` script

This stage is required to make sure your code and service are secure from vulnerabilities
in libraries you use, to analysing your code against OWASP standards. 

Here is a list of the tools, again in no specific order, you can look at to secure your code

- **Snyk** is a developer-friendly security platform for anyone responsible for securing code. This includes developers, DevOps, Security, DevSecOps, Compliance, AppSec, and any other team that asks the question, “Is this software safe to put out in the world?”
- **Checkmarx** is an enterprise-grade flexible and accurate static analysis solution used to identify hundreds of security vulnerabilities in custom code.
- **SonarQube** is a Code Quality Assurance tool that collects and analyzes source code, and provides reports for the code quality of your project. It combines static and dynamic analysis tools and enables quality to be measured continually over time
- **Github Dependabot** checks for outdated dependencies as soon as it's enabled. You may see new pull requests for version updates within minutes of adding the configuration file, depending on the number of manifest files for which you configure updates
- **OWASP** Zap is an open-source web application security scanner
- **Anchore** is an open-source tool for scanning and analyzing container images for security vulnerabilities and policy issues
