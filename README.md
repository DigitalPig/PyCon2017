[![Join the chat at https://gitter.im/PyCon2017BayesianMachineLearning/Lobby](https://badges.gitter.im/PyCon2017BayesianMachineLearning/Lobby.svg)](https://gitter.im/PyCon2017BayesianMachineLearning/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# Bayesian Machine Learning
## Reasoning under Uncertainty with Edward

Thursday, May 18, 9 a.m.–12:20 p.m.

[Torsten Scholak](https://twitter.com/tscholak), [Diego Maniloff](https://us.pycon.org/2017/speaker/profile/1894/)

## Abstract

There has been uprising of probabilistic programming and Bayesian statistics. These techniques are tremendously useful, because they help us to understand, to explain, and to predict data through building a model that accounts for the data and is capable of synthesizing it. This is called the generative approach to statistical pattern recognition.

Estimating the parameters of Bayesian models has always been hard, impossibly hard actually in many cases for anyone but experts. However, recent advances in probabilistic programming have endowed us with tools to estimate models with a lot of parameters and for a lot of data. In this tutorial, we will discuss one of these tools, [Edward](http://edwardlib.org). Edward is a black box tool, a Swiss army knife for Bayesian modeling that does not require knowledge in calculus or numerical integration. This puts the power of Bayesian statistics into the hands of everyone, not only experts of the field. And, it's great that Edward is implemented in Python with its rich, beginner-friendly ecosystem. It means we can immediately start playing with it.

## Outline

* Introduction

* Coin Flip

* A/B/... Testing

* Bayesian Curve Fitting

* Fitting Categorical Data

* The Bayesian Netflix Problem

## Software Setup

This tutorial will be based on **Python 2**. Everything should work with Python 3 as well, but we can't guarantee it.

1. Leave your current [virtualenv](https://virtualenv.pypa.io) if applicable:
	```sh
	$ deactivate
	```

2. Create a new virtualenv called `pycon` (you can change the name and location of course):
	```sh
	$ mkdir -p ~/VirtualEnv/pycon
	$ virtualenv -p $(which python2.7) ~/VirtualEnv/pycon
	$ source ~/VirtualEnv/pycon/bin/activate
	```

3. Install TensorFlow, Edward, and Seaborn to the virtualenv `pycon`:
	```sh
	(pycon) $ pip install --upgrade tensorflow
	(pycon) $ pip install -e "git+https://github.com/blei-lab/edward.git#egg=edward"
	(pycon) $ pip install seaborn
	```
	If you have a CUDA-capable NVIDIA graphics chip in your laptop, you may want to follow special installation instructions available on the [TensorFlow web page](https://www.tensorflow.org/install/). If you don't, everything will work just fine as well.

4. Install Jupyter Notebook into the `pycon` virtual environment:
	```sh
	(pycon) $ pip install jupyter
	(pycon) $ ipython kernel install --user --name python2_pycon --display-name "Python 2 (PyCon)"
	```

5. Start the Jupyter Notebook:
	```sh
	(pycon) $ jupyter notebook --no-browser
	```

6. Clone this repository.
	```sh
	(pycon) $ git clone git@github.com:UnataInc/PyCon2017.git
	```

7. Open the notebook, `tutorial.ipynb`, in Jupyter and make sure the kernel is set to "Python 2 (PyCon)".

8. (Optional) In the notebook, there is the option to render a video. For this to work properly, you need [FFmpeg](https://ffmpeg.org) and one out of two video encoding libraries:
    * H.264. Please follow the installation instructions [here](https://trac.ffmpeg.org/wiki/How%20to%20quickly%20compile%20FFmpeg%20with%20libx264%20(x264%2C%20H.264)) or use a packaging tool (e.g., just `sudo apt-get install ffmpeg` on Ubuntu Linux).
    * Webm. Please follow the installation instructions [here](http://wiki.webmproject.org/ffmpeg/building-with-libvpx) or use a packaging tool.
