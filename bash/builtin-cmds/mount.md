# mount

## Linux 挂载 Windows 贡献文件夹

0. 确保两台机器的网络互通，且可以通过防火墙

1. 开放 Windows 共享文件夹：右键 ->“属性”-> 共享 ->  点击“共享...”，

2. 在 Linux 上挂载

```bash
# Ubuntu 安装 cifs
$ sudo apt-get install cifs\*

# 挂载
# username,password 分别是 windows 的用户名和密码
# //172.16.1.101/Share 是 Windows 共享文件夹的网络逻辑
# /home/xxx/windows 是 Linux 挂载的路径，xxx 通常是你的当前用户名
# uid,gid 是 xxx 用户的 UID（`id -u`）和 GID（`id -g`），如果不指定，/home/xxx/windows 的默认所有者和所属组为 root
$ sudo mount -t cifs -o username='alice',password='123456',uid=1000,gid=1000 //172.16.1.101/Share /home/xxx/windows
```
