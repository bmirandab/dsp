[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

### Creating Function for Cohen's d
```python
# Import libraries
import nsfg
import first
import numpy as np

# Read Data & Create DataFrames
preg = nsfg.ReadFemPreg()
live = preg[preg.outcome == 1]
firsts = live[live.birthord == 1]
others = live[live.birthord != 1]

# Create Cohen's d function
def CohenEffectSize(group1, group2):

    mean_diff = group1.mean() - group2.mean()
    pooled_std = (np.sqrt((np.std(group1) ** 2 + np.std(group2) ** 2) / 2))
    d = mean_diff / pooled_std
    return d
```
### Applying Code 

```python
# Apply function to problem
CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
-0.08865350345261151
```

### Solution Explanation

When interpreting Cohen's d, the general rule of thumb is that if the result is less than 0.5 the effect size 
is considered small. Therefore, even though the result is higher than in pregnancy lengths, the effect is still small, 
it can only be determined through a careful study.
