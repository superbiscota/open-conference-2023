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
