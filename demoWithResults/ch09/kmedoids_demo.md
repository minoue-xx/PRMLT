```matlab
close all; clear;
d = 2;
k = 3;
n = 5000;
[X,label] = kmeansRnd(d,k,n);
init = ceil(k*rand(1,n));
[y, idx, v] = kmedoids(X,init);
plotClass(X,label);
```

![](kmedoids_demo_images/)

```matlab
figure;
plotClass(X,y);
```

![](kmedoids_demo_images/)

