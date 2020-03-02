# RVM for classification
```matlab
clear; close all
k = 2;
d = 2;
n = 1000;
[X,t] = kmeansRnd(d,k,n);

[model, llh] = rvmBinFp(X,t-1);
plot(llh);
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch07/rvmBinFp_demo_images/figure_0.png)

```matlab
y = rvmBinPred(model,X)+1;
figure;
plotClass(X,y);
```

![figure_1.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch07/rvmBinFp_demo_images/figure_1.png)

