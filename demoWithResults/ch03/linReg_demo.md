# demos for ch03
```matlab
clear; close all;
d = 1;
n = 200;
[x,t] = linRnd(d,n);
```
# Linear regression
```matlab
model = linReg(x,t);
[y,sigma] = linRegPred(model,x,t);
plotCurveBar( x, y, sigma );
hold on;
plot(x,t,'o');
hold off;
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch03/linReg_demo_images/figure_0.png)

