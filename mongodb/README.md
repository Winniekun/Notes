## MongoDB

| SQL术语/概念 | MongoDB术语/概念 |              解释/说明              |
| :----------: | :--------------: | :---------------------------------: |
|   database   |     database     |               数据库                |
|    table     |    collection    |            数据库表/集合            |
|     row      |     document     |           数据记录行/文档           |
|    column    |      field       |             数据字段/域             |
|    index     |      index       |                索引                 |
| table joins  |                  |        表连接,MongoDB不支持         |
| primary key  |   primary key    | 主键,MongoDB自动将_id字段设置为主键 |

## 基础

数据库可通过名字来标识。数据库名可以是满足以下条件的任意UTF-8字符串。

- 不能是空字符串（"")。
- 不得含有' '（空格)、.、$、/、\和\0 (空字符)。
- 应全部小写。
- 最多64字节。

有一些数据库名是保留的，可以直接访问这些有特殊作用的数据库。

- **admin**： 从权限的角度来看，这是"root"数据库。要是将一个用户添加到这个数据库，这个用户自动继承所有数据库的权限。一些特定的服务器端命令也只能从这个数据库运行，比如列出所有的数据库或者关闭服务器。
- **local:** 这个数据永远不会被复制，可以用来存储限于本地单台服务器的任意集合
- **config**: 当Mongo用于分片设置时，config数据库在内部使用，用于保存分片的相关信息。



## 基本命令

* **show dbs** 显示所有数据的列表

  ![image](https://i.loli.net/2019/04/27/5cc3dd1aa81df.png)

  

* **use** 连接到一个指定数据库

  ![image](https://i.loli.net/2019/04/27/5cc3dd1a4d509.png)

  

* **db** 显示当前数据库对象或集合

  ![image](https://i.loli.net/2019/04/27/5cc3dd1a9d0cf.png)

* 插入数据

  ![image](https://i.loli.net/2019/04/27/5cc3dd1b50b29.png)

* **备注**

  若是数据库不存在，使用use之后会创建该数据库，创建之后若无数据，则**show dbs** 不会展示新创建的数据库，插入一条数据之后方可显示。
