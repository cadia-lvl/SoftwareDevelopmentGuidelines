Packaging / Releasing (Haukur)
When a project should be released it should be packaged so that it can be easily used by the intended user. The packaging depends on the deliverable type.
[Add translation from SÍM deliverables]
[start complaining about storage location, maybe use cadia ftp]
[github large file storage]
UI: compiled and optimized executable
Library: According to language convention
Terminal client: Same as library
Model: Model parameters and other necessary files as well as a reference to the git label where the model can be run.
Each release needs to have a git tag, so that the artifact can be recreated if need be. The label can be a version number, date or another meaningful reference. [explain how this works with semantic versioning]
When releasing an artifact, be sure that all changes have been committed and a proper README file is in place so that the release process can be repeated by someone else.
For more complex deliverables (which have many dependencies) we also recommend packaging the deliverable using docker.
