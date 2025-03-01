# 关系型与非关系型数据库

## 关系数据库

关系型数据库把复杂的数据结构归结为简单的二位表格的形式。 即以行和列的形式存储数据，一系列的行和被称为表，一组表归成一个库。现实世界中实体与实体之间均用关系模型来表式，关系型数据库就是建立在这种关系模型上的数据库。  

## 非关系数据库

非关系型数据库可以看成传统关系型数据库的阉割版本，基于键值存储数据，不需要经过sql解析，性能非常高，同时减少不常用的功能，进一步提高性能。  

### 非关系型数据库案例

#### key-value型数据库

缺点是无法像关系型数据库那样通过筛选条件过滤数据，不知道去哪里找数据需要遍历所有的key，非常消耗计算。  

#### 文档型数据库

比较流行的是mongodb,也可以看成key-value的形式，知识value是文件。  

### 搜索引擎的数据库

主要产品Solr 

### 列式数据库

一般的关系型数据库都采用的式行式存储，理解：一行的数据存储在一个连续的内存单元中，而列式存储是将一列的数据存储在连续的内存单元中。  可以大量降低系统的I/O--在只读取个别列的数据时，列示存储内存只需要加载需要的列，不像行式存储加载所有的列，这样就降低I/O。   图片数据库  

### 图片数据库

主要利用图形的形式存储复杂关系的，如社交网络中人物于人物的关系。

# E-R（entity-relationship 实体和联系）模型的理解：实体集，属性，联系集三个概念

## 实体集和属性

 对比面向对象编程类的思想，关系型数据库中一个表<-------->类,一行<---------->对象，一列<-------------->属性。

## 关系  ：一对一，一对多，多对多，和自我引用的关系

一对一的关系：一张表的记录对应另外一张表的一条记录  

一对多的关系：一张表的记录对应另外一张表的多条记录，客户-订单表  

多对多的关系：需要一个中间表，中间表和另外俩张表都是一对多的关系，整体上就是多对多的关系

![29a2c484-d34a-4900-8bcf-55ab9b259f1d](file:///C:/Users/wwwda/Pictures/Typedown/29a2c484-d34a-4900-8bcf-55ab9b259f1d.png)

自我引用：    

<img title="" src="file:///C:/Users/wwwda/Pictures/Typedown/12d3e6b8-c1a7-453c-be4c-0944f2748581.png" alt="12d3e6b8-c1a7-453c-be4c-0944f2748581" style="zoom:150%;">












