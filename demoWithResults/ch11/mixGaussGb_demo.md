# Collapse Gibbs sampling for Dirichelt process gaussian mixture model
```matlab
close all; clear;
d = 2;
k = 3;
n = 500;
[X,z] = mixGaussRnd(d,k,n);
plotClass(X,z);
```

![](mixGaussGb_demo_images/)

```matlab

[z,Theta,w,llh] = mixGaussGb(X);
figure
plotClass(X,z);
```

![](mixGaussGb_demo_images/)

```matlab

[X,z] = mixGaussSample(Theta,w,n);
figure
plotClass(X,z);
```

![](mixGaussGb_demo_images/)

