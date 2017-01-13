![](http://jupyter.org/assets/nav_logo.svg)  
#Using **Jupyter Notebook**  
**Jupyter Notebook** is a very handy tool for documenting the learning process of python. It supports **Markdown (.md)** editing style.  

It is _interactive_, and automatically records the output of a python code on the notebook.  
It can contain both code and rich text elements, such as figures, links, equations, ... Because of the mix of code and text elements, these documents are the ideal place to bring together an analysis description and its results as well as they can be executed perform the data analysis in real time.  
[http://jupyter.org/](http://jupyter.org/)  

**IPython.display** can also be very helpful when editing **Jupyter Notebook**.  
[IPython's Rich Display System](http://nbviewer.jupyter.org/github/ipython/ipython/blob/2.x/examples/Notebook/Display%20System.ipynb)

##1.Installation  
There are two ways to install **Jupyter Notebook**:  
####Option 1: Install using **Anaconda** and **Conda**  
  For new users, we highly recommend [installing Anaconda](https://www.continuum.io/downloads). Anaconda conveniently installs Python, the Jupyter Notebook, and other commonly used packages for scientific computing and data science.  
####Option 2: Alternative for experienced Python users: Installing Jupyter with pip  
  As an existing Python user, you may wish to install Jupyter using Python’s package manager, pip, instead of Anaconda.  
  First, ensure that you have the latest pip; older versions may have trouble with some dependencies:  
  ```
  pip install --upgrade pip
  ```
  Then install the Jupyter Notebook using:  
  ```
  pip install jupyter
  ```
  [Reference](http://jupyter.org/install.html)
##2.Running Jupyter Notebook
 In the command line, type:  
 ```
 jupyter notebook
 ```
 Select `new` and `Python 2` or `Python 3` to start editing.  
 
 [Reference](https://jupyter.readthedocs.io/en/latest/running.html#running)  
 
##3.Change the default directory  
  In command line, type:
  ```
  jupyter notebook --generate-config
  ```
  This generates the config file to `C:\Users\username\.jupyter\jupyter_notebook_config`.  
  
  _**Note:**For Mac OSX, in command line use_ 
  ```
  defaults write com.apple.finder AppleShowAllFiles NO
  killall Finder
  ```
  _to show hidden folders (.jupyter)._
  ```
  defaults write com.apple.finder AppleShowAllFiles YES
  killall Finder
  ```
  _to return back to normal._  
  
  Locate and open `jupyter_notebook_config`, and unmark `#c.NotebookApp.notebook_dir = ''`,  
  Add in the desired path `#c.NotebookApp.notebook_dir = 'my path'`.  
  
  **Be sure to use backslash `\` instead of forwardslash `/`**.
  
  See links for more methods: [Reference](http://stackoverflow.com/questions/35254852/how-to-change-jupyter-start-folder) [Reference](http://stackoverflow.com/questions/15680463/change-ipython-working-directory)  

##4.Mathematics style equations
  **Jupyter Notebook** supports using LaTex notations for entering equations. Just add `$` before and after the equation for _inline_ mathematics, and `$$` for _displayed_ mathematics. For showing  
  ![](http://latex.codecogs.com/png.latex?c=%5csqrt%7ba%5e2%2bb%5e2%7d)
  ```
  $c = \sqrt{a^2 + b^2}$
  ```
  or
  ```
  $$c = \sqrt{a^2 + b^2}$$
  ```
  For more examples using LaTex notations on **Jupyter Notebook**, [look here](http://nbviewer.jupyter.org/github/ipython/ipython/blob/2.x/examples/Notebook/Display%20System.ipynb#LaTeX).
