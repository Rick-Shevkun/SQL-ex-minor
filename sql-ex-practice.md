+ [1](#1)
+ [2](#2)
+ [3](#3)
+ [4](#4)
+ [5](#5)
+ [6](#6)
+ [7](#7)
+ [8](#8)
+ [9](#9)
+ [10](#10)

## 1

https://sql-ex.ru/learn_exercises.php?LN=1

```sql
SELECT model, speed, hd
FROM PC
WHERE price < 500
```

## 2

https://sql-ex.ru/learn_exercises.php?LN=2

```sql
SELECT DISTINCT maker FROM Product WHERE type='Printer'
```

## 3

https://sql-ex.ru/learn_exercises.php?LN=3

```sql
Select model, ram, screen from laptop where price > 1000
```

## 4

https://sql-ex.ru/learn_exercises.php?LN=4

```sql
SELECT * FROM Printer WHERE color = 'y'
```

## 5

https://sql-ex.ru/learn_exercises.php?LN=5

```sql
SELECT PC.model, PC.speed, PC.hd FROM PC WHERE (cd = '12x' OR cd = '24x') AND price < 600
```

## 6

https://sql-ex.ru/learn_exercises.php?LN=6

```sql
SELECT DISTINCT p.maker, l.speed
FROM laptop l
JOIN product p ON p.model = l.model
WHERE l.hd >= 10
```

## 7

https://sql-ex.ru/learn_exercises.php?LN=7

```sql
SELECT DISTINCT product.model, pc.price 
FROM PRODUCT join pc ON product.model = pc.model WHERE maker = 'B'
UNION
SELECT DISTINCT product.model, laptop.price 
FROM PRODUCT join laptop ON product.model = laptop.model WHERE maker = 'B'
UNION
SELECT DISTINCT product.model, printer.price 
FROM PRODUCT join printer ON product.model = printer.model WHERE maker = 'B'
```

## 8

https://sql-ex.ru/learn_exercises.php?LN=8

```sql
SELECT DISTINCT maker FROM product WHERE type = 'PC'
EXCEPT
SELECT DISTINCT maker FROM product WHERE type = 'laptop'
```
