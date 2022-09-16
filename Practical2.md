# Practical #2



<br>

**Experiment:** Estimate the standardised death rates for the two countries from the given data.

<img src="file:///C:/Users/Pranav/AppData/Roaming/marktext/images/2022-08-17-01-01-26-image.png" title="" alt="" width="592">


**Aim:** To calculate standardised death rate

**Theory:** *Standardised Death Rates* of *A* and *B* are given respectively by :

$$
m^a=\frac{D^a}{P^a}\times1000 =\frac{\sum_xm_x^aP_x^a}{\sum_xp_x^a}
$$

$$
m^b=\frac{D^b}{P^b}\times1000=\frac{\sum_xm_x^bP_x^b}{\sum_xp_x^b}
$$

<br>

<br>



**R code:** 

```r
rm(list=ls())
m_a=c(20.0,1.0,1.4,2.0,3.3,7.0,15.0,40.0,120.0)
m_b=c(5.0,0.5,1.0,1.0,2.0,5.0,12.0,35.0,110.0)
P_s=c(100,200,190,180,120,100,70,30,10)
L_a=m_a *P_s
L_b=m_b *P_s
STDR_A=sum(L_a)/sum(P_s)
STDR_A
STDR_B=sum(L_b)/sum(P_s)
STDR_B
```

<br>

<br>

<br>





**R console:** 

``` R
> rm(list=ls())
> m_a=c(20.0,1.0,1.4,2.0,3.3,7.0,15.0,40.0,120.0)
> m_b=c(5.0,0.5,1.0,1.0,2.0,5.0,12.0,35.0,110.0)
> P_s=c(100,200,190,180,120,100,70,30,10)
> L_a=m_a *P_s
> L_b=m_b *P_s
> STDR_A=sum(L_a)/sum(P_s)
> STDR_A
[1] 7.372
> STDR_B=sum(L_b)/sum(P_s)
> STDR_B
[1] 4.7
> 
```



<br>

**CONCLUSION:**

From the above Experiment we conclude that:

$(STDR)_A=7.372$

$(STDR)_B=4.7$
