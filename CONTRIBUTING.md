<!-- omit in toc -->
# Contributing to CADIA-LVL

👍🎉 First off, thanks for taking the time to contribute! 🎉👍

The following is a set of guidelines for contributing to CADIA-LVL and its packages, which are hosted in the [CADIA-LVL Organization](https://github.com/cadia-lvl) on GitHub. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

<!-- omit in toc -->
## Table of Contents

<details>
<summary>Click to expand</summary>

- [1. Code of Conduct](#1-code-of-conduct)
- [2. What should I know before I get started](#2-what-should-i-know-before-i-get-started)
  - [2.1. Cadia-LVL and Packages](#21-cadia-lvl-and-packages)
- [3. How to contribute](#3-how-to-contribute)
  - [3.1. How to report a bug](#31-how-to-report-a-bug)
  - [3.2. How to submit a feature request](#32-how-to-submit-a-feature-request)
  - [3.3. How to create a pull requests](#33-how-to-create-a-pull-requests)
- [4. Styleguides](#4-styleguides)
  - [4.1. Git Commit Messages](#41-git-commit-messages)
  - [4.2. JavaScript Style Guide](#42-javascript-style-guide)
  - [4.3. Python Style Guide](#43-python-style-guide)
  - [4.4. Markdown Style Guide](#44-markdown-style-guide)

</details>

## 1. Code of Conduct

This project and everyone participating in it is governed by the [Cadia-LVL Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report unacceptable behavior to [lvl@ru.is](mailto:lvl@ru.is).

## 2. What should I know before I get started

### 2.1. Cadia-LVL and Packages

Cadia-LVL is a large open source project &mdash; it's made up of over [50 repositories](https://github.com/cadia-lvl). When you initially consider contributing to Cadia-LVL, you might be unsure about which of those 50 repositories implements the functionality you want to change or report a bug for. This section should help you with that.
Here's a list of the big ones:

<details>
<summary>List of all repositories</summary>

- [broadcast_data_prep](https://github.com/cadia-lvl/broadcast_data_prep) - This repository has scripts to extract data from various sources for ASR and speaker diarization.
- [compute](https://github.com/cadia-lvl/compute) - LVL Computing Resources
- [DAD](https://github.com/cadia-lvl/DAD) - Detect Audio Defects
- [deCODE](https://github.com/cadia-lvl/deCODE) - Voice Source and Vocal tract features
- [docker-festival](https://github.com/cadia-lvl/docker-festival) - Text-to-Speech tutorial at SLTU 2016
- [dscore](https://github.com/cadia-lvl/dscore) - Diarization scoring tools.
- [Eyra](https://github.com/cadia-lvl/Eyra)
- [FeatExtDiarization](https://github.com/cadia-lvl/FeatExtDiarization)
- [festival](https://github.com/cadia-lvl/festival) - Festival Speech Synthesis System
- [ice-asr](https://github.com/cadia-lvl/ice-asr) - An automatic speech recognition environment for Icelandic based on Kaldi
- [Icelandic-Curses](https://github.com/cadia-lvl/Icelandic-Curses) - This is a list of icelandic taboo words/phrases.
- [Icelandic-textnorm](https://github.com/cadia-lvl/Icelandic-textnorm) - Text normalization for Icelandic
- [ictk](https://github.com/cadia-lvl/ictk) - 📚 Icelandic Corpora Toolkit -  A collection of scripts to use with various Icelandic text corpora
- [kaldi](https://github.com/cadia-lvl/kaldi) - This is not the official kaldi repository. If searching for Kaldi it is better to fork https://github.com/kaldi-asr/kaldi instead. This repository is built around the project to built an automatic speech recognizer for the Icelandic parliament, Althingi.
- [kaldi-speaker-diarization](https://github.com/cadia-lvl/kaldi-speaker-diarization) - This repository creates speaker diarization recipes to be used within the egs folder of kaldi.
- [lirfa](https://github.com/cadia-lvl/lirfa) - This packages the Alþingi ASR along with code which connects to the Alþingi servers.
- [LOBE](https://github.com/cadia-lvl/LOBE) - LOBE is a recording client made specifically for TTS data collections. It supports multiple collections, single and multi-speaker, and can prompt sentences based on phonetic coverage.
- [lvl_tts_frontend](https://github.com/cadia-lvl/lvl_tts_frontend) - TTS frontend processing for Icelandic
- [marytts](https://github.com/cadia-lvl/marytts) - MARY TTS -- an open-source, multilingual text-to-speech synthesis system written in pure java
- [merlin](https://github.com/cadia-lvl/merlin) - Fork of the Merlin project focused on improving Keras integration. The official project is located at:
- [metawave](https://github.com/cadia-lvl/metawave) - Meta-information tool for TTS datasets
- [NER](https://github.com/cadia-lvl/NER) - Named entity recognition for Icelandic
- [NLM](https://github.com/cadia-lvl/NLM) - A word-level neural language model
- [Ossian](https://github.com/cadia-lvl/Ossian)
- [POS](https://github.com/cadia-lvl/POS) - A part-of-speech tagger, tailored to Icelandic
- [punctuation-prediction](https://github.com/cadia-lvl/punctuation-prediction) - Support tools for punctuation and boundary detection for ASR output.
- [RPNSD](https://github.com/cadia-lvl/RPNSD) - PyTorch implementation of RPNSD
- [samromur-asr](https://github.com/cadia-lvl/samromur-asr) - 👾 An automatic speech recognition environment for Samrómur speech corpus.
- [SEA](https://github.com/cadia-lvl/SEA)
- [SLT2018](https://github.com/cadia-lvl/SLT2018) - Resources described in the paper \An Icelandic Pronunciation Dictionary for TTS

</details>

## 3. How to contribute

### 3.1. How to report a bug

Bugs are tracked as [GitHub issues](https://guides.github.com/features/issues/). After you've determined which repository your bug is related to, create an issue on that repository and provide the following information by filling in [the template](/bug_report.md).

Explain the problem and include additional details to help maintainers reproduce the problem:

- **Use a clear and descriptive title** for the issue to identify the problem.
- **Describe the exact steps which reproduce the problem** in as many details as possible. For example, start by explaining how you started Cadia-LVL, e.g. which command exactly you used in the terminal, or how you started Cadia-LVL otherwise. When listing steps, **don't just say what you did, but explain how you did it**. For example, if you moved the cursor to the end of a line, explain if you used the mouse, or a keyboard shortcut and if so which one?
- **Provide specific examples to demonstrate the steps**. Include links to files or GitHub projects, or copy/pasteable snippets, which you use in those examples. If you're providing snippets in the issue, use [Markdown code blocks](https://help.github.com/articles/markdown-basics/#multiple-lines).
- **Describe the behavior you observed after following the steps** and point out what exactly is the problem with that behavior.
- **Explain which behavior you expected to see instead and why.**
- **Include screenshots and animated GIFs** which show you following the described steps and clearly demonstrate the problem. If you use the keyboard while following the steps, **record the GIF with the [Keybinding Resolver](https://github.com/cadia-lvl/keybinding-resolver) shown**. You can use [this tool](https://www.cockos.com/licecap/) to record GIFs on macOS and Windows, and [this tool](https://github.com/colinkeenan/silentcast) or [this tool](https://github.com/GNOME/byzanz) on Linux.

### 3.2. How to submit a feature request

This section guides you through submitting an enhancement suggestion for a Cadia-LVL project, including completely new features and minor improvements to existing functionality. Following these guidelines helps maintainers and the community understand your suggestion :pencil: and find related suggestions :mag_right:.

When you are creating an enhancement suggestion, please [include as many details as possible](#how-do-i-submit-a-good-enhancement-suggestion). Fill in the [feature request template](./templates/feature_request_template.md), including the steps that you imagine you would take if the feature you're requesting existed.

Enhancement suggestions are tracked as [GitHub issues](https://guides.github.com/features/issues/). After you've determined [which repository](#cadia-lvl-and-packages) your enhancement suggestion is related to, create an issue on that repository and provide the following information:

- **Use a clear and descriptive title** for the issue to identify the suggestion.
- **Provide a step-by-step description of the suggested enhancement** in as many details as possible.
- **Provide specific examples to demonstrate the steps**. Include copy/pasteable snippets which you use in those examples, as [Markdown code blocks](https://help.github.com/articles/markdown-basics/#multiple-lines).
- **Describe the current behavior** and **explain which behavior you expected to see instead** and why.
- **Include screenshots and animated GIFs** which help you demonstrate the steps or point out the part of Cadia-LVL which the suggestion is related to. You can use [this tool](https://www.cockos.com/licecap/) to record GIFs on macOS and Windows, and [this tool](https://github.com/colinkeenan/silentcast) or [this tool](https://github.com/GNOME/byzanz) on Linux.
- **Explain why this enhancement would be useful** to most Cadia-LVL users and isn't something that can or should be implemented as a community package / project.
- **Specify which version of a Cadia-LVL project you're using.**
- **Specify the name and version of the OS you're using.**

### 3.3. How to create a pull requests

The process described here has several goals:

- Maintain Cadia-LVL's quality
- Fix problems that are important to users
- Engage the community in working toward the best possible Cadia-LVL
- Enable a sustainable system for Cadia-LVL's maintainers to review contributions

Please follow these steps to have your contribution considered by the maintainers:

1. Follow all instructions in [the template](PULL_REQUEST_TEMPLATE.md)
2. Follow the [styleguides](#styleguides)
3. After you submit your pull request, verify that all [status checks](https://help.github.com/articles/about-status-checks/) are passing <details><summary>What if the status checks are failing?</summary>If a status check is failing, and you believe that the failure is unrelated to your change, please leave a comment on the pull request explaining why you believe the failure is unrelated. A maintainer will re-run the status check for you. If we conclude that the failure was a false positive, then we will open an issue to track that problem with our status check suite.</details>

While the prerequisites above must be satisfied prior to having your pull request reviewed, the reviewer(s) may ask you to complete additional design work, tests, or other changes before your pull request can be ultimately accepted.

## 4. Styleguides

### 4.1. Git Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line
- Consider starting the commit message with an applicable emoji:
  - :art: `:art:` when improving the format/structure of the code
  - :racehorse: `:racehorse:` when improving performance
  - :non-potable_water: `:non-potable_water:` when plugging memory leaks
  - :memo: `:memo:` when writing docs
  - :penguin: `:penguin:` when fixing something on Linux
  - :apple: `:apple:` when fixing something on macOS
  - :checkered_flag: `:checkered_flag:` when fixing something on Windows
  - :bug: `:bug:` when fixing a bug
  - :fire: `:fire:` when removing code or files
  - :green_heart: `:green_heart:` when fixing the CI build
  - :white_check_mark: `:white_check_mark:` when adding tests
  - :lock: `:lock:` when dealing with security
  - :arrow_up: `:arrow_up:` when upgrading dependencies
  - :arrow_down: `:arrow_down:` when downgrading dependencies
  - :shirt: `:shirt:` when removing linter warnings

### 4.2. JavaScript Style Guide

All JavaScript must adhere to [JavaScript Standard Style](https://standardjs.com/).

### 4.3. Python Style Guide

All Python must adhere to [PEP 8 Style Guide](https://www.python.org/dev/peps/pep-0008/)

### 4.4. Markdown Style Guide

All Markdown mostly adhere to [GitHub Markdown Style Guide](https://guides.github.com/features/mastering-markdown/).

We encourage you to use Markdown All in One, VS Code Extension.

Each repository should contain the following files:

- `README.md`
- `LICENCE.md`
- `CONTRIBUTING.md`
- `ROADMAP.md`

You will find templates for these files [here](./templates/).
