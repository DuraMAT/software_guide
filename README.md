

#  Guidelines for the open-source software development


## Purposes
To help you share software products effectively, including:

- Sharing best practices in software dissemination

- Save time and effort in the dissemination process

- Establishing some consistency across projects

- Getting you (and DuraMat) more credit for software products


## Overview of dissemination levels
The level of dissemination should depend on the purpose of the software

<img src="https://github.com/DuraMAT/software_guide/blob/main/doc_img/levels.png" width="700"/>



## Level 1: 

To do list for Level 1:
<!-- TOC tocDepth:2..3 chapterDepth:2..6 -->

 - [1.1 Approval for code release](#11-approval-for-code-release)
 - [1.2 Inline code documentation](#12-inline-code-documentation)
 - [1.3 Add README](#13-add-readme)
 - [1.4 Add LICENSE](#14-add-license)

<!-- /TOC -->


### 1.1 Approval for code release 
Follow Laboratory-specific guidelines for approval to release your code

### 1.2 Inline code documentation

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


## Level 2: Repository used for lifetime of a project 

### 2.1 All Level 1 items

### 2.2 Ensure that DOE requirements are being met
In addition to lab-specific guidelines, ensure that DOE requirements are being met. For example, this likely includes:
- Software Record (gets recorded in [OSTI.gov](https://www.osti.gov/) and helps in reporting purposes / credit)
- Lab-specific approval to release code

### 2.3 Set up a public facing Github repository
This could be hosted by the project organization, by your institution, or by your research lab. Examples include:
- github.com/DURAMAT
- github.com/NREL


### 2.4 Additional README components
- Screenshot or visual aid of the project
- Current status of the project (testing use, production use, actively maintained, etc.)
- Funding information and institutional branding (logo, funding acknowledgement text)

### 2.5 Add Contributor license agreement (CLA)

Example of CLA (the bottom of the LBL BSD-3 license):
>You are under no obligation whatsoever to provide any bug fixes, patches, or upgrades to the features, functionality or performance of the source code ("Enhancements") to anyone; however, if you choose to make your Enhancements available either publicly, or directly to Lawrence Berkeley National Laboratory or its contributors, without imposing a separate written license agreement for such Enhancements, then you hereby grant the following license: a non-exclusive, royalty-free perpetual license to install, use, modify, prepare derivative works, incorporate into other computer software, distribute, and sublicense such enhancements or derivative works thereof, in binary and source code form.

(*https://spdx.org/licenses/BSD-3-Clause-LBNL.html*)


### 2.5 Use a standard layout for the repository 
You can look up standard project layouts for the programming language you are using. Some details of the layout may depend on the tools you are using for other tasks such as code distribution or continuous integration. An example is shown as:

<img src="https://github.com/DuraMAT/software_guide/blob/main/doc_img/layout.png" width="300"/>

Files (like setup.py) can help users install the correct dependencies with the correct versions to ensure your software runs smoothly with an example as follows:

<img src="https://github.com/DuraMAT/software_guide/blob/main/doc_img/setup.png" width="300"/>

### 2.5 Add a consistent versioning scheme

### 2.5 Ensure your software is easy to install locally

### 2.5 Report your software to your funding
Report your software to your funding program so it can be included in accomplishments




## Level 3: 
