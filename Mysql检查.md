### Mysql的健康检查

* 检查的指标
```
1. 连接数
  select count(*) from information_schema.processlist

2. 线程检查
  select * from information_schema.GLOBAL_STATUS where Variable_name like 'Thread%‘
  
  Thread_cached：线程池中还有多少可以被复用的线程
  Thread_connected：和show processlist一样
  Thread_created：新创建的thread
  Thread_running：正在运行的连接(非sleep)
```
