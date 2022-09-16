# Practical #5



**Experiment:** Given the following table for $l_x$, the number of rabbits living at age $x$ complete the life table for rabbits.

 ![](C:\Users\Pranav\AppData\Roaming\marktext\images\2022-08-21-16-57-20-image.png)

$X,Y,Z$ are three rabbits of age 1,2 and 3 years respectively. Find the probability that:

$(i)$ at least one of rabbit will be alive for one year more,

$(ii)$X,Y,Z will be alive for two years time,

(iii) exactly one of the three is alive in two years, and

(iv) all will be dead in two years time.



**AIM:** To find probability 

$(i)$at least one of rabbit  will be alive for one year more,

$(ii)$ $X,Y,Z$ will be alive for two years time,

$(iii)$ exactly one of the three is alive in two years, and

$(iv)$ all will be dead in two years time.






**Theory:**

For life aged $x$ probability of survival of $d$ more years will be given by $l_{(x+d)}/l_x$

For two independent event with probability p and q respectively will be given by $pq$.

Probability of death in next $d$ years of life aged x is given by ${l_x-l_{(x+d)}}/l_x$

<br>



**R-Code:**

```r
#Given rabbit X,Y,Z aged 1,2,3 respectively 
rm(list=ls())
lx<-c(100,90,80,75,60,30,0)
dx<- lx[-7]-lx[-1]
qx<- dx/lx[-7]
#I) Probability that one won't survive to next year is given by qx 
P_none=qx[2]*qx[3]*qx[4] #Proability that none of X,Y,Z Survive to next year
P_atleastone=1-P_none; P_atleastone # Probability that atleast one survive next year

#II) 2year time 
P_s=lx[4:6]/lx[2:4]
P_all_Survive=P_s[1]*P_s[2]*P_s[3];P_all_Survive

#III) 
P_alive_onlyone=P_s[1]*(1-P_s[2])*(1-P_s[3])+P_s[2]*(1-P_s[1])*(1-P_s[3])+P_s[3]*(1-P_s[2])*(1-P_s[1])
P_alive_onlyone
#IV)
P_alldead=(1-P_s[1])*(1-P_s[2])*(1-P_s[3]);P_alldead
```



**R-Console:**

```R
> #Given rabbit X,Y,Z aged 1,2,3 respectively 
> rm(list=ls())
> lx<-c(100,90,80,75,60,30,0)
> dx<- lx[-7]-lx[-1]
> qx<- dx/lx[-7]
> #I) Probability that one won't survive to next year is given by qx 
> P_none=qx[2]*qx[3]*qx[4] #Proability that none of X,Y,Z Survive to next year
> P_atleastone=1-P_none; P_atleastone # Probability that atleast one survive next year
[1] 0.9986111
> 
> #II) 2year time 
> P_s=lx[4:6]/lx[2:4]
> P_all_Survive=P_s[1]*P_s[2]*P_s[3];P_all_Survive
[1] 0.25
> 
> #III) 
> P_alive_onlyone=P_s[1]*(1-P_s[2])*(1-P_s[3])+P_s[2]*(1-P_s[1])*(1-P_s[3])+P_s[3]*(1-P_s[2])*(1-P_s[1])
> P_alive_onlyone
[1] 0.2166667
> #IV)
> P_alldead=(1-P_s[1])*(1-P_s[2])*(1-P_s[3]);P_alldead
[1] 0.025
> 
```

**Observation:**

At least one of rabbit will be alive for one year more$=0.9986111$

$X,Y,Z$ will be alive for two years time$=0.25$

exactly one of the three is alive in two years $=0.2166667$ and all will be dead in two years time $= 0.025$

