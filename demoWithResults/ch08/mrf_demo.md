```matlab
% Done!
clear; close all;
% load letterA.mat;
% X = A;
load letterX.mat
```
# Original image
```matlab
img = double(X);
img = sign(img-mean(img(:)));

figure;
subplot(2,2,1);
imagesc(img);
title('Original image');
axis image;
colormap gray;
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch08/mrf_demo_images/figure_0.png)

# Noisy image
```matlab
sigma = 1; % noise level
x = img + sigma*randn(size(img)); % noisy signal
subplot(2,2,2);
imagesc(x);
title('Noisy image');
axis image;
colormap gray;
```

![figure_1.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch08/mrf_demo_images/figure_1.png)

# Construct MRF data
```matlab
epoch = 20;
J = 1;   % ising parameter
[A,nodePot,edgePot] = mrfIsGa(x,sigma,J);
```
# Mean Field
```matlab
[nodeBel0,edgeBel0,lnZ0] = mrfMf(A,nodePot,edgePot,epoch);

L0 = mrfGibbs(A,nodePot,edgePot,nodeBel0);
L1 = mrfBethe(A,nodePot,edgePot,nodeBel0,edgeBel0);
maxdiff(L0,lnZ0(end))
```
```
ans = 0
```
```matlab
maxdiff(L0,L1)
```
```
ans = 0
```
```matlab

subplot(2,2,3);
imagesc(reshape(nodeBel0(1,:),size(img)));
title('Mean Field');
axis image;
colormap gray;
```

![figure_2.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch08/mrf_demo_images/figure_2.png)

# Belief Propagation
```matlab
[nodeBel1,edgeBel1,lnZ1] = mrfBp(A,nodePot,edgePot,epoch);

subplot(2,2,4);
imagesc(reshape(nodeBel1(1,:),size(img)));
title('Belief Propagation');
axis image;
colormap gray;
```

![figure_3.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch08/mrf_demo_images/figure_3.png)

# Energy comparation
```matlab
figure
epochs = 1:epoch;
plot( epochs,lnZ0,'-', ...
      epochs,lnZ1,'-');
xlabel('epoch');       %  add axis labels and plot title
ylabel('energy');
title('Energy Comparation');
legend('MF','BP');
```

![figure_4.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch08/mrf_demo_images/figure_4.png)

