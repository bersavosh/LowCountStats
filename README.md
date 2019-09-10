# LowCountStats
A fast and light-weight script to estimate uncertainties for low-count Poissonian events based on [Gehrels et al. 1986](https://ui.adsabs.harvard.edu/abs/1986ApJ...303..336G/abstract) and [Kraft et al. 1991](https://ui.adsabs.harvard.edu/abs/1991ApJ...374..344K/abstract). If no information about the background is provided, the estimated limits will be based on Poisson statistics as prescribed by Gehrels. Otherwise, they will be limits on the background-subtracted number of events, following the method from Kraft.

## Prerequisites 
- Python 2.6 or higher.
- [Numpy](https://numpy.org/)
- [Scipy](https://www.scipy.org/)

## Use:
You can download the script quickly in the terminal with `wget`:
```
wget https://raw.githubusercontent.com/bersavosh/LowCountStats/master/LowCountStats.py
```

And then run it simply with python:
```
python LowCountStats.py -h
```

## Examples:

Estimating Gehrels 1-sigma confidence limits for 6 counts:
```
> python LowCountStats.py 6
```

Estimating Gehrels 0.95 confidence limits for 5 counts:
```
> python LowCountStats.py 5 --cl 0.95
```

Estimating Kraft 1-sigma confidence limits for 7 counts and 4.2 bkg counts
```
> python LowCountStats.py 7 --bkg 4.2
```

Estimating Kraft 0.95 confidence limits for 11 counts and 6 bkg counts
```
> python LowCountStats.py 11 --bkg 6 --cl 0.95.
```

