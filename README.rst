scorr
=====

Fast two- and three-point correlation analysis for time series
using spectral methods.

The calculations are FFT-based for optimal performance and offer many options 
for normalisation, mean removal, averaging, and zero-padding. In particular, 
averaging over pandas groups of different sizes (e.g. different days) is 
supported.
    
======================  ======================================================
Function                Synopsis
======================  ======================================================
acorr                   Calculate autocorrelation or autocovariance
acorr_grouped_df        Calculate acorr for pandas groups and average
corr_mat                Convert correlation vector to matrix
fft2x                   Calculate cross-bispectrum
fftcrop                 Return cropped fft or correlation
get_nfft                Find a good FFT segment size for pandas groups of 
                        different sizes 
padded_x3corr_norm      Normalise and debias three-point cross-correlations
padded_xcorr_norm       Normalise and debias two-point cross-correlations
x3corr                  Calculate three-point cross-correlation matrix
x3corr_grouped_df       Calculate x3corr for pandas groups and average
xcorr                   Calculate two-point cross-correlation or covariance
xcorr_grouped_df        Calculate xcorr for pandas groups and average
xcorrshift              Convert xcorr output so lag zero is centered
======================  ======================================================

The algorithms to calculate three-point correlations and details of daily
averaging over high-frequency trading data are described in:
	
    Patzelt, F. and Bouchaud, J-P. (2017):
    Nonlinear price impact from linear models. 
    Journal of Statistical Mechanics: Theory and Experiment, 12, 123404. 
    Preprint at `arXiv:1708.02411 <//arxiv.org/abs/1708.02411>`_.

More code from the same publication is released in the `priceprop 
<https://github.com/felixpatzelt/priceprop>`_ package. 

Please find further 
explanations in the docstrings and in the examples 
directory. 


Installation
------------

	pip install scorr
	

Dependencies (automatically installed)
--------------------------------------

    - Python 2.7 or 3.6
    - NumPy
    - SciPy
    - Pandas    
   
    
Optional Dependencies required only for the examples (pip installable)
----------------------------------------------------------------------

    - Jupyter
    - Matplotlib
    - colorednoise
