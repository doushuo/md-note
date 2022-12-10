## Jenkins

### 拉取镜像

```
## 拉取镜像
docker pull jenkins/jenkins:lt

## 新建目录
/data/jenkins_home
```

### 安装

```
docker run -d --name jenkins -p 8081:8080 -v /data/jenkins_home:/var/jenkins_home jenkins/jenkins:lts
备注：
-d //启动在后台
--name //容器名字
-p //端口映射（8081：宿主主机端口，8080：容器内部端口）
-v //数据卷挂载映射（/data/jenkins_home：宿主主机目录，另外一个即是容器目录）
enkins/jenkins:lts //Jenkins镜像（最新版）
```



解决：
chown -R 1000:1000 /data/jenkins_home //用户组改变

访问

http://192.168.1.19:8081/login?from=%2F





查看密码

```
在安装完成后，默认生成了一个登录密码，首次登录需要这个密码。
密码路径：var/jenkins_home/secrets/initialAdminPassword //容器内部
查找密码：
docker exec -it jenkins_01 bash //进入jenkins容器
cat /var/jenkins_home/secrets/initialAdminPassword //查看密码
```

