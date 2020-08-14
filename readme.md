<h1 align="center">
LVL Software Development Guidelines
</h1>

<p align="center"><i>
  This repository contains the software development guidelines for LVL.<br/>
  Center for Analysis and Design of Intelligent Agents, Language and Voice Lab <br/>
  Reykjavik University - School of Computer Science, Menntavegur 1, IS-101 Reykjavik, Iceland
</i></p>

<img src="https://user-images.githubusercontent.com/9976294/86356451-cddbc780-bc5b-11ea-89fb-f2d5d242d661.png" alt="Cover Image" align="center"/>
<!-- <div>Icons made by <a href="https://www.flaticon.com/free-icon/strategy_2819519?term=Roadmap&page=1&position=5" title="surang">surang</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div> -->

<!-- omit in toc -->
## Table of Contents

<details>
<summary>Click to expand</summary>

- [1. Notes for writing the guide](#1-notes-for-writing-the-guide)
- [2. About the guide](#2-about-the-guide)
	- [2.1. Goals](#21-goals)
	- [2.2. Contributors](#22-contributors)
	- [2.3. Deliverables](#23-deliverables)
	- [2.4. Dictionary](#24-dictionary)
- [3. Project Structure](#3-project-structure)
	- [3.1. Template README.md](#31-template-readmemd)
- [4. License](#4-license)
- [5. Documentation](#5-documentation)
	- [5.1. All Projects](#51-all-projects)
		- [5.1.1. Code should be self-documenting](#511-code-should-be-self-documenting)
		- [5.1.2. Developer documentation](#512-developer-documentation)
		- [5.1.3. User guides](#513-user-guides)
		- [5.1.4. Publishing documentation](#514-publishing-documentation)
		- [5.1.5. More information](#515-more-information)
	- [5.2. APIs](#52-apis)
		- [5.2.1. Further information](#521-further-information)
	- [5.3. Command-line tools](#53-command-line-tools)
		- [5.3.1. Further information](#531-further-information)
	- [5.4. Language/Tool specific documentation help](#54-languagetool-specific-documentation-help)
		- [5.4.1. help](#541-help)
		- [5.4.2. tools](#542-tools)
- [6. Version control](#6-version-control)
	- [6.1. Workflow](#61-workflow)
		- [6.1.1. Branching](#611-branching)
		- [6.1.2. Pull requests](#612-pull-requests)
	- [6.2. Commits](#62-commits)
	- [6.3. Semantic versioning](#63-semantic-versioning)
	- [6.4. Further information](#64-further-information)
- [7. Testing](#7-testing)
	- [7.1. Code](#71-code)
	- [7.2. Web](#72-web)
		- [7.2.1. Browsers](#721-browsers)
		- [7.2.2. Suggested strategy](#722-suggested-strategy)
	- [7.3. User testing](#73-user-testing)
		- [7.3.1. User tests should only be used if you have planned time to make adjustments](#731-user-tests-should-only-be-used-if-you-have-planned-time-to-make-adjustments)
		- [7.3.2. User testing should focus on a specific task](#732-user-testing-should-focus-on-a-specific-task)
		- [7.3.3. Up to 4 people for tests](#733-up-to-4-people-for-tests)
		- [7.3.4. Testing prototypes often gives no useful information](#734-testing-prototypes-often-gives-no-useful-information)
- [8. Continuous integration](#8-continuous-integration)
	- [8.1. What is Continuous integration?](#81-what-is-continuous-integration)
	- [8.2. Getting started with Github Actions](#82-getting-started-with-github-actions)
		- [8.2.1. Triggering workflows](#821-triggering-workflows)
		- [8.2.2. Jobs](#822-jobs)
		- [8.2.3. Example of a workflow:](#823-example-of-a-workflow)
	- [8.3. Further information](#83-further-information)
- [9. Packaging / Releasing](#9-packaging--releasing)
	- [9.1. All deliverables](#91-all-deliverables)
	- [9.2. Further information](#92-further-information)
- [10. Examples](#10-examples)
	- [10.1. Python library](#101-python-library)
	- [10.2. PyTorch model](#102-pytorch-model)
	- [10.3. Web Technologies](#103-web-technologies)
		- [10.3.1. JavaScript](#1031-javascript)
	- [10.4. Bash](#104-bash)
		- [10.4.1. Documentation](#1041-documentation)
	- [10.5. Kaldi recipes](#105-kaldi-recipes)
		- [10.5.1. README](#1051-readme)
		- [10.5.2. Documentation:](#1052-documentation)
	- [10.6. C++](#106-c)
	- [10.7. Java](#107-java)
		- [10.7.1. Documentation](#1071-documentation)
</details>
<!-- <a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>-->

## 1. Notes for writing the guide
This should be removed before releasing the guide.

- This guide should be short and simple and mention what is required or optional
- Offer examples
- Add links to good resources

## 2. About the guide

### 2.1. Goals
These guidelines should help us achieve the following goals:
- Make our lives **easier** by not having to reinvent the wheel in each of our induvidual projects and find **good resources** and guides which we are all aware of.
- Help us write **quality software** by following good software development proceedures.
- Enable **collaboration** by having collaboration as a part of our workflow.


### 2.2. Contributors
<a href="https://github.com/cadia-lvl/SoftwareDevelopmentGuidelines/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=cadia-lvl/SoftwareDevelopmentGuidelines" />
</a>
<!-- Made with [contributors-img](https://contributors-img.web.app). -->


### 2.3. Deliverables
The [SÍM guidelines](https://docs.google.com/document/d/1O_yhAnMVft6AJNoRjOFFRwnZKN8YmEE6GNM_8w1tq14/edit) define the deliverable types APP, MOD, ADD-ON, WEB and RES.

These types are quite abstract and LVL does not deliver all of them.
Due to this we further break down these deliverables to offer more concrete guidelines:
- UI (webpage, mobile, browser-plugin) = WEB, APP or ADD-ON
- Server (restful webserver) = WEB
- Library (python package) = MOD
- Model (trained model, runnable trained model) = RES, APP or MOD
- Command line client (python package, bash) = APP, MOD

Translating from the SÍM requirements to these deliverables will need to be discussed with a SÍM project manager to answer the question of "what do they expect?".

### 2.4. Dictionary

| Word   | Meaning                                                |
| :----- | :-----------------------------------------------------:|
| ADD-ON | a plugin to a larger framework                         |
| APP    | stand-alone application                                |
| CD     | Continuous Deployment / Continuous Delivery            |
| CI     | Continuous Integration                                 |
| MOD    | a module which can be embedded into other applications |
| RES    | language resource                                      |

[back to TOC](#table-of-contents)

---

## 3. Project Structure

It is a good idea to try to maintain a standardized project structure across our projects, as they always need to contain certain things. We suggest the following:

- `README.md`
- `LICENCE`
- `docs/`

In this example, the docs folder contains other documents. Other scripts such as .py and .sh files should be in the root folder.

### 3.1. Template README.md
```
# Title 
Project description as a paragraph or so explaining what this project does and perhaps why.

# Table of Contents
[Easy to use TOC generator](https://ecotrust-canada.github.io/markdown-toc/)

# Installation

* software requirements
* dependencies

It is also helpful to provide commands which assist user installing the program or even providing an `install.sh` script which does it for the user.

# Running
How to run the program/application/model and common use-cases and outputs.
For the program to be easily usable this section can be quite long.

## API reference (Optional)
If lengthy, this should be a separate document placed as HTML into the `docs/` folder. For more inforation see `documentation`

# License
Mention which LICENSE the code uses. For more information about licensing see later.

# Authors/Credit
Reykjavik University

Main authors <email.addresses>

## Acknowledgements
If the funding is from a public grant, mention the source of the funding and link to their website.

"This project was funded by the Language Technology Programme for Icelandic 2019-2023. The programme, which is managed and coordinated by [Almannarómur](https://almannaromur.is/), is funded by the Icelandic Ministry of Education, Science and Culture."

# Contribution guidelines (Optional)
Explain how people can contribute to this repository. This can also link to a separate Developer reference

* how to contribute
* creating issues
* where to get data
* testing

## Description of folder structure (Optional)

# Changelog/Versions (Optional)
# Papers/References (Optional)
You would have a citation snippet here as a code block
```
For papers not yet accepted it is fine to mention you have submitted a paper to a particular conference and mention how you
will reference it once has been accepted. For example you could add a citation or include the paper in the docs folder. 

[back to TOC](#table-of-contents)

## 4. License
All of the projects we work on need to have licenses. A single LICENSE file, mentioned and linked from the README, suffices. Adding a license header in every single file is optional.

If a project does not contain a license, the default copyright is in place which means that no-one is allowed to make derivative work with your code.

We want our code to be freely available for everyone so we prefer permissive licenses such as
- Apache 2.0 (quite permissive)
- MIT License (very permissive)
- CC BY 4.0 (for resources)

For more help choosing a license, see [Choosing a license](https://choosealicense.com/). Keep in mind that if you are working through SÍM you have agreed to use open licenses such as these. Furthermore, according to RU contracts you are the copyright owner.

When a license has been chosen, simply copy the license text, fill in any additional information required (like copyright owner and year) and write it to a LICENCE file in the repository.


[back to TOC](#table-of-contents)

---

## 5. Documentation
[Some motivation missing]


### 5.1. All Projects

#### 5.1.1. Code should be self-documenting 
When that’s not possible it should be well documented within comments and overall documentation. 

In the case of python, documentation can be automatically generated from “docstrings.” Other languages and frameworks have similar features. Use easy to understand variables and function names, that is avoid ambiguous names. Use consistent styles throughout the whole codebase. The code should also be consistent with the general guidelines of the programming language.

#### 5.1.2. Developer documentation
Developer documentation should generally be in English. Developer guides would be like installation guides, API documentation, contribution guidelines, just any information that would help a developer use and modify this codebase faster. Along these lines, code examples, code snippets, and examples of (function/API) calls and the possible outputs would help users to understand much quicker.

#### 5.1.3. User guides
User guides should be in the language of the users. User guides is documentation for user facing code. Within LVL example projects which might need user guides are [LOBE](https://github.com/cadia-lvl/LOBE.git) and [Eyra](https://github.com/cadia-lvl/Eyra.git) because both have user interfaces that don't involve code. These guides should also contain lots of examples. This can work as a tutorial within the webpage with popups that walks first time users through the different steps in a webpage or a standalone guide perhaps with videos or pictures walking users through the more difficult aspects of using the tool or webpage.

Add research papers to the repository in a docs folder if possible. [Eyra has a conference paper in its docs folder](https://github.com/Eyra-is/Eyra/blob/master/Docs/Petursson_et_al_2016.pdf)

#### 5.1.4. Publishing documentation
Documentation for git repositories can live in the docs folder as a website. Github has a feature called github-pages. This allows us to host a website directory from our code respositories. This is especially useful if we have user guides or API documentation. Thus, we don't need a whole server just for a few webpages. GitHub has a step by step guide of how to do that on their platform which is linked [here](https://pages.github.com/).

#### 5.1.5. More information 
We have provided a template for your projects' [README.md file](readme_template.md). It provides both the minimum sections and the optional sections. You can read more about why those sections here at [GitHub's guide](https://guides.github.com/features/wikis/). After you've read that explanation, you can delete whichever sections you don't need. 


### 5.2. APIs
The documentation should explain how to use an endpoint and outline outputs for both good and bad input. Remember, it's better to have some documentation than none at all. These often can be automatically generated and put into a docs folder in your repository as a html pages which can then be hosted as a Github Pages website.

#### 5.2.1. Further information
- [API documentation example](http://docs.apis.is/)
- [Eyra API documentation](https://github.com/cadia-lvl/Eyra/blob/master/ClientServerAPI.md)

### 5.3. Command-line tools
Terminal based software should have a help option: `--help` or `-h` or both. Typing in the filename then either of these options should bring up some text explaining what the script does, an example command, and list explanations of the parameters.

[TODO: include code snippets for creating help in python and bash directly in the file.]
#### 5.3.1. Further information
- [broadcast_data_prep/master/ruv/extract_from_ruv_api.py has an example at the bottom](https://github.com/cadia-lvl/broadcast_data_prep/blob/master/ruv/extract_from_ruv_api.py)
- [bash example](https://github.com/cadia-lvl/broadcast_data_prep/blob/master/ruv/compare_hypothesis_and_expanded_888.sh)

### 5.4. Language/Tool specific documentation help
- [Python](examples.md#Python)
- [Bash](examples.md#bash)
- [C++](examples.md#C)
- [Java](examples.md#Java)

#### 5.4.1. help
In python3.8, creating a help usage is really easy once you import the [argparse](https://docs.python.org/3/library/argparse.html) package.
[broadcast_data_prep/master/ruv/extract_from_ruv_api.py has an example at the bottom](https://github.com/cadia-lvl/broadcast_data_prep/blob/master/ruv/extract_from_ruv_api.py)

#### 5.4.2. tools
[List of python tools to auto generate documentation](https://wiki.python.org/moin/DocumentationTools)

- [Sphinx](https://www.sphinx-doc.org/en/master/) : automatically creates documentation from docstrings. [example of PyTorch documentation generated by Sphinx](https://pytorch.org/docs/stable/nn.html#parameters)
- pdoc3 : Another python documentation tool is pdoc3 which also uses docstrings. Installing it is as easy as `pip3 install pdoc3`. Generating the documentation is `pdoc --html --output-dir docs <path-to-your-module-with-init-py>`. There should be no subdirectories.


[back to TOC](#table-of-contents)

---

## 6. Version control
Within Cadia-LVL, using git for version control is required. A clean repository with descriptive comments makes for a good representation of your project which makes it easier for new developers to join it. The following guidelines describe a way to maintain a project as such.


### 6.1. Workflow
If a project is public, **the master branch should always contain production ready code**. All merges to the master branch should include semantic version tags as listed below.

#### 6.1.1. Branching
For smaller projects and teams, feature branching is sufficient, where each feature gets a branch, created from master, used while developing until it is merged into the master.

For larger projects, [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) is the recommended workflow. It includes two main branches, the master branch that stores release history and a development branch that lives between the master branch and feature branches. It also recommends a clear way to implement hotfixes.

#### 6.1.2. Pull requests
When adding new features or updates to the master branch, developers should write a pull request and let at least one other team member review their code before merging.

Code reviews across projects are recommended but not required. Keeping more team members informed about your work can benefit the team as a whole.


### 6.2. Commits
Every commit message should include a short description of work being commited. Pull request comments should be more detailed. 

### 6.3. Semantic versioning
Version tags can be informative, especially to current users. Given a version number *v[major].[minor].[patch]*, increments represent the following:
- Major: Incompatible API changes, ***when you break something***
- Minor: Added backwards compatible functionality, ***when you add features***
- Patch: Backwards compatible fixes, ***when you fix bugs***

### 6.4. Further information
- [Read more about semantic versioning](https://semver.org/)
- [How to use tags to apply semantic versioning](https://www.atlassian.com/git/tutorials/inspecting-a-repository/git-tag)
- [Back to top](https://github.com/cadia-lvl/SoftwareDevelopmentGuidelines#table-of-contents)

[back to TOC](#table-of-contents)

---

## 7. Testing
TODO: Add motivation


### 7.1. Code
All projects should attempt to do as much unit testing as possible.
At minimum aim to have tests for mission critical algorithms and functions.
Unit tests inside each module cover this nicely but the implementation is dependent on the programming language and environment. 


### 7.2. Web
A huge part of the web is portability and accessibility, so making sure your website works on all major devices and platforms is very important.

#### 7.2.1. Browsers
When testing your website keep in mind the demographic that will be using the site, what devices they are using (mobile vs. desktop), and which browsers.
Preferebly test each deplpoyment on these devices and browsers.
You can see browsers usage statistics [here](https://en.wikipedia.org/wiki/Usage_share_of_web_browsers#Summary_tables) to decide which browsers to test.

Major browsers on desktop are:

- Chrome, 
- Firefox, 
- Safari, and 
- Edge

Major browsers for mobile are: 
- Chrome, 
- Safari. and 
- Samsung Internet

[Caniuse.com](https://caniuse.com/) is helpful if you are unsure about browser support for specific features.

If for some specific and clear reason a particular browser is needed make sure it is clearly stated on the page.
You can use the [User-Agent](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/User-Agent) HTTP header to display warnings to all unsopported browsers.

#### 7.2.2. Suggested strategy
Keep two entirely separate deployments up and running, staging and production.
Deploy all changes first to the staging environment (this can be done automatically).

Preferably have multiple users test all major changes on the staging deployment before deploying to production.
This part could be done automatically but is often time consuming and difficlut to keep up to date.
Suggested tools for automated testing: [Selenium with Python](https://selenium-python.readthedocs.io/index.html) and (Cucumber)[https://github.com/cucumber/cucumber]


### 7.3. User testing
User testing is a great way to see how the users interact with your product. 
However, user testing is difficult to do well. When doing user tests keep the following points in mind.

#### 7.3.1. User tests should only be used if you have planned time to make adjustments
There is no reason to spend time user testing if the results won't be used to make adjustments and improve the product.

#### 7.3.2. User testing should focus on a specific task
Focusing on a specific scope or task helps to keep the user focusing on what is important.
This does not mean the same user can not test different tasks, only that each task you give the users should be clearly defined.

#### 7.3.3. Up to 4 people for tests
Asking too many users to do the same tests will only result in more of the same responses.
Every users experience matters and should be taken into account.
If you have more users to test, think about trying to test different things or do another round when adjustments have been made from the first one.

#### 7.3.4. Testing prototypes often gives no useful information 
Users will most likely point out things that you know are missing and are less likely to give the feedback you are looking for.
This can be reduced somewhat by targetting very specific tasks early in the development, see point about specific tasks.


[back to TOC](#table-of-contents)

---

## 8. Continuous integration

When **working on a project with others** and preferably while working alone, **Github Actions should be used for continuous integration**.

### 8.1. What is Continuous integration?
Continuous integration is a way to **build software, automaticly run tests and alert developers when a test doesn't pass**. This way developers can fix mistakes before they pile up and become difficult to manage. It also gives developers more confidance in their code and minimizes unknown errors. 


### 8.2. Getting started with Github Actions
Simply navigate to your repository and click the **Actions** on the right side of the *Pull request* button.
Here you can choose to use workflows from others or click **set up a workflow yourself** to create your own.

#### 8.2.1. Triggering workflows
Your workflow should run at minimum each time a push or a pull request is made to the master. It is also recomended to run a [scheduled](https://help.github.com/en/actions/reference/events-that-trigger-workflows#scheduled-events-schedule) workflow once a day for building, testing and packaging projects. If workflows take a long time to run it is advisable to run them over night. 

#### 8.2.2. Jobs
Jobs should at minimum include [testing](#testing) and [packaging](#packaging--releasing) for the project.

Multiple jobs can be specified within each workflow. Besides testing and packaging, which are required, it is also recommended to run a linter on the project to ensure consistent styling across the project.

Keep in mind that each job may take no longer than 6 hours to complete or it will be automatically ended.

When running a job we need to specify which machine it [runs on](https://help.github.com/en/actions/reference/workflow-syntax-for-github-actions#jobsjob_idruns-on). It is **strongly recommended to use github hosted runners**.

#### 8.2.3. Example of a workflow:
```
name: LVL_CI_example

# on controls when this specific action will run.
on:
  # The event/s you want to trigger this action
  [push, pull_request]:
    # Which branch/es the action will run on
    branches: [ master ]

#job defines a sequence of tasks that will run when this workflow is triggered. 
job: 
  # A unique id for a job containing only _ or letters, this one is called build
  build:
    # Specifies which kind of machine the job is run on. 
    # It's up to you which machine to use but github hosted runners are highly encouraged.
    runs-on: ubuntu-latest
    
    #steps defines a tasks to run as part of the job, the following steps 
    steps: 
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: actions/checkout@v2
      
      #--build project--
      
      ## Below are some examples of how to run code
      
      - name: example 1
      run: echo run can run scripts
      
      - name: example 2
      run: |
      echo it can also run
      echo multi-line scripts
      
      # this example uses a code from another file
      - name: example 3
        uses: ./.github/actions/my-action
      
      
      
  test: 
     runs-on: ubuntu-latest
     
     steps:
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: actions/checkout@v2
      
      #--run your tests--
      
  package:
    runs-on: ubuntu-latest
     
     steps:
      # Checks-out your repository under $GITHUB_WORKSPACE, so your job can access it
      - uses: actions/checkout@v2
      
      #--run your packaging steps--
  
```


### 8.3. Further information
- [Language and framework guidelines](https://help.github.com/en/actions/language-and-framework-guides) 
- [Packaging on Github](https://help.github.com/en/actions/publishing-packages-with-github-actions/about-packaging-with-github-actions) (optional)
- [Workflow triggers](https://help.github.com/en/actions/reference/events-that-trigger-workflows#webhook-events)
- [Further on triggering workflows](https://help.github.com/en/actions/reference/workflow-syntax-for-github-actions#on).
- Further on jobs](https://help.github.com/en/actions/reference/workflow-syntax-for-github-actions#jobs).


[back to TOC](#table-of-contents)

---

## 9. Packaging / Releasing
When a project should be released it should be packaged so that it can be easily used by the intended users. The packaging depends on the deliverable type, see [deliverables](#deliverables).

General reference for specific deliverables:
- UI: Compiled and optimized executable.
- Server: Compiled and optimized executable.
- Library: According to language convention.
- Model: Model files uploaded to CLARIN. Reference to a git tag.
- Command line: Compiled and optimized executable.

Packaging should be done after [testing](#testing) and be a part of the [continuous integration](#continuous-integration) setup for all projects (excluding models).

### 9.1. All deliverables
All deliverables should be provided along with instructions on how to run them and examples.

All deliverables should be referenced with a git tag (f.ex. a version).
This is done so that the code of a deliverable can be easily reviewed and for easy recreation.

When releasing an artifact, be sure that all changes have been committed and a proper README file is in place so that the release process can be repeated by someone else.

For more complex deliverables (which have many dependencies) we also recommend packaging the deliverable using docker.

### 9.2. Further information
- An example on how to make pip packages can be found [here](https://packaging.python.org/tutorials/packaging-projects/).
- An example of a pip package is the [Mideind tokenizer](https://github.com/mideind/Tokenizer#installation) 


[back to TOC](#table-of-contents)

---

## 10. Examples

### 10.1. Python library

### 10.2. PyTorch model

### 10.3. Web Technologies
[Web Technologies reference](https://developer.mozilla.org/en-US/docs/Web)

#### 10.3.1. JavaScript
JavaScript backend & frontend

### 10.4. Bash

#### 10.4.1. Documentation
[bash help usage example](https://github.com/cadia-lvl/broadcast_data_prep/blob/master/ruv/compare_hypothesis_and_expanded_888.sh)

[Better Programming has a short list of Bash Best Practices](https://medium.com/better-programming/best-practices-for-bash-scripts-17229889774d)

### 10.5. Kaldi recipes

#### 10.5.1. README
Explains the folder structure: [kaldi-for-dummies](http://kaldi-asr.org/doc/kaldi_for_dummies.html#kaldi_for_dummies_directories)

#### 10.5.2. Documentation: 
A good documentation is provided: [kaldi-asr](http://kaldi-asr.org/doc/about.html#about_reference)

### 10.6. C++

[Google C++ style guide](https://google.github.io/styleguide/cppguide.html)

### 10.7. Java

#### 10.7.1. Documentation
[Maven](https://maven.apache.org/) automatically creates documentation for your API.

[back to TOC](#table-of-contents)
