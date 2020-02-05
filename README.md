# compile-spark
1.在Dockerfile所在目录下构建镜像
```
docker build -t spark:v2.4.0 .
```
2.启动主节点
```
docker run -itd --name spark-master -p 6066:6066 -p 7077:7077 -p 8081:8080 -h spark-master spark:v2.4.0 ./bin/spark-class org.apache.spark.deploy.master.Master
```
