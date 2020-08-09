### SQL 注入

输入的字符串中注入 SQL 指令，若程序当中忽略了字符检查，导致恶意指令被执行而遭到破坏或入侵

#### SQL 注入示例

```
$id = $_GET['id'];
$sql = "SELECT * FROM `user` WHERE `id`={$id}";
```

将传递参数改为

> 1;DROP TABLE OrdersTable--

#### SQL 注入防御

- 使用预编译语句绑定变量(最佳方式)
- 检查输入数据的数据类型(可对抗注入)
- 数据库最小权限原则



#### why

1. PreparedStatement能预编译，这条预编译的SQL查询语句能在将来的查询中重用，这样一来，它比Statement对象生成的查询速度更快。
2. PreparedStatement可以写动态参数化的查询
3. 参数会被当作整体的字符串处理，而不会被解析成sql指令



