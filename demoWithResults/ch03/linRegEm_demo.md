# Empirical Bayesian linear regression via EM
```matlab
close all; clear;
d = 5;
n = 200;
[x,t] = linRnd(d,n);
[model,llh] = linRegEm(x,t);
plot(llh);
```

![](linRegEm_demo_images/)

