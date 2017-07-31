# docker

 ## ctop_docker

  ### docker 安装：

 * > docker run --rm -ti --name=ctop -v /var/run/docker.sock:/var/run/docker.sock quay.io/vektorlab/ctop:latest

## CockroachDB
### docker 安装：
* >docker pull cockroachdb/cockroach:v1.0.4
* >docker run --rm cockroachdb/cockroach:v1.0.4 version
* >docker network create -d bridge roachnet
* >docker run -d --name=roach1 --hostname=roach1 --net=roachnet -P 26257:26257 -p 3306:3306 -v C:\Users\yzt\docker\roach:/cockroach/winston cockroachdb/cockroach:v1.0.4 start --insecure
* >docker exec -it winston ./cockroach sql --insecure
