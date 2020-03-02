# Gausssian Mixture via EM
```matlab
close all; clear;
d = 2;
k = 3;
n = 1000;
[X,label] = mixGaussRnd(d,k,n);
plotClass(X,label);
```

![figure_0.png](mixGaussEm_demo_images/figure_0.png)

```matlab

m = floor(n/2);
X1 = X(:,1:m);
X2 = X(:,(m+1):end);
% train
[z1,model,llh] = mixGaussEm(X1,k);
```
```
EM for Gaussian mixture: running ... 
```
```matlab
figure;
plot(llh);
```

![figure_1.png](mixGaussEm_demo_images/figure_1.png)

```matlab
figure;
plotClass(X1,z1);
```

![figure_2.png](mixGaussEm_demo_images/figure_2.png)

```matlab
% predict
z2 = mixGaussPred(model,X2);
figure;
plotClass(X2,z2);
```

![figure_3.png](mixGaussEm_demo_images/figure_3.png)

