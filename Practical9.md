# Practical #9



**Experiment:	** The following are the mean and ranges of 20 samples of size 5 each. The data pertain to the overall length of a fragmentation bomb base manufactured during the war by the American store camp.

![image-20220906214546684](https://raw.githubusercontent.com/ydvpratik/img/master/2022/09/upgit_20220916_1663341119.png) 

$(a)$ From these data, obtain the control limits for $\bar{X}$ and $R-$charts to control the length of bomb bases produced in the future.

$(b)$ The above samples were taken every 15 minutes in order of production. The production rate was 350 units per hour and the tolerance were 0.820 and 0.840 inches.

On the assumption  that the lengths of bases are normally distributed, what percentage of the bomb base would you estimate to have length outside the tolerance limits when the process is under control at the levels indicated by the above data?

​       [For $n=5$, use $A_2=0.58$,     $D_3=0$ ,   $D_4=2.12$,  $d_2=2.326$  ]

**Aim:**

**Methodology:**

**R-Code:**

```R
rm(list=ls())
M_ean=c(0.8372,0.8324,0.8318,0.8344,0.8346,0.8332,0.8340,0.8344,0.8308,0.8350,0.8380,0.8322,0.8356,0.8322,0.8404,0.8372,0.8282,0.8346,0.8360,0.8374)
R_ange=c(0.010,0.009,0.008,0.004,0.005,0.011,0.009,0.003,0.002,0.006,0.006,0.002,0.013,0.005,0.008,0.011,0.006,0.006,0.004,0.006)
n=5
A_2=0.58
D_3=0
D_4=2.12
d_2=2.326
X_2bar=mean(M_ean)
X_2bar
R_mean=mean(R_ange)
R_mean
UCL=X_2bar+(A_2*R_mean)
UCL
CL=X_2bar
CL
LCL=X_2bar-(A_2*R_mean)
LCL
X_2barUpdated=(sum(M_ean)-0.8380-0.8282)/18
X_2barUpdated
R_meanUpdated=(sum(R_ange)-0.006-0.006)/18
R_meanUpdated
UCL_R=D_4*R_mean
UCL_R
CL_R=R_mean
CL_R
LCL_R=D_3*R_mean
LCL_R
Mue_hat=X_2barUpdated
Mue_hat
Sigma_hat=R_meanUpdated/d_2
Sigma_hat
p = pnorm(0.82,mean=0.834077,sd=0.00291392)+pnorm(0.84,mean=0.834077,sd=0.00291392)
p
```

**R-Console:** 

```R
> rm(list=ls())
> M_ean=c(0.8372,0.8324,0.8318,0.8344,0.8346,0.8332,0.8340,0.8344,0.8308,0.8350,0.8380,0.8322,0.8356,0.8322,0.8404,0.8372,0.8282,0.8346,0.8360,0.8374)
> R_ange=c(0.010,0.009,0.008,0.004,0.005,0.011,0.009,0.003,0.002,0.006,0.006,0.002,0.013,0.005,0.008,0.011,0.006,0.006,0.004,0.006)
> n=5
> A_2=0.58
> D_3=0
> D_4=2.12
> d_2=2.326
> X_2bar=mean(M_ean)
> X_2bar
[1] 0.83448
> R_mean=mean(R_ange)
> R_mean
[1] 0.0067
> UCL=X_2bar+(A_2*R_mean)
> UCL
[1] 0.838366
> CL=X_2bar
> CL
[1] 0.83448
> LCL=X_2bar-(A_2*R_mean)
> LCL
[1] 0.830594
> X_2barUpdated=(sum(M_ean)-0.8380-0.8282)/18
> X_2barUpdated
[1] 0.8346333
> R_meanUpdated=(sum(R_ange)-0.006-0.006)/18
> R_meanUpdated
[1] 0.006777778
> UCL_R=D_4*R_mean
> UCL_R
[1] 0.014204
> CL_R=R_mean
> CL_R
[1] 0.0067
> LCL_R=D_3*R_mean
> LCL_R
[1] 0
> Mue_hat=X_2barUpdated
> Mue_hat
[1] 0.8346333
> Sigma_hat=R_meanUpdated/d_2
> Sigma_hat
[1] 0.00291392
> p = pnorm(0.82,mean=0.834077,sd=0.00291392)+pnorm(0.84,mean=0.834077,sd=0.00291392)
> p
[1] 0.9789571
> 

```

