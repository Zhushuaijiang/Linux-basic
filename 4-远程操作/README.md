#给 Ubuntu 安装 OpenSSH

    打开终端添加SSh服务
     sudo apt-get install openssh-server
    检查ssh的服务状态
    sudo service ssh status
    开启ssh服务
    sudo service ssh restart

VNC:
   1: sudo apt-get install x11vnc

   2: 登录密码设置

    x11vnc -storepasswd

   3: 执行命令后，提示信息有文件路径

   4: x11vnc启动

    x11vnc  -rfbport 5900 -rfbauth ~/.vnc/passwd -display :0 -forever -bg -repeat -nowf -o ~/.vnc/x11vnc.log

    -rfbport:指定启动端口
    -rfbauth:指定密码文件路径
    -o:日志文件路径

   5: 验证是否启动

    ps -aux | grep x11vnc
    netstat -nap | grep 5900

windows下VNC启动
    1：下载 TightVNC  https://www.tightvnc.com/licensing-tvnserver.php
    2：安装后启动 ip/5900 登陆即可


