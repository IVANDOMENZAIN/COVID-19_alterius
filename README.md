# COVID-19_alterius
Public repository for statistical analysis of epidemiological data on COVID-19

This repository is administered by [@IVANDOMENZAIN](https://github.com/IVANDOMENZAIN), Division of Systems and Synthetic Biology, Department of Biology and Biological Engineering, Chalmers University of Technology

## Installation
### Required Software
* [R](https://www.r-project.org/) (version v3.6 or later)
* [RStudio](https://rstudio.com/) (version v1.2 or later)
* [Rtools](https://cran.r-project.org/bin/windows/Rtools/) (in case of a windows setup)
* [Git](https://git-scm.com/) (or any Git client of your choice, e.g. [Github Desktop](https://desktop.github.com/))

### Installation Instructions
* Clone locally this repository.

## Repository Structure
--------------------
    |- code/            # all programmatic code relating to the project
    |  +- templates/    # scripts for generating template files
    |
    |- data/            # all data from the study
    |  |- raw_internal/ # raw data generated in-lab or by collaborators, will not be altered
    |  |- raw_external/ # data from third-party sources, databases etc, will not be altered
    |     +- colormaps/ # color palettes used for all figures
    |
    |- doc/             # documentation for the study and other explanatory material
    |
    |- results          # all output from workflows and analyses
    |  |- figures/      # graphs, designated for manuscript figures or publishable material
    |  +- pictures/     # diagrams, images, and other non-graph graphics
    |
    |- .gitignore       # files that will not sync to Github
    |- LICENSE          # license
    |- README.md        # the top level description of content
    +- requirements.txt # the requirements file for reproducing the analysis environment

## Development Guidelines

Anybody is welcome to contribute to the development of **COVID-19_alterius**, but please abide by the following guidelines.

Each function should start with a commented section describing the function and explaining the parameters. Existing functions can clarify what style should be used. When making *any* changes to an existing function (`*.R`-file), change the date and name of developer near the bottom of this commented section.

### Bugfixes, new features and functions
* For any development, whether bugfixes, introducing new functions or new/updated features for existing functions: make a separate branch from `devel` and name the branch for instance after the function/feature you are fixing/developing. If you work on a fix, start the branch name with `fix/`, if you work on a feature, start the branch name with `feat/`. Examples: `fix/format_reactions` or `feat/new_algorithms`.
* Make commits to this branch while developing. Aim for backwards compatibility.
* When you are happy with your new function/feature, make a pull request to the `devel` branch. Also, see [Pull request](#pull-request) below.

### Semantic commits
Use semantic commit messages to make it easier to show what you are aiming to do:
* `chore`: updating binaries (`R` workspaces), UniProt databases, omics data files, etc.
* `doc`: updating documentation (`README` files) or explanatory comments in functions.
* `feat`: new feature added, e.g. new function introduced / new parameters / new algorithm / etc.
* `fix`: bugfix.
* `refactor`: see [code refactoring](https://en.wikipedia.org/wiki/Code_refactoring).
* `style`: minor format changes of functions (spaces, semi-colons, etc., no code change).

Examples:
```
feat: add new proteins normalization method
chore: update UniProt database for CENPK113-7D
fix: variable name corrected in `load_ProtData` function
```
More detailed explanation or comments can be left in the commit description.

### Pull request
* No changes should be directly commited to the `master` or `devel` branches. Commits are made to side-branches, after which pull requests are made for merging with `master` or `devel`.
* The person making the pull request and the one accepting the merge _cannot_ be the same person.
* A merge with the master branch invokes a new release.

