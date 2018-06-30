[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> 
```python
lower = 177.8
upper = 185.4

lower_bound = scipy.stats.norm.cdf(lower, mu, sigma)
upper_bound = scipy.stats.norm.cdf(upper, mu, sigma)
pop_share = (upper_bound - lower_bound) * 100

print(str(round(pop_share, 2))+ "% of total male population would be eligible to join the Blue Man Group.")
```  
34.21% of total male population would be eligible to join the Blue Man Group.