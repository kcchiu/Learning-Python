#Issues and Solutions for OSX

##1.Installing pip on OSX
  In command line, type:
  ```
  sudo easy_install pip
  ```
##2.Failure in installing matplotlib with pip
  When using pip to install **matplotlib**
  ```
  sudo pip install matplotlib
  ```
  An error is encountered
  >Command "python setup.py egg_info" failed with error code 1 in /private/tmp/pip-build-6iqtlmz0/matplotlib  
  
  Check the **matplotlib** installation log from the terminal, see if there are any **Required Dependencies and Extensions** that is not available.  
  The most common missing is `freetype`.  
  Building **matplotlib** requires `libpng` and `freetype` as well, which isn't a python library, so `pip` doesn't handle installing them.  
  To install `freetype` and/or other missing extensions,
  ```
  brew install libpng freetype pkg-config
  brew link libpng freetype
  sudo pip install matplotlib
  ```
  
