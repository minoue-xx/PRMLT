```matlab
% demos for HMM in ch13
d = 3; k = 2; n = 10000;
[x,model] = hmmRnd(d,k,n);
```
# Viterbi algorithm
```matlab
[z, llh] = hmmViterbi(model, x);
```
# HMM filter (forward algorithm)
```matlab
[alpha, llh] = hmmFilter(model, x);
```
# HMM smoother (forward backward)
```matlab
[gamma,alpha,beta,c] = hmmSmoother(model, x);
```
# Baum-Welch algorithm
```matlab
[model, llh] = hmmEm(x,k);
plot(llh)
```

![figure_0.png](C:/Users/minoue/github/PRMLT/demoWithResults/ch13/hmm_demo_images/figure_0.png)

