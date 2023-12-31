How to install Boost
====================
From PyPI
^^^^^^^^^
    $ pip3 install boost

From sources
^^^^^^^^^^^^
* You need at least Python 3.4.

* On some Linux Distribution **setuptools** package does not come with default python install, you need to install it.

* Install **PIP**::

    	$ wget https://bootstrap.pypa.io/get-pip.py -O - | sudo python3
    
    
* Install **setuptools** module::    
  
    $ wget https://bootstrap.pypa.io/ez_setup.py -O - | sudo python3
  (Alternatively, Setuptools may be installed to a user-local path)::
	  
	       $ wget https://bootstrap.pypa.io/ez_setup.py -O - | python3 - --user

* Untar the tarball and go to the source directory with the following commands::

    $ tar zxvf boost-0.1.tar.gz
    $ cd boost

* Next, to install Boost on your computer, type the following command with the root user::

    $ python3 setup.py install
    $ # or
    $ python3 setup.py install --install-scripts=/usr/bin

