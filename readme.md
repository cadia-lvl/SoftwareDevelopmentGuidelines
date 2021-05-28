<h1 align="center">
LVL Software Development Guidelines
</h1>

<p align="center"><i>
This repository contains the software development guidelines for LVL.<br/>
Center for Analysis and Design of Intelligent Agents, Language and Voice Lab <br/>
<a href="https://ru.is">Reykjavik University</a>
</i></p>

<img src="https://user-images.githubusercontent.com/9976294/86356451-cddbc780-bc5b-11ea-89fb-f2d5d242d661.png" alt="Cover Image" align="center"/>
<!-- <div>Icons made by <a href="https://www.flaticon.com/free-icon/strategy_2819519?term=Roadmap&page=1&position=5" title="surang">surang</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></-->

<!-- omit in toc -->
## Table of Contents

<details>
<summary>Click to expand</summary>

- [1. About the guide](#1-about-the-guide)
  * [1.1. Goals](#11-goals)
  * [1.2. TLDR](#12-tldr)
  * [1.3. Other resources](#13-other-resources)
  * [1.4. Deliverables](#14-deliverables)
  * [1.5. Contributors](#15-contributors)
  * [1.5.1. Notes for writing the guide](#151-notes-for-writing-the-guide)
    + [1.5.2. Maintainers](#152-maintainers)
  * [1.6. Dictionary](#16-dictionary)
- [2. Project Structure](#2-project-structure)
  * [2.1. Template README.md](#21-template-readmemd)
- [3. License](#3-license)
- [4. Documentation](#4-documentation)
  * [4.1. Code](#41-code)
    + [4.1.1. Python](#411-python)
  * [4.2. Publishing documentation](#42-publishing-documentation)
  * [4.3. Developer documentation](#43-developer-documentation)
  * [4.4. User guide](#44-user-guide)
- [5. Version control](#5-version-control)
  * [5.1. Workflow](#51-workflow)
    + [5.1.1. Branching](#511-branching)
    + [5.1.2. Pull requests](#512-pull-requests)
  * [5.2. Commits](#52-commits)
  * [5.3. Semantic versioning](#53-semantic-versioning)
  * [5.4. Further information](#54-further-information)
- [6. Testing](#6-testing)
  * [6.1. Unit tests](#61-unit-tests)
  * [6.2. Web](#62-web)
    + [6.2.1. Browsers](#621-browsers)
    + [6.2.2. Deployment strategy](#622-deployment-strategy)
  * [6.3. User testing](#63-user-testing)
- [7. Supporting tools](#7-supporting-tools)
  * [7.1. Linters](#71-linters)
  * [7.1.1. Python](#711-python)
  * [7.1.2. JavaScript](#712-javascript)
  * [7.1.3. Bash](#713-bash)
  * [7.1.4. CSS](#714-css)
- [7.2. Style](#72-style)
  * [7.2.1. Python](#721-python)
- [8. Continuous integration](#8-continuous-integration)
  * [8.1. Github Actions](#81-github-actions)
    + [8.1.1. Further information](#811-further-information)
- [9. Packaging / Releasing](#9-packaging---releasing)
  * [9.1. Versioning](#91-versioning)
  * [9.2. Python](#92-python)
  * [9.3. Docker](#93-docker)
- [10. Examples](#10-examples)
- [11. Other resources](#11-other-resources)
- [12. License](#12-license)

<small><i><a href='http://ecotrust-canada.github.io/markdown-toc/'>Table of contents generated with markdown-toc</a></i></small>
</details>

## 1. About the guide

### 1.1. Goals
These guidelines should help us achieve the following goals:
- Make our lives **easier** by not having to reinvent the wheel in each of our induvidual projects and find **good resources** and guides which we are all aware of.
- Help us write **quality software** by following good software development proceedures.
- Enable **collaboration** by having collaboration as a part of our workflow.

### 1.2. TLDR
The guide can be summarized as the following:
- Have a good `README.md`, see our [template](readme_template.md).
- Provide a `License`.
- Write documentation within the code so that you can automatically generate it later (if you need to).
- Use `git` for semantic versioning.
- Test your code, preferably automatically.
- Setup "GitHub actions" to run testing and linting.
- Check out our [examples](#11-examples).

### 1.3. Other resources
- [Compute](https://github.com/cadia-lvl/compute) for information about the cluster (called Terra) at LVL.
- [SÍM guidelines](SIM_software_development_standards.pdf) for writing and delivering software.

### 1.4. Deliverables
The [SÍM guidelines](SIM_software_development_standards.pdf) define the deliverable types APP, MOD, ADD-ON, WEB and RES.

These types are quite abstract and LVL does not deliver all of them.
Due to this we further break down these deliverables to offer more concrete guidelines:
- UI (webpage, mobile, browser-plugin) = WEB, APP or ADD-ON
- Server (restful webserver) = WEB
- Library (python package) = MOD
- Model (trained model, runnable trained model) = RES, APP or MOD
- Command line client (python package, bash) = APP, MOD

Translating from the SÍM requirements to these deliverables will need to be discussed with a SÍM project manager to answer the question of "what do they expect?".

### 1.5. Contributors
To contribute to this project please submit a pull request to the master branch and request a review from someone in the software guidelines team. If you have a lot of suggestions feel free to make multiple requests.

### 1.5.1. Notes for writing the guide

- This guide should be short and simple and mention what is required or optional
- Offer examples
- Add links to good resources

<a href="https://github.com/cadia-lvl/SoftwareDevelopmentGuidelines/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=cadia-lvl/SoftwareDevelopmentGuidelines" />
</a>
<!-- Made with [contributors-img](https://contributors-img.web.app). -->

#### 1.5.2. Maintainers

* Gunnar Thor Örnólfsson <gunnaro@ru.is>
* Judy Yum Fong <judyfong@ru.is>
* Safa Jemai
* Staffan J. S. Hedström <staffanh@ru.is>
* Smári Freyr Guðmundsson <smarig@ru.is>
* Þorsteinn Daði Gunnarsson <thorsteinng@ru.is>
### 1.6. Dictionary

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

## 2. Project Structure

Try to maintain a standardized project structure across your projects, as they always need to contain certain things. We suggest the following:

```
README.md  # See more information below
LICENSE    # See license section
docs/      # Contains automatically generated documentation in HTML.
```

Other scripts such as .py and .sh files should be in the root folder.

### 2.1. Template README.md
A readme.md template can be found [here](./readme_template.md).

[back to TOC](#table-of-contents)

## 3. License
All of the projects we work on need to have licenses. A single LICENSE file, mentioned and linked from the README, suffices. Adding a license header in every single file is optional.

If a project does not contain a license, the default copyright is in place which means that no-one is allowed to make derivative work with your code.

We want our code to be freely available for everyone so we prefer permissive licenses such as
- Apache 2.0 (quite permissive)
- MIT License (very permissive)
- CC BY 4.0 (for resources)

For more help choosing a license, see [Choosing a license](https://choosealicense.com/). Keep in mind that if you are working through SÍM you have agreed to use open licenses such as these. Furthermore, according to RU are the copyright owner.

When a license has been chosen, simply copy the license text, fill in any additional information required (like copyright owner and year) and write it to a LICENCE file in the repository.

[back to TOC](#table-of-contents)

---

## 4. Documentation
We all know that documentation is key if software is supposed to be usable.
Writing documentation can be hard but we have some suggestions to make it easier, but keep in mind that a good `#Running` section the `README.md` is complementary to the documentation, i.e. you need to write both.
- The `#Running` section handles common use-cases. This can be seen as a small [user guide](#54-user-guide).
- Write the documentation for functions and classes in your code using your language's conventions since all (common) languages have tools which can extract this documentation. This documentation is more detailed than the  section but can also contain the same examples.

### 4.1. Code
- Use **easy to understand variables and function names**, that is avoid ambiguous names.
- Settle on a **single format** for the documentation. This is for automatic documentation generation.
- When you have settled on a format, find a **tool** which supports that format which can generate HTML and place it in the `docs/` folder.
- Write documentation in English, unless you have a good reason not to do so.
- Be sure to define **accepted inputs** and **return values**.

#### 4.1.1. Python
We suggest the following format and tool for Python
- Format: [Google](https://github.com/google/styleguide/blob/gh-pages/pyguide.md#38-comments-and-docstrings). It's easily readable in code, widely support and not verbose.
- Tool: [`Sphinx` with `napoleon`](https://www.sphinx-doc.org/en/master/usage/extensions/napoleon.html)

### 4.2. Publishing documentation
Given that you have generated HTML pages using your documentation tool, this documentation can be hosted on GitHub using [github-pages](https://pages.github.com/).
This allows us to host a website directory from our code respositories.
This avoids us having to host the documentation in some remote server.

### 4.3. Developer documentation
For larger projects a developer guide can be helpful for newcomers.
These contain **installation guides** and **contribution guidelines** or any information that would help a developer use and modify this codebase faster.

### 4.4. User guide
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

## 5. Version control
Within Cadia-LVL, using git for version control is required. A clean repository with descriptive comments makes for a good representation of your project which makes it easier for new developers to join it. The following is a way to maintain a project as such.

### 5.1. Workflow
We use the [GitHub flow](https://guides.github.com/introduction/flow/) workflow.
We further clarify how we use this workflow in the next sections.

All merges to the master branch should include semantic version tags as listed below.

Here is a short guide 

#### 5.1.1. Branching
In short, **the master branch should always contain production ready code**.
To achieve this, create "feature branches" from the master branch.
In the feature branch you develop your changes.
When the work is done, create/open a "Pull Request" in GitHub.

#### 5.1.2. Pull requests
When you have finished working on the feature branch you should create a **pull request** to the master branch.
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

### 5.2. Commits
Every commit message should include a short description of work being commited.
Pull request comments should be more detailed.

### 5.3. Semantic versioning
Version tags can be informative, especially to current users. Given a version number *v[major].[minor].[patch]*, increments represent the following:
- Major: Incompatible API changes, ***when you break something***
- Minor: Added backwards compatible functionality, ***when you add features***
- Patch: Backwards compatible fixes, ***when you fix bugs***

### 5.4. Further information
- [Read more about semantic versioning](https://semver.org/) and [how to use tags to apply semantic versioning](https://www.atlassian.com/git/tutorials/inspecting-a-repository/git-tag).
- Developers and maintainers of a project should always [Watch](https://docs.github.com/en/free-pro-team@latest/rest/reference/activity#watching) their repos to be notified of all issues and pull requests created.

[back to TOC](#table-of-contents)

---

## 6. Testing
How do you know that your code works?
No-one writes code that is without bugs, and even though you could, testing the code might provide useful feedback (design, userability, architecture, etc.).
We suggest testing your code often and thouroughly.
Since doing that "manually" can be dull and cumbersome, we further suggest making these tests automatic.

### 6.1. Unit tests
Unit tests are conceptually the smallest tests possible, they can be thought of as "function tests", i.e. testing wether the function works.
All projects should attempt to do as much unit testing as possible.
At minimum aim to have tests for mission critical algorithms and functions.
Every programming language has a unit testing framework, google it.

- Python: [pytest](https://docs.pytest.org/en/stable/)

### 6.2. Web
A huge part of the web is portability and accessibility, so making sure your website works on all major devices and platforms is very important.

#### 6.2.1. Browsers
When testing your website keep in mind the demographic that will be using the site, what devices they are using (mobile vs. desktop), and which browsers.
Preferebly test each deplpoyment on these devices and browsers.
You can see browsers usage statistics [here](https://en.wikipedia.org/wiki/Usage_share_of_web_browsers#Summary_tables) to decide which browsers to test.

Major browsers on desktop are:

- Chrome
- Firefox 
- Safari 
- Edge

Major browsers for mobile are: 
- Chrome 
- Safari 
- Samsung Internet

[Caniuse.com](https://caniuse.com/) is helpful if you are unsure about browser support for specific features.

If for some specific and clear reason a particular browser is needed make sure it is clearly stated on the page.
You can use the [User-Agent](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/User-Agent) HTTP header to display warnings to all unsupported browsers.

#### 6.2.2. Deployment strategy
Keep two entirely separate deployments up and running, staging and production.
Deploy all changes first to the staging environment (this can be done automatically).

Preferably have multiple users test all major changes on the staging deployment before deploying to production.
This part could be done automatically but is often time consuming and difficlut to keep up to date.
Suggested tools for automated testing: [Selenium with Python](https://selenium-python.readthedocs.io/index.html) and [Cucumber](https://github.com/cucumber/cucumber)


### 6.3. User testing
User testing is a great way to see how the users interact with your product. 
However, user testing is difficult to do well.
When doing user tests keep the following points in mind.

- `User tests should only be used if you have planned time to make adjustments`
	- There is no reason to spend time user testing if the results won't be used to make adjustments and improve the product.

- `User testing should focus on a specific task`
	- Focusing on a specific scope or task helps to keep the user focusing on what is important. This does not mean the same user can not test different tasks, only that each task you give the users should be clearly defined.

- `Up to 4 people for tests`
	- Asking too many users to do the same tests will only result in more of the same responses. Every users experience matters and should be taken into account. If you have more users to test, think about trying to test different things or do another round when adjustments have been made from the first one.

- `Testing prototypes often gives no useful information `
	- Users will most likely point out things that you know are missing and are less likely to give the feedback you are looking for. This can be reduced somewhat by targetting very specific tasks early in the development, see point about specific tasks.


[back to TOC](#table-of-contents)

---

## 7. Supporting tools
When writing code, additional tools can help you find bugs, make your code look consistent and generally help you write better code.

### 7.1. Linters
Linters perform **static analysis** on code without running it.
They alert you of **possible errors**, **missing documentation** or **overly complex code** without writing tests.
They are easily incorporated into the continuous integration system and should be run on "Push" to notify of errors.
Using (some) linters is **required** in all projects.
Adding linters to your **IDE** is very easy and can be configured to run on file-save.

### 7.1.1. Python
For Python we suggest the following tools for all projects.
- Common errors: [`flake8`](https://github.com/PyCQA/flake8)
- Type checks: [`mypy`](https://github.com/python/mypy)
- Documentation checker: [`pydocstyle`](https://github.com/PyCQA/pydocstyle)

### 7.1.2. JavaScript
- Best practices and errors: [`eslint`](https://www.npmjs.com/package/eslint)

### 7.1.3. Bash
- Best practices and errors: [`shellcheck`](https://www.shellcheck.net/)

### 7.1.4. CSS
- Best practices and errors: [`stylelint`](https://www.npmjs.com/package/stylelint)

## 7.2. Style
Maintaining the same style across a project makes the code more readable.
We suggest using a tool which automatically formats/styles your code.
This eliminates inconsistent styles in the code and allows you to focus on the rather than the format.

### 7.2.1. Python
We highly suggest [`black`](https://github.com/psf/black)

## 8. Continuous integration
Continuous integration is a way to **build software (compile), automatically run tests, lint, check documentation and alert developers when something is wrong**.
We suggest running all these steps automatically in the CI system.
We suggest using **Github Actions** as a CI system for all your projects.

### 8.1. Github Actions
Simply navigate to your repository and click the **Actions** on the right side of the *Pull request* button.
Here you can choose to use workflows from others or click **set up a workflow yourself** to create your own.
This defines the steps you would like to perform when you push changes.

Your workflow should run at minimum each time a push or a pull request is made to the master.
It is also recomended to run a [scheduled](https://help.github.com/en/actions/reference/events-that-trigger-workflows#scheduled-events-schedule) workflow once a day, in-case a dependency of your project is updated and breaks your code.

An example workflow can be found [here](./workflow_example.md)

#### 8.1.1. Further information
- [Language and framework guidelines](https://help.github.com/en/actions/language-and-framework-guides) 
- [Packaging on Github](https://help.github.com/en/actions/publishing-packages-with-github-actions/about-packaging-with-github-actions) (optional)
- [Workflow triggers](https://help.github.com/en/actions/reference/events-that-trigger-workflows#webhook-events)
- [Further on triggering workflows](https://help.github.com/en/actions/reference/workflow-syntax-for-github-actions#on).
- [Further on jobs](https://help.github.com/en/actions/reference/workflow-syntax-for-github-actions#jobs).

[back to TOC](#table-of-contents)

---

## 9. Packaging / Releasing
When a project should be released try to:
- Package it so that it can be **easily used by other people**.
- Make sure that it includes all the main parts mentioned in the [2.2. TLDR](#22-tldr) section.
- Make sure that all changes have been committed and a proper README file is in place so that the release process can be repeated by someone else.

### 9.1. Versioning
All deliverables should be referenced with a git tag (f.ex. a version).
This is done so that the code of a deliverable can be easily reviewed and for easy recreation.
- Such as for milestone 4, add the `m4` tag. Here's an example for the [samromur-asr repo](https://github.com/cadia-lvl/samromur-asr/releases/tag/m4).

### 9.2. Python
We suggest using `poetry` for dependency management, building and packaging.

### 9.3. Docker
For more complex deliverables (which have many dependencies) we also recommend packaging the deliverable using docker.

[back to TOC](#table-of-contents)

---

## 10. Examples
- An example of good documentation is provided: [kaldi-asr](http://kaldi-asr.org/doc/about.html#about_reference)

## 11. Other resources
- [Web Technologies reference](https://developer.mozilla.org/en-US/docs/Web)
- [bash help usage example](https://github.com/cadia-lvl/broadcast_data_prep/blob/master/ruv/compare_hypothesis_and_expanded_888.sh)
- [Better Programming has a short list of Bash Best Practices](https://medium.com/better-programming/best-practices-for-bash-scripts-17229889774d)
- Explains the Kaldi folder structure: [kaldi-for-dummies](http://kaldi-asr.org/doc/kaldi_for_dummies.html#kaldi_for_dummies_directories)

## 12. License
CC BY 4.0

[back to TOC](#table-of-contents)
