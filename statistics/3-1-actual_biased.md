[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> 
```python
resp = nsfg.ReadFemResp()

actual = thinkstats2.Pmf(resp.numkdhh, label = 'actual')
biased = BiasPmf(actual, label = 'biased')

thinkplot.PrePlot(2)
thinkplot.Pmfs([actual, biased])
thinkplot.Config(xlabel = 'PMF', ylabel = 'Number of Children in Household')
```

![Actual vs. Biased Plot](Actual_vs_Biased_Plot.png | width=100)

```python
print('The mean of the actual distribution is', str(round(actual.Mean(), 2)))
print('The mean of the biased distribution is', str(round(biased.Mean(), 2)))
```

The mean of the actual distribution is 1.02
The mean of the biased distribution is 2.4

```python
act_numkdhh = [0, 1, 2, 3, 4, 5]

diffs = []
for num in act_numkdhh:
    p1 = actual.Prob(num)
    p2 = biased.Prob(num)
    diff = 100 * (p1 - p2)
    diffs.append(diff)

thinkplot.Bar(act_numkdhh, diffs)
```

![Differences Plot](Diff_Plot.png | width=100)