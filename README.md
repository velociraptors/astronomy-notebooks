astronomy-notebooks
===================

iPython Notebooks showing off NumPy, matplotlib, and our universe

Getting Started
---------------
The short version: make sure you have all of the appropriate dependencies installed and then run the appropriate setup script for your platform.

### Linux
1. Install/build the required dependencies. Most dependencies other than Python and virtualenv are automatically installed via the setup script.
2. Clone or fork this repo.
3. Run setup.sh to create a new virtualenv, install any missing dependencies, and download required data sets.

### Windows
1. Install the required dependencies. See below for details.
2. Clone or fork this repo.
3. Run setup.bat to create a new virtualenv, install any missing dependencies, and download required data sets.

#### Windows Dependencies (the simple way)
The easiest way to get all of the dependencies in Windows is to use a special Python distribution meant for scientific computing. Pick one of the following options:
- Install [Python(x,y)][pxy]. You can reduce the disk space required by only selecting the dependencies listed below (and any components required by those dependencies). Mayavi is included as part of the 'ETS' component. If you already have Python 2.7 installed, Python(x,y) may clobber your existing installation.
- Install [EPD][epd]. The [free version][epd-free] of EPD does not include Mayavi, but it does contain the tools required to build it from source. If you don't want 3D visualizations, you don't need Mayavi.

#### Windows Dependencies (the harder way)
1. Install Python 2.7 and virtualenv. You may also want to install setuptools or distribute.
2. Download and install binaries for wxPython, iPython, pyreadline, numpy, scipy, matplotlib.
3. Use pip or easy_install to install tornado, pyzmq, sympy, pyephem, jplephem, de405, sgp4. (I'm pretty sure these libraries can all be installed without a compiler.)
4. (optional) If you're using regular Python, rather than EPD, you'll need to install or build VTK. Python(x,y) bundles an [installer][vtk-bin] which is listed on the [standard plugins][pxy-plug] page. If you want to try building VTK from source, you'll also need [CMake][cmake], a compiler such as MinGW or Visual Studio, and a very large bottle of whiskey.
5. [Build Mayavi][mayavi-build] from source. You could also try installing the ETS package from the Python(x,y) standard plugins.

Dependencies
------------

#### Python
- [Python][py] (obviously), [virtualenv][venv]
- [distribute](http://pypi.python.org/pypi/distribute/) (optional)
[py]: http://python.org/
[venv]: http://pypi.python.org/pypi/virtualenv/

#### iPython
- [ipython][ipy], [tornado][tornado], [pyzmq][zmq]
- [pyreadline][pyrl] (Windows only)
- [sympy][sympy] (only required for the 'iPython Features' notebook)
[ipy]: http://ipython.org/
[tornado]: http://pypi.python.org/pypi/tornado/
[zmq]: http://pypi.python.org/pypi/pyzmq/2.2.0.1
[pyrl]: http://ipython.org/pyreadline.html
[sympy]: http://pypi.python.org/pypi/sympy/

#### Visualization tools
- [numpy][numpy], [scipy][scipy], [matplotlib][mpl]
- [VTK][vtk] (must be compiled from source to include python support)
- [mayavi][mayavi] (may need to be compiled from source?)
- [wxPython][wxpy]
[numpy]: http://www.numpy.org/
[scipy]: http://www.scipy.org/
[mpl]: http://matplotlib.org/
[vtk]: http://www.vtk.org/VTK/resources/software.html
[mayavi]: http://code.enthought.com/projects/mayavi/
[wxpy]: http://wxpython.org/

#### Astronomical software
- [pyephem][pye], [jplephem][jpl], [de405][de405], [sgp4][sgp4]
- Large data sets required by these packages are downloaded automatically by the setup script
[pye]: http://pypi.python.org/pypi/pyephem/
[jpl]: http://pypi.python.org/pypi/jplephem/
[de405]: http://pypi.python.org/pypi/de405
[sgp4]: http://pypi.python.org/pypi/sgp4/

[pxy]: http://code.google.com/p/pythonxy/
[epd]: http://www.enthought.com/products/epd.php
[epd-free]: http://www.enthought.com/products/epd_free.php
[vtk-bin]: http://pythonxy.googlecode.com/files/vtk-5.10.0_py27.exe
[pxy-plug]: http://code.google.com/p/pythonxy/wiki/StandardPlugins
[cmake]: http://www.cmake.org/
[mayavi-build]: http://docs.enthought.com/mayavi/mayavi/installation.html
