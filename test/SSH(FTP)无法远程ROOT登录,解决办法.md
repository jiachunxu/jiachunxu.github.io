# SSH(FTP)无法远程ROOT登录,解决办法

## 1.检查是否为root用户创建密码
    '''
    如果没有为root用户创建密码运行下方命令为root用户创建密码

    sudo passwd root
    '''
## 2.检查是否安装sshd服务
    '''
    如果没有安装sshd,运行下方命令

    sudo apt install openssh-server
    '''

## 3.打开此路径/etc/ssh/sshd_config下配置文件
    '''
    sudo vim /etc/ssh/sshd_config
    将此行 # PermitRootLogin hibit-password
    修改为 PermitRootLogin yes
    '''
## 4.重启linux
    '''
    reboot
    '''
    


