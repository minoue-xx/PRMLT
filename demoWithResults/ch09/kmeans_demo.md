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

![](kmeans_demo_images/)

# kmeans with random initialization
```matlab
y = kmeans(X,k);
figure;
plotClass(X,y);
```

![](kmeans_demo_images/)

# kmeans init with labels
```matlab
y = kmeans(X,label);
figure;
plotClass(X,y);
```

![](kmeans_demo_images/)

# kmeans init with centers
```matlab
mu = rand(d,k);
y = kmeans(X,mu);
figure;
plotClass(X,y);
```

![](kmeans_demo_images/)

# kmeans init with kmeans++ seeding
```matlab
y = kmeans(X,kseeds(X,k));
figure;
plotClass(X,y);
```

![](kmeans_demo_images/)

# kmeans++ seeding
```matlab
mu = kseeds(X,k);
[~,y] = min(dot(mu,mu,1)'/2-mu'*X,[],1); % assign sample labels
figure;
plotClass(X,y);
```

![](kmeans_demo_images/)

