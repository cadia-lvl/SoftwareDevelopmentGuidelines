# Documentation
## All Projects
**Code should be self-documenting and when that’s not possible then it should be well documented within comments and overall documentation.** In the case of python, documentation can be automatically generated from “docstrings.” Other languages and frameworks have similar features. Use easy to understand variables and function names; avoid ambiguous names. Use consistent styles throughout the whole codebase. The code should also be consistent with the general guidelines of the programming language.

**Developer documentation should generally be in English.** Developer guides would be like installation guides, API documentation, Contribution guidelines, just any information that would help a developer use and modify this codebase faster.
**User guides should be in the same language of the users.** User guides is documentation for user facing code. Within LVL example projects are [LOBE](https://github.com/cadia-lvl/LOBE.git) and [Eyra](https://github.com/cadia-lvl/Eyra.git) because both have user interfaces that don't involve code.
Add research papers to the repository in a docs folder if possible. [Eyra has a conference paper in its docs folder](https://github.com/Eyra-is/Eyra/blob/master/Docs/Petursson_et_al_2016.pdf)

Documentation for git repositories can live in the docs folder as a website. Github has a feature called github-pages. This allows us to host a website directory from our code respositories. This is especially useful if we have user guides or API documentation. We don't need a whole server just for a few webpages. GitHub has a step by step guide of how to do that on their platform which is linked [here](https://pages.github.com/)

We have provided a template for your projects' [README.md file](readme_template.md). It provides both the minimum sections and the optional sections. You can read more about why those sections here at [GitHub's guide](https://guides.github.com/features/wikis/). After you've read that explanation, you can delete whichever sections you don't need. 

## APIs

The documentation should explain how to use an endpoint and outline outputs for both good and bad input. Remember, it's better to have some documentation than none at all. 

These often can be automatically generated and put into a docs folder in your repository as a html pages which can then be hosted as a Github Pages website.

[API documentation example](http://docs.apis.is/)

[Eyra API documentation](https://github.com/cadia-lvl/Eyra/blob/master/ClientServerAPI.md)

## Command-line tools
Terminal based software should have a help option: `--help` or `-h` or both.Typing in the filename then either of these options should bring up some text explaining what the script does, an example command, and list explanations of the parameters.
**TODO: include code snippets for creating help in python and bash directly in the file.**
* [broadcast_data_prep/master/ruv/extract_from_ruv_api.py has an example at the bottom](https://github.com/cadia-lvl/broadcast_data_prep/blob/master/ruv/extract_from_ruv_api.py)
* [bash example](https://github.com/cadia-lvl/broadcast_data_prep/blob/master/ruv/compare_hypothesis_and_expanded_888.sh)

## Language/Tool specific documentation help
* [Python](examples.md#Python)
* [Bash](examples.md#bash)
* [C++](examples.md#C)
* [Java](examples.md#Java)
