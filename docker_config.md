# docker配置阿里云镜像源
```
sudo mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["https://f9dk003m.mirror.aliyuncs.com"]
}
EOF
sudo systemctl daemon-reload
sudo systemctl restart docker
```

# docker登录
```
docker login

```

# docker 拉去一个linux系统带上版本号
```
sudo docker pull ubuntu:16.04
sudo docker run -it ubuntu:16.04

```

# 查看docker 容器ID
```
docker ps -a
```
# docker 拷贝主机文件
```
sudo docker cp /usr/local/openresty containerID:/usr/local/openresty
sudo docker cp host_path containerID:container_path

```
# 启动容器或者进入容器
```
docker attach 容器ID
docker exec -it 容器ID bash
```

# 批量启动和关闭
```
1、启动所有容器

docker start $(docker ps -a | awk '{ print $1}' | tail -n +2)
2、关闭所有容器

docker stop $(docker ps -a | awk '{ print $1}' | tail -n +2)
3、删除所有容器

docker rm $(docker ps -a | awk '{ print $1}' | tail -n +2)
4、删除所有镜像（慎用）

docker rmi $(docker images | awk '{print $3}' |tail -n +2)

```


# 拉去容器到本地本推送到自己仓库

```
https://blog.csdn.net/Scirhh/article/details/85248193
```
# 保存自己刚才修改的容器到本地
```
docker commit -m="have changes" -a="skon" d8a39e9be192 skon2626/skon-hub:sc_mysql

说明：
docker commit [OPTIONS] CONTAINER [REPOSITORY[:TAG]]
CONTAINER : 容器ID
REPOSITORY 仓库名，就是登录ID ： chenwj
TAG       :     给容器起一个名字
```










