# NeuroSpin fMRI workshop 2023
February 14-15-16  
Organization: Pauline Favre  
Speakers:
- Day 1: Preprocessing. Antonio Moreno, Yann Leprince
- Day 2: Encoding analyses. Florent Meyniel
- Day 3: Decoding analyses and functional connectivity. Bertrand Thirion

# Videos of the talk
Available on the [neurospin's wiki](https://www.neurospin-wiki.org/pmwiki/Main/MRIDataAnalysisTutorials)

# Slides
Slides from the different speakers

# Notebooks

Notebooks for fMRI training that took place at Neurospin.  
There are two options to run the notebooks.

## Binder link:

Link to base of repository to *access and run* all notebooks:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/neurospin/fMRI_workshop/HEAD)

**Note**: Running multiple notebooks without shutting down any kernels of ones you have finished with might lead to a notebook crashing because of exceeding the 2GB of memory allocated by Binder. You can shut down the kernels of individual notebooks to free up memory or shut down all kernels to have a fresh start. 


## Local installation instructions:

If you would like to run the tutorial locally you will need a few things:

- **Python 3:** Most recent systems come with Python pre-installed. **Nilearn supports Python>=3.7.**
- **git:** `git` is the most popular VCS (version controlled software). Although we recommend having `git` installed to download these notebooks, you can also use the download button on GitHub. You can learn more on `git` [here](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F).

If you have these tools installed, you can download the repository with the notebooks:

```
$ git clone https://github.com/neurospin/fMRI_workshop.git
$ cd fMRI_workshop
```

Although not required, we recommend creating and activating a virtual environment before installing the requirements.
The example below shows how to do this using Python venv module but you can use any environment manager you're used to:

```
python3 -m venv tutorial
source tutorial/bin/activate
```

Install the requirements (this will install nilearn and its dependencies, as well as Jupyter-notebooks):

```
$ pip install -r requirements.txt
```

Launch the notebooks:

```
$ cd notebooks
$ jupyter-notebook
```
