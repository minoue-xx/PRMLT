```matlab
clear; close all;

d = 100;
beta = 1e-1;
X = rand(1,d);
w = randn;
b = randn;
t = w'*X+b+beta*randn(1,d);
x = linspace(min(X),max(X),d);   % test data

[model,llh] = linRegVb(X,t);
% [model,llh] = rvmRegVb(X,t);
plot(llh);
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch10/rvmRegVb_demo_images/figure_0.png)

```matlab
[y, sigma] = linRegPred(model,x,t);
figure
plotCurveBar(x,y,sigma);
hold on;
plot(X,t,'o');
hold off
```

![figure_1.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch10/rvmRegVb_demo_images/figure_1.png)

