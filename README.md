# LowCountStats
A fast and light-weight script to estimate uncertainties for low-count Poissonian events based on [Gehrels et al. 1986](https://ui.adsabs.harvard.edu/abs/1986ApJ...303..336G/abstract) and [Kraft et al. 1991](https://ui.adsabs.harvard.edu/abs/1991ApJ...374..344K/abstract). If no information about the background is provided, the estimated limits will be based on Poisson statistics as prescribed by Gehrels. Otherwise, they will be limits on the background-subtracted number of events, following the method from Kraft.

## Prerequisites 
- Python 2.6 or higher.
- [Numpy](https://numpy.org/)
- [Scipy](https://www.scipy.org/)

## Use:
The intetion here is to get numbers quickly. So, no installation needed. You can simply download the script with any method you prefer and run it. If you're not familiar with Github, you can quickly download the script in the terminal using `wget`:
```
wget https://raw.githubusercontent.com/bersavosh/LowCountStats/master/LowCountStats.py
```

And then run it simply with python:
```
python LowCountStats.py -h
```

The `-h` will bring up the help documentation. Below are a few examples of how to run it. 

## Examples:

Estimating 1-sigma confidence limits for 6 counts:
```
$ python LowCountStats.py 6
For 6 events, Gehrels 0.8413 confidence level boundaries are:

3.62 -- 9.58 

```

Estimating 0.95 confidence limits for 5 counts:
```
$ python LowCountStats.py 5 --cl 0.95
For 5 events, Gehrels 0.95 confidence level boundaries are:

1.97 -- 10.51 

```

Estimating 1-sigma confidence limits for 6 counts and 1.2 bkg counts
```
$ python LowCountStats.py 6 --bkg 1.2
For 6 events and a background of 1.2, Kraft 0.8413 confidence level boundaries are:

1.95 -- 9.01 

```

Estimating 0.99 confidence limits for 9 counts and 1.5 bkg counts
```
$ python LowCountStats.py 9 --bkg 1.5 --cl 0.99
For 9 events and a background of 1.5, Kraft 0.99 confidence level boundaries are:

1.77 -- 17.7 

```

## License:
This script is developed and maintained by [Arash Bahramian](https://bersavosh.github.io/). Feel free to contact me if you have any comments/questions/suggestions. Licensed under GNU v3.

