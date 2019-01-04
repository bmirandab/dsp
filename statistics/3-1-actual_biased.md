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
### Applying Function and Plotting Results

```python
# Apply function to pmf
biased = BiasPmf(pmf, label='biased')

thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased])
thinkplot.Config(xlabel='Number of children', ylabel='PMF')
```
### Computing Means
```python
pmf.Mean()
biased.Mean()
1.024205155043831
2.403679100664282
```
### Solution Explanation

When interpreting Cohen's d, the general rule of thumb is that if the result is less than 0.5 the effect size 
is considered small. Therefore, even though the result is higher than in pregnancy lengths, the effect is still small, 
it can only be determined through a careful study.
