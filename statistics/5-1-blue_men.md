[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

### Generating Data
```python
# Import libraries
from scipy import stats

# Inputting Given Values and Generating Distribution
mu = 178
sigma = 7.7
dist = stats.norm(loc=mu, scale=sigma)
```

### Creating Function for Conversion
```python
def HeightInches(ft, inches):

    inches += ft * 12
    h_cm = round(inches * 2.54, 1)
    return h_cm
```
### Applying Function to Generate Values
```python
min_height = HeightInches(5,10)
max_height = HeightInches(6,1)
```
### Calculating Height Percentages

```python
#Percent of men under 5'10 tall
min_height_total = norm.cdf(min_height)
0.48963902786483265

#Percent of men under 6'1 tall
max_height_total = norm.cdf(max_height)
0.8317337108107857

#Percent of men between 5'10 and 6'1 tall
max_min_diff = max_height_total-min_height_total
0.3420946829459531
```

### Intrepreting Results
Around 34% of the U.S. male could potentially be part of the Blue Map Group.

