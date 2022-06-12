## 1. Функція add2(x, y), яка повертає суму двох чисел.

```
add2 <- function(x,y) {
return (x+y)
}
add2(10,28)
```

## Результати 

```
> add2 <- function(x,y) {
+ return (x+y)
+ }
> add2(10,28)
[1] 38
```


## 2. Функція above(x, n), яка приймає вектор та число n, та повертає всі елементі вектору, які більше n.По замовчуванню n = 10.

```
above <- function(x,n=10) {
return (x[x > n])
}
var <- c(1:12)
above(var)
above(var,5)
above(var,20)
```

## Результати 

```
> above <- function(x,n=10) {
+ return (x[x > n])
+ }
> var <- c(1:12)
> above(var)
[1] 11 12
> above(var,5)
[1]  6  7  8  9 10 11 12
> above(var,20)
integer(0)
```

## 3. Функція my_ifelse(x, exp, n), яка приймає вектор x, порівнює всі його елементи за допомогою exp з n, та повертає елементи вектору, які відповідають умові expression. Наприклад, my_ifelse(x, “>”, 0) повертає всі елементи x, які більші 0.Exp може дорівнювати “<”, “>”, “<=”, “>=”, “==”. Якщо exp не співпадає ні з одним з цих виразів, повертається вектор x.

```
my_ifelse <- function(x,expression,n) {
if (expression == '>') return (x[x>n])
if (expression == '<')  return (x[x<n])
if (expression == '>=') return (x[x>=n])
if (expression == '<=') return (x[x<=n])
if (expression == '==') return (x[x==n])
return (x)
}

my_ifelse(var, '>=' ,12)
```
## Результати 

```
> my_ifelse <- function(x,expression,n) {
+   if (expression == '>')  return (x[x>n])
+   if (expression == '<')  return (x[x<n])
+   if (expression == '>=') return (x[x>=n])
+   if (expression == '<=') return (x[x<=n])
+   if (expression == '==') return (x[x==n])
+   return (x)
+ }
> 
> my_ifelse(test_vec, '>=' ,12)
[1] 12 13 14 15
```

## 4. Функція columnmean(x, removeNA), яка розраховує середнє значення (mean) по кожному стовпцю матриці, або data frame. Логічний параметр removeNA вказує, чи видаляти NA значення. По замовчуванню він дорівнює TRUE.

```
columnmean <- function(x,removeNA=TRUE) {
apply(x, 2, function (column) mean(column, na.rm = removeNA))
}

my_matrix = cbind(c(1,1,4,NA,1), c(1,NA,1,4,4), c(0,1,1,1,1))
columnmean(my_matrix)
columnmean(my_matrix, FALSE)
```

## Результати 

```
> columnmean <- function(x,removeNA=TRUE) {
+ apply(x, 2, function (column) mean(column, na.rm = removeNA))
+ }
> 
> my_matrix = cbind(c(1,1,4,NA,1), c(1,NA,1,4,4), c(0,1,1,1,1))
> columnmean(my_matrix)
[1] 1.75 2.50 0.80
> columnmean(my_matrix, FALSE)
[1]  NA  NA 0.8
```

