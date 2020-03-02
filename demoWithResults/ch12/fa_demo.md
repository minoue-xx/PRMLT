```matlab
% demos for ch12

clear; close all;
d = 3;
m = 2;
n = 1000;

X = ppcaRnd(m,d,n);
plotClass(X);
```

![figure_0.png](fa_demo_images/figure_0.png)

# Factor analysis
```matlab
[W, mu, psi, llh] = fa(X, m);
plot(llh);
```

![figure_1.png](fa_demo_images/figure_1.png)

