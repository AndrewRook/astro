This folder contains the combined Python/C++ scripts I used to perform Levenberg-Marquardt galaxy model fitting in Schechtman-Rook & Bershady (in prep). The codes have been packaged up as a tarball using distutils, so it can be installed using the 'python setup.py install' syntax common for Python libraries.

This package has been *highly* customized for use on the UW-Madison Center for High Throughput Computing distributed Condor cluster, and as a result will likely require significant modification to operate on other systems. This code is therefore provided more as a resource for other researchers to look at and both learn how such a galaxy fitting code can be written as well as check my work. Towards that end I have provided a sample configuration file ('NGC891_3disk_woutertrunc.cfg') for inspection to hopefully make understanding the inputs of the fitting algorithm easier (this file is provided at the command line when calling the fitter).

Dependencies:
numpy, scipy, astropy, lmfit*

*Note that the package actually requires a version of lmfit 0.3 with minor tweaks, to pass more information about the free parameters through the minimizer. To make a compatible version of lmfit, you will need to add the keyword argument 'compid=None' to the add method of the Parameters class (line 48) as well as to the Parameter initialization definition (line 80), set the keyword argument 'compid=compid' on line 57, and then set 'self.compid = compid' on line 87. 

Tested on: Python 2.7
