#Linux 基本指令 ls 和 cd
    Linux 的深度玩家, 基本上都是用 Terminal 和指令 (command) 来超控电脑的.
    有些时候甚至你的电脑没有屏幕, 也只能用指令来超控. 比如服务器, 树莓派(raspberry pi).

    #cd 指令
        第一个要知道的指令就是怎么样去到你想去的地方. cd (Change Directory)
        找到 Linux 的 terminal 窗口, 然后他默认跳出来是在你的用户目录 (Home). Terminal 中的 ~ $ 就是说你输入指令将在 ~ 这个目录下执行. 而 ~ 这个符号代表的是你的 Home 目录. 如果在文件管理器中可视化出来
        使用 cd 指令, 我们能在 Terminal 中轻松切换到不同的文件夹. 想从 Home 去 Documents 这个文件夹? 输入下面的命令就可以了.
            ~$ cd Documents/
        接着你会看到它在下一行跳出了这个东西, 在 $ 前面的 ~/Documents 就说明你现在已经在 Documents 这个文件夹里了. 你现在要执行的命令将会在这个目录下生效.
            ~/Documents$

        --常用的 cd 命令.
            1:返回上一级目录  ~/Documents$ cd ..
            2:去往子文件夹  ~$ cd Documents/folder1/
            3:返回你刚刚所在的目录 ~/Documents/folder1$ cd -/home/zsj
            4:向上返回两次  ~/Documents/folder1$ cd ../../
            5:去往 Home  ~/Documents/folder1$ cd ~
            6:去往电脑任何地方, 你需要的是一个绝对路径  ~$ cd /home/morvan/Documents/folder1

    #ls指令
        查看该目录下的所有文件列表
             ls
         1 输出详细信息 -l (long 的简写). 这个指令会打印出文件的权限 (-rw-rw-r-- 之后我们在细说这个), 用户名, 文件大小, 修改日期, 文件名
             ls -l
         2 -a (all 的简写) 显示所有文件 . 这里还会显示隐藏的文件 (以 . 开头的)
             ls -a
         3 -lh (human), 直接 -l 不方便人看, 这个指令是为了方便给人观看的. 注意这里的文件大小使用了 K, MB, GB 之类概括
             ls -lh
         4 还有很多其他的功能, 我们可以通过 --help 来查看

     #touch 新建
        touch 的使用很简单, 我们先去往 Documents 的文件夹, 里面已经有了 folder1 和 file1, 如果我们想新建一个 file2 使用下面的语句就好. 一个空文件就建立好了.
        touch file
        cp 老文件 新文件
        1:cp file1 file1copy
        2:cp -i file1 file1copy(注意: 如果 file1copy 已经存在, 它将会直接覆盖已存在的 file1copy)
        3:cp file1 folder1 (复制去文件夹)
        4:cp -R folder1 (复制文件夹, 需要加上 -R (recursive))
        5:cp file* folder2/ (复制多个文件. 复制名字部分相同的多个文件, * 是说”你就找文件前面是 file 的文件, 后面是什么名字无所谓”)

    #mv 剪切
        知道了 cp, mv就好理解多了, 基本是一样的.
       1:移动去另一个文件夹
        mv file1 folder1/
       2:重命名文件
        mv  file1 file1rename

     #mkdir, rmdir 和 rm

     mkdir 建立文件夹
     mkdir (make directory) 就是创建一个文件夹的意思, 使用起来很简单.
     mkdir folder2/f2
     这样, f2 这个文件夹就被新建在了 folder2 里面.

     #rmdir 移除文件夹
     rmdir (remove directory) 也就是字面意思, 移除文件夹. 不过这有一个前提条件. 这些要移除的文件夹必须是空的. 不然会失败. 所以如果想刚刚建立的那个 folder2 就不能被移除, 因为里面有个 f2 文件夹.

     #rm 移除文件
     1 移除单个文件
     rm file1
     2 -i 或 -I 有提示地移除文件 (为了避免误删)
     rm -i f1 f2 f3 f4
     3 -r 或 -R (recursively) 用来删文件夹
      rm -r folder1



    #nano
    nano 是 linux 的一款文字编辑工具. 我们可以拿它来做最基本的 terminal 端的文本编辑, 甚至可以写代码~ 下面我们用 touch 创建一个 Python 脚本. 如果大家不懂 Python 也没关系, 你就知道我们可以拿 nano 来编辑文字或者脚本就好了.

    #cat

    1：cat t.py
    2 > 将文件的内容放到另一个文件里
     cat t.py > t1.py
    3：> 将多个文件的内容打包一起放入另一个文件
     cat t.py t1.py > t2.py
    4:>> 将内容添加在一个文件末尾
      cat t.py t1.py>>t3.py
      ****究极操作请务必慎重：rm /

