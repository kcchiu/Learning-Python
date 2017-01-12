![](http://jupyter.org/assets/nav_logo.svg)  
##Using **Jupyter Notebook**  
**Jupyter Notebook** is a very handy tool for documenting the learning process of python.  
It is interactive, and automatically records the output of a python code on the notebook.  
It can contain both code and rich text elements, such as figures, links, equations, ... Because of the mix of code and text elements, these documents are the ideal place to bring together an analysis description and its results as well as they can be executed perform the data analysis in real time.  
[http://jupyter.org/](http://jupyter.org/)  

###Installation  
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
###Running Jupyter Notebook
 In the command line, type:  
 ```
 jupyter notebook
 ```
 Select `new` and `Python 2` or `Python 3` to start editing.  
 
 [Reference](https://jupyter.readthedocs.io/en/latest/running.html#running)  
 
###Change the default directory  
  In command line, type:
  ```
  jupyter notebook --generate-config
  ```
  This generates the config file to `C:\Users\username\.jupyter\jupyter_notebook_config`.  
  Locate and open `jupyter_notebook_config`, and unmark `#c.NotebookApp.notebook_dir = ''`,  
  Add in the desired path `#c.NotebookApp.notebook_dir = 'my path'`.  
  
  **Be sure to use backslash `\` instead of forwardslash `/`**.
  
  See links for more methods: [Reference](http://stackoverflow.com/questions/35254852/how-to-change-jupyter-start-folder) [Reference](http://stackoverflow.com/questions/15680463/change-ipython-working-directory)
