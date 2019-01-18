# PyCrypto-Wheels
Built Distributions of PyCrypto on Windows

To install PyCrypto 2.6.1 for a 64-bit Python 3.5 installation run:
```
pip install --use-wheel --no-index --find-links=https://github.com/sfbahr/PyCrypto-Wheels/raw/master/pycrypto-2.6.1-cp35-none-win_amd64.whl pycrypto
```

To install on a 32-bit Python installation run:
```
pip install --use-wheel --no-index --find-links=https://github.com/sfbahr/PyCrypto-Wheels/raw/master/pycrypto-2.6.1-cp35-none-win32.whl pycrypto
```

These built distributions were compiled with VS Enterprise 2015 on Windows 10. They should work on any Windows installation.

For more info on how I built these and how to build them for yourself: [Stack Overflow: PyCrypto on python 3.5](http://stackoverflow.com/questions/32800336/pycrypto-on-python-3-5)


If you're looking for a built distribution for a different version of PyCrypto or Python, check out [Voidspace](http://www.voidspace.org.uk/python/modules.shtml#pycrypto). I made these originally because Voidspace was not updated with a build for Python 3.5.

## How to build it

Ref the [Marko Rothstein's](https://stackoverflow.com/questions/41843266/microsoft-windows-python-3-6-pycrypto-installation-error) answer. 

1. open "x86_x64 Cross-Tools Command Prompt for VS 2017" with administrator privilege in start menu
2. set CL=-FI"%VCINSTALLDIR%Tools\MSVC\14.11.25503\include\stdint.h"  **make sure the folder version number is right**
3. `pip install wheel`
4. `python setup.py bdist_wheel`