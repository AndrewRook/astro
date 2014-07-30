This folder contains the Python script I used to do the Voronoi binning in Schechtman-Rook & Bershady (in prep).

Running the program is fairly simple. The only command line argument you need to provide is the name of a configuration file, an example of which is provided here (NGC891_voronoi.cfg). The arguments should be fairly self-explanatory, with the few exceptions possibly being 'cvt_iters' (the number of iterations to do the algorithm over), 'max_z_kpc' (above this height don't bother trying to bin the data), and 'max_bin_size_pix' (bins larger than this will be ignored and the pixels will be treated individually).

The program can take a while (~an hour for the example images) to run, and so I recommend trying it out first on a smaller image to make sure everything is copacetic. While it runs it will print out diagnostic information so you know stuff is happening.  

Dependencies:
numpy, astropy, scikit-learn, scipy

Tested on: Python 2.7
