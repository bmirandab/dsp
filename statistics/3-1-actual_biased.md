[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

### Calculating PMF and Plotting Results
```python
# Import libraries
import nsfg
import first
import thinkstats2
import thinkplot

# Read Data, Calculating & Plotting PMF
resp = nsfg.ReadFemResp()
pmf = thinkstats2.Pmf(resp.numkdhh, label = 'numkdhh')
thinkplot.Pmf(pmf)
thinkplot.Config(xlabel='Number of children', ylabel='PMF')
```
![Actual PMF](https://github.com/bmirandab/dsp/blob/master/PMF(Actual).png)

### Computing Biased Distribution
```python
# Function created to calculate biased distribution
def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf
```
### Applying Function and Plotting Comparative Results

```python
# Apply function to pmf
biased = BiasPmf(pmf, label='biased')

thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased])
thinkplot.Config(xlabel='Number of children', ylabel='PMF')
```
![Actual PMF](https://github.com/bmirandab/dsp/blob/master/PMF(Actual:Biased).png)

### Computing Means
```python
pmf.Mean()
biased.Mean()
1.024205155043831
2.403679100664282
```
