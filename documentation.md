Documentation (Judy)
All Projects
Code should be self-documenting and when that’s not possible then it should be well documented within comments and overall documentation. In the case of python, documentation can be automatically generated from “docstrings.” Other languages and frameworks have similar features. Use easy to understand variables and function names; avoid ambiguous names. Use consistent styles throughout the whole codebase. The code should also be consistent with the general guidelines of the programming language.
In complex projects, explain the folder structure in the README/document so it’s easier for new developers to get started
Developer documentation should generally be in English. User guides should be in the same language of the users. [what are user guides]
Add research papers to the repository if possible:  e.g. https://github.com/Eyra-is/Eyra/blob/master/Docs/Petursson_et_al_2016.pdf

Documentation for git repositories can live in the docs folder as a website. [explain] GitHub has a step by step guide of how to do that on their platform https://pages.github.com/
Example: https://github.com/cadia-lvl/Eyra

Minimum README template (write in Markdown or rst): Explanation at: https://guides.github.com/features/wikis/
Title
Project description
Table of Contents
Installation
software requirements
dependencies
Contribution guidelines
This can also link to a separate Developer reference
how to contribute
creating issues
(optional) where to get data
(optional) testing
(optional) design strategy
Authors/Credit
(if public grant) Mention the source of the funding and link
Mention RU and the main authors with email
License
Mention which LICENSE the code uses (more examples in the LICENSE section)

You also might want add the following sections in your README:
Changelog (if you have releases)
Tutorial
Description of folder structure
    ex: http://kaldi-asr.org/doc/kaldi_for_dummies.html#kaldi_for_dummies_directories
Papers/References
citation snippet
Ex: http://kaldi-asr.org/doc/about.html#about_reference
API reference 
If lengthy this should be a separate document
APIs
The documentation should explain how to use an endpoint and outline outputs for both good and bad input. These often can be automatically generated and put into a docs folder in your repository. [consider outputting html TODO]
API documentation example: http://docs.apis.is/
Eyra API documentation: https://github.com/cadia-lvl/Eyra/blob/master/ClientServerAPI.md
Command-line
Terminal based software should have a help option “--help” “-h”
This should explain what the script does, an example command, and explain the parameters.
TODO: include code snippets for creating help in python and bash but otherwise these scripts have examples: https://github.com/cadia-lvl/broadcast_data_prep/tree/master/ruv
Language specific documentation help
Java - Maven automatically creates documentation for your API.
Python - Sphinx automatically creates documentation from docstrings [TODO add that help usage is really easy to do for inputparser]
List of python tools to auto generate documentation
Google C++ style guide
