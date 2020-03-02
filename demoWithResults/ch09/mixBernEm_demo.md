# Bernoulli Mixture via EM
```matlab
close all; clear;
d = 2;
k = 3;
n = 5000;
[X,z,mu] = mixBernRnd(d,k,n);
[label,model,llh] = mixBernEm(X,k);
```
```
EM for mixture model: running ... 
```
```matlab
plot(llh);
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch09/mixBernEm_demo_images/figure_0.png)

