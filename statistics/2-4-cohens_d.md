[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>>
**Basic Analysis**
-------------------
```python
fwt = firsts.totalwgt_lb
owt = others.totalwgt_lb

avg_firstsWeight = fwt.mean()
avg_othersWeight = owt.mean()

diff = avg_firstsWeight - avg_othersWeight

print("The mean weight (in lb) of first borns' is", str(round(avg_firstsWeight, 1)), ", while that of non-first borns' is", str(round(avg_othersWeight, 1)))
if avg_firstsWeight > avg_othersWeight:
    print("The first borns are, on average,", str(round(abs(diff), 2)), 'lb', "("+ str(round(abs(diff * 16), 2))+" ounces)", "heavier than non-first borns.")
elif avg_firstsWeight < avg_othersWeight:
    print("The first borns are, on average,", str(round(abs(diff), 2))+ 'lb', "("+ str(round(abs(diff * 16), 2))+" ounces)", "lighter than non-first borns.")
else:
    print('The first borns are, on average, the same weight as the non-first borns.')

fwt_var = fwt.var()
owt_var = owt.var()

print("First borns' weight also has slightly more variance", "("+str(round(fwt_var - owt_var, 2))+")", "than that of non-first borns.")
```

**Results**
------------

The mean weight (in lb) of first borns' is  7.2, while that of non-first borns' is 7.3.  
The first borns are, on average, 0.12 lb (2.0 ounces) lighter than non-first borns.  
First borns' weight also has slightly more variance (0.07) than that of non-first borns.  

**Cohen's Effect Size**
---------------------
```python
d_weight = CohenEffectSize(fwt, owt)

print("The Cohen's Effect Size on weight is", str(round(d_weight, 2))+ ", which is considered small.\n"
     "Cohen's Effect Size on weight ("+ str(round(d_weight, 2))+") "+ "is slightly larger than that of pregnancy length ("+ str(round(d_prglngth, 2))+")"
     ", however, since both are very small, "
      "my conclusion is that pregnancy order does not play a significant role either on pregnancy length "
      "or on the weight of the baby.")
```

**Cohen's Effect Size Results**
-------------------------------

The Cohen's Effect Size on weight is -0.09, which is considered small.
Therefore, the results suggest that there is no clear difference between the weight of the first borns
and the weight of non-first born babies. 

Cohen's Effect Size on weight (-0.09) is slightly larger than that of pregnancy length (0.03), however since both are very small, my conclusion is that pregnancy order does not play a significant role either on pregnancy length or on the weight of the baby.
