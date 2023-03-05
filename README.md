# open-conference-2023

# MySQL - 20230305-01

##　問　次のテーブル《items》のidが2であるデータについて、priorityが重複していないかを調べるクエリを書きましょう
### 《items》

|  id  |  priority  |
| ---- | ---- |
|  1  |  0  |
|  1  |  1  |
|  2  |  0  |
|  2  |  1  |
|  2  |  1  |
|  3  |  0  |
|  3  |  1  |
|  3  |  2  |

~~~
  create table items ( id int , priority int ) ;
  insert into items values (1,0),(1,1),(2,0),(2,1),(2,1),(3,0),(3,1),(3,2);
~~~

解答例　以下の２つのクエリの結果の数が　２と３であることから重複を判断する。。。　等  
~~~
mysql> select * from items where id = 2 group by priority;
+------+----------+
| id   | priority |
+------+----------+
|    2 |        0 |
|    2 |        1 |
+------+----------+
2 rows in set (0.01 sec)

mysql> select count(*) from items where id = 2 ;
+----------+
| count(*) |
+----------+
|        3 |
+----------+
1 row in set (0.00 sec)
~~~
