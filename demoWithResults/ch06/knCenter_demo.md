# demo for knCenter
```matlab
clear; close all;
kn = @knGauss;
X=rand(2,100);
X1=rand(2,10);
X2=rand(2,5);

maxdiff(knCenter(kn,X,X1),diag(knCenter(kn,X,X1,X1))')
```
```
ans = 2.2204e-16
```
```matlab
maxdiff(knCenter(kn,X),knCenter(kn,X,X,X))
```
```
ans = 0
```
