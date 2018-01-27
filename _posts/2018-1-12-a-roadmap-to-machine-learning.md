---
layout: post
title:  "A Roadmap to Machine Learning"
date:   2018-1-12 12:30:00
comments: true
categories: Machine_Learning
excerpt: "I couldn't find a good roadmap to machine learning, so I did some research and created my own."
cover: '/assets/images/post-images/roadmap-to-machine-learning/roadmap-to-machine-learning.jpg'
---

Up until a point in my life, I was learning stuff left and right aimlessly, and leaving the knowledge at an unfinished, quite frankly unusable level.
I changed that when I started learning web development. I found enough resources to create a plan, a roadmap of stuff I'd have to learn in order to become a real Web Developer.
That roadmap changed quite a bit according to new technologies I discovered, but ultimately having a clear plan worked wonders for me.

![pointing on a map](/assets/images/post-images/roadmap-to-machine-learning/map1.jpg)

Last year, after meeting a lot of academics and talking about machine learning with them, I became fascinated with it. So much so, that I decided to start learning it, alongside my ever-evolving web application development skills.

I looked around and, to my surprise, even though there is a crazy amount of courses and resources available for machine learning *-and it seems that a lot of major companies are putting them out-*, I found not a single clear path on how to tackle learning it.

If you have no idea what machine learning is, check out the [Wikipedia entry](https://en.wikipedia.org/wiki/Machine_learning).

![searching on a map](/assets/images/post-images/roadmap-to-machine-learning/map2.jpeg)

So I did some research, talked to an [expert in the field](https://ispscientist.wordpress.com) about it, and here I present to you the roadmap I came up with. It is focused on Python as the programming language, since it has a great selection of machine learning packages and libraries, and it's extremely easy to learn. You can get through this list without spending a dime, and it's focused on a hands-on approach of directly applying what you learn.

Get yourself set up with a notebook, a pen or pencil, and a mandatory cup of coffee, and let's dive in!

![notebook](/assets/images/post-images/roadmap-to-machine-learning/map3.jpg) 

***

## Roadmap to Machine Learning

<br>

### Step 0: Prerequisites

You can get around using machine learning libraries and doing some data science even if you don't have a strong foundation in math, however you probably won't get very far without it. If you don't, this roadmap includes a couple links to math courses when you'll actually need them later on. **By the end, you should be familiar with:**

* **Calculus**: computational math (integration, derivatives), optimization (finding maxima/minima of a function)
* **Linear Algebra**: vectors, matrices, matrix multiplication, vector spaces
* **Statistics**: probability, random variables, distributions (Gaussian, mixture models etc.), standard deviations, probability density
* **Python** (not math, but a prerequisite nonetheless)
    - You can use other languages but Python is the easiest to learn. Below are two great, free courses.
        - [Introduction to Python (Udacity course)](https://www.udacity.com/course/introduction-to-python--ud1110)
        - [Learn Python (Codecademy course)](https://www.codecademy.com/learn/learn-python)

### Step 1: Environment

The first thing is to set up our environment so we can actually run the algorithms and programs on our computer. **Strictly speaking, we only need Python and whichever libraries we choose to use** (and that's what I've been using until now) but having specialized tools sometimes makes us more productive.

* Install Python/pip
  1. Python libraries for math and graph plotting:
      1. [SciPy](https://www.scipy.org/) used for scientific calculations by scientists and engineers
      2. [NumPy](http://www.numpy.org/) used for linear algebra operations, Fourier transforms, random number generation etc.
      3. [Pandas](http://pandas.pydata.org/) used for data structures and data analysis tools
      4. [MatPlotLib](https://matplotlib.org/) used for plotting our data so we can gain insight on its structure
  2. Python libraries for machine learning:
      1. [Scikit-Learn (or sklearn)](http://scikit-learn.org/stable/index.html) Easy to use machine learning library
      2. [Tensorflow](https://www.tensorflow.org/) Google's machine learning library
      3. [PyTorch](http://pytorch.org/) Deep Learning framework
      4. [Theano](http://www.deeplearning.net/software/theano/) library that allows you to define, optimize, and evaluate mathematical expressions involving multi-dimensional arrays efficiently. 
      5. [Keras](https://keras.io/) Deep Learning library that runs on top of Tensorflow or Theano

* Learn how to use IPython
* Learn how Jupyter Notebooks work
* Install Anaconda and learn how to use it
    - Anaconda and it's package manager, conda, is a distribution of Python specialized for machine learning and data science.

### Step 2: Classroom - Basics

In this step, we'll **focus on learning the basics of machine learning**. We need to learn what it is, where it's used, what different types of machine learning algorithms and techniques exist, and get familiar with some of the major algorithms and working with data. You should get a good feel for how good, usable data is structured after finishing either of these courses and/or books. **I recommend you pick both a book and a course.**

* [Intro to Machine Learning (Udacity course)](https://www.udacity.com/course/intro-to-machine-learning--ud120)
    - This course is the standard one you should follow if you're not really strong with math.

    *or*

* [Andrew Ng's Course on Machine Learning (Coursera course)](https://www.coursera.org/learn/machine-learning)
    - If you are already familiar with the math from step 0, then this is the all-around best course since it goes deeper in the math and is taught by one of the field's best researchers.

    *or*

* [Data Camp](https://www.datacamp.com/)
    - This is a website with a lot of different courses in things like Python, math in Python, visualizing data, statistics, machine learning and supervised learning. It's a good alternative to the others, but you have to pick the courses or paths yourself and that's not always ideal.

    *course &uarr;*
    <br>
    **and**
    <br>
    *book &darr;*

* [Python Machine Learning (Book)](https://www.amazon.com/Python-Machine-Learning-scikit-learn-TensorFlow/dp/1787125939)
    - This book is not free, however I see it strongly recommended and having bought it, I can say it's a great practical book and I've found that reading a book cover-to-cover on a particular subject gives you in-depth knowledge of aforementioned subject. You'll also always have it laying around for quick reference.

    *or*

* [Elements of Statistical Learning (Free ebook)](https://web.stanford.edu/~hastie/Papers/ESLII.pdf)
    - This book is free, it's from Stanford and it includes a whole lot of information on machine learning. While not as practical as the first one, it goes a lot deeper on the concepts and math behind machine learning and data science.

    *or*

* [Pattern Recognition and Machine Learning by Christopher Bishop](http://www.springer.com/us/book/9780387310732)
    - This is the machine learning bible, and it is not free. However, I could not leave it out of this list since it paved the way for machine learning.


### Step 3: Get Your Feet Wet (Project #1)

This will be different for everyone. **I recommend going to [Kaggle](https://www.kaggle.com/) and using one of their datasets** for something you want to figure out, using machine learning. You can see more alternatives and why I chose Kaggle in [this comment](http://disq.us/p/1pdln8z). Personally, I have a plan for a project using an IoT sensor network that I will reveal in due time.

### Step 4: Classroom - Going Deeper

Now that we've used machine learning in an actual, real world dataset, without any guidance, **we're ready to get a deeper understanding of data and the math behind machine learning.** If you feel the MIT stuff is too hard, you can try some [KhanAcademy](https://www.khanacademy.org/) courses first.

* [Intro to Data Science (Udacity course)](https://www.udacity.com/course/intro-to-data-science--ud359)
* [Linear Algebra (MIT OpenCourseware)](https://ocw.mit.edu/courses/mathematics/18-06-linear-algebra-spring-2010/)
* [Single Variable Calculus (MIT OpenCourseware)](https://ocw.mit.edu/courses/mathematics/18-01sc-single-variable-calculus-fall-2010/)
* [Intro to Descriptive Statistics (Udacity course)](https://www.udacity.com/course/intro-to-descriptive-statistics--ud827)
* [Intro to Inferential Statistics (Udacity course)](https://www.udacity.com/course/intro-to-inferential-statistics--ud201)
* [Elements of Statistical Learning (Free ebook)](https://web.stanford.edu/~hastie/Papers/ESLII.pdf)
    - I also have this in step 2, but by now you should go deeper in it.

### Step 5: Build a Portfolio

We now have a really good understanding of machine learning, but if we don't practice it, it will only be theoretical. **This step is probably the most important part.** We have to go ahead and work on Kaggle datasets, join competitions, hopefully find a dataset that's specifically interesting to us and something we want to learn about - this is actually where we can shine!

### Step 6: One Step Further

We can stop there, or we can move on to the very specialized area of machine learning that is slowly taking the world by storm, **Deep Learning**. This field of machine learning is very prevalent today, due to the incredible success story of Computer Vision and the ability to work with raw data. This will have to be a roadmap in itself, but for now, I'll add a couple of links.

* [Deep Learning (Udacity course)](https://www.udacity.com/course/deep-learning--ud730)
* [Deep Learning (Coursera course by Andrew Ng)](https://www.deeplearning.ai/)

So there you have it. I wish you the best in this journey, and happy new year!