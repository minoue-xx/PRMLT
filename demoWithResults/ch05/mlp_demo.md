```matlab
clear; close all
```
# Regression
```matlab
n = 200;
x = linspace(0,2*pi,n);
y = sin(x);

h = [10,6];            % two hidden layers with 10 and 6 neurons
lambda = 1e-2;
[model, L] = mlpReg(x,y,h,lambda);
t = mlpRegPred(model,x);
plot(L);
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch05/mlp_demo_images/figure_0.png)

```matlab
figure;
hold on
plot(x,y,'.');
plot(x,t);
hold off
```

![figure_1.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch05/mlp_demo_images/figure_1.png)

# Classification
```matlab
clear;
k = 2;
n = 200;
[X,y] = kmeansRnd(2,k,n);
figure;
plotClass(X,y);
```

![figure_2.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch05/mlp_demo_images/figure_2.png)

```matlab

h = 3;
lambda = 1e-2;
[model, llh] = mlpClass(X,y,h,lambda);
[t,p] = mlpClassPred(model,X);
plot(llh);
```

![figure_3.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch05/mlp_demo_images/figure_3.png)

```matlab
figure;
plotClass(X,t);
```

![figure_4.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch05/mlp_demo_images/figure_4.png)

```matlab
figure;
```
