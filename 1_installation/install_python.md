# Installing Python

> Whenever I say Python in this tutorial, I mean Python 3. DO NOT INSTALL Python 2.

## Installing from python.org

**Note**: Sometimes you machine comes with a pre-installed copy of Python. If that is the case, you should still install a new Python copy, because the pre-installed one might serve as a part of your operating system.

There are various ways to install Python. The simplest way is to directly download the installation package matching your operating system and architecture from [python.org](https://www.python.org/), which is recommended for those who have not installed Python on their machines and want a painless installation process. Once you have finished, open your terminal and type `python3`. If you see no error message and something like below, it means your installation is successful.

```python
❯ python
Python 3.10.4 (main, Mar 31 2022, 03:37:37) [Clang 12.0.0 ] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> 1 + 1
2
```

Like I did above, you can double-check by typing `1 + 1` to see if it gives you `2`. If you installed Python in this way, proceed to [here](#creating-a-standalone-environment-optional).

## Installing miniconda

If you have experience with data science, you might have also heard of [Anaconda](https://www.anaconda.com/), another package manager that can install Python (and more than that). Here, I'll use [miniconda](https://docs.conda.io/en/latest/miniconda.html), a minimal version of Anaconda, as an example. If you want to know the difference between Anaconda and miniconda, check out [this page](https://docs.conda.io/projects/conda/en/latest/user-guide/install/download.html#anaconda-or-miniconda).

Go to miniconda's [homepage](https://docs.conda.io/en/latest/miniconda.html), and select the installer matching your platform (i.e., operating system) and architecture. For example, if you have a Mac with an M1 chip, choose either `Miniconda3 macOS Apple M1 64-bit bash` or `Miniconda3 macOS Apple M1 64-bit pkg`. The `bash` installer is a command line installer, whereas the `pkg` suffix means it is a GUI installer.

![miniconda](images/miniconda.png)

Once you have downloaded the installer, go to the [installation instruction page](https://conda.io/projects/conda/en/latest/user-guide/install/index.html). Under "Regular installation," choose your operating system. For macOS, the page assumes you downloaded the command line installer with `bash` suffix, and you can accept most of the defaults (unless you know a certain default is not what you want). The same applies to a graphical installer.

**Note**: You can skip step 2 in the instruction below, as that does not affect your installation.

![miniconda macOS installation instruction](images/miniconda-macos.png)

## Creating a standalone environment (optional)

There is nothing wrong with using an out-of-the-box version of Python, but it is sometimes better to use an "environment," which can be considered as a container that is safe enough for you to play with. People sometimes create a new environment when they have a new "project."

In the case of this course, the course itself is a project, and when you later take other courses that require you to write Python code, you can create individual environments for each of those courses. When you interact with Python in a particular environment, what you do will not affect the state of other environments. This can be helpful if you accidentally corrupt some of the Python-related files or packages in that environment, because you can simply go ahead and create a new one if you like. You can also select a specific version of Python (i.e., Python 3.\*) for a certain environment. If you want to know more, check out the [`venv` module](https://docs.python.org/3/library/venv.html#module-venv) in Python.

As you might have already guessed, miniconda also comes with this functionality. If you want to create a new environment named `cse20` for this course with Python `3.9`, you can simply execte the line below in your terminal:

```shell
conda create -n cse20 python=3.9
```

When you want to enable this environment, run

```shell
conda activate cse20
```

And once you are done and want to go back to the base environment, use

```shell
conda deactivate
```

If the python version is missing, it by defaults gives you the latest version. For further details and how to manage environment, please refer to [this page](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-with-commands).
