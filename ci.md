CI (Sunneva)
When working on a project with others and preferably while working alone, a CI/CD system should be used to help the team collaborate. 
CI stands for continuous integration and CI systems help to automate tests and keep our code base clean
CD stands for Continuous delivery and Continuous deployment. That helps automate the delivery/deployment process by running our code through pipelines to prepare it for deployment.


We use both Github Actions and Gitlab CI as CI/CD systems
Easy to get started by adding the CI to the version control system we already use
Both CI systems support Docker 
Can both be hosted in the cloud so our devices don’t get clogged with tests and builds
GitLab CI is already built into the core design of Gitlab so easy to get started
Getting started guide: https://docs.gitlab.com/ee/ci/quick_start/
More general information about GitLab CI: https://docs.gitlab.com/ee/ci/ 

Github Actions can be added directly to your repository.
Language and framework guidelines: https://help.github.com/en/actions/language-and-framework-guides 
Packaging: https://help.github.com/en/actions/publishing-packages-with-github-actions/about-packaging-with-github-actions 
TO DO: 
[Explain better what a CI system does, building, etc.]
[We only use Github Actions]
