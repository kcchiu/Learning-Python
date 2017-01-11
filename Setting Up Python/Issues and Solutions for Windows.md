#Issues and Solutions  

###1.Installing numpy and scipy for 32-bit Python
  The numpy package have to be installed before scipy.  
  If you are using the 32-bit version of python on Windows, the **numpy+MKL** version have to be used.  
  Refer to [this link](http://www.lfd.uci.edu/~gohlke/pythonlibs/#numpy) to download **numpy+MKL**.  
  cp27 is for python 2.7, cp36 is for python 3.6  
  use `pip install` to install the package.  
  Refer to [this link](http://www.lfd.uci.edu/~gohlke/pythonlibs/#scipy) to download **scipy**.  
  
###2.pip error: Unknown or unsupported command 'install'
  This error will appear when **Perl** is installed.  
  To check:  
  ```
  C:\>where pip
  ```
  This will potentially output the following:  
  ```
  C:\strawberry\perl\bin\pip
  C:\strawberry\perl\bin\pip.bat
  ```
  This error is because the system is finding pip.bat before it finds pip.exe.  
  You can solve this problem without removing Strawberry Perl or type the whole path.Move to this `C:\Python2.7\Scripts` directory,then use `pip` command.  

###3.
