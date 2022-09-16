# Practical #10



```R
rm(list=ls())
N=117
n=17
X=143968
x=c(1129,1144,1125,1138,1137,1127,1163,1153,1164,1130,1153,1125,1116,1115,1112,1112,1123)
y=c(1141,1144,1127,1153,1117,1140,1153,1146,1189,1137,1170,1115,1130,1118,1122,1113,1166)
smean_y=mean(y)
smean_y;
smean_x=mean(x)
smean_x;
est_R=smean_y/smean_x
est_R;
est_mean_Y=(est_R*(X/N))
est_mean_Y;
f=n/N 
f;
Sx2=sum((x-smean_x)^2)/(N-1)
Sx2;
Sy2=sum((y-smean_y)^2)/(N-1)
Sy2;
Sxy=sum((x-smean_x)*(y-smean_y))/(N-1)
Sxy;
var.est.mean_Y=((1-f)/n)*(Sy2+Sx2*(est_R)^2-2*(est_R)*Sxy);
var.est.mean_Y;

```

