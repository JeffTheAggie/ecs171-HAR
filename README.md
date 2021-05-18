# ECS171 Group 19 Final Project Repository - Ryan's Branch

## Repo Rules

1. Unless we've all agreed, **never edit the master branch**. Make your own branch, push it upstream, and push to that. I recommend setting up your own branch as soon as you clone the repo so you don't forget and need to fix things later.
1. Have a .gitignore file! You don't want to clutter the repo even on your own branch in case merges need to happen. 

## Ryan's Notes

Since ML algorithms generally don't work well with time series data, we will try to instead perform learning on spectral components of the data. 

To this end, we do the following:

1. Pre-emphasize
2. Framing
3. FFT (magnitude spectrum and power spectrum)
4. Band Filtering
5. DCT (cepstral coefficents)

From here we have several possible features we can extract:
- magnitude spectrum bands
- power spectrum bands
- cepstral coefficients

See the notebook for exact implementation details.

Also check out the discrete wavelet transform for cleaning the data. (DDT and D5) And potentially the S-G filter

#### 5/17

Finished initial data preprocessing. 
There are 16 chosen frequency bands filtered out using overlapping triangle filters. Because the overlap causes high correlation between adjacent frequency bands, I may go back and change the filtering method.

Note that the notebook makes use of the multiprocessing module to speed up all the reads and writes to the 3000+ files. Python's multiprocessing module can be buggy depending on the system you're on, so proceed with caution when using it. 

Environment:
Python 3.9.2
jupyter-notebook 6.3.0
ipython 7.22.0
ipykernel 5.5.3

Hardware:
Macbook Pro 2015 Mojave
Intel Core i7 
16GB RAM, 4 CPUs




## Helpful Links:

- [Overleaf](https://www.overleaf.com/2831641793btyqfpdprfht)
- [Google Drive](https://drive.google.com/drive/u/1/folders/0AMQYoN24YgDyUk9PVA)