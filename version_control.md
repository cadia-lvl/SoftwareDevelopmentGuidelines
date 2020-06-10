Version control (required) (Olli)

Semantic versioning
v[major].[minor].[patch]
Major: When you make incompatible API changes, when you break something
Minor: When you add backwards compatible functionality, when you add features
Patch: When you make backwards compatible fixes, when you fix bugs

Further reading about semantic versioning: https://semver.org/

Git
Using git for version control is required. Github vs Gitlab requirement?

Workflow
The master branch should always contain production ready code.
All merges to the master branch should include semantic version tags.
For smaller projects and teams, feature branching is sufficient, where each feature gets a branch, created from master, used while developing until it is merged into the master.
For larger projects and teams, Gitflow is the recommended workflow. It has two main branches, the master branch that stores release history and a development branch that lives between the master branch and feature branches. It also recommends a clear way to implement hotfixes.
[descriptive comments about code]...
[more motivation about why we do this]...
[how to use tags and apply semantic versioning and descriptive comments]

Pull requests
When adding new features or updates to the master branch, developers should write a pull request and let at least one other team member review their code before merging.
Code reviews across projects are recommended but not required. Keeping more team members informed about your work can benefit everybody.
