# MiaoSQL

## 介绍
基于pymysql的更适合喵喵体质的SQL库，旨在减少SQL代码的编写。

## 下载
通过`pip`下载
```shell
pip install MySQL
```

## 使用实例
```python
from MiaoSQL.miaosql import MySql as Sql
# 数据库信息
config_sql = {
    "host": 'localhost',
    "user": '用户名',
    "password": '密码',
    "database": '数据库名'
}
# 连接数据库
sql = Sql(config_sql)

# 插入
if not sql.if_in_it('表名',["列名"],["数值"]):  # 如果数据不存在表中
    sql.add('表名',["列名1","列名2","列名3"],["数值1","数值2","数值3"])

# 查询某表
sql.sel()
# 打印查询结果
print(sql)
```