# MongoDB 初学（一）

> 安装目录

  `usr/local/mongodb/bin`

## 一、启动mongdb

* 启动服务

  `./mongod`

## 二、进入MongDB后台管理Shell

* 打开Shell

  `./mongo`

* 第一个命令将数字 10 插入到 runoob 集合的 x 字段中。

  ```(linux)
  > db.runoob.insert({x:10})
  WriteResult({ "nInserted" : 1 })
  > db.runoob.find()
  { "_id" : ObjectId("5604ff74a274a611b0c990aa"), "x" : 10 }
  >
  ```