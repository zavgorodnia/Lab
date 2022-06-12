
##  1. Написати функцію pmean, яка обчислює середнє значення (mean) забруднення сульфатами або нітратами серед заданого переліка моніторів.
```
pmean("specdata","sulfate",1:10)
```

```
sulfate 
4.064128   
```

## 2. Написати функцію complete, яка виводить кількість повних спостережень (the number of completely observed cases) для кожного файлу.
```
complete("specdata", c(1,2,4,8,50:55))
```

```
id nobs
1 1 117
2 2 1041
3 3 243
4 4 474
5 5 402
6 6 228
7 7 442
8 8 192
9 9 275
10 10 148
```
## 3.  Написати функцію corr, яка приймає два аргументи: directory (папка, де знаходяться файли спостережень) та threshold (порогове значення, за замовчуванням дорівнює 0) та обчислює кореляцію між сульфатами та нітратами для моніторів, кількість повних спостережень для яких більше порогового значення
```
cr<-corr("specdata",150)
head(cr); summary(cr)
```

```
[1] -0.01895754 -0.14051254 -0.04389737 -0.06815956 -0.12350667 -0.07588814
    Min.  1st Qu.   Median     Mean  3rd Qu.     Max. 
-0.21057 -0.04999  0.09463  0.12525  0.26844  0.76313 
```
