# Some Practice with TensorFlow

This is a record of my practice in moving from formal courses and independent study in machine learning to using TensorFlow on my own.

## Prerequisites

#### What things you need to install the software and how to install them.

*   I am using a Dell XPS-13 9370 Developer Edition laptop  
    with Ubuntu 18.04.1 LTS installed. [This machine has an  
    Thunderbolt 3 usb C port and an external NVIDIA GTX 1070Ti  
    GPU in an Alito Node Pro enclosure]

*   I also use an Alienware 15 laptop running both  
    Linux Mint 18.3 Your account has been flagged. Because of that, your profile is hidden from the public. If you believe this is a mistake, contact support to have your account status reviewed.and Windows 10\. [This machine has an  
    internal NVIDIA GTX 1070 GPU]

*   FYI: For the time being I’m using the CPU-only versions  
    of TensorFlow.

*   I downloaded the latest anaconda linux distribution for python 3.7 from: [https://www.anaconda.com/download/#linux](https://www.anaconda.com/download/#linux)

## Install

#### first install the latest anaconda python 3.7 or whatever, open a terminal, and update your “base” environment

    $ conda update conda
    $ conda update --all

#### create new environment called “tensorFlow” (note this name can be anything … I use a capital ‘F’) which has the version 3.6 of python and all of anaconda packages compatible with that (numpy, matplotlib, scikits, tqdm, …) and activate this new environment

    $ conda create -n tensorFlow python=3.6 anaconda
    $ conda activate tensorFlow

#### now you are in that environment, install tensorflow and keras and update all

    $ conda install tensorflow
    $ conda install keras
    $ conda update --all

#### now you can deactivate this and return to the “base” environment if you want

    $ conda deactivate

#### then you can list your environments

    $ conda info -e

#### later once you are sick of this, you can remove the environment and all of its contents

    $ conda env remove --name tensorFlow

## Ready to go

### Start up a jupyter notebook which can use TensorFlow

#### activate your environment

    $ conda activate tensorFlow

#### run jupyter notebook

    $ jupyter notebook

a new web browser page will open, if not open a browser and point to the URL displayed in this terminal

#### when you are all done - close your browser and kill the jupyter notebook server by typing:

    ^c^c

### Running some programs

In the main jupyter notebook web page you can browse your file system for a specific jupyter notebook to work on.

### Start up TensorBoard to to look at the workings of your TensorFlow computation graph, perhaps a deep neural network

#### open another terminal and activate “tensorFlow” and then run tensorboard :

    $ conda activate tensorFlow
    $ tensorboard --logdir=./tmp/example --port=8002 --reload_interval=5

“./tmp/example” is the path to the folder containing your tensorboard log files … we’ll see more about this in the code examples

#### to see the TensorBoard interface you’ll need to open a new tab in your web browser to:

    http://localhost:8002/

## License

This project is licensed under the MIT License. Please read [LICENSE.md](LICENSE.md) for details

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Authors

*   **Stephen Brown** - _Initial work_ - [MIT](https://erlweb.mit.edu/users/srbrownmitedu)

See also the list of [contributors](CONTRIBUTORS.md) who participated in this project.

## Acknowledgments

*   Hat tips to everyone whose code I use.
*   Inspiration from:
    *   Andrew Ng’s excellent courses on machine learning:
        *   [https://www.coursera.org/learn/machine-learning](https://www.coursera.org/learn/machine-learning)
        *   [https://www.coursera.org/specializations/deep-learning](https://www.coursera.org/specializations/deep-learning)
    *   for my own first trials I read blogs with nice examples, such as:
        *   [https://liufuyang.github.io/2017/03/12/just-another-tensorflow-beginner-guide-1.html](https://liufuyang.github.io/2017/03/12/just-another-tensorflow-beginner-guide-1.html)
        *   [https://liufuyang.github.io/2017/03/17/just-another-tensorflow-beginner-guide-2.html](https://liufuyang.github.io/2017/03/17/just-another-tensorflow-beginner-guide-2.html)
*   In trying to get up to speed in tensorflow beyond Andrew Ng’s homework, I found I just wasn’t quite comfortable with some of the new obscure programming syntax. So, I took this class by Jose Portilla:
    *   [https://www.udemy.com/complete-guide-to-tensorflow-for-deep-learning-with-python](https://www.udemy.com/complete-guide-to-tensorflow-for-deep-learning-with-python), in which I particularly liked the exercise of building a tiny tensorflow yourself using some object-oriented programming.
    *   This really confused me at first as this is a new world for me (I have found myself using classes in python before without really understanding them), so I had to step aside and study OOP a bit:
        *   first by looking at this helpful blog for a gentle intro to inheritance:
            *   [https://www.digitalocean.com/community/tutorials/how-to-construct-classes-and-define-objects-in-python-3](https://www.digitalocean.com/community/tutorials/how-to-construct-classes-and-define-objects-in-python-3)
        *   then buying and reading the first part of this book
            *   [https://www.amazon.com/Python-3-Object-Oriented-Programming/dp/1849511268](https://www.amazon.com/Python-3-Object-Oriented-Programming/dp/1849511268)
    *   In the end I conclude that this side trip was well worth it!
    *   Now I feel like I understand how the computation graphs are built and stored and just what the weird tensorflow syntax of creating and running sessions is really doing! Yay!

> Written with [StackEdit](https://stackedit.io/).
