# MongoDB 初学（二）[数据库]

> 安装目录

`usr/local/mongodb/bin`

## 一、概念解析

| sql 术语/概念 | MongoDB 术语/概念 | 解释/说明                              |
| ------------- | ----------------- | -------------------------------------- |
| database      | database          | 数据库                                 |
| table         | collection        | 数据库表/集合                          |
| row           | document          | 数据记录行/文档                        |
| column        | field             | 数据字段/域                            |
| index         | index             | 索引                                   |
| table joins   |                   | 表连接,MongoDB 不支持                  |
| primary key   | primary key       | 主键,MongoDB 自动将\_id 字段设置为主键 |

## 二、数据库

* 显示所有数据的列表

  > `show dbs`

  ```
  > show dbs
  local  0.078GB
  study  0.078GB
  >
  ```

* 显示当前数据库对象或集合

  > `db`

  ```
  > db   
  test   
  ```

* 连接到一个指定的数据库(创建数据库)。

  > `use <database>`

  ```
  > use test
  switched to db test
  ```

* 往数据库添加数据/查看数据库列表

  > `db.<database>.inser({'key':'value'})`

  
  ```
  > db.test_table.insert({"content":"xxxxx"})
  WriteResult({ "nInserted" : 1 })
  >
  >
  >
  > show tables
  system.indexes
  test_table
  >
  >
  > db.test_table.find()
  { "_id" : ObjectId("5d188e93c8f86afac898121b"), "content" : "xxxxx" }
  ```


* 删除数据库

  >`db.dropDatabase()`

  ```
  > db.dropDatabase()
  { "dropped" : "test2data", "ok" : 1 }
  ```