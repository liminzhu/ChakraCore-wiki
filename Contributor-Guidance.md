## Contributing Code

ChakraCore accepts bug fix pull requests. For a bug fix PR to be accepted, it must first have a tracking issue that has been marked approved. Your PR should link to the bug you are fixing. If you've submitted a PR for a bug, please post a comment in the bug to avoid duplication of effort. 

ChakraCore also accepts new feature pull requests. For a feature-level PR to be accepted, it first needs to have design discussion. Design discussion can take one of two forms a) a feature request in the issue tracker that has been marked as approved or b) the PR must be accompanied by a full design spec and this spec is later approved in the open design discussion. Features are evaluated against their complexity, impact on other features, roadmap alignment, and maintainability.

Only contributions against the master branch will be accepted. Authors submitting pull requests that target experimental feature branches or release branches will likely be asked target their pull request at the master branch.

Pull requests that do not merge easily with the tip of the master branch will be declined. The author will be asked to merge with tip and update the pull request.

Pull requests that do not pass all checks by Jenkins will also be declined.

Submissions must meet functional and performance expectations, including scenarios for which the team doesn’t yet have open source tests. This means you may be asked to fix and resubmit your pull request against a new open test case if it fails one of these tests.

Pull requests that reformat the code will not be accepted.

These two blogs posts on contributing code to open source projects are a good reference: Open Source Contribution Etiquette by Miguel de Icaza and Don’t “Push” Your Pull Requests by Ilya Grigorik.

### Legal

You will need to complete a Contributor License Agreement (CLA) before your pull request can be accepted. This agreement testifies that you are granting us permission to use the source code you are submitting, and that this work is being submitted under appropriate license that we can use it.

You can complete the CLA by going through the steps at https://cla.microsoft.com. Once we have received the signed CLA, we'll review the request. You will only need to do this once.

### Housekeeping

Your pull request should:
* Include a description of what your change intends to do
* Be a child commit of a reasonably recent commit in the master branch
* Pass all unit tests
* Have a clear commit message
* Include adequate tests
  * At least one test should fail in the absence of your non-test code changes. If your PR does not match this criteria, please specify why
  * Tests should include reasonable permutations of the target fix/change
  * Include baseline changes with your change

ChakraCore is an organically grown codebase. The consistency of style reflects this. For the most part, the team follows these coding conventions. Contributors should also follow them when making submissions. Otherwise, follow the general coding conventions adhered to in the code surrounding your changes. 

### Running the tests

The unit tests can be run by:
* Choose a build configuration to build and test, e.g. debug and x64.
* Build that config. 
  * Ensure rl.exe is built by building the all configuration or building the rl project directly.

* Call  tools\runtests.cmd  and specify the build config

e.g.  tools\runtests.cmd -x64debug 

For full coverage, please run unit tests against debug and test for both x86 and x64:
* test\runtests.cmd -x64debug 
* test\runtests.cmd -x64test 
* test\runtests.cmd -x86debug 
* test\runtests.cmd -x86test 

# 