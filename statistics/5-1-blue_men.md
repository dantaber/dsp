[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

```Python
import scipy.stats

mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc = mu, scale = sigma)
type(dist)

# Calculate CDF for upper and lower bounds
cdf_low = dist.cdf(177.8)
cdf_high = dist.cdf(185.42)

# Calculate and print the difference
answer = (cdf_high - cdf_low)*100
print(round(answer, 1), 'percent of of the U.S. male population is the right height for Blue Man Group')
```

**ANSWER**  

```
34.3 percent of of the U.S. male population is the right height for Blue Man Group
```

