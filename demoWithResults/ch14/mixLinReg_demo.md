# Mixture of linear regression
```matlab
close all; clear
d = 1;
k = 2;
n = 500;
[X,y] = mixLinRnd(d,k,n);
plot(X,y,'.');
```

![figure_0.png](mixLinReg_demo_images/figure_0.png)

```matlab
[label,model,llh] = mixLinReg(X, y, k);
plotClass([X;y],label);
```

![figure_1.png](mixLinReg_demo_images/figure_1.png)

```matlab
figure
plot(llh);
```

![figure_2.png](mixLinReg_demo_images/figure_2.png)

```matlab
[y_,z,p] = mixLinPred(model,X,y);
figure;
plotClass([X;y],label);
```

![figure_3.png](mixLinReg_demo_images/figure_3.png)

