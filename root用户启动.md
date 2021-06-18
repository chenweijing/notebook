1、使用:sudo passwd root设置root的密码

2、使用su root来测试是否可以进入root用户

3、进入到/usr/share/lightdm/lightdm.conf.d/目录，使用gedit 50-unity-greeter.conf
user-session=ubuntu
greeter-show-manual-login=true
all-guest=false


4. 使用vi /root/.profile命令修改文件，找到mesg n，修改为：tty -s && mesg n，


redis
https://zhuanlan.zhihu.com/p/268548048

#进入 root用户下
#apt-get update
#apt-get install redis-server
Do you want to continue? [Y/n] 

#redis-cli

ping一下

redis 127.0.0.1:6379> ping
PONG
127.0.0.1:6379> exit


# service redis-server restart