# Version control

## Why
Within Cadia-LVL, using git for version control is required. A clean repository with descriptive comments makes for a good representation of your project which makes it easier for new developers to join it. The following guidelines describe a way to maintain a project as such.

## Workflow
If a project is public, the master branch should always contain production ready code. All merges to the master branch should include semantic version tags as listed below.

### Branching
* For smaller projects and teams, feature branching is sufficient, where each feature gets a branch, created from master, used while developing until it is merged into the master.

* For larger projects, [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) is the recommended workflow. It includes two main branches, the master branch that stores release history and a development branch that lives between the master branch and feature branches. It also recommends a clear way to implement hotfixes.

### Pull requests
* When adding new features or updates to the master branch, developers should write a pull request and let at least one other team member review their code before merging.

* Code reviews across projects are recommended but not required. Keeping more team members informed about your work can benefit the team as a whole.

### Comments

Every commit message should include a short description of work being commited. Pull request comments should be more detailed. 

## Semantic versioning

Version tags can be informative, especially to current users. Given a version number *v[major].[minor].[patch]*, increments represent the following:
* Major: Incompatible API changes, ***when you break something***
* Minor: Added backwards compatible functionality, ***when you add features***
* Patch: Backwards compatible fixes, ***when you fix bugs***

[Read more about semantic versioning](https://semver.org/)

[How to use tags to apply semantic versioning](https://www.atlassian.com/git/tutorials/inspecting-a-repository/git-tag)
