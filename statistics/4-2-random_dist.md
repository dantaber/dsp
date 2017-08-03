[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

**PYTHON CODE**  

```Python

import import numpy as np
import thinkstats2
import thinkplot
import pylab

x = np.random.random(1000)

# CDF
cdf = thinkstats2.Cdf(x)
thinkplot.Cdf(cdf)
thinkplot.Config(xlabel='Random number', ylabel= 'CDF')
pylab.savefig('Ch4_Ex2_CDF.png')
thinkplot.Show()

# PMF
pmf = thinkstats2.Pmf(x)
thinkplot.Pmf(pmf)
thinkplot.Config(xlabel='Random number', ylabel='PMF')
pylab.savefig('Ch4_Ex2_PMF.png')
thinkplot.Show()
```
**ANSWER**  
The CDF and PMF figures both clearly suggest that the distribution is uniform. As you'd expect, the PMF indicates that numbers are equally likely to appear (p=.001) and the CDF indicates that the cumulative distribution increases at a steady rate.  
  
![Ch4_Ex2_CDF](https://github.com/dantaber/dsp/blob/master/img/Ch4_Ex2_CDF.png?raw=true)
![Ch4_Ex2_PMF](https://github.com/dantaber/dsp/blob/master/img/Ch4_Ex2_PMF.png?\
raw=true)