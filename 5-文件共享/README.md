#
    输入 scp (secure copy), 加密传输复制 ~/Desktop/{a,b}.py 在我桌面上的 a.py 和 b.py 两个文件到 云端zsj@192.168.10.132的桌面 ~/Desktop
    scp ~/Desktop/{a,b}.py zsj@192.168.10.132:~/Desktop
本地有要运行的文件
单个文件的话可以直接 ssh 去云端运行
多个文件可以先复制去云端, 然后在 ssh 运行
如果在云端有产生文件, 可以用 scp 复制回来