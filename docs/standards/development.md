---
category: Guides
type: Development and Architecture
subtype: Standards
icon: fas fa-building fa-2x
description: Development standards and governance
order: 1000
---


# Why do we do this?

The standards and practices below are for the benefit of the team and its combined outcome as a whole. They show that the developer is thinking of and working for the team outcome not just in solving the immediate programming problem. 

It shows that the problem has been solved well, in a way that does not disrupt other developers or testers, is of acceptable quality, is mainatainable, is testable, is tested, is ready for others to spend time on, and is fit for purpose.

# Development standards

The following standards are a condensation of many years of experience in software development gained in small medium and large development teams.

Development, in any language or framework combination, will be working on feature, bug or issue or task `ticket's`, usually recorded with Gherkin like statements in an `issue management system` such as `Jira`.

Tickets are agreed within the Analysis and Design phases, that have passed the accepted `Definition of Ready` (DoR), are completed to the prevailing best practices to the accepted `Defintiion of Done` (DoD).

Code written will be managed with a source code management system, probably `Git`, and the team you work within will usually decide on which source code workflow to be adhered to. 

You may assume a default of `trunk-based-workflow` unless your issue is long running in which case  `Gitflow` approach may be adopted. Either way your team will decide on its own ways of working. Some sort of branching flow will be adopted.

Source code should be commited and pushed often to your working branch with small discrete changes to allow yourself or any other developer to branch or pull from that small change at any time for any reason.

For the `DoR` and `DoD` all `Must` and as many as possible of the `Should` criteria are to be fulfilled.

## DoR - Definition of Ready
Agreed minima (within the team) for a use case / issue to be ready for developers to commence technical analysis, sub-tasking and proceed to work.

### Example DoR

| Status | Definition |
|--------|-------------|
| Must    | Describe bug with expected behaviour, actual behaviour and how it can be replicated. |
| Must    | Describe feature as Given-when-then |
| Must    | Describe issue as Given-when-then |
| Must    | Define acceptance criteria |
| Could   | Define input and output values for testing |

## DoD - Defintion of done

Agreed minima (within the team) for development work to be considered completed and ready to pass to the testing phase.

### Example DoD

All issues run from commencement through iteration to completion.

#### Commencement

| Status | Definition | 
|--------|-------------|
| Must | Code is branched from the development main branch and named accordingly |
| Should | The Issue management system item is advanced to `in development` [^1] |


#### Iteration

| Status | Definition | 
|--------|-------------|
| Must/Should | Code is written via Test driven development [^2] |
| Must | Code is written to SOLID principles |
| Must | Code is secure |
| Must | Code is understandable |
| Must | Code is maintainable |
| Must | Code configuration is not hard coded  |
| Should | Code is cleaned and improved along the way  |
| Should | Tests are re-run for everything regularly |
| Must | Code is commited and pushed regularly (at least once a day [^3] |

#### Completion

| Status | Definition | 
|--------|-------------|
| Must | All code written by you is covered by at least one automated test |
| Must | All automated code tests pass  |
| Must | Code is manually tested locally  |
| Must | Code cold-setup instructions are reviewed and adjusted accordingly  |
| Must | Code is pushed to branch and a Pull request generated nominating reviewers  |
| Must | Code is peer reviewed  |
| Must | Code is modified according to peer review comments  |
| Must | Code peer review passes/ is accepted  |
| Must | Issue branch is merged, and deployed to automated testing  |
| Should | The Issue management system item is advanced to `in test` [^1] |

## Best practices 

These best practices will be guidelines on the subjects (in no order) of;

- Security
- Test driven development
- Clean code
- Maintainability
- Architecture
- The Principles of;
    - SOLID
    - KISS
    - DRY-SHY-Tell the other guy
    - DAMP (testing)
    - YAGNI 
    - and others
- Code management
- Code workflows



# Footnotes

[^1]: may be automated

[^2]: Some clients may insist on TDD, some wont. If in doubt, do it.

[^3]: if you are taken ill or other mishap there is a copy to continue with, by yourself or by others.
