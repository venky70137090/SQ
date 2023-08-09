create table bank(
    -> a_holdername char(17),
    -> a_no int,
    -> a_adress varchar(17),
    -> a_phno int,
    -> a_pricing int);
Query OK, 0 rows affected (0.04 sec)

mysql> insert into bank values('venky',1234,'guntur',450);
ERROR 1136 (21S01): Column count doesn't match value count at row 1
mysql> insert into bank values('venky',1234,'guntur',7013419027,450);
ERROR 1264 (22003): Out of range value for column 'a_phno' at row 1
mysql> insert into bank values('venky',1234,'guntur',7013,450);
Query OK, 1 row affected (0.00 sec)

mysql> insert into bank values('sai',1235,'ongole',9013,299);
Query OK, 1 row affected (0.01 sec)

mysql> insert into bank values('jaswanth',1237,'kurnool',9913,256);
Query OK, 1 row affected (0.01 sec)

mysql> insert into bank values('abhi',1239,'vizag',9989,178);
Query OK, 1 row affected (0.01 sec)

mysql> insert into bank values('vikram',1275,'hyd',7689,234);
Query OK, 1 row affected (0.01 sec)

mysql> insert into bank values('viswanth',1375,'chennai',7999,294);
Query OK, 1 row affected (0.01 sec)

mysql> insert into bank values('aravind',1387,'kakinda',9999,890);
Query OK, 1 row affected (0.01 sec)

mysql> select*from bank;
+--------------+------+----------+--------+-----------+
| a_holdername | a_no | a_adress | a_phno | a_pricing |
+--------------+------+----------+--------+-----------+
| venky        | 1234 | guntur   |   7013 |       450 |
| sai          | 1235 | ongole   |   9013 |       299 |
| jaswanth     | 1237 | kurnool  |   9913 |       256 |
| abhi         | 1239 | vizag    |   9989 |       178 |
| vikram       | 1275 | hyd      |   7689 |       234 |
| viswanth     | 1375 | chennai  |   7999 |       294 |
| aravind      | 1387 | kakinda  |   9999 |       890 |
+--------------+------+----------+--------+-----------+
7 rows in set (0.00 sec)

mysql> select*from bank where 220<a_pricing<300;
+--------------+------+----------+--------+-----------+
| a_holdername | a_no | a_adress | a_phno | a_pricing |
+--------------+------+----------+--------+-----------+
| venky        | 1234 | guntur   |   7013 |       450 |
| sai          | 1235 | ongole   |   9013 |       299 |
| jaswanth     | 1237 | kurnool  |   9913 |       256 |
| abhi         | 1239 | vizag    |   9989 |       178 |
| vikram       | 1275 | hyd      |   7689 |       234 |
| viswanth     | 1375 | chennai  |   7999 |       294 |
| aravind      | 1387 | kakinda  |   9999 |       890 |
+--------------+------+----------+--------+-----------+
7 rows in set (0.00 sec)

mysql> select*from bank where 220<a_pricing>300;
Empty set (0.00 sec)

mysql> select*from bank where a_pricing BETWEEN 220 and 300;
+--------------+------+----------+--------+-----------+
| a_holdername | a_no | a_adress | a_phno | a_pricing |
+--------------+------+----------+--------+-----------+
| sai          | 1235 | ongole   |   9013 |       299 |
| jaswanth     | 1237 | kurnool  |   9913 |       256 |
| vikram       | 1275 | hyd      |   7689 |       234 |
| viswanth     | 1375 | chennai  |   7999 |       294 |
+--------------+------+----------+--------+-----------+
4 rows in set (0.00 sec)

mysql>
