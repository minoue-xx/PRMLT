# Collapse Gibbs sampling for Dirichelt process gaussian mixture model
```matlab
close all; clear;
d = 2;
k = 3;
n = 500;
[X,z] = mixGaussRnd(d,k,n);
plotClass(X,z);
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch11/mixGaussGb_demo_images/figure_0.png)

```matlab

[z,Theta,w,llh] = mixGaussGb(X);
figure
plotClass(X,z);
```

![figure_1.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch11/mixGaussGb_demo_images/figure_1.png)

```matlab

[X,z] = mixGaussSample(Theta,w,n);
figure
plotClass(X,z);
```

![figure_2.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch11/mixGaussGb_demo_images/figure_2.png)

