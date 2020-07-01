# LVL Software development guidelines
This repository contains the software development guidelines for LVL.

This is work in progress.

## Table of Contents
<details>
<summary>Click to see table of contents</summary>
 <br/>
 <ol>
  <details>
   <summary><a href="#about-the-guide">About the guide</a></summary>
    <ul>
     <li><a href="#goals">Goals</a></li>
     <li><a href="#contributors">Contributors</a></li>
     <li><a href="#deliverables">Deliverables</a></li>
     <li><a href="#dictionary">Dictionary</a></li>
    </ul>
  </details>
  <details>
   <summary><a href="#project-structure">Project Structure</a></summary>
   <ul>
    <li><a href="#template-readmemd">README template</a></li>
   </ul>
  </details>
  <details>
   <summary><a href="#license">License</a></summary>
  </details>
  <details>
   <summary><a href="#documentation">Documentation</a></summary>
   <ul>
    <li><a href="#all-projects">All Projects</a>
     <ul>
    <li><a href="#code-should-be-self-documenting">Code should be self-documenting</a></li>
    <li><a href="#developer-documentation">Developer documentation](#</a></li>
    <li><a href="#user-guides">User guides</a></li>
    <li><a href="#git-documentation">Git documentation</a></li>
    <li><a href="#more-information">More information</a></li>
   </ul>
    </li>
    <li><a href="#apis">APIs</a>
     <ul>
      <li><a href="#further-information">Further information</a></li>
     </ul>
    </li>
    <li><a href="#command-line-tools">Command-line tools</a>
     <ul>
      <li><a href="#further-information-1">Further information</a></li>
     </ul>
    </li>
    <li><a href="#languagetool-specific-documentation-help">Language/Tool specific documentation help</a>
     <ul>
      <li><a href="#help">help</a></li>
      <li><a href="#tools">tools</a></li>
     </ul>
    </li>
   </ul>
  </details>
  <details>
  <summary><a href="#version-control">Version control</a></summary>
  <ul>
   <li><a href="#workflow">Workflow</a>
    <ul>
     <li><a href="#branching">Branching</a></li>
     <li><a href="#pull-requests">Pull requests</a></li>
    </ul>
   </li>
   <li><a href="#commits">Commits</a></li>
   <li><a href="#semantic-versioning">Semantic versioning</a></li>
   <li><a href="#further-information-2">Further information</a></li>
  </ul>
  </details>
  <details>
  <summary><a href="#testing">Testing</a></summary>
  <ul>
   <li><a href="#code">Code</a></li>
   <li><a href="#web">Web</a>
    <ul>
     <li><a href="#browsers">Browsers</a></li>
     <li><a href="#suggested-strategy">Suggested strategy</a></li>
    </ul>
   </li>
   <li><a href="#user-testing">User testing</a>
    <ul>
     <li><a href="#user-tests-should-only-be-used-if-you-have-planned-time-to-make-adjustments">User tests should only be used if you have planned time to make adjustments</a></li>
     <li><a href="#user-testing-should-focus-on-a-specific-task">User testing should focus on a specific task</a></li>
     <li><a href="#testing-prototypes-often-gives-no-useful-information">Testing prototypes often gives no useful information</a></li>
    </ul>
   </li>
  </ul>
  </details>
  <details>
   <summary><a href="#continuous-integration">Continuous integration</a></summary>
   <ul>
    <li><a href="#what-is-continuous-integration">What is Continuous integration?</a></li>
    <li><a href="#getting-started-with-github-actions">Getting started with Github Actions</a>
     <ul>
      <li><a href="#triggering-workflows">Triggering workflows</a></li>
      <li><a href="#jobs">Jobs</a></li>
      <li><a href="#example-of-a-workflow">Example of a workflow:</a></li>
     </ul>
    </li>
    <li><a href="#further-information-3">Further information</a></li>
   </ul>
  </details>
  <details>
   <summary><a href="#packaging--releasing">Packaging / Releasing</a></summary>
   <ul>
    <li><a href="#all-deliverables">All deliverables</a></li>
    <li><a href="#further-information-4">Further information</a></li>
   </ul>
  </details>
  <details>
   <summary><a href="#examples">Examples</a></summary>
   <ul>
    <li><a href="#python-library">Python library</a></li>
    <li><a href="#pytorch-model">PyTorch model</a></li>
    <li><a href="#javascript">JavaScript</a></li>
    <li><a href="#bash">Bash</a>
     <ul>
      <li><a href="#documentation-1">Documentation</a></li>
     </ul>
    </li>
    <li><a href="#kaldi-recipes">Kaldi recipes</a>
     <ul>
      <li><a href="#readme">README</a></li>
      <li><a href="#documentation-2">Documentation:</a></li>
     </ul>
    </li>
    <li><a href="#c">C++</a></li>
    <li><a href="java">Java</a>
     <ul>
      <li><a href="#documentation-3">Documentation</a></li>
     </ul>
    </li>
   </ul>
  </details>
</ol>
</details>
<!-- <a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>-->

## Notes for writing the guide
This should be removed before releasing the guide.

- This guide should be short and simple and mention what is required or optional
- Offer examples
- Add links to good resources

## About the guide

### Goals
These guidelines should help us achieve the following goals:
- Make our lives **easier** by not having to reinvent the wheel in each of our induvidual projects and find **good resources** and guides which we are all aware of.
- Help us write **quality software** by following good software development proceedures.
- Enable **collaboration** by having collaboration as a part of our workflow.

### TLDR
The guide can be summarized as the following:
- Have a good `README.md`, see our [template](#template-readme.md).
- Provide a `License`.
- Write documentation within the code so that you can automatically generate it later (if you need to).
- Use `git` for semantic versioning.
- Test your code, preferably automatically.
- Setup "GitHub actions" to run testing and linting.
- Check out our [examples](#examples).

### Other resources
- [Compute](https://github.com/cadia-lvl/compute) for information about the cluster (called Terra) at LVL.
- The [SÍM guidelines](https://docs.google.com/document/d/1O_yhAnMVft6AJNoRjOFFRwnZKN8YmEE6GNM_8w1tq14/edit) for writing and delivering software.

### Deliverables
The [SÍM guidelines](https://docs.google.com/document/d/1O_yhAnMVft6AJNoRjOFFRwnZKN8YmEE6GNM_8w1tq14/edit) define the deliverable types APP, MOD, ADD-ON, WEB and RES.

These types are quite abstract and LVL does not deliver all of them.
Due to this we further break down these deliverables to offer more concrete guidelines:
- UI (webpage, mobile, browser-plugin) = WEB, APP or ADD-ON
- Server (restful webserver) = WEB
- Library (python package) = MOD
- Model (trained model, runnable trained model) = RES, APP or MOD
- Command line client (python package, bash) = APP, MOD

Translating from the SÍM requirements to these deliverables will need to be discussed with a SÍM project manager to answer the question of "what do they expect?".

### Contributors
<a href="https://github.com/cadia-lvl/SoftwareDevelopmentGuidelines/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=cadia-lvl/SoftwareDevelopmentGuidelines" />
</a>
<!-- Made with [contributors-img](https://contributors-img.web.app). -->

### Dictionary

| Word   | Meaning                                                |
| :----- | :-----------------------------------------------------:|
| ADD-ON | a plugin to a larger framework                         |
| APP    | stand-alone application                                |
| CD     | Continuous Deployment / Continuous Delivery            |
| CI     | Continuous Integration                                 |
| MOD    | a module which can be embedded into other applications |
| RES    | language resource                                      |
| IDE    | Integrated development environment                     |

[back to TOC](#table-of-contents)

---

## Project Structure
Try to maintain a standardized project structure across your projects, as they always need to contain certain things. We suggest the following:

```
README.md  # See template below
LICENSE    # See license section
docs/      # Contains automatically generated documentation in HTML.
```
Other scripts such as .py and .sh files should be in the root folder.

### Template README.md
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
Mention which LICENSE the code uses a refer to the LICENSE file. For more information about licensing later.

# Authors/Credit
Reykjavik University

Main authors <email.addresses>

## Acknowledgements
If the funding is from a public grant, mention the source of the funding and link to their website.

"This project was funded by the Language Technology Programme for Icelandic 2019-2023. The programme, which is managed and coordinated by [Almannarómur](https://almannaromur.is/), is funded by the Icelandic Ministry of Education, Science and Culture."

# Contributing (Optional)
Explain how people can contribute to this repository. This can also link to a separate Developer reference (Contributing.md)

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

## License
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

## Documentation
We all know that documentation is key if software is supposed to be usable.
Writing documentation can be hard but we have some suggestions to make it easier, but keep in mind that a good `#Running` section the `README.md` is complementary to the documentation, i.e. you need to write both.
- The `#Running` section handles common use-cases. This can be seen as a small [user guide](#user-guide).
- Write the documentation for functions and classes in your code using your language's conventions since all (common) languages have tools which can extract this documentation. This documentation is more detailed than the `#Running` section but can also contain the same examples.

### Code
- Use **easy to understand variables and function names**, that is avoid ambiguous names.
- Settle on a **single format** for the documentation. This is for automatic documentation generation.
- When you have settled on a format, find a **tool** which supports that format which can generate HTML and place it in the `docs/` folder.
- Write documentation in English, unless you have a good reason not to do so.
- Be sure to define **accepted inputs** and **return values**.

#### Python
We suggest the following format and tool for Python
- Format: [Google](https://github.com/google/styleguide/blob/gh-pages/pyguide.md#38-comments-and-docstrings). It's easily readable in code, widely support and not verbose.
- Tool: [`Sphinx` with `napoleon`](https://www.sphinx-doc.org/en/master/usage/extensions/napoleon.html)

#### JavaScript
TODO

### Publishing documentation
Given that you have generated HTML pages using your documentation tool, this documentation can be hosted on GitHub using [github-pages](https://pages.github.com/).
This allows us to host a website directory from our code respositories.
This avoids us having to host the documentation in some remote server.

### Developer documentation
For larger projects a developer guide can be helpful for newcomers.
These contain **installation guides** and **contribution guidelines** or any information that would help a developer use and modify this codebase faster.
Place this information into `Contributing.md`.

### User guide
User guides are (generally) **not as technical** as documentation and are thought for the **end-user**.
For larger projects which require a user guide the guide should be in the **language of the user**.
These guides should contain **a lot of examples** and lead the user through common-use cases.
For example:
- This could be implemented as a tutorial within a webpage with popups that guide the user through the UI.
- This could be a video guide which go through the same steps as above.
- This could be implemented as a Wiki on GitHub.
- This could be implemented as a long `#Running` section.
- If working with the command-line your program should support `--help / -h` commands which should offer some text explaining what the script does, examples and description of parameters. For Python [argparse](https://docs.python.org/3/library/argparse.html) and [click](https://click.palletsprojects.com/en/7.x/) make it easy to get this functionality.

[back to TOC](#table-of-contents)

---

## Version control
Within Cadia-LVL, using git for version control is required. A clean repository with descriptive commit messages makes for a good representation of your project which makes it easier for new developers to join it. The following guidelines describe a way to maintain a project as such.

### Workflow
If a project is public, **the master branch should always contain production ready code**.
All merges to the master branch should include semantic version tags as listed below.

#### Branching
For smaller projects and teams, **feature branching** is sufficient, where each feature gets a branch, created from master, used while developing until it is merged into the master.

For larger projects, [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) is the recommended workflow. It includes **two main branches**, the master branch that stores release history and a development branch that lives between the master branch and feature branches. It also recommends a clear way to implement hotfixes.

#### Pull requests
When you have finished your work on the feature branch you should create a **pull request** to the master branch.
Assign **someone other than yourself to review** the pull request (the code).
The **reviewer is responsible** for making sure that everything is (within limits) tested and documented.
If the reviewer has issues with the pull request (very common) the reviewer **requests fixes** and repeats this process until satisfied.
When there are no more issues, the **reviewer accepts the pull request** and merges it into the main branch.

To clearly state the benefits of this, if enforced:
- No-one works in isolation, more people understand the project.
- Code quality generally increases.
- More tests are written.
- The project is well documented.

For more information about pull requests see [here](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests)

### Commits
Every commit message should include a short description of work being commited. Pull request comments should be more detailed. 

### Semantic versioning
Version tags can be informative, especially to current users. Given a version number *v[major].[minor].[patch]*, increments represent the following:
- Major: Incompatible API changes, ***when you break something***
- Minor: Added backwards compatible functionality, ***when you add features***
- Patch: Backwards compatible fixes, ***when you fix bugs***

[Read more about semantic versioning](https://semver.org/) and [how to use tags to apply semantic versioning](https://www.atlassian.com/git/tutorials/inspecting-a-repository/git-tag)

[back to TOC](#table-of-contents)

---

## Testing
TODO: Add motivation


### Code
All projects should attempt to do as much unit testing as possible.
At minimum aim to have tests for mission critical algorithms and functions.
Unit tests inside each module cover this nicely but the implementation is dependent on the programming language and environment. 


### Web
A huge part of the web is portability and accessibility, so making sure your website works on all major devices and platforms is very important.

#### Browsers
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

#### Suggested strategy
Keep two entirely separate deployments up and running, staging and production.
Deploy all changes first to the staging environment (this can be done automatically).

Preferably have multiple users test all major changes on the staging deployment before deploying to production.
This part could be done automatically but is often time consuming and difficlut to keep up to date.
Suggested tools for automated testing: [Selenium with Python](https://selenium-python.readthedocs.io/index.html) and (Cucumber)[https://github.com/cucumber/cucumber]


### User testing
User testing is a great way to see how the users interact with your product. 
However, user testing is difficult to do well. When doing user tests keep the following points in mind.

#### User tests should only be used if you have planned time to make adjustments
There is no reason to spend time user testing if the results won't be used to make adjustments and improve the product.

#### User testing should focus on a specific task
Focusing on a specific scope or task helps to keep the user focusing on what is important.
This does not mean the same user can not test different tasks, only that each task you give the users should be clearly defined.

#### Up to 4 people for tests
Asking too many users to do the same tests will only result in more of the same responses.
Every users experience matters and should be taken into account.
If you have more users to test, think about trying to test different things or do another round when adjustments have been made from the first one.

#### Testing prototypes often gives no useful information 
Users will most likely point out things that you know are missing and are less likely to give the feedback you are looking for.
This can be reduced somewhat by targetting very specific tasks early in the development, see point about specific tasks.


[back to TOC](#table-of-contents)

---

## Linting
Linting is any form of **static analysis** on code without running it.
It alerts you of **possible errors**, **missing documentation** or **overly complex code** without writing tests.
These are easily incorporated into the [continuous integration system](#continuous-integration)
Using (some) linting is **required** in all projects.
Adding linters to your **IDE** is very easy and can be configured to run on file-save.

### Python
For Python we suggest the following tools for all projects.
- Common errors: [`flake8`](https://github.com/PyCQA/flake8)
- Type checks: [`mypy`](https://github.com/python/mypy)
- Documentation checker: [`pydocstyle`](https://github.com/PyCQA/pydocstyle)

### JavaScript
TODO

### Bash
- Best practices and errors: [`shellcheck`](https://www.shellcheck.net/)

## Style
Maintaining the same style across a project makes the code more readable. We suggest using a tool which automatically formats/styles your code. This eliminates inconsistent styles in the code and allows you to focus on the code, rather than the format.

### Python
We highly suggest [`black`](https://github.com/psf/black)

### JavaScript

## Continuous integration

When **working on a project with others** and preferably while working alone, we recommend **Github Actions for continuous integration**.

### What is Continuous integration?
Continuous integration is a way to **build software (compile), automatically run [tests](#testing), [lint and check documentation](#linting) and alert developers when something is wrong**.
We suggests running all these steps automatically in the CI system.
This way developers can fix mistakes before they pile up and become difficult to manage.
It also gives developers more confidance in their code and minimizes unknown errors. 

### Getting started with Github Actions
Simply navigate to your repository and click the **Actions** on the right side of the *Pull request* button.
Here you can choose to use workflows from others or click **set up a workflow yourself** to create your own.
This defines the steps you would like to perform when you push changes.

#### Triggering workflows
Your workflow should run at minimum each time a push or a pull request is made to the master.
It is also recomended to run a [scheduled](https://help.github.com/en/actions/reference/events-that-trigger-workflows#scheduled-events-schedule) workflow once a day, in-case a dependency of your project is updated and breaks your code.

#### Example of a workflow:
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


### Further information
- [Language and framework guidelines](https://help.github.com/en/actions/language-and-framework-guides) 
- [Packaging on Github](https://help.github.com/en/actions/publishing-packages-with-github-actions/about-packaging-with-github-actions) (optional)
- [Workflow triggers](https://help.github.com/en/actions/reference/events-that-trigger-workflows#webhook-events)
- [Further on triggering workflows](https://help.github.com/en/actions/reference/workflow-syntax-for-github-actions#on).
- Further on jobs](https://help.github.com/en/actions/reference/workflow-syntax-for-github-actions#jobs).


[back to TOC](#table-of-contents)

---

## Packaging / Releasing
When a project should be released it should be packaged so that it can be easily used by the intended users. The packaging depends on the deliverable type, see [deliverables](#deliverables).

General reference for specific deliverables:
- UI: Compiled and optimized executable.
- Server: Compiled and optimized executable.
- Library: According to language convention.
- Model: Model files uploaded to CLARIN. Reference to a git tag.
- Command line: Compiled and optimized executable.

Packaging should be done after [testing](#testing) and be a part of the [continuous integration](#continuous-integration) setup for all projects (excluding models).

### All deliverables
All deliverables should be provided along with instructions on how to run them and examples.

All deliverables should be referenced with a git tag (f.ex. a version).
This is done so that the code of a deliverable can be easily reviewed and for easy recreation.

When releasing an artifact, be sure that all changes have been committed and a proper README file is in place so that the release process can be repeated by someone else.

For more complex deliverables (which have many dependencies) we also recommend packaging the deliverable using docker.

### Further information
- An example on how to make pip packages can be found [here](https://packaging.python.org/tutorials/packaging-projects/).
- An example of a pip package is the [Mideind tokenizer](https://github.com/mideind/Tokenizer#installation) 


[back to TOC](#table-of-contents)

---

## Examples

### Python library

### PyTorch model

### Web Technologies
[Web Technologies reference](https://developer.mozilla.org/en-US/docs/Web)

#### JavaScript
JavaScript backend & frontend

### Bash

#### Documentation
[bash help usage example](https://github.com/cadia-lvl/broadcast_data_prep/blob/master/ruv/compare_hypothesis_and_expanded_888.sh)

[Better Programming has a short list of Bash Best Practices](https://medium.com/better-programming/best-practices-for-bash-scripts-17229889774d)

### Kaldi recipes

#### README
Explains the folder structure: [kaldi-for-dummies](http://kaldi-asr.org/doc/kaldi_for_dummies.html#kaldi_for_dummies_directories)

#### Documentation: 
A good documentation is provided: [kaldi-asr](http://kaldi-asr.org/doc/about.html#about_reference)

### C++

[Google C++ style guide](https://google.github.io/styleguide/cppguide.html)

### Java

#### Documentation
[Maven](https://maven.apache.org/) automatically creates documentation for your API.

[back to TOC](#table-of-contents)
