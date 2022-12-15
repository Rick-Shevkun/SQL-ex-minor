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
+ [11](#11)
+ [12](#12)
+ [13](#13)
+ [14](#14)
+ [15](#15)
+ [16](#16)
+ [17](#17)
+ [18](#18)
+ [19](#19)
+ [20](#20)
+ [21](#21)
+ [22](#22)
+ [23](#23)
+ [24](#24)
+ [25](#25)
+ [26](#26)
+ [27](#27)
+ [28](#28)
+ [29](#29)
+ [30](#30)
+ [31](#31)
+ [32](#32)
+ [33](#33)
+ [34](#34)
+ [35](#35)
+ [36](#36)
+ [37](#37)
+ [38](#38)
+ [39](#39)
+ [40](#40)
+ [41](#41)
+ [42](#42)
+ [43](#43)
+ [44](#44)
+ [45](#45)
+ [46](#46)
+ [47](#47)
+ [48](#48)
+ [49](#49)
+ [50](#50)
+ [51](#51)
+ [52](#52)
+ [53](#53)
+ [54](#54)
+ [55](#55)
+ [56](#56)
+ [57](#57)
+ [58](#58)
+ [59](#59)
+ [60](#60)
+ [61](#61)
+ [62](#62)
+ [63](#63)
+ [64](#64)
+ [65](#65)
+ [66](#66)
+ [67](#67)
+ [68](#68)
+ [69](#69)
+ [70](#70)
+ [71](#71)
+ [72](#72)
+ [73](#73)
+ [74](#74)
+ [75](#75)
+ [76](#76)
+ [77](#77)
+ [78](#78)
+ [79](#79)
+ [80](#80)
+ [81](#81)
+ [82](#82)
+ [83](#83)
+ [84](#84)
+ [85](#85)
+ [86](#86)
+ [87](#87)
+ [88](#88)
+ [89](#89)
+ [90](#90)
+ [91](#91)
+ [92](#92)
+ [93](#93)
+ [94](#94)
+ [95](#95)
+ [96](#96)
+ [97](#97)
+ [98](#98)
+ [99](#99)
+ [100](#100)

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

## 9

https://sql-ex.ru/learn_exercises.php?LN=9

```sql
SELECT DISTINCT product.maker from product
JOIN pc ON product.model = pc.model WHERE pc.speed >= '450'
```

## 10

https://sql-ex.ru/learn_exercises.php?LN=10

```sql
SELECT DISTINCT model, price FROM printer WHERE price = (SELECT MAX(price) FROM printer)
```

## 11

https://sql-ex.ru/learn_exercises.php?LN=11

```sql
SELECT AVG(speed) FROM pc
```

## 12

https://sql-ex.ru/learn_exercises.php?LN=12

```sql
SELECT AVG(speed) FROM laptop WHERE price > '1000'
```

## 13

https://sql-ex.ru/learn_exercises.php?LN=13

```sql
SELECT AVG(PC.speed) FROM PC
JOIN product a ON PC.model = a.model WHERE maker = 'A'
```

## 14

https://sql-ex.ru/learn_exercises.php?LN=14

```sql
SELECT s.class, s.name, c.country FROM classes c
JOIN ships s ON c.class = s.class WHERE numguns >= '10'
```

## 15

https://sql-ex.ru/learn_exercises.php?LN=15

```sql
SELECT hd FROM PC
GROUP BY hd
HAVING count(model) >=2
```

## 16

https://sql-ex.ru/learn_exercises.php?LN=16

```sql
SELECT DISTINCT B.model AS model, A.model AS model, A.speed, A.ram 
FROM PC AS A, PC B 
WHERE A.speed = B.speed AND A.ram = B.ram and A.model < B.model 
```

## 17

https://sql-ex.ru/learn_exercises.php?LN=17

```sql
Select distinct type,laptop.model,speed from laptop inner join product on laptop.model= product.model  
where speed < (select MIN(speed) from pc)  
```

## 18

https://sql-ex.ru/learn_exercises.php?LN=18

```sql
SELECT DISTINCT maker,price  FROM printer inner JOIN product ON printer.model= product.model  
WHERE price = (select min(price)from printer where color = 'y' ) and color = 'y'  
```

## 19

https://sql-ex.ru/learn_exercises.php?LN=19

```sql
Select maker ,avg(screen)as Avg_screen 
from laptop inner join product on laptop.model =  product.model group by maker  
```

## 20

https://sql-ex.ru/learn_exercises.php?LN=20

```sql
Select maker , count(model) as Count_Model from product where type = 'pc' group by maker 
having count(model) >= 3  
```

## 21

https://sql-ex.ru/learn_exercises.php?LN=21

```sql
Select maker , max(price)as Max_price from pc inner join product on pc.model= product.model  
group by maker 
```

## 21

https://sql-ex.ru/learn_exercises.php?LN=21

```sql
Select maker , max(price)as Max_price from pc inner join product on pc.model= product.model  
group by maker 
```

## 22

https://sql-ex.ru/learn_exercises.php?LN=22

```sql
Select speed , avg(price) as Avg_price from pc  where speed > 600 group by speed  
```

## 23

https://sql-ex.ru/learn_exercises.php?LN=23

```sql
select distinct maker  from pc inner join product on pc.model = product.model  
where pc.speed >= 750 and maker in (select  maker  
from laptop inner join product on laptop.model = product.model where laptop.speed >= 750)  
```

## 24

https://sql-ex.ru/learn_exercises.php?LN=24

```sql
SELECT model FROM( 
SELECT distinct model, price FROM laptop WHERE laptop.price = (SELECT MAX(price) FROM laptop)  
UNION 
SELECT distinct model, price FROM pc WHERE pc.price = (SELECT MAX(price) FROM pc)  
UNION 
SELECT distinct model, price FROM printer WHERE printer.price = (SELECT MAX(price) FROM printer)  
) as t 
WHERE t.price=(SELECT MAX(price) FROM ( 
SELECT distinct price FROM laptop WHERE laptop.price = (SELECT MAX(price) FROM laptop)  
UNION 
SELECT distinct price FROM pc WHERE pc.price = (SELECT MAX(price) FROM pc)  
UNION 
SELECT distinct price FROM printer WHERE printer.price = (SELECT MAX(price) FROM printer)  
) as t1 )  
```

## 25

https://sql-ex.ru/learn_exercises.php?LN=25

```sql
SELECT distinct product.maker FROM product WHERE product.type='Printer'  
INTERSECT 
SELECT distinct product.maker FROM product INNER JOIN pc ON pc.model=product.model  
WHERE product.type='PC' AND pc.ram=(SELECT MIN(ram) FROM pc)  
AND pc.speed = (SELECT MAX(speed) FROM (SELECT distinct speed FROM pc 
WHERE pc.ram=(SELECT MIN(ram) FROM pc)) as t) 
```

## 26

https://sql-ex.ru/learn_exercises.php?LN=26

```sql
SELECT t1.c/t1.d FROM( SELECT SUM(t.a) as c, SUM(t.b) as d FROM(  
SELECT SUM(pc.price) as a, COUNT(pc.code) as b FROM pc 
INNER JOIN product ON pc.model=product.model WHERE product.maker='A'  
UNION 
SELECT SUM(laptop.price) as a, COUNT(laptop.code) as b FROM laptop 
INNER JOIN product ON laptop.model=product.model WHERE product.maker='A') as t) as t1  
```

## 26

https://sql-ex.ru/learn_exercises.php?LN=26

```sql
SELECT t1.c/t1.d FROM( SELECT SUM(t.a) as c, SUM(t.b) as d FROM(  
SELECT SUM(pc.price) as a, COUNT(pc.code) as b FROM pc 
INNER JOIN product ON pc.model=product.model WHERE product.maker='A'  
UNION 
SELECT SUM(laptop.price) as a, COUNT(laptop.code) as b FROM laptop 
INNER JOIN product ON laptop.model=product.model WHERE product.maker='A') as t) as t1  
```

## 27

https://sql-ex.ru/learn_exercises.php?LN=27

```sql
select maker,avg(hd)  from product inner join pc on product.model=pc.model   
where maker in(select maker  from product  where type='printer')  group by maker  
```

## 28

https://sql-ex.ru/learn_exercises.php?LN=28

```sql
select avg(hd)  from product inner join pc on product.model = pc.model   
where maker in(select maker from product where type='printer') 
```

## 29

https://sql-ex.ru/learn_exercises.php?LN=29

```sql
select t.point, t.date, SUM(t.inc), sum(t.out) from( select point, date, inc, null as out from Income_o  
Union 
select point, date, null as inc, Outcome_o.out from Outcome_o) as t group by t.point, t.date  
```

## 30

https://sql-ex.ru/learn_exercises.php?LN=30

```sql
select point, date, SUM(sum_out), SUM(sum_inc) 
from( select point, date, SUM(inc) as sum_inc, null as sum_out from Income Group by point, date  
Union 
select point, date, null as sum_inc, SUM(out) as sum_out from Outcome Group by point, date ) as t  
group by point, date order by point  
```

## 31

https://sql-ex.ru/learn_exercises.php?LN=31

```sql
Select class , country from classes where bore >= 16  
```

## 32

https://sql-ex.ru/learn_exercises.php?LN=32

```sql
Select country, cast(avg((power(bore,3)/2)) as numeric(6,2)) as weight 
from (select country, classes.class, bore, name from classes left join ships on classes.class=ships.class  
union all 
select distinct country, class, bore, ship from classes t1 left join outcomes t2 on t1.class=t2.ship  
where ship=class and ship not in (select name from ships) ) a  
where name!='null' group by country  
```

## 33

https://sql-ex.ru/learn_exercises.php?LN=33

```sql
Select ship from outcomes,battles where result= 'sunk' and battle = 'North Atlantic' group by ship  
```

## 34

https://sql-ex.ru/learn_exercises.php?LN=34

```sql
Select name  from classes,shipswhere launched>=1922 and displacement>35000 and type='bb' and    
ships.class = classes.class
```

## 35

https://sql-ex.ru/learn_exercises.php?LN=35

```sql
SELECT model, type FROM product 
WHERE model NOT LIKE '%[^0-9]%' OR model NOT LIKE '%[^a-z]
```

## 36

https://sql-ex.ru/learn_exercises.php?LN=36

```sql
Select name  from ships  where class = name   
union  
select ship as name  from classes,outcomes  where classes.class = outcomes.ship  
```

## 37

https://sql-ex.ru/learn_exercises.php?LN=37

```sql
Select class  from(select name,class from ships  
union  
select class as name,class  from classes,outcomes  where classes.class=outcomes.ship) A   
group by class  having count(A.name)=1  
```

## 38

https://sql-ex.ru/learn_exercises.php?LN=38

```sql
Select distinct country  from classes  where type='bb'   
intersect  
Select distinct country  from classes  where type='bc'  
```

## 39

https://sql-ex.ru/learn_exercises.php?LN=39

```sql
select distinct B.ship 
from(select * from outcomes left join battles on battle=name where result='damaged')as B 
where exists (select shipfrom outcomes left join battles on battle=name 
where ship=B.ship and B.date<date) 
```

## 40

https://sql-ex.ru/learn_exercises.php?LN=40

```sql
Select classes.class , name,country from classes inner join ships on classes.class = ships.class  
where numguns >= 10  
```

## 41

https://sql-ex.ru/learn_exercises.php?LN=41

```sql
select 'speed' as m, CAST(speed as char) as a from pc where code >= all(select code from pc)  
union  
select 'model' as m, CAST(model as char) as a from pc where code >= all(select code from pc)  
union  
select 'ram' as m, CAST(ram as char) as a from pc where code >= all(select code from pc)  
union  
select 'hd' as m, CAST(hd as char) as a from pc where code >= all(select code from pc)  
union  
select 'cd' as m, CAST(cd as char) as a from pc where code >= all(select code from pc)  
union  
select 'price' as m, CAST(price as char) as a from pc where code >= all(select code from pc) 
```

## 42

https://sql-ex.ru/learn_exercises.php?LN=42

```sql
Select ship,battle from outcomes where result ='sunk' 
```

## 43

https://sql-ex.ru/learn_exercises.php?LN=43

```sql
select name from battles where DATEPART(yy, date) not in (select DATEPART(yy, date)  
from battles join ships on DATEPART(yy, date)=launched) 
```

## 44

https://sql-ex.ru/learn_exercises.php?LN=44

```sql
Select name from ships where name like 'R%'   
union   
Select name from battles where name like 'R%'   
union   
Select ship from outcomes where ship like 'R%'  
```

## 45

https://sql-ex.ru/learn_exercises.php?LN=45

```sql
Select name from ships where name like '% % %'  
union   
Select ship from outcomes where ship like '% % %'   
```

## 46

https://sql-ex.ru/learn_exercises.php?LN=46

```sql
select name as n, displacement as d, numguns as ng from ships inner join classes on ships.class=classes.class where name in (select ship from outcomes where battle = 'Guadalcanal')   
union 
select ship as n, displacement as d, numguns as ng from outcomes inner join classes on outcomes.ship=classes.class where battle = 'Guadalcanal' and ship not in (select name from ships)   
union  
select ship as n, null as d, null as ng from outcomes where battle = 'Guadalcanal' and ship not in (select name from ships) and ship not in  (select class from classes)  
```

## 47

https://sql-ex.ru/learn_exercises.php?LN=47

```sql
select ROW_NUMBER() OVER(ORDER BY co desc, m, model) no, m, model  
from ( Select one.maker as m, model, co   
from product as one join (Select maker, count(model) as co from product group by maker) as two on one.maker=two.maker ) as ddd  
```

## 48

https://sql-ex.ru/learn_exercises.php?LN=48

```sql
Select class as n from ships where name in(select ship from outcomes where result='sunk')   
union  
Select ship as n from outcomes  
where ship not in(Select name from ships) and ship in(Select class from classes) and result='sunk'
```

## 49

https://sql-ex.ru/learn_exercises.php?LN=49

```sql
select name from ships where class in( Select class from classes where bore=16)   
union  
select ship from outcomes where ship in( Select class from classes where bore=16)  
```

## 49

https://sql-ex.ru/learn_exercises.php?LN=49

```sql
select name from ships where class in( Select class from classes where bore=16)   
union  
select ship from outcomes where ship in( Select class from classes where bore=16)  
```

## 49

https://sql-ex.ru/learn_exercises.php?LN=49

```sql
select name from ships where class in( Select class from classes where bore=16)   
union  
select ship from outcomes where ship in( Select class from classes where bore=16)  
```

## 50

https://sql-ex.ru/learn_exercises.php?LN=50

```sql
SELECT distinct battle FROM Classes  inner JOIN Ships  ON ships.class = classes.class   
inner JOIN Outcomes  ON Classes.class=Outcomes.ship or Ships.name=Outcomes.ship   
WHERE classes.class = 'Kongo'  
```

## 51

https://sql-ex.ru/learn_exercises.php?LN=51

```sql
select NAME from(select name as NAME, displacement, numguns  
from ships inner join classes on ships.class = classes.class 
union 
select ship as NAME, displacement, numguns from outcomes inner join classes on outcomes.ship= classes.class) as d1 inner join (select displacement, max(numGuns) as numguns from ( select displacement, numguns from ships inner join classes on ships.class = classes.class  
union 
select displacement, numguns  from outcomes inner join classes on outcomes.ship= classes.class) as f 
group by displacement) as d2 on d1.displacement=d2.displacement and d1.numguns =d2.numguns 
```

## 51

https://sql-ex.ru/learn_exercises.php?LN=51

```sql
select NAME from(select name as NAME, displacement, numguns  
from ships inner join classes on ships.class = classes.class 
union 
select ship as NAME, displacement, numguns from outcomes inner join classes on outcomes.ship= classes.class) as d1 inner join (select displacement, max(numGuns) as numguns from ( select displacement, numguns from ships inner join classes on ships.class = classes.class  
union 
select displacement, numguns  from outcomes inner join classes on outcomes.ship= classes.class) as f 
group by displacement) as d2 on d1.displacement=d2.displacement and d1.numguns =d2.numguns 
```

## 52

https://sql-ex.ru/learn_exercises.php?LN=52

```sql
Select distinct name from ships  inner join classes cl on ships.class=cl.class 
where (numGuns>=9 or numguns is NULL) and (bore<19 or bore is NULL) and (displacement<=65000 or displacement is NULL) and type='bb' and country='japan' 
```

## 53

https://sql-ex.ru/learn_exercises.php?LN=53

```sql
select cast(avg(numguns*1.0) as numeric(4,2)) as Avg_numGuns  from classes where type='bb' 
```

## 54

https://sql-ex.ru/learn_exercises.php?LN=54

```sql
SELECT CAST(AVG(numguns*1.0) AS NUMERIC (4,2)) as AVG_nmg 
FROM (SELECT ship, type, numguns   FROM Outcomes LEFT JOIN Classes ON ship = class  
UNION  
SELECT name, type, numguns FROM Ships as S INNER JOIN  Classes as C ON c.class = s.class ) AS T 
WHERE type = 'bb'
```

## 55

https://sql-ex.ru/learn_exercises.php?LN=55

```sql
select C.class, min(launched)  from ships as S right join classes as C on s.class=c.class group by C.class 
```

## 56

https://sql-ex.ru/learn_exercises.php?LN=56

```sql
select classes.class, count(T.ship) from classes left join(select ship, class from outcomes left join ships on ship=name where result='sunk'union select ship, class from outcomes left join classes on ship=class where result='sunk') as T on classes.class=T.classgroup by classes.class 
```

## 57

https://sql-ex.ru/learn_exercises.php?LN=57

```sql
select class as cls, count(class) as sunked from( 
select C.class, O.ship from classes as C join outcomes as O on C.class=O.ship where O.result='sunk' 
union 
select S.class, O.ship from outcomes as O join ships as S on S.name=O.ship where O.result='sunk') as T 
where class in ( select distinct X.class from  (select C.class, O.ship from classes as C join outcomes as O on C.class=O.ship 
union 
select C.class, S.name from classes as C join ships as S on C.class=S.class) as X group by X.class 
having count(X.class)>=3 )  group by class
```

## 58

https://sql-ex.ru/learn_exercises.php?LN=58

```sql
select main_maker ,main_type ,CONVERT(NUMERIC(6,2),((sub_num*100.00)/(total_num*100.00)*100.00))  
from (select count(p5.model) total_num ,p5.maker main_maker 
 from product p5 group by p5.maker) p6 JOIN (select p3.maker sub_maker ,p3.type main_type ,count(p4.model) sub_num 
 from (select p1.maker maker, p2.type type from product p1 cross join product p2 group by p1.maker, p2.type) p3 left join product p4 on p3.maker = p4.maker and p3.type = p4.type group by  p3.maker,p3.type) p7 ON p7.sub_maker = p6.main_maker
 ```

## 59

https://sql-ex.ru/learn_exercises.php?LN=59

```sql
select a.point, case when o is null then i else i-o end remain FROM  (select point, sum(inc) as i 
from Income_o group by point) as A left join (select point, sum(out) as o from Outcome_o group by point) as B on A.point=B.point 
 ```

## 60

https://sql-ex.ru/learn_exercises.php?LN=60

```sql
select a.point,  case when o is null  then i else i-o end remain FROM (select point, sum(inc) as i 
from Income_o where '20010415' > date group by point) as A left join (select point, sum(out) as o 
from Outcome_o  where '20010415' > date group by point) as B on A.point=B.point 
 ```
 
## 61

https://sql-ex.ru/learn_exercises.php?LN=61

```sql
select (select sum(inc) from income_o) - (select sum(out) from outcome_o) as remain  
 ```

## 62

https://sql-ex.ru/learn_exercises.php?LN=62

```sql
select  (select sum(inc) from income_o where '20010415' > date)   
-  
(select sum(out) from outcome_o where '20010415' > date)  as remain 
 ```

## 63

https://sql-ex.ru/learn_exercises.php?LN=63

```sql
select name from Passenger where ID_psg in(Select Left([ol],CHARINDEX ( ' ', ol)) from ( 
Select CAST(concat(ID_psg,' ', place) AS VARCHAR(30)) as ol, trip_no as o, ID_psg as psg 
from Pass_in_trip ) as lll group by ol having count(o)>1) 
 ```
 
## 64

https://sql-ex.ru/learn_exercises.php?LN=64

```sql
Select income.point, income.date, 'inc' as operation, sum(income.inc) 
from income left join outcome on income.point=outcome.point and income.date=outcome.date 
where outcome.date is null  group by income.point, income.date 
union 
Select outcome.point, outcome.date, 'out' as operation, sum(outcome.out) 
from income right join outcome on income.point=outcome.point and income.date=outcome.date 
where income.date is null group by outcome.point, outcome.date 
 ```
 
## 65

https://sql-ex.ru/learn_exercises.php?LN=65

```sql
Select row_number() over(order by maker, ans) c1, 
case when maker = lag(maker) over(order by maker) then ''
else maker end c2, type
from (select distinct maker, type, case when type = 'pc' then 1 when type = 'Laptop' then 2 when type = 'printer' then 3 end ans from product)t1 
 ```

## 66

https://sql-ex.ru/learn_exercises.php?LN=66

```sql
SELECT date, max(c) FROM
(SELECT date,count(*) AS c FROM Trip,
(SELECT trip_no,date FROM Pass_in_trip WHERE date>='2003-04-01' AND date<='2003-04-07' GROUP BY trip_no, date) AS t1
WHERE Trip.trip_no=t1.trip_no AND town_from='Rostov'
GROUP BY date
UNION ALL
SELECT '2003-04-01',0
UNION ALL
SELECT '2003-04-02',0
UNION ALL
SELECT '2003-04-03',0
UNION ALL
SELECT '2003-04-04',0
UNION ALL
SELECT '2003-04-05',0
UNION ALL
SELECT '2003-04-06',0
UNION ALL
SELECT '2003-04-07',0) AS t2
GROUP BY date
 ```
 
## 67

https://sql-ex.ru/learn_exercises.php?LN=67

```sql
select count(*) from
(SELECT TOP 1 WITH TIES count(*) c, town_from, town_to from trip
group by town_from, town_to
order by c desc) as t
 ```
 
## 68

https://sql-ex.ru/learn_exercises.php?LN=68

```sql
select count(*) from (
select TOP 1 WITH TIES sum(c) cc, c1, c2 from (
SELECT count(*) c, town_from c1, town_to c2 from trip
where town_from>=town_to
group by town_from, town_to
union all
SELECT count(*) c,town_to, town_from from trip
where town_to>town_from
group by town_from, town_to
) as t
group by c1,c2
order by cc desc
) as tt
 ```
 
## 69

https://sql-ex.ru/learn_exercises.php?LN=69

```sql
with t as
(
  select point, "date", inc, 0 AS "out" from income
  union all
  select point, "date", 0 AS inc, "out" from outcome
)
SELECT t.point, TO_CHAR ( t."date", 'DD/MM/YYYY') AS day,
 ( select SUM(i.inc) from t i
   where i."date" <= t."date" and i.point = t.point )
-
( select SUM(i."out") from t i
  where i."date" <= t."date" and i.point = t.point ) AS rem
from t
group by t.point, t."date"
 ```
 
## 70

https://sql-ex.ru/learn_exercises.php?LN=70

```sql
SELECT DISTINCT o.battle
FROM outcomes o
LEFT JOIN ships s ON s.name = o.ship
LEFT JOIN classes c ON o.ship = c.class OR s.class = c.class
WHERE c.country IS NOT NULL
GROUP BY c.country, o.battle
HAVING COUNT(o.ship) >= 3;
 ```
 
## 71

https://sql-ex.ru/learn_exercises.php?LN=71

```sql
SELECT p.maker
FROM product p
LEFT JOIN pc ON pc.model = p.model
WHERE p.type = 'PC'
GROUP BY p.maker
HAVING COUNT(p.model) = COUNT(pc.model)
```
 
## 72

https://sql-ex.ru/learn_exercises.php?LN=72

```sql
SELECT p.maker
FROM product p
LEFT JOIN pc ON pc.model = p.model
WHERE p.type = 'PC'
GROUP BY p.maker
HAVING COUNT(p.model) = COUNT(pc.model)
```

## 73

https://sql-ex.ru/learn_exercises.php?LN=73

```sql
SELECT DISTINCT c.country, b.name
FROM battles b, classes c
MINUS
SELECT c.country, o.battle
FROM outcomes o
LEFT JOIN ships s ON s.name = o.ship
LEFT JOIN classes c ON o.ship = c.class OR s.class = c.class
WHERE c.country IS NOT NULL
GROUP BY c.country, o.battle
```

## 74

https://sql-ex.ru/learn_exercises.php?LN=74

```sql
SELECT c.country, c.class
FROM classes c
WHERE UPPER(c.country) = 'RUSSIA' AND EXISTS (
SELECT c.country, c.class
FROM classes c
WHERE UPPER(c.country) = 'RUSSIA' )
UNION ALL
SELECT c.country, c.class
FROM classes c
WHERE NOT EXISTS (SELECT c.country, c.class
FROM classes c
WHERE UPPER(c.country) = 'RUSSIA' )
```

## 75

https://sql-ex.ru/learn_exercises.php?LN=75


```sql
select shipname,launched,batname
from
(select s.name as shipname,launched,b.name as batname,
row_number() over (partition by s.name order by "date") as num
from ships s,battles b
where to_char("date",'yyyy')>=launched
and launched is not null)
where num = 1
union
(
select name,launched,(select name from battles
where "date" = (select max("date") from battles)) as batname
from ships
where launched is null
)
```

## 76

https://sql-ex.ru/learn_exercises.php?LN=76

```sql
select shipname,launched,batname
from
(select s.name as shipname,launched,b.name as batname,
row_number() over (partition by s.name order by "date") as num
from ships s,battles b
where to_char("date",'yyyy')>=launched
and launched is not null)
where num = 1
union
(
select name,launched,(select name from battles
where "date" = (select max("date") from battles)) as batname
from ships
where launched is null
)
```

## 77

https://sql-ex.ru/learn_exercises.php?LN=77

```sql
SELECT TOP 1 WITH TIES * FROM (
SELECT COUNT (DISTINCT P.trip_no) count, date
FROM Pass_in_trip P
JOIN Trip T ON T.trip_no = P.trip_no AND town_from = 'Rostov'
GROUP BY P.trip_no, date) X
ORDER BY 1 DESC
```

## 78

https://sql-ex.ru/learn_exercises.php?LN=78

```sql
SELECT name, REPLACE(CONVERT(CHAR(12), DATEADD(m, DATEDIFF(m,0,date),0), 102),'.','-') AS first_day,
REPLACE(CONVERT(CHAR(12), DATEADD(s,-1,DATEADD(m, DATEDIFF(m,0,date)+1,0)), 102),'.','-') AS last_day
FROM Battles
```

## 79

https://sql-ex.ru/learn_exercises.php?LN=79

```sql
SELECT Passenger.name, A.minutes
FROM (SELECT P.ID_psg,
      SUM((DATEDIFF(minute, time_out, time_in) + 1440)%1440) AS minutes,
      MAX(SUM((DATEDIFF(minute, time_out, time_in) + 1440)%1440)) OVER() AS MaxMinutes
      FROM Pass_in_trip P JOIN
       Trip AS T ON P.trip_no = T.trip_no
      GROUP BY P.ID_psg
      ) AS A JOIN
 Passenger ON Passenger.ID_psg = A.ID_psg
WHERE A.minutes = A.MaxMinutes
```

## 80

https://sql-ex.ru/learn_exercises.php?LN=80

```sql
SELECT DISTINCT maker
FROM product
WHERE maker NOT IN (
     SELECT maker
     FROM product
     WHERE type='PC' AND model NOT IN (
          SELECT model
          FROM PC))
```

## 81

https://sql-ex.ru/learn_exercises.php?LN=81

```sql
SELECT O.*
FROM outcome O
INNER JOIN
(
SELECT TOP 1 WITH TIES YEAR(date) AS Y, MONTH(date) AS M, SUM(out) AS ALL_TOTAL
FROM outcome
GROUP BY YEAR(date), MONTH(date)
ORDER BY ALL_TOTAL DESC
) R ON YEAR(O.date) = R.Y AND MONTH(O.date) = R.M
```

## 82

https://sql-ex.ru/learn_exercises.php?LN=82

```sql
WITH CTE(code,price,number)
AS
(
SELECT PC.code,PC.price, number= ROW_NUMBER() OVER (ORDER BY PC.code)
FROM PC
)
SELECT CTE.code, AVG(C.price)
FROM CTE
JOIN CTE C ON (C.number-CTE.number)<6 AND (C.number-CTE.number)> =0
GROUP BY CTE.number,CTE.code
HAVING COUNT(CTE.number)=6
```

## 83

https://sql-ex.ru/learn_exercises.php?LN=83

```sql
SELECT name
FROM Ships AS s JOIN Classes AS cl1 ON s.class = cl1.class
WHERE
CASE WHEN numGuns = 8 THEN 1 ELSE 0 END +
CASE WHEN bore = 15 THEN 1 ELSE 0 END +
CASE WHEN displacement = 32000 THEN 1 ELSE 0 END +
CASE WHEN type = 'bb' THEN 1 ELSE 0 END +
CASE WHEN launched = 1915 THEN 1 ELSE 0 END +
CASE WHEN s.class = 'Kongo' THEN 1 ELSE 0 END +
CASE WHEN country = 'USA' THEN 1 ELSE 0 END > = 4
```

## 85

https://sql-ex.ru/learn_exercises.php?LN=85

```sql
SELECT C.name, A.N_1_10, A.N_11_21, A.N_21_30
FROM (SELECT T.ID_comp,
       SUM(CASE WHEN DAY(P.date) < 11 THEN 1 ELSE 0 END) AS N_1_10,
       SUM(CASE WHEN (DAY(P.date) > 10 AND DAY(P.date) < 21) THEN 1 ELSE 0 END) AS N_11_21,
       SUM(CASE WHEN DAY(P.date) > 20 THEN 1 ELSE 0 END) AS N_21_30
      FROM Trip AS T JOIN
       Pass_in_trip AS P ON T.trip_no = P.trip_no AND CONVERT(char(6), P.date, 112) = '200304'
      GROUP BY T.ID_comp
      ) AS A JOIN
 Company AS C ON A.ID_comp = C.ID_comp
```

## 85

https://sql-ex.ru/learn_exercises.php?LN=85

```sql
select maker
from product
group by maker
having count(distinct type) = 1 and
       (min(type) = 'pc' or
       (min(type) = 'printer' and count(model) > 2))
```

## 86

https://sql-ex.ru/learn_exercises.php?LN=86

```sql
SELECT maker,
       CASE count(distinct type) when 2 then MIN(type) + '/' + MAX(type)
                                 when 1 then MAX(type)
                                 when 3 then 'Laptop/PC/Printer' END
FROM Product
GROUP BY maker
```

## 87

https://sql-ex.ru/learn_exercises.php?LN=87

```sql
SELECT DISTINCT name, COUNT(town_to) Qty
FROM Trip tr JOIN Pass_in_trip pit ON tr.trip_no = pit.trip_no JOIN
         Passenger psg ON pit.ID_psg = psg.ID_psg
WHERE town_to = 'Moscow' AND pit.ID_psg NOT IN(SELECT DISTINCT ID_psg
FROM Trip tr JOIN Pass_in_trip pit ON tr.trip_no = pit.trip_no
WHERE date+time_out = (SELECT MIN (date+time_out)
                       FROM Trip tr1 JOIN Pass_in_trip pit1 ON tr1.trip_no = pit1.trip_no
                       WHERE pit.ID_psg = pit1.ID_psg)
AND town_from = 'Moscow')
GROUP BY pit.ID_psg, name
HAVING COUNT(town_to) > 1
```

## 88

https://sql-ex.ru/learn_exercises.php?LN=88

```sql
SELECT
 (SELECT name FROM Passenger WHERE ID_psg = B.ID_psg) AS name,
 B.trip_Qty,
 (SELECT name FROM Company WHERE ID_comp = B.ID_comp) AS Company
FROM (SELECT P.ID_psg, MIN(T.ID_comp) AS ID_comp, COUNT(*) AS trip_Qty, MAX(COUNT(*)) OVER() AS Max_Qty
      FROM Pass_in_trip AS P JOIN
       Trip AS T ON P.trip_no = T.trip_no
      GROUP BY P.ID_psg
      HAVING MIN(T.ID_comp) = MAX(T.ID_comp)
      ) AS B
WHERE B.trip_Qty = B.Max_Qty
```

## 89

https://sql-ex.ru/learn_exercises.php?LN=89

```sql
select Maker , count(distinct model) Qty from Product
group by maker
having count(distinct model) > = ALL
(select count(distinct model) from Product
group by maker)
or
count(distinct model) <= ALL
(select count(distinct model) from Product
group by maker)
```

## 90

https://sql-ex.ru/learn_exercises.php?LN=90

```sql
Select maker, model, type from
(
Select
row_number() over (order by model) p1,
row_number() over (order by model DESC) p2,
from Product
) t1
where p1 > 3 and p2 > 3
```

## 91

https://sql-ex.ru/learn_exercises.php?LN=91

```sql
select count(maker)
from product
where maker in
(
  Select maker from product
  group by maker
  having count(model) = 1
)
```

## 92

https://sql-ex.ru/learn_exercises.php?LN=92

```sql
SELECT Q_NAME
FROM utQ
WHERE Q_ID IN (SELECT DISTINCT B.B_Q_ID
                FROM (SELECT B_Q_ID
                        FROM utB
                        GROUP BY B_Q_ID
                        HAVING SUM(B_VOL) = 765) AS B
                WHERE B.B_Q_ID NOT IN (SELECT B_Q_ID
                                        FROM utB
                                        WHERE B_V_ID IN (SELECT B_V_ID
                                                          FROM utB
                                                          GROUP BY B_V_ID
                                                          HAVING SUM(B_VOL) < 255)))
```

## 93

https://sql-ex.ru/learn_exercises.php?LN=93

```sql
select c.name, sum(vr.vr)
from
(select distinct t.id_comp, pt.trip_no, pt.date,t.time_out,t.time_in,--pt.id_psg,
case
     when DATEDIFF(mi, t.time_out,t.time_in)> 0 then DATEDIFF(mi, t.time_out,t.time_in)
     when DATEDIFF(mi, t.time_out,t.time_in)<=0 then DATEDIFF(mi, t.time_out,t.time_in+1)
end vr
from pass_in_trip pt left join trip t on pt.trip_no=t.trip_no
) vr left join company c on vr.id_comp=c.id_comp
group by c.name
```

## 94

https://sql-ex.ru/learn_exercises.php?LN=94

```sql
SELECT DATEADD(day, S.Num, D.date) AS Dt,
       (SELECT COUNT(DISTINCT P.trip_no)
        FROM Pass_in_trip P
               JOIN Trip T
                 ON P.trip_no = T.trip_no
                    AND T.town_from = 'Rostov'
                    AND P.date = DATEADD(day, S.Num, D.date)) AS Qty
FROM (SELECT (3 * ( x - 1 ) + y - 1) AS Num
        FROM (SELECT 1 AS x UNION ALL SELECT 2 UNION ALL SELECT 3) AS N1
               CROSS JOIN (SELECT 1 AS y UNION ALL SELECT 2 UNION ALL SELECT 3) AS N2
        WHERE (3 * ( x - 1 ) + y ) < 8) AS S,
       (SELECT MIN(A.date) AS date
        FROM (SELECT P.date,
                       COUNT(DISTINCT P.trip_no) AS Qty,
                       MAX(COUNT(DISTINCT P.trip_no)) OVER() AS M_Qty
                FROM Pass_in_trip AS P
                       JOIN Trip AS T
                         ON P.trip_no = T.trip_no
                            AND T.town_from = 'Rostov'
                GROUP BY P.date) AS A
        WHERE A.Qty = A.M_Qty) AS D
```

## 95

https://sql-ex.ru/learn_exercises.php?LN=95

```sql
SELECT name,
    COUNT(DISTINCT CONVERT(CHAR(24),date)+CONVERT(CHAR(4),Trip.trip_no)),
    COUNT(DISTINCT plane),
    COUNT(DISTINCT ID_psg),
    COUNT(*)
FROM Company,Pass_in_trip,Trip
WHERE Company.ID_comp=Trip.ID_comp and Trip.trip_no=Pass_in_trip.trip_no
GROUP BY Company.ID_comp,name
```

## 96

https://sql-ex.ru/learn_exercises.php?LN=96

```sql
with r as (select v.v_name,
       v.v_id,
       count(case when v_color = 'R' then 1 end) over(partition by v_id) cnt_r,
       count(case when v_color = 'B' then 1 end) over(partition by b_q_id) cnt_b
  from utV v join utB b on v.v_id = b.b_v_id)
select v_name
  from r
where cnt_r > 1
  and cnt_b > 0
group by v_name
```

## 97

https://sql-ex.ru/learn_exercises.php?LN=97

```sql
select code, speed, ram, price, screen
from laptop where exists (
  select 1 x
  from (
    select v, rank()over(order by v) rn
    from ( select cast(speed as float) sp, cast(ram as float) rm,
                  cast(price as float) pr, cast(screen as float) sc
    )l unpivot(v for c in (sp, rm, pr, sc))u
  )l pivot(max(v) for rn in ([1],[2],[3],[4]))p
  where [1]*2 <= [2] and [2]*2 <= [3] and [3]*2 <= [4]
)
```

## 98

https://sql-ex.ru/learn_exercises.php?LN=98

```sql
with CTE AS
(select
1 n, cast (0 as varchar(16)) bit_or,
code, speed, ram FROM PC
UNION ALL
select n*2,
cast (convert(bit,(speed|ram)&n) as varchar(1))+cast(bit_or as varchar(15))
, code, speed, ram
from CTE where n < 65536
)
select code, speed, ram from CTE
where n = 65536
and CHARINDEX('1111', bit_or )> 0
```

## 99

https://sql-ex.ru/learn_exercises.php?LN=99

```sql
select point,
       "date" income_date,
       "date" + nvl(
                  min(case when diff > cnt then cnt else null end),
                  max(cnt)+1
                ) incass_date
from (select i.point,
             i."date",
             (trunc(o."date") - trunc(i."date")) diff, -- разница дней
             -- количество запрещенных для инкассации дней после прихода и до текущего запрещенного дня
             count(1) over (partition by i.point, i."date" order by o."date" rows between unbounded preceding and current row)-1 cnt
      from income_o i
               join (select point, "date", 1 disabled from outcome_o
                     union
                     select point, trunc("date"+7,'DAY'), 1 disabled from income_o) o
                 on i.point = o.point
      where o."date" > = i."date")
group by point, "date"
```

## 100

https://sql-ex.ru/learn_exercises.php?LN=100

```sql
Select distinct A.date , A.R, B.point, B.inc, C.point, C.out
From (Select distinct date, ROW_Number() OVER(PARTITION BY date ORDER BY code asc) as R From Income
Union Select distinct date, ROW_Number() OVER(PARTITION BY date ORDER BY code asc) From Outcome) A
LEFT Join (Select date, point, inc
                , ROW_Number() OVER(PARTITION BY date ORDER BY code asc) as RI FROM Income
           ) B on B.date=A.date and B.RI=A.R
LEFT Join (Select date, point, out
                , ROW_Number() OVER(PARTITION BY date ORDER BY code asc) as RO FROM Outcome
           ) C on C.date=A.date and C.RO=A.R
```
