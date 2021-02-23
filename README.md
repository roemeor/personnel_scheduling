# Personnel Scheduling Library
> This library provides data structures and code that are useful for personnel scheduling


We will have more documentation later.

## Install

To install on your computer, the easiest way may be to use a distribution such as Anaconda or Miniconda. 

I would recommend creating an own conda environment (see https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) for this project, you can set up the environment by calling `conda env create -f environment.yml` from the root directory of the clone of the git repository. 

After having done this, you can start Jupyter Lab from your original `base` environment, and choose the `personnel_scheduling` kernel that has all needed packages installed.


## General Project Structure

The project uses [nbdev](https://nbdev.fast.ai/) an environment where we can develop in notebooks, and code can be automatically exported in python files. This way, we can use multiple notebooks. (nbdev has a lot more functionality, but this is most important for us here.). Please find the documentation for nbdev at https://nbdev.fast.ai/

Currently, two basic notebooks (00_datastructures and 00_reporting) and two notebooks for shift scheduling problem instances (The Demassey instances, and the Dahmen instances), providing implementations of the rulesets and functionality for reading instances.


## Workflow for development and experimentation
When you have changed something in one of the non-experiment-notebooks, make sure that you save the notebook and execute the function `notebook2script()` (which you already find in the last cells of each notebook and at the beginning of the experimentation notebook).

After that, to make sure that everything is clean, it is recommended to shutdown and restart the current kernel.

## Workflow for collaboration / git

The repository is hosted on git, and you should regularly commit your changes to a git and push them to github. Please only develop in your own branches, you can later create pull requests that are merged in the master branch. See https://ericmjl.github.io/essays-on-data-science/workflow/gitflow/ for a good description of the workflow I intend to use.



### Before committing 

Before commiting, please do the following steps:
- save and close all notebooks
- make sure that all notebooks work
- call the follown cell which:
    - syncs the notebooks with the python-files
    - cleans the notebooks and removes all outputs.
- after running this cell, please just close this index-notebook without saving.


If there are any merge conflicts, conflicts in the auto-generated python files can be more or less ignored or resolved easily using "use mine or sth". To resolve conflicts in the notebooks, we should use the package nbdime.

If there are any merge conflicts, please open the local repo folder in the prompt and type `nbdime mergetool`, then you can resolve conflicts more easily.

