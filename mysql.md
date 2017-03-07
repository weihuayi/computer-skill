# MySQL

**数据库**是一个存储数据集的单独应用. 每个数据库都有一个或多个不同的 API,
用来创建(creating), 访问(accessing), 管理(managing), 查找(searching),
和复制(replicating)它所存储的数据.

关系型数据库管理系统 (relational database management systems, RDBMS)

1. tables
1. primary key
1. foreign key

一个 RDBMS 可以做:

1. 用表(table), 列(columns), 和索引(indexes) 实现一个数据库
1. 保证不同表的行之间关系的完整性
1. 自动更新索引
1. 解释一个 SQL 查寻和综合不同表之间的信息

术语

1. **DataBase**: 就是有联系的数据组成的表的集合
1. **Table**: 就是一个数据矩阵
1. **Column**: 同一列包含同一类型的数据, 比如说一列邮政编码.
1. **Row**: 一行就是一组相关的数据
1. **Redundancy**: 冗余, 存储数据两次, 系统可以更快.
1. **Primary Key**: 主键是唯一的, 在一个表中主键不能出现两次.
   一个主键最多只能找到一行数据.
1. **Foreign Key**: 是两个表之间的 Linking Pin
1. **Compound Key**: 复合键值, 由多列组成, 因为一列可能不能保证唯一.
1. **Index**: 索引, 类似书后面的索引
1. **Referential Integrity**: 引用完整性, 保证一个外部键值问题指向一个存在的行


## MySQL 数据库

特点:
1. fast
1. easy-to-use
1. RDBMS


为什么好?

1. Open Source
1. Powerful
1. Standard form of the well-known SQL data language
1. work on many operating systems
1. very quickly and works well even with big data sets
1. very frindly to PHP
1. supports large databases, 50 million rows or more in a table
1. customizable


## 基本命令

1. CREATE DATABASE TUTORIALS
1. DROP DATABSE TUTORIALS
1. CREATE TABLE table_name( )
1. DROP TABLE table_name 

数据类型:
1. numeric 
1. date and time
1. string types
```
CREATE TABLE tutorials_tbl(
   tutorial_id INT NOT NULL AUTO_INCREMENT,
   tutorial_title VARCHAR(100) NOT NULL,
   tutorial_author VARCHAR(40) NOT NULL,
   submission_date DATE,
   PRIMARY KEY ( tutorial_id )
   );
```

