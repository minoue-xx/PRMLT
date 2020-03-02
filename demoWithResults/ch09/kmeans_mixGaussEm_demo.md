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

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch09/kmeans_mixGaussEm_demo_images/figure_0.png)

```matlab
figure;
plotClass(X,init);
```

![figure_1.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch09/kmeans_mixGaussEm_demo_images/figure_1.png)

```matlab
figure;
plotClass(X,z);
```

![figure_2.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch09/kmeans_mixGaussEm_demo_images/figure_2.png)

```matlab
figure;
plot(llh);
```

![figure_3.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch09/kmeans_mixGaussEm_demo_images/figure_3.png)

