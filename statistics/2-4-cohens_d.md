[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

```python
import numpy as np
import nsfg

# Read data
df = nsfg.ReadFemPreg()

# Restrict to live births
live = df[df.outcome==1]

# Divide into first babies vs. other
first = live[live.birthord == 1]
other = live[live.birthord != 1]

# Define Cohen's effect size
def CohenEffectSize(group1, group2):
    diff = group1.mean() - group2.mean()

    var1 = group1.var()
    var2 = group2.var()
    n1, n2 = len(group1), len(group2)

    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / np.sqrt(pooled_var)
    return d

# Calculate Cohen's effect size for birthweight
answer = CohenEffectSize(answer = CohenEffectSize(first.totalwgt_lb, other.totalwgt_lb)

print ("Mean birthweight for first babies =", round(first.totalwgt_lb.mean(), 2))
print ("Mean birthweight for other babies =", round(other.totalwgt_lb.mean(), 2))
print ("Cohen's effect size for birthweight =", round(answer, 3)) 
```

**ANSWER**
First babies tend to be less heavy than other babies, but the difference is almost negligible (Cohen's *d* = -0.089, or less than 10% of a standard deviation). This is larger than the difference in pregnancy length (Cohen's *d* = 0.029) but still a small effect size. 
