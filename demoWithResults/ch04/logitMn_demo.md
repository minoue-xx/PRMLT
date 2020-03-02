# Logistic logistic regression for multiclass classification
```matlab
clear
k = 3;
n = 1000;
[X,t] = kmeansRnd(2,k,n);
[model, llh] = logitMn(X,t);
y = logitMnPred(model,X);
plotClass(X,y)
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch04/logitMn_demo_images/figure_0.png)

