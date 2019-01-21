---
layout: post
title:  "Setting up a Machine Learning environment"
date:   2018-8-23 12:30:00
comments: true
math: false
categories: Machine_Learning
excerpt: "An easy-to-follow guide on setting up an environment for Machine Learning development"
cover: '/assets/images/post-images/ml-env/ml-env.jpg'
---
1. [Introduction](#introduction)
2. [Text Editor vs. Jupyter Notebooks](#text-editor-vs-jupyter-notebooks)
3. [To Contain, Or Not To Contain?](#to-contain-or-not-to-contain)
    1. [Using containers for Machine Learning](#using-containers-for-machine-learning)
4. [Option 1) Create a Conda Environment Using the Anaconda Python Distribution](#option-1-create-a-conda-environment-using-the-anaconda-python-distribution)
    1. [Installing Anaconda and setting up a virtual environment](#installing-anaconda-and-setting-up-a-virtual-environment)
5. [Option 2) Using Docker Containers](#option-2-using-docker-containers)
    1. [Premade Docker images](#premade-docker-images)
    2. [Creating a Docker container from scratch](#creating-a-docker-container-from-scratch)
6. [Option 3) Set Up Your Main System For Machine Learning Development](#option-3-set-up-your-main-system-for-machine-learning-development)
    1. [Machine Learning-specific packages](#machine-learning-specific-packages)
        1. [Tensorflow](#tensorflow)
        2. [Scikit-learn (sklearn)](#scikit-learn-sklearn)
        3. [PyTorch](#pytorch)
        4. [Keras](#keras)
7. [Other Options](#other-options)
    1. [Virtualenv](#virtualenv)
8. [Synopsis](#synopsis)

### Introduction

In this article, I'm going to go over the steps one can take in order to set up a system for Machine Learning development in Python.

There are basically three ways to do the coding part of a data science project; a (traditional or modern) text editor (like Visual Studio Code, Atom, Sublime or Vim), Jupyter Notebooks, and IDEs like Spyder.

I personally don't use Spyder, although if you're familiar with Matlab, you will feel right at home. Depending on the application and the indivdual project, I use notebooks and VSCode.

After briefly going over why one might use a text editor over Jupyter Notebooks and vice versa, we will take a look at why we would use a container, and then I'll illustrate three options, step by step, for setting your environment up, and offer a couple more I don't personally tend to use.

### Text Editor vs. Jupyter Notebooks

This is a hard one. "*Should I develop Machine Learning models in a text editor or in a Jupyter Notebook?*"

Well, it depends. Do you need to visualize your data often? Do you need to write a lot of raw code?
To be fair, some modern text editors feature plugins that may give them Jupyter Notebook functionality - I'd prefer the plain notebook.

As I said above, I use both text editors and notebooks, but if I had to choose between them, I'd go with the notebooks. Inline plotting, mixing in good ol' Markdown cells with code cells, clearly separated sections and efficient keybinds make them readable, understandable, uncomplicated and, well, ["comfy"](https://www.urbandictionary.com/define.php?term=Comfy).

However, if you're more of a programmer than just a straight up data scientist, you probably understand why a powerful editor will be much quicker to write code with for those projects that require it; that's why I use both!

### To Contain, Or Not To Contain?

That is the question.

Well, to be honest, it most likely won't spark a philosophical debate like Hamlet's famous opening phrase in the Shakespearean play's nunnery scene. I would argue it's more of a practical question: Do we want to install all those new, potentially unstable Python packages into our main system, or contain them into a dedicated Machine Learning environment with almost no extra work?

If you can't tell, I personally lean towards the latter. However, I've never broken my system by installing any Machine Learning package, and I totally still use my main system for Machine Learning sometimes.

Setting up your system for development instead of a dedicated container is not all cons, though. The big pro is you can use whatever text editor or IDE you prefer, natively, without any hassle. You also won't have to start a container service every time you log in to work on your projects.

I present both ways here; the choice is yours.

![Containers](/assets/images/post-images/ml-env/containers.jpeg)

#### Using containers for Machine Learning

Most, if not all, of the process of installing the packages you need, is the same whether you use a container or not. The only real difference is creating the container, and afterwards running/closing it.

We can think of virtual environments as containers for the purposes of this guide, even though that's not totally accurate.

\**Sidenote: Do not confuse containers with virtual machines (VMs). Although a VM is in fact a type of container, a container is not necessarily a VM. We will take a look into VMs (a topic that should interest Windows and Mac users especially) in a later article.*



### Option 1) Create a Conda Environment Using the Anaconda Python Distribution

[Anaconda](https://www.anaconda.com/distribution/) is a Python (and R) distribution that comes loaded with essential packages, and makes it extremely easy to install and manage packages, dependencies and environments.

Conda, its package manager, in addition to being arguably the best Python package manager around and being FOSS (Free and Open Source Software), features creating and switching between virtual environments.

This means you can set up a virtual environment for tackling all your Machine Learning projects, without affecting your main system!

#### Installing Anaconda and setting up a virtual environment

1. [Download Anaconda](https://www.anaconda.com/download/) and install it using the provided instructions according to your operating system.
2. Create a virtual environment

    ```bash
    conda create -n my_env python=3.5
    ```
    - In the above command, the `-n` option stands for "name". You can name it whatever you want and choose any Python version.
    - [The Conda user guide](https://conda.io/docs/user-guide/tasks/manage-environments.html) is a great resource for creating and managing your environments. You can find the full palette of options there.
    - [The Conda cheat sheet](https://conda.io/docs/_downloads/conda-cheatsheet.pdf) is another, more condensed resource for lazier people like myself.
3. Activate and enter your newly created virtual environment

  ```bash
  source activate my_env
  ```

4. Install general and Machine Learning packages

    ```bash
    # EXAMPLE: install the "numpy" package
    conda install numpy
    # or
    conda install -c anaconda numpy
    ```
    - The `-c` option specifies the channel from where to install the package
    - You can use `pip` instead of `conda` if you want to
    - See [Option 3](#option-3-set-up-your-main-system-for-machine-learning-development) for quick commands on installing some popular libraries/frameworks like TensorFlow
5. Install Jyputer Notebook

    ```bash
    conda install -c anaconda notebook
    ```
    - Note that this package might already be present in anaconda

We can now launch the notebook by entering:

```bash
jupyter notebook
```

If it asks for a token, open another terminal, repeat step 3 and enter:

```bash
jupyter notebook list
```

 to view it. You can afterwards set a password that you will enter instead, from now on.

Exit the virtual environment by entering:

```bash
source deactivate
```

### Option 2) Using Docker Containers

Docker containers are a fast and secure way to set up your environment for Machine Learning. You can make your own with exactly the packages you need from scratch, or you can just use any of the open source ones provided by the community, ready with pre-installed libraries and packages.

#### Premade Docker images

Here's my favorite ones, [Deepo docker images](https://github.com/ufoym/deepo). The README contains really nice, detailed and very comprehensible documentation on using them.

#### Creating a Docker container from scratch

If you do decide you want to create one from scratch, please refer to their [website](https://docs.docker.com/get-started/)

### Option 3) Set Up Your Main System For Machine Learning Development

Most of the steps here are directly applicable to any other option.

First up, we have to install Python 3. I still recommend using the Anaconda distribution, but you can also install Python and its package manager, pip, the old-fashioned way (the command presented here is for Ubuntu and other Debian based distributions):

```bash
sudo apt install python3-dev python3-pip
```

Then, install any packages you may need, for example:

```bash
pip3 install numpy scipy pandas matplotlib
```

Install Jupyter Notebook:

```bash
pip3 install jupyter
```

Note that you might need superuser privileges.

#### Machine Learning-specific packages

##### Tensorflow

```bash
sudo pip3 install -U tensorflow
```

for the CPU version, or

```bash
sudo pip3 install -U tensorflow-gpu
```

for the GPU version.

You can find the full directions for any platform on the [official TensorFlow website](https://www.tensorflow.org/install/)

##### Scikit-learn (sklearn)

```bash
sudo pip3 install scikit-learn
```

##### PyTorch

```bash
sudo pip3 install pytorch torchvision
```

##### Keras

```bash
sudo pip3 install keras
```

Finally, if you're using a text editor, find if there are any editor-specific packages you can install to make your life easier. I personally use Visual Studio Code, with the package "Tools for AI".

### Other Options

#### Virtualenv

1. Install virtualenv
    ```bash
    sudo apt install python-virtualenv
    ```
2. Create a new directory for your environment and enter it:
    ```bash
    mkdir ~/<dir_name>
    cd ~/<dir_name>
    ```
3. Choose a Python interpreter for the virtual environment

    ```bash
   virtualenv --system-site-packages -p python3 venv
    ```

4. Activate the environment

   ```bash
   source ~/<dir_name>/venv/bin/activate
   ```

5. Upgrade pip in the virtual environment

   ```bash
   pip install -U pip
   ```

6. Install any packages the same way as with [Option 3](#option-3-set-up-your-main-system-for-machine-learning-development)

### Synopsis

After reading this article, you hopefully have a better understanding on why and how you would use a text editor vs. a jupyter notebook, using a container or virtual environment vs. your own system's environment, and how to set up any Python packages, libraries and frameworks you may need for your Machine Learning endeavours.
