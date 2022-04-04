---
category: Guides
type: Development and Architecture
subtype: Standards
icon: fas fa-building fa-2x
description: Development standards and governance
order: 1000
---

# Development standards

Development, in any language or framework combination, will be working on use cases, usually recorded with Gherkin like statemetns in an issue managemtn system, agreed with and by the Analysis and Design phases and that have passed the Definition of Ready (DoR), are completed to the prevailing best practices to a Defintiion of Done (DoD).


The team will usually decide on which source code workflow to be adhered to but assume a default of `trunk-based-workflow` unless your issue is long running  in which case  `Gitflow` approach may be adopted. Either way your team will decide on its own ways fo working. Some sort of branching flow will be adopted.

All `Must` and as many `Should` status criteria will be fulfilled as possible.

## Definition of Ready (DoR)

Agreed minima (within the team) for a use case / issue to be ready for developers to commence sub-tasking and proceed to work.

### Example Definition of Ready (DoR)


| Status | Definition | 
|--------|-------------|
| Must    | Describe bug with expected behaviour, actual behaviour and means/process to replicate. |
| Must    | Describe feature as  Given-when-then |
| Must    | Describe issue as Given-when-then |
| Must    | Define acceptance criterion |
| Should  | Define input and output values |


## Defintion of done (DoD)

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
| Must | Code is manually tested locally  |
| Must | Code cold-setup instructions are reviewed and adjusted accordingly  |
| Must | Code is pushed to branch and a Pull request generated nominating reviewers  |
| Must | Code is peer reviewed  |
| Must | Code is modified according to peer review comments  |
| Must | Code peer review passes/ is accepted  |
| Must | Issue branch is merged, and deployed to automated testing  |
| Should | The Issue management system item is advanced to `in test` [^1] |


## Best pracices 

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


# Why do we do this?

The practices above are for the benefit of the team as a whole. And show that the developer is thinking of the team outcome not just in solving the immediate programming problem. It shows that the problem has been well produced in a way that does not disrupt other developers or testers, is of acceptable quality, is testable and is tested, is ready for others to spend time on, and is fit for purpose.

# Footnotes

[^1]: may be automated

[^2]: Some clients may insist on TDD, some wont. If in doubt, do it.

[^3]: if you are taken ill or other mishap there is a copy to continue with, by yourself or by others.
