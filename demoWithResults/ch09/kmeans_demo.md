```matlab
close all; clear;
d = 2;
k = 3;
n = 5000;
```
# Generate data
```matlab
[X,label] = kmeansRnd(d,k,n);
plotClass(X,label);
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch09/kmeans_demo_images/figure_0.png)

# kmeans with random initialization
```matlab
y = kmeans(X,k);
figure;
plotClass(X,y);
```

![figure_1.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch09/kmeans_demo_images/figure_1.png)

# kmeans init with labels
```matlab
y = kmeans(X,label);
figure;
plotClass(X,y);
```

![figure_2.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch09/kmeans_demo_images/figure_2.png)

# kmeans init with centers
```matlab
mu = rand(d,k);
y = kmeans(X,mu);
figure;
plotClass(X,y);
```

![figure_3.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch09/kmeans_demo_images/figure_3.png)

# kmeans init with kmeans++ seeding
```matlab
y = kmeans(X,kseeds(X,k));
figure;
plotClass(X,y);
```

![figure_4.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch09/kmeans_demo_images/figure_4.png)

# kmeans++ seeding
```matlab
mu = kseeds(X,k);
[~,y] = min(dot(mu,mu,1)'/2-mu'*X,[],1); % assign sample labels
figure;
plotClass(X,y);
```

![figure_5.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch09/kmeans_demo_images/figure_5.png)

