# huizhi-docker

晖致mac电脑的可用docker信息

## pg数据库连接信息

```
# 数据库url
DB_URI=postgresql://postgres:sxl_pwd_123@localhost:5433/doctor_agent_db?sslmode=disable
```

如果docker镜像未启动，请启动。禁止自己写yml启动pg的docker，本机docker的name为postgres-pgvector-17，已经用镜像部署完成了。

## rabbitmq
- 先检查`rabbitmq-gd25`是否启动成功
- 启动命令
```
docker start rabbitmq-gd25
```
- 再确认配置是否正确
端口映射：
5672：AMQP 协议端口（用于 Celery Broker）
15672：Web 管理界面端口
访问信息：
Web 管理界面：http://localhost:15672
默认用户名：admin
默认密码：admin123

## redis 
- 先检查`redis-gd25`是否启动成功
- 启动命令
```
docker start redis-gd25
```
- 连接方式 redis://redis-gd25:6379/0