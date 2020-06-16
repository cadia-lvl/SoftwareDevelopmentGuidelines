## Packaging / Releasing
When a project should be released it should be packaged so that it can be easily used by the intended user. The packaging depends on the deliverable type, see [deliverables.md](deliverables.md).
- UI: Compiled and optimized executable.
- Server: Compiled and optimized executable.
- Library: According to language convention.
- Model: Model files uploaded to CLARIN. Reference to a git label.
- Command line: Compiled and optimized executable.

All deliverables should be provided along with instructions on how to run them and examples.

All deliverables should be referenced with a git tag (f.ex. a version).
This is done so that the code of a deliverable can be easily reviewed and for easy recreation.

When releasing an artifact, be sure that all changes have been committed and a proper README file is in place so that the release process can be repeated by someone else.

For more complex deliverables (which have many dependencies) we also recommend packaging the deliverable using docker.

Packaging should be done after testing and be a part of the CI setup for all projects (excluding models).