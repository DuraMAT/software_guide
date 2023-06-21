

#  Guidelines for the open-source software development

Table of content

<!-- TOC tocDepth:2..3 chapterDepth:2..6 -->

- [Purposes](#purposes)
- [Overview of dissemination levels](#overview-of-dissemination-levels)
- [Level 1:](#level-1)
    - [1.1 Approval for code release](#11-approval-for-code-release)
    - [1.2 Inline code documentation](#12-inline-code-documentation)
    - [1.3 Add README](#13-add-readme)
    - [1.4 Add LICENSE](#14-add-license)
- [Level 2: Repository used for lifetime of a project](#level-2-repository-used-for-lifetime-of-a-project)
    - [2.1 All Level 1 items](#21-all-level-1-items)
    - [2.2 Ensure that DOE requirements are being met](#22-ensure-that-doe-requirements-are-being-met)
    - [2.3 Set up a public facing Github repository](#23-set-up-a-public-facing-github-repository)
    - [2.4 Additional README components](#24-additional-readme-components)
    - [2.5 Add Contributor license agreement (CLA)](#25-add-contributor-license-agreement-cla)
    - [2.6 Use a standard layout for the repository](#26-use-a-standard-layout-for-the-repository)
    - [2.7 Add a consistent versioning scheme](#27-add-a-consistent-versioning-scheme)
    - [2.8 Ensure your software is easy to install locally](#28-ensure-your-software-is-easy-to-install-locally)
    - [2.9 Report your software to your funding](#29-report-your-software-to-your-funding)
- [Level 3:](#level-3)
    - [3.1 All Level 1 items](#31-all-level-1-items)
    - [3.2 All Level 2 items](#32-all-level-2-items)
    - [3.3 Implement a release system](#33-implement-a-release-system)
    - [3.4 Set up continuous integration (CI) tools](#34-set-up-continuous-integration-ci-tools)
    - [3.5 Check for consistent code formatting](#35-check-for-consistent-code-formatting)
    - [3.6 Add Documentation pages](#36-add-documentation-pages)
    - [3.7 Release large data sets with code](#37-release-large-data-sets-with-code)
    - [3.8 Upload to other code services](#38-upload-to-other-code-services)
    - [3.9 Submit to a code-centric journal (optional)](#39-submit-to-a-code-centric-journal-optional)
- [Some useful links](#some-useful-links)
- [Contributors](#contributors)

<!-- /TOC -->


## Purposes
To help you share software products effectively, including:

- Sharing best practices in software dissemination

- Save time and effort in the dissemination process

- Establishing some consistency across projects

- Getting you (and DuraMat) more credit for software products


## Overview of dissemination levels
The level of dissemination should depend on the purpose of the software

<img src="https://github.com/DuraMAT/software_guide/blob/main/doc_img/levels.png" width="700"/>



## Level 1: Basic repository to support a document
Typically, Level 1 repository is used to support and document published analyses for enhanced reproducibility – e.g., something akin to supporting information for a journal publication.

To build up Level 1 repository:
<!-- TOC tocDepth:2..3 chapterDepth:2..6 -->
- [1.1 Approval for code release](#11-approval-for-code-release)
- [1.2 Inline code documentation](#12-inline-code-documentation)
- [1.3 Add README](#13-add-readme)
- [1.4 Add LICENSE](#14-add-license)
<!-- /TOC -->

### 1.1 Get approval for code release 
Follow Laboratory-specific guidelines for approval to release your code

### 1.2 Add inline code documentation

Some notes:

 - The formatting of the docstring can depend on if you are autoconverting the docstrings to HTML documentation

 - Common formatting examples include reST (restructured text), Google formatting, epyDoc, etc.

 - You can add type hinting to further help in code readability as well as the ability to use static type checking  tools


Example of inline code documentation:

<img src="https://github.com/DuraMAT/software_guide/blob/main/doc_img/inline_example.png" width="600"/>



### 1.3 Add README

<img src="https://github.com/DuraMAT/software_guide/blob/main/doc_img/readme_example.png" width="900"/>

(*https://github.com/DuraMAT/pv-terms/blob/master/README.md*)



### 1.4 Add LICENSE

- Talk to your lab’s IP / IT departments for guidance

- BSD/MIT licenses are examples of very “open” licenses that allow others to do what they’d like with the software
    - BSD typically gives some more protection against others using your name to promote their product, e.g. “our commercial product uses
    - LBL-approved software technology for its analysis” or “uses the same algorithms developed by the brilliant scientist <your_name_here>”

- Be careful about choosing licenses that require all downstream code to also use the same license
    - e.g. GPL/Apache
    - e.g., if you leave DuraMat and work for a company, you may no longer be able to use your own code as companies typically avoid any GPL code

Example of license: 

> <font size= 1> BSD 3-Clause License
> 
> Copyright 2020-2023 Alliance for Sustainable Energy, LLC
> 
> Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:
> 
> Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
> 
> Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
> 
> The name of the copyright holder, contributors, the United States Government, the United States Department of Energy, or any of their employees may not be used to endorse or promote products derived from this software without specific prior written permission.
> 
> THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER, CONTRIBUTORS, UNITED STATES GOVERNMENT OR UNITED STATES DEPARTMENT OF ENERGY, NOR ANY OF THEIR EMPLOYEES, BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE. </font>

(*https://github.com/NREL/PV_ICE/blob/main/LICENSE.md*)


## Level 2: Repository to support an entire project
Typically, may serve as documentation for the innovations of an entire project, e.g., for multiple publications. However, the project may no longer be actively maintained after project end.

To build up Level 2 repository:
<!-- TOC tocDepth:2..3 chapterDepth:2..6 -->
- [2.1 All Level 1 items](#21-all-level-1-items)
- [2.2 Ensure that DOE requirements are being met](#22-ensure-that-doe-requirements-are-being-met)
- [2.3 Set up a public facing Github repository](#23-set-up-a-public-facing-github-repository)
- [2.4 Additional README components](#24-additional-readme-components)
- [2.5 Add Contributor license agreement (CLA)](#25-add-contributor-license-agreement-cla)
- [2.6 Use a standard layout for the repository](#26-use-a-standard-layout-for-the-repository)
- [2.7 Add a consistent versioning scheme](#27-add-a-consistent-versioning-scheme)
- [2.8 Ensure your software is easy to install locally](#28-ensure-your-software-is-easy-to-install-locally)
- [2.9 Report your software to your funding](#29-report-your-software-to-your-funding)
<!-- /TOC -->

### 2.1 All Level 1 items

### 2.2 Ensure that DOE requirements are being met
In addition to lab-specific guidelines, ensure that DOE requirements are being met. For example, this likely includes:
- Software Record (gets recorded in [OSTI.gov](https://www.osti.gov/) and helps in reporting purposes / credit)
- Lab-specific approval to release code

### 2.3 Set up a public facing Github repository
This could be hosted by the project organization, by your institution, or by your research lab. Examples include:
- [github.com/DURAMAT](https://github.com/DURAMAT)
- [github.com/NREL](https://github.com/NREL)


### 2.4 Additional README components
- Screenshot or visual aid of the project
- Current status of the project (testing use, production use, actively maintained, etc.)
- Funding information and institutional branding (logo, funding acknowledgement text)

### 2.5 Add Contributor license agreement (CLA)
A CLA defines the terms under which intellectual property has been contributed to a company/project.

Example of CLA (the bottom of the LBL BSD-3 license):
>You are under no obligation whatsoever to provide any bug fixes, patches, or upgrades to the features, functionality or performance of the source code ("Enhancements") to anyone; however, if you choose to make your Enhancements available either publicly, or directly to Lawrence Berkeley National Laboratory or its contributors, without imposing a separate written license agreement for such Enhancements, then you hereby grant the following license: a non-exclusive, royalty-free perpetual license to install, use, modify, prepare derivative works, incorporate into other computer software, distribute, and sublicense such enhancements or derivative works thereof, in binary and source code form.

(*https://spdx.org/licenses/BSD-3-Clause-LBNL.html*)


### 2.6 Use a standard layout for the repository 
You can look up standard project layouts for the programming language you are using. Some details of the layout may depend on the tools you are using for other tasks such as code distribution or continuous integration. An example is shown as:

<img src="https://github.com/DuraMAT/software_guide/blob/main/doc_img/layout.png" width="300"/>

### 2.7 Add a consistent versioning scheme
Examples include semantic versioning (v0.0.1) and date-based versioning (v2023.01.25); tools like [versioneer](https://pypi.org/project/versioneer/0.10/) may help.

### 2.8 Ensure your software is easy to install locally
Ensure your software is easy to install locally, including any necessary dependencies. For example, Python projects may include files such as setup.py or requirements.txt.

Files (like setup.py) can help users install the correct dependencies with the correct versions to ensure your software runs smoothly with an example as follows:

<img src="https://github.com/DuraMAT/software_guide/blob/main/doc_img/setup.png" width="600"/>

### 2.9 Report your software to your funding
Report your software to your funding program so it can be included in accomplishments




## Level 3: Repository for long-term projects
The project is intended to be used and maintained **long-term** by the project team and a community of users; project lives on even if/when initial developers exit the project

To build a Level 3 repository:
<!-- TOC tocDepth:2..3 chapterDepth:2..6 -->
- [3.1 All Level 1 items](#31-all-level-1-items)
- [3.2 All Level 2 items](#32-all-level-2-items)
- [3.3 Implement a release system](#33-implement-a-release-system)
- [3.4 Set up continuous integration (CI) tools](#34-set-up-continuous-integration-ci-tools)
- [3.5 Check for consistent code formatting](#35-check-for-consistent-code-formatting)
- [3.6 Add Documentation pages](#36-add-documentation-pages)
- [3.7 Release large data sets with code](#37-release-large-data-sets-with-code)
- [3.8 Upload to other code services](#38-upload-to-other-code-services)
- [3.9 Submit to a code-centric journal (optional)](#39-submit-to-a-code-centric-journal-optional)
<!-- /TOC -->

### 3.1 All Level 1 items

### 3.2 All Level 2 items

### 3.3 Implement a release system
One option is to use Github tags and releases. You can obtain a digital object identifier (DOI) for each release via [Zenodo](https://zenodo.org/):
- Link the Github repo to Zenodo
- Perform the release and tag it
- Update the README to include the DOI identifier Zenodo provides in the “how to cite” section

### 3.4 Set up continuous integration (CI) tools 
Continuous integration (CI) is a software practice that requires frequently committing code to a shared repository. Examples include Github actions to execute [CircleCI](https://circleci.com/), [Travis CI](https://www.travis-ci.com/), etc. against pull requests.

A code coverage tool (e.g. [coveralls](https://coveralls.io/)) can help establish that tests cover the entire codebase and publish test status (pass/fail, test coverage)

<img src="https://github.com/DuraMAT/software_guide/blob/main/doc_img/pvlib.png" width="600"/>

### 3.5 Check for consistent code formatting
A format checker (e.g., [pylint](https://pypi.org/project/pylint/) or [Python black](https://pypi.org/project/black/)) can be used to check the formatting of pull requests and/or automatically reformat code

### 3.6 Add Documentation pages
Documents can be deployed at several places (e.g., [Github pages](https://pages.github.com/), [Jupyter books](https://jupyterbook.org/en/stable/intro.html), [readthedocs](https://readthedocs.org/)). Documentation pages should provide:
- Getting started. Provide simple instructions to install the code and run a sample problem. Links here to Tutorials.
- Examples / Tutorials. Links here to illustrations of using the code.
- API reference. Links here to the documentation of each public Class, function and/or method. Note that this can typically be auto-generated.
- Release notes. Links here to logs of changes with each tagged release.

### 3.7 Release large data sets with code
- Data sets should be formally released into a separate archival repository (project-specific data hub (e.g., [DuraMat Data Hub](https://datahub.duramat.org/)), [Figshare](https://figshare.com/), [Dryad](https://datadryad.org/stash), etc.).


- If there are smaller files that are needed for the code, for example for unit tests, document and include these datasets in the repository, provided they have been cleared for release and are not infringing copyright from other sources or NDAs.

- Do not use links to local files on your computer!


### 3.8 Upload to other code services
Upload to PyPI, Conda, or other easy install code service.

<img src="https://pypi.org/static/images/logo-large.9f732b5f.svg" width="100"/>(https://pypi.org/)
<img src="https://docs.conda.io/en/latest/_images/conda_logo.svg" width="150"/>

### 3.9 Submit to a code-centric journal (optional)
Consider submitting to a code-centric journal publication such as [Journal of Open Source Software](https://joss.theoj.org/).

Example of [pvlib on JOSS](https://joss.theoj.org/papers/10.21105/joss.00884): 

<img src="https://github.com/DuraMAT/software_guide/blob/main/doc_img/pvlib_joss.png" width="500"/>

Reviews can be done via Github repo:

<img src="https://github.com/DuraMAT/software_guide/blob/main/doc_img/git_review.png" width="500"/>


## Some useful links
https://michal.karzynski.pl/blog/2019/05/26/python-project-maturity-checklist/

https://dbader.org/blog/write-a-great-readme-for-your-github-project

https://www.patricksoftwareblog.com/software-development-checklist-for-python-applications/

## Contributors
Anubhav Jain, Silvana Ovaitt, Cliff Hansen, Robert White, Baojie Li
