---
id: k6pqpyhgiyyl2vuzky78xfu
title: Documentation
desc: ''
updated: 1710154721771
created: 1710151461752
---

# Documentation
Documentation is an important step for all kind of projects.
Specially then, when you want to share it and used by the community.
Mostly the mayority of time is spend for coding and some small part for documentation.
To make the documentation easier and less timeconsuming, some packages are developped.


## Mkdocs
[Mkdocs](https://www.mkdocs.org) is a tool for documentation.
It can build out of a markdown (*.md) file a website.
Github provides the possibility to add "Actions" (actions that would be run after a specific event) and also host this website.

### Installation
We recommend to use Poetry for this task. Remember: the best practice would be using one environment for one project.
```bash
# basic installation
poetry add mkdocs

# for more material <https://squidfunk.github.io/mkdocs-material/>
poetry add mkdocs-material
```

Alternativaly it can also be done with Pypi:
```bash
# basic installation
pip install mkdocs

# for more material <https://squidfunk.github.io/mkdocs-material/>
pip install mkdocs-material
```
It also exist some other themes, which can be found here: <https://github.com/mkdocs/mkdocs/wiki/MkDocs-Themes>.  

### Project layout
If you run the first time `mkdocs new <project_name>`, it will create new folders for the documentation and a confic file (mkdocs.yml). 

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.  

### Configuration
Open the configuration file (mkdocs.yml) and customize it. This file has some basic functions, which can be very usefull.
This file was used in this project <https://commons-research.github.io/dataset-extractor-lotus/>.

```yaml
site_name: Dataset Extractor for LOTUS  #websitename (name of project) 
site_description: "Python script to extract data from the LOTUS Database" #description
site_url: https://commons-research.github.io/dataset-extractor-lotus/ #website to mkdocs (will be deployd after running 'mkdocs gh-deploy')
site_author: <your-name> #your name
repo_url: https://github.com/commons-research/dataset-extractor-lotus #Github repository
repo_name: GitHub - Dataset Extractor for LOTUS #name of repository

nav: #links to the documentation files in the "/docs" folder.
  - Home: index.md
  - About: about.md
not_in_nav: #files, which shouldn't be published with mkdocs, but still in the repo.
theme: readthedocs #theme
language: en

theme: #advanced changes
  name: material
  features:
    - navigation.tabs
    - navigation.sections
    - toc.integrate
    - navigation.top
    - search.suggest
    - search.highlight
    - content.tabs.link
    - content.code.annotation
    - content.code.copy
  language: en
  palette:
    - scheme: default
      toggle:
        icon: material/toggle-switch-off-outline 
        name: Switch to dark mode
      primary: teal
      accent: purple 
    - scheme: slate 
      toggle:
        icon: material/toggle-switch
        name: Switch to light mode    
      primary: teal
      accent: lime


copyright: |
  &copy; 2024 <a href="https://github.com/pamrein"  target="_blank" rel="noopener"> YOUR-NAME </a>
```

### Commands
* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.
* `mkdocs gh-deploy` - Deploy the documentation to GitHub pages.
* `mkdocs gh-deploy --help` - Print help of gh-deploy

