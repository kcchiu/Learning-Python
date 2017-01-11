#Issues and Solutions for OSX

##1.Installing pip on OSX
  In command line, type:
  ```
  sudo easy_install pip
  ```
##2.Installing Microsoft Visual C++ Complier for Python 2.7
  Reference to [this link](https://www.microsoft.com/en-us/download/details.aspx?id=44266) to download and install.
##3.Failure in installing matplotlib with pip
  When using pip to install **matplotlib**,
  ```
  sudo pip install matplotlib
  ```
  An error is encountered
  >Command "python setup.py egg_info" failed with error code 1 in /private/tmp/pip-build-6iqtlmz0/matplotlib  
  
###_First_  

  Upgrade the `Setuptool`,
  ```
  pip install --upgrade setuptools
  ```
  or
  ```
  easy_install -U setuptools
  ```
  
###_Second_

  Check the **matplotlib** installation log from the terminal, see if there are any **Required Dependencies and Extensions** that is not available.  
  The most common missing is `freetype` and `libpng`.  
  
  Building **matplotlib** requires `libpng` and `freetype` as well, which isn't a python library, so `pip` doesn't handle installing them.  
  To install `freetype` and/or other missing extensions,
  ```
  brew install libpng freetype pkg-config
  brew link libpng freetype
  sudo pip install matplotlib
  ```
  `matplotlib` should be able to install successfully. If not, try installing a older version of `matplotlib`,
  ```
  pip install matplotlib==1.4.0
  ```
