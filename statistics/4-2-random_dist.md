[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>>
```python
sample = np.random.random(1000)
sample_pmf = thinkstats2.Pmf(sample)

thinkplot.Pmf(sample_pmf, linewidth = 0.1)
thinkplot.Config(xlabel = 'Randon number', ylabel = 'PMF')
```
**PMF**  
<img src="Random Number PMF.png" width="450">

```python
sample_cdf = thinkstats2.Cdf(sample, label = 'Randoms')
thinkplot.Cdf(sample_cdf)
thinkplot.Config(xlabel = 'Random Numbers', ylabel = 'CDF')
```  
**CDF**  
<img src="Random Number CDF.png" width="450">