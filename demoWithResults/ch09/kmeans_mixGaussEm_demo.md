# Gauss mixture initialized by kmeans
```matlab
close all; clear;
d = 2;
k = 3;
n = 500;
[X,label] = mixGaussRnd(d,k,n);
init = kmeans(X,k);
[z,model,llh] = mixGaussEm(X,init);
```
```
EM for Gaussian mixture: running ... 
```
```matlab
plotClass(X,label);
```

![](kmeans_mixGaussEm_demo_images/)

```matlab
figure;
plotClass(X,init);
```

![](kmeans_mixGaussEm_demo_images/)

```matlab
figure;
plotClass(X,z);
```

![](kmeans_mixGaussEm_demo_images/)

```matlab
figure;
plot(llh);
```

![](kmeans_mixGaussEm_demo_images/)

