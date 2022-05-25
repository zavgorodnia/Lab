

## 1. Створити змінні базових (atomic) типів. Базові типи: character, numeric, integer, complex, logical.
var1 <- 'Hello' 
print(class(var1))
var2 <- 33 
print(class(var2))
var3 <- 20L 
print(class(var3))
var4 <-  x <- 1-2i 
print(class(var4))
var5 <- TRUE 
print(class(var5))

## 2. Створити вектори, які: містить послідовність з 5 до 75; містить числа 3.14, 2.71, 0, 13; 100 значень TRUE.

v1 <- c(5:75)
v2 <- c(3.14,2.71,0,13)
v3 <- rep(TRUE, times=100)

## 3. Створити наступну матрицю за допомогою matrix, та за допомогою cbind або rbind

matrx <- c(3, 6, 0.9, 12, 78, 9.7, 0.12, 33, 1.2)
matrix(matrx, nrow = 3)
a <- matrx[1:3]
b <- matrx[4:6]
c <- matrx[7:9]
cbind(a,b,c)

## 4. Створити довільний список (list), в який включити всі базові типи.

list("hello",var2,var3,var4,TRUE)

## 5. Створити фактор з трьома рівнями «baby», «child», «adult».

var6 <- factor(c('baby', 'child', 'adult'))

## 6. Знайти індекс першого значення NA в векторі 1, 2, 3, 4, NA, 6, 7, NA, 9, NA, 11. Знайти кількість значень NA.

var7 <- c(1, 2, 3, 4, NA, 6, 7, NA, 9, NA, 11)
print(match(NA,var7))
print(sum(is.na(var7)))

## 7. Створити довільний data frame та вивести в консоль.

city <- c('Kyiv', 'Odessa', 'Lviv')
population <- c('3000000', '200000', '10000')
data <- data.frame(city,population)
data

## 8. Змінити імена стовпців цього data frame.

colnames(data) <- c('big_city','population')
data