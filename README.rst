Python XMP Toolkit is a library for working with XMP metadata, as well as
reading/writing XMP metadata stored in many different file formats. 

Python XMP Toolkit is wrapping Exempi (using ctypes), a C/C++ XMP library
based on Adobe XMP Toolkit, ensuring that future updates to the XMP standard
are easily incorporated into the library with a minimum amount of work.

Python XMP Toolkit has been developed by: 
 * ESA/Hubble - European Space Agency 
 * ESO - European Southern Observatory
 * CRS4 - Centre for Advanced Studies, Research and Development in Sardinia

Installation
============

Requirements
------------

 * Python 2.5+
 * Exempi 2.1.1
 * Linux or OS X (see notes below for Windows)


Python XMP Toolkit
----------------------
The short version of installation is::

  python setup.py install

Note, in case you haven't installed Exempi you will get an
:exc:`ExempiLoadError` exception once you try to load :mod:`libxmp`.

Exempi
------
Python XMP Toolkit requires Exempi 2.1 which can be downloaded from
http://libopenraw.freedesktop.org/wiki/Exempi. To install Exempi, unpack the
distribution and run::

  ./configure
  make
  sudo make install


Mac OS X
--------
Note Exempi requires boost (http://www.boost.org/) to compile, so on OS X you
probably need to run configure with one of the following options.::

  ./configure --with-darwinports
  ./configure --with-fink

.. warning::
	Note, only Exempi 2.1.1 compiles on OS X and Exempi 2.1.1 also fixes an issue over 2.1
	that could lead to complete crash of the Python interpreter.

Windows
-------
The library has not been tested on Windows, and nor has any serious effort
been made to test it. Hence, developers wanting to use the library on Windows
are encouraged to try it out and let us know if it works.

The library ought to work on Windows, if Exempi can be compiled as a DLL using
e.g. Cygwin.

Additional documentation is included in the docs/ directory in both HTML and
PDF versions.