---


---

<h1 id="some-practice-with-tensorflow">Some Practice with TensorFlow</h1>
<p>This is a record of my practice in moving from formal courses and independent study in machine learning to using TensorFlow on my own.</p>
<h2 id="prerequisites">Prerequisites</h2>
<h4 id="what-things-you-need-to-install-the-software-and-how-to-install-them.">What things you need to install the software and how to install them.</h4>
<ul>
<li>
<p>I am using a Dell XPS-13 9370 Developer Edition laptop<br>
with Ubuntu 18.04.1 LTS installed. [This machine has an<br>
Thunderbolt 3 usb C port and an external NVIDIA GTX 1070Ti<br>
GPU in an Alito Node Pro enclosure]</p>
</li>
<li>
<p>I also use an Alienware 15 laptop running both<br>
Linux Mint 18.3 and Windows 10. [This machine has an<br>
internal NVIDIA GTX 1070 GPU]</p>
</li>
<li>
<p>FYI: For the time being I’m using the CPU-only versions<br>
of TensorFlow.</p>
</li>
<li>
<p>I downloaded the latest anaconda linux distribution for python 3.7 from: <a href="https://www.anaconda.com/download/#linux">https://www.anaconda.com/download/#linux</a></p>
</li>
</ul>
<h2 id="install">Install</h2>
<h4 id="first-install-the-latest-anaconda-python-3.7-or-whatever-open-a-terminal-and-update-your-base-environment">first install the latest anaconda python 3.7 or whatever, open a terminal, and update your “base” environment</h4>
<pre class=" language-console"><code class="prism  language-console">$ conda update conda
$ conda update --all
</code></pre>
<h4 id="create-new-environment-called-tensorflow-note-this-name-can-be-anything-...-i-use-a-capital-f-which-has-the-latest-tensorflow-and-the-compatible-versions-of-python-along-with-the-compatible-versions-of-anaconda-numpy-matplotlib-scikits-...">create new environment called “tensorFlow” (note this name can be anything … I use a capital ‘F’) which has the latest tensorflow and the compatible versions of python along with the compatible versions of anaconda (numpy, matplotlib, scikits …)</h4>
<pre class=" language-console"><code class="prism  language-console">$ conda create -n tensorFlow tensorflow
$ conda activate tensorFlow
</code></pre>
<h4 id="now-you-are-in-that-environment-so-install-a-few-more-things-and-update-all">now you are in that environment, so install a few more things and update all</h4>
<pre class=" language-console"><code class="prism  language-console">$ conda install keras
$ conda install anaconda
$ conda update --all
</code></pre>
<h4 id="now-you-can-deactivate-this-and-return-to-the-base-environment-if-you-want">now you can deactivate this and return to the “base” environment if you want</h4>
<pre class=" language-console"><code class="prism  language-console">$ conda deactivate
</code></pre>
<h4 id="then-you-can-list-your-environments">then you can list your environments</h4>
<pre class=" language-console"><code class="prism  language-console">$ conda info -e
</code></pre>
<h4 id="later-once-you-are-sick-of-this-you-can-remove-the-environment-and-all-of-its-contents">later once you are sick of this, you can remove the environment and all of its contents</h4>
<pre class=" language-console"><code class="prism  language-console">$ conda env remove --name tensorFlow
</code></pre>
<h2 id="ready-to-go">Ready to go</h2>
<h3 id="start-up-a-jupyter-notebook-which-can-use-tensorflow">Start up a jupyter notebook which can use TensorFlow</h3>
<h4 id="activate-your-environment">activate your environment</h4>
<pre class=" language-console"><code class="prism  language-console">$ conda activate tensorFlow
</code></pre>
<h4 id="run-jupyter-notebook">run jupyter notebook</h4>
<pre class=" language-console"><code class="prism  language-console">$ jupyter notebook
</code></pre>
<p>a new web browser page will open, if not open a browser and point to the URL displayed in this terminal</p>
<h4 id="when-you-are-all-done-close-your-browser-and-to-kill-the-jupyter-notebook-server-type">when you are all done, close your browser and to kill the jupyter notebook server type:</h4>
<pre class=" language-console"><code class="prism  language-console">^c^c
</code></pre>
<h3 id="running-some-programs">Running some programs</h3>
<p>In the main jupyter notebook web page you can browse your file system for a specific jupyter notebook to work on.</p>
<h3 id="start-up-tensorboard-to-to-look-at-the-workings-of-your-tensorflow-computation-graph-perhaps-a-deep-neural-network">Start up TensorBoard to to look at the workings of your TensorFlow computation graph, perhaps a deep neural network</h3>
<h4 id="open-another-terminal-and-activate-tensorflow-and-then-run-tensorboard-">open another terminal and activate “tensorFlow” and then run tensorboard :</h4>
<pre class=" language-console"><code class="prism  language-console">$ conda activate tensorFlow
$ tensorboard --logdir=./tmp/example --port=8002 --reload_interval=5
</code></pre>
<p>“./tmp/example” is the path to the folder containing your tensorboard log files … we’ll see more about this in the code examples</p>
<h4 id="to-see-the-tensorboard-interface-youll-need-to-open-a-new-tab-in-your-web-browser-to">to see the TensorBoard interface you’ll need to open a new tab in your web browser to:</h4>
<pre class=" language-console"><code class="prism  language-console">http://localhost:8002/
</code></pre>
<h2 id="license">License</h2>
<p>This project is licensed under the MIT License. Please read [file not here yet] for details</p>
<h2 id="contributing">Contributing</h2>
<p>Please read [file not here yet] for details on our code of conduct, and the process for submitting pull requests to us.</p>
<h2 id="authors">Authors</h2>
<ul>
<li><strong>Stephen Brown</strong> - <em>Initial work</em> - <a href="https://erlweb.mit.edu/users/srbrownmitedu">MIT</a></li>
</ul>
<h2 id="acknowledgments">Acknowledgments</h2>
<ul>
<li>Hat tips to everyone whose code I use. I’ll try my best to acknowledge the source.</li>
<li>Inspiration
<ul>
<li>Andrew Ng’s excellent courses on machine learning:
<ul>
<li><a href="https://www.coursera.org/learn/machine-learning">https://www.coursera.org/learn/machine-learning</a></li>
<li><a href="https://www.coursera.org/specializations/deep-learning">https://www.coursera.org/specializations/deep-learning</a></li>
</ul>
</li>
<li>for my own first trials I read blogs with nice examples, such as:
<ul>
<li><a href="https://liufuyang.github.io/2017/03/12/just-another-tensorflow-beginner-guide-1.html">https://liufuyang.github.io/2017/03/12/just-another-tensorflow-beginner-guide-1.html</a></li>
<li><a href="https://liufuyang.github.io/2017/03/17/just-another-tensorflow-beginner-guide-2.html">https://liufuyang.github.io/2017/03/17/just-another-tensorflow-beginner-guide-2.html</a></li>
</ul>
</li>
</ul>
</li>
<li>In trying to get up to speed in tensorflow beyond Andrew Ng’s homework, I found I just wasn’t quite comfortable with some of the new obscure programming syntax. So, I took this class by Jose Portilla:
<ul>
<li><a href="https://www.udemy.com/complete-guide-to-tensorflow-for-deep-learning-with-python">https://www.udemy.com/complete-guide-to-tensorflow-for-deep-learning-with-python</a>, in which I particularly liked the exercise of building a tiny tensorflow yourself using some object-oriented programming.</li>
<li>This really confused me at first as this is a new world for me (I have found myself using classes in python before without really understanding them), so I had to step aside and study OOP a bit
<ul>
<li>first  by looking at this helpful blog for a gentle intro to inheritance:
<ul>
<li><a href="https://www.digitalocean.com/community/tutorials/how-to-construct-classes-and-define-objects-in-python-3">https://www.digitalocean.com/community/tutorials/how-to-construct-classes-and-define-objects-in-python-3</a></li>
</ul>
</li>
<li>then buying and reading the first part of this book
<ul>
<li><a href="https://www.amazon.com/Python-3-Object-Oriented-Programming/dp/1849511268">https://www.amazon.com/Python-3-Object-Oriented-Programming/dp/1849511268</a></li>
</ul>
</li>
<li>this exercise was well worth it!</li>
</ul>
</li>
<li>Now I feel like I understand how the computation graphs are built and stored and just what the weird tensorflow syntax of creating and running sessions is really doing! Yay!</li>
</ul>
</li>
</ul>
<blockquote>
<p>Written with <a href="https://stackedit.io/">StackEdit</a>.</p>
</blockquote>

