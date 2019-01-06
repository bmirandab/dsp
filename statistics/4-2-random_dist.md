[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

### Calculating PMF and Plotting Results
```python
# Import libraries
import thinkstats2
import thinkplot
import numpy as np

# Generating Random Numbers
t = np.random.random(1000)
```

### Computing and Plotting PMF
```python
pmf = thinkstats2.Pmf(t)
thinkplot.Pmf(pmf, linewidth=0.1)
thinkplot.Config(xlabel='Random variate', ylabel='PMF')
```
![Actual PMF](https://github.com/bmirandab/dsp/blob/master/PMF%20Random%20Numbers.png)

### Computing and Plotting CDF

```python
cdf = thinkstats2.Cdf(t)
thinkplot.Cdf(cdf)
thinkplot.Config(xlabel='Random variate', ylabel='CDF')
```
![Actual PMF](https://github.com/bmirandab/dsp/blob/master/CDF%20Random%20Numbers.png)

### Intrepreting Results
The results obtained from 1000 random numbers is of a uniform distribution, meaning that each variable has the same probability of being an outcome, and all outcomes are equally likely. The uniform distribution can be observed by the shape of both PMF (rectangular) and CDF (straight line).
