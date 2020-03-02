# demos for ch04
# Logistic logistic regression for binary classification
```matlab
close all;
clear; 
d = 2;
k = 2;
n = 1000;
[X,t] = kmeansRnd(d,k,n);
[model, llh] = logitBin(X,t-1);
plot(llh);
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch04/logitBin_demo_images/figure_0.png)

```matlab
y = logitBinPred(model,X)+1;
figure
binPlot(model,X,y)
```

![figure_1.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch04/logitBin_demo_images/figure_1.png)

