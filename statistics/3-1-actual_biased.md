[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

**PYTHON CODE**  
  

```Python
from __future__ import print_function, division
%matplotlib inline
import numpy as np
import nsfg
import first
import thinkstats2
import thinkplot
import pylab

# Read data
df = nsfg.ReadFemResp()

# Actual distribution
pmf = thinkstats2.Pmf(df.numkdhh, label='actual')

thinkplot.PrePlot(2)
thinkplot.Pmf(pmf)
thinkplot.Config(xlabel='Number of kids', ylabel='PMF')

actual = pmf.Mean()

# Biased distribution
def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf

biased_pmf = BiasPmf(pmf, label='observed')

thinkplot.PrePlot(2)
thinkplot.Pmf(biased_pmf)
thinkplot.Config(xlabel='Number of kids', ylabel='PMF')

bias = biased_pmf.Mean()

# Plot both distributions
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased_pmf])
thinkplot.Config(xlabel='Number of kids', ylabel='PMF')

pylab.savefig('Ch 3, Exercise 1.png')

print ("The actual mean number of kids per household =", round(actual, 3))
print ("The biased estimate of the mean numnber of kids per household =", round(bias, 3))
```
![Ch3_Ex1](https://github.com/dantaber/dsp/blob/master/img/Ch3_Ex1.png?raw=true)

**ANSWER**  
The actual mean is 1.024  
The biased estimate of the mean is 2.404