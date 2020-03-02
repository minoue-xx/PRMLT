# Empirical Bayesian linear regression via EM
```matlab
close all; clear;
d = 5;
n = 200;
[x,t] = linRnd(d,n);
[model,llh] = linRegEm(x,t);
plot(llh);
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch03/linRegEm_demo_images/figure_0.png)

