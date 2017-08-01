# CockroachDB
## docker 安装：
* >docker pull cockroachdb/cockroach:v1.0.4
* >docker run --rm cockroachdb/cockroach:v1.0.4 version


## 运行：
* >docker network create -d bridge roachnet
* >docker run -d --name=roach1 --hostname=roach1 --net=roachnet -P 26257:26257 -p 3306:3306 -v C:\Users\yzt\docker\roach:/cockroach/winston cockroachdb/cockroach:v1.0.4 start --insecure


## 进入：
* >docker start winston
* >docker exec -it winston ./cockroach sql --insecure


## 创建用户:
 ```sql
CREATE USER core_acc WITH PASSWORD 'J8Mct1UxL5';
```

## 用户授权:
```sql
GRANT SELECT, INSERT, UPDATE ON TABLE winston.users TO core_acc;
GRANT SELECT, INSERT, UPDATE ON TABLE winston.messages TO core_acc;
```
![img](https://www.cockroachlabs.com/uploads/2016/10/running-cockroachdb-on-kubernetes.png)
