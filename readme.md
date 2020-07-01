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
  <details>
   <summary><a href="#dictionary">Dictionary</a></summary>
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


### Contributors
<a href="https://github.com/cadia-lvl/SoftwareDevelopmentGuidelines/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=cadia-lvl/SoftwareDevelopmentGuidelines" />
</a>
<!-- Made with [contributors-img](https://contributors-img.web.app). -->


### Deliverables
The [SÍM guidelines](https://docs.google.com/document/d/1O_yhAnMVft6AJNoRjOFFRwnZKN8YmEE6GNM_8w1tq14/edit) define the following deliverable types:
- APP: stand-alone application
- MOD: a module which can be embedded into other applications
- ADD-ON: a plugin to a larger framework
- WEB: website with UI and/or API
- RES: language resource

These types are quite abstract and LVL does not deliver all of them.
Due to this we further break down these deliverables to offer more concrete guidelines:
- UI (webpage, mobile, browser-plugin) = WEB, APP or ADD-ON
- Server (restful webserver) = WEB
- Library (python package) = MOD
- Model (trained model, runnable trained model) = RES, APP or MOD
- Command line client (python package, bash) = APP, MOD

Translating from the SÍM requirements to these deliverables will need to be discussed with a SÍM project manager to answer the question of "what do they expect?".


[back to TOC](#table-of-contents)

---

## Project Structure

It is a good idea to try to maintain a standardized project structure across our projects, as they always need to contain certain things. We suggest the following:

```
README.md
LICENSE
docs/
```
In this example, the docs folder contains other documents. Other scripts such as .py and .sh files should be in the root folder.

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
[Some motivation missing]


### All Projects

#### Code should be self-documenting 
When that’s not possible it should be well documented within comments and overall documentation. 

In the case of python, documentation can be automatically generated from “docstrings.” Other languages and frameworks have similar features. Use easy to understand variables and function names, that is avoid ambiguous names. Use consistent styles throughout the whole codebase. The code should also be consistent with the general guidelines of the programming language.

#### Developer documentation
Developer documentation should generally be in English. Developer guides would be like installation guides, API documentation, contribution guidelines, just any information that would help a developer use and modify this codebase faster. Along these lines, code examples, code snippets, and examples of (function/API) calls and the possible outputs would help users to understand much quicker.

#### User guides
User guides should be in the language of the users. User guides is documentation for user facing code. Within LVL example projects which might need user guides are [LOBE](https://github.com/cadia-lvl/LOBE.git) and [Eyra](https://github.com/cadia-lvl/Eyra.git) because both have user interfaces that don't involve code. These guides should also contain lots of examples. This can work as a tutorial within the webpage with popups that walks first time users through the different steps in a webpage or a standalone guide perhaps with videos or pictures walking users through the more difficult aspects of using the tool or webpage.

Add research papers to the repository in a docs folder if possible. [Eyra has a conference paper in its docs folder](https://github.com/Eyra-is/Eyra/blob/master/Docs/Petursson_et_al_2016.pdf)

#### Publishing documentation
Documentation for git repositories can live in the docs folder as a website. Github has a feature called github-pages. This allows us to host a website directory from our code respositories. This is especially useful if we have user guides or API documentation. Thus, we don't need a whole server just for a few webpages. GitHub has a step by step guide of how to do that on their platform which is linked [here](https://pages.github.com/).

#### More information 
We have provided a template for your projects' [README.md file](readme_template.md). It provides both the minimum sections and the optional sections. You can read more about why those sections here at [GitHub's guide](https://guides.github.com/features/wikis/). After you've read that explanation, you can delete whichever sections you don't need. 


### APIs
The documentation should explain how to use an endpoint and outline outputs for both good and bad input. Remember, it's better to have some documentation than none at all. These often can be automatically generated and put into a docs folder in your repository as a html pages which can then be hosted as a Github Pages website.

#### Further information
- [API documentation example](http://docs.apis.is/)
- [Eyra API documentation](https://github.com/cadia-lvl/Eyra/blob/master/ClientServerAPI.md)

### Command-line tools
Terminal based software should have a help option: `--help` or `-h` or both. Typing in the filename then either of these options should bring up some text explaining what the script does, an example command, and list explanations of the parameters.

[TODO: include code snippets for creating help in python and bash directly in the file.]
#### Further information
- [broadcast_data_prep/master/ruv/extract_from_ruv_api.py has an example at the bottom](https://github.com/cadia-lvl/broadcast_data_prep/blob/master/ruv/extract_from_ruv_api.py)
- [bash example](https://github.com/cadia-lvl/broadcast_data_prep/blob/master/ruv/compare_hypothesis_and_expanded_888.sh)

### Language/Tool specific documentation help
- [Python](examples.md#Python)
- [Bash](examples.md#bash)
- [C++](examples.md#C)
- [Java](examples.md#Java)

#### help
In python3.8, creating a help usage is really easy once you import the [argparse](https://docs.python.org/3/library/argparse.html) package.
[broadcast_data_prep/master/ruv/extract_from_ruv_api.py has an example at the bottom](https://github.com/cadia-lvl/broadcast_data_prep/blob/master/ruv/extract_from_ruv_api.py)

#### tools
[List of python tools to auto generate documentation](https://wiki.python.org/moin/DocumentationTools)

- [Sphinx](https://www.sphinx-doc.org/en/master/) : automatically creates documentation from docstrings. [example of PyTorch documentation generated by Sphinx](https://pytorch.org/docs/stable/nn.html#parameters)
- pdoc3 : Another python documentation tool is pdoc3 which also uses docstrings. Installing it is as easy as `pip3 install pdoc3`. Generating the documentation is `pdoc --html --output-dir docs <path-to-your-module-with-init-py>`. There should be no subdirectories.


[back to TOC](#table-of-contents)

---

## Version control
Within Cadia-LVL, using git for version control is required. A clean repository with descriptive comments makes for a good representation of your project which makes it easier for new developers to join it. The following guidelines describe a way to maintain a project as such.


### Workflow
If a project is public, **the master branch should always contain production ready code**. All merges to the master branch should include semantic version tags as listed below.

#### Branching
For smaller projects and teams, feature branching is sufficient, where each feature gets a branch, created from master, used while developing until it is merged into the master.

For larger projects, [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) is the recommended workflow. It includes two main branches, the master branch that stores release history and a development branch that lives between the master branch and feature branches. It also recommends a clear way to implement hotfixes.

#### Pull requests
When adding new features or updates to the master branch, developers should write a pull request and let at least one other team member review their code before merging.

Code reviews across projects are recommended but not required. Keeping more team members informed about your work can benefit the team as a whole.


### Commits
Every commit message should include a short description of work being commited. Pull request comments should be more detailed. 

### Semantic versioning
Version tags can be informative, especially to current users. Given a version number *v[major].[minor].[patch]*, increments represent the following:
- Major: Incompatible API changes, ***when you break something***
- Minor: Added backwards compatible functionality, ***when you add features***
- Patch: Backwards compatible fixes, ***when you fix bugs***

### Further information
- [Read more about semantic versioning](https://semver.org/)
- [How to use tags to apply semantic versioning](https://www.atlassian.com/git/tutorials/inspecting-a-repository/git-tag)
- [Back to top](https://github.com/cadia-lvl/SoftwareDevelopmentGuidelines#table-of-contents)

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

## Continuous integration

When **working on a project with others** and preferably while working alone, **Github Actions should be used for continuous integration**.

### What is Continuous integration?
Continuous integration is a way to **build software, automaticly run tests and alert developers when a test doesn't pass**. This way developers can fix mistakes before they pile up and become difficult to manage. It also gives developers more confidance in their code and minimizes unknown errors. 


### Getting started with Github Actions
Simply navigate to your repository and click the **Actions** on the right side of the *Pull request* button.
Here you can choose to use workflows from others or click **set up a workflow yourself** to create your own.

#### Triggering workflows
Your workflow should run at minimum each time a push or a pull request is made to the master. It is also recomended to run a [scheduled](https://help.github.com/en/actions/reference/events-that-trigger-workflows#scheduled-events-schedule) workflow once a day for building, testing and packaging projects. If workflows take a long time to run it is advisable to run them over night. 

#### Jobs
Jobs should at minimum include [testing](#testing) and [packaging](#packaging--releasing) for the project.

Multiple jobs can be specified within each workflow. Besides testing and packaging, which are required, it is also recommended to run a linter on the project to ensure consistent styling across the project.

Keep in mind that each job may take no longer than 6 hours to complete or it will be automatically ended.

When running a job we need to specify which machine it [runs on](https://help.github.com/en/actions/reference/workflow-syntax-for-github-actions#jobsjob_idruns-on). It is **strongly recommended to use github hosted runners**.

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

## Dictionary

| Word   | Meaning                                                |
| :----- | :-----------------------------------------------------:|
| ADD-ON | a plugin to a larger framework                         |
| APP    | stand-alone application                                |
| CD     | Continuous Deployment / Continuous Delivery            |
| CI     | Continuous Integration                                 |
| MOD    | a module which can be embedded into other applications |
| RES    | language resource                                      |
