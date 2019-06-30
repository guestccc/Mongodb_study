# MongoDB 初学（三）[表/集合]

> 安装目录

`usr/local/mongodb/bin`

## 二、表

* 创建表(显性)

  > `db.createCollection('<tableName>')`

  ```
  > db.createCollection('table_test')
  { "ok" : 1 }
  >
  >
  > show tables
  system.indexes
  table_test
  ```

* 创建表(隐性)

  > `db.table_test2.insert({'content':'隐性的创建了个表，也就是说直接插入数据就可以了'})`

  ```
  > db.table_test2.insert({'content':'隐性的创建了个表，也就是说直接插入数据就可以了'})
  WriteResult({ "nInserted" : 1 })
  >              
  >              
  > show tables  
  system.indexes 
  table_test     
  table_test2  
  ```


* 查看表

  > `db.<tableName>.find()`

  ```
  > db.test_table.find()
  { "_id" : ObjectId("5d188e93c8f86afac898121b"), "content" : "xxxxx" }
  >
  ```

* 更新表

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
  table_test2 
  >
  >
  > db.test_table.find()
  { "_id" : ObjectId("5d188e93c8f86afac898121b"), "content" : "xxxxx" }
  ```

* 删除表

  >`db.<tableName>.drop()`

  ```
  > db.test_table.drop()
  true
  >
  >
  > show tables
  system.indexes   
  table_test2 
  ```
