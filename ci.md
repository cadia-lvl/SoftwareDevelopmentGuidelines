# CI

When **working on a project with others** and preferably while working alone, a **CI system should be used**.
- CI stands for continuous integration and CI.
- **CI systems build software, run tests and alerts developers when a test doesn't pass**. This way developers can fix mistakes right away while they are still fresh in their memory. This also helps to avoid larger, more time consuming conflicts and gives developers more confidance in their code.
- CD is often used with CI and stands for Continuous Delivery and/or Continuous Deployment. That helps automate the delivery/deployment process by running code through pipelines to prepare it for deployment.

**The CI system we use is Github Actions**
- Easy to get started by adding the CI to Github.
- Includes Docker support
- Is free for open repositories
- Possible to use actions from others
  * Azure and AWS for examplea
- Tests can run on Github owned servers
  * This spares our computers from hosting everything 

### Further information:
- [Core concepts](https://help.github.com/en/actions/getting-started-with-github-actions/core-concepts-for-github-actions)
- [Language and framework guideline](https://help.github.com/en/actions/language-and-framework-guides) 
- [Triggering workflows](https://help.github.com/en/actions/reference/events-that-trigger-workflows)
- [Packaging](https://help.github.com/en/actions/publishing-packages-with-github-actions/about-packaging-with-github-actions) (optional)

