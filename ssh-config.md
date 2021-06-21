# 远程登录
```
sudp apt-get update
sudo apt-get install openssh-server

vim /etc/ssh/sshd_config
line: 28 PermitRootLogin yes


sudo ssh restart
```

# ssh dns设置

```
vim /etc/hosts
47.98.202.83 node

127.0.0.1 localhost
::1       localhost
```


# ssh-keygen

```
cd ~/.ssh 存储了各种公钥私钥

-rw-r--r--  1 chenwj  staff   247B  6 11 14:11 config
-rw-------  1 chenwj  staff   1.8K  6 11 14:09 gitee_id_rsa
-rw-r--r--  1 chenwj  staff   397B  6 11 14:09 gitee_id_rsa.pub
-rw-------  1 chenwj  staff   1.8K  6 11 14:10 github_id_rsa
-rw-r--r--  1 chenwj  staff   397B  6 11 14:10 github_id_rsa.pub
-rw-------  1 chenwj  staff   1.8K  4  8  2020 id_rsa
-rw-r--r--  1 chenwj  staff   397B  4  8  2020 id_rsa.pub
-rw-r--r--  1 chenwj  staff   2.5K  6 21 14:36 known_hosts

create:
ssh-keygen -t rsa -C "66969721@qq.com"  -f github_id_rsa
ssh-keygen -t rsa -C "66969721@qq.com"  -f gitee_id_rsa 

config:
cat config
~/.ssh cat config
ServerAliveInterval 60
# gitee
Host gitee.com
HostName gitee.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/gitee_id_rsa
# github
Host github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/github_id_rsa

ssh-keygen -t rsa -C "66969721@qq.com"  -f github_id_rsa
ssh-keygen -t rsa -C "66969721@qq.com"  -f gitee_id_rsa 

复制SSH密钥到目标主机，开启无密码SSH登录
ssh-copy-id user@host
```
 

