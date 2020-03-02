# Mixture of linear regression
```matlab
close all; clear
d = 1;
k = 2;
n = 500;
[X,y] = mixLinRnd(d,k,n);
plot(X,y,'.');
```

![](mixLinReg_demo_images/)

```matlab
[label,model,llh] = mixLinReg(X, y, k);
plotClass([X;y],label);
```

![](mixLinReg_demo_images/)

```matlab
figure
plot(llh);
```

![](mixLinReg_demo_images/)

```matlab
[y_,z,p] = mixLinPred(model,X,y);
figure;
plotClass([X;y],label);
```

![](mixLinReg_demo_images/)

