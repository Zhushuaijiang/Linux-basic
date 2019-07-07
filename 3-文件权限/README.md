#ls 查看权限
     ls -l
    total 16
    ----rw-r-- 1 morvan morvan 34 Oct 12 09:51 t1.py
    -rw----r-- 1 morvan morvan 80 Oct 12 09:57 t2.py
    -rw-rw-r-- 1 morvan morvan 12 Oct 12 09:56 t3
    -rwxrw-r-- 1 morvan morvan 55 Oct 13 17:28 t.py

    在这里, 像-rw-rw-r--这种, 就是权限的说明. 细节展示在下面的图中. 在下图中, 这串字符得拆成4个部分,
    Type: 很多种 (最常见的是 - 为文件, d 为文件夹, 其他的还有l, n … 这种东西, 真正自己遇到了, 网上再搜就好, 一次性说太多记不住的).
    User: 后面跟着的三个空是使用 User 的身份能对这个做什么处理 (r 能读; w 能写; x 能执行; - 不能完成某个操作).
    Group: 一个 Group 里可能有一个或多个 user, 这些权限的样式和 User 一样.
    Others: 除了 User 和 Group 以外人的权限.
    [怎么修改]

    +, -, =: 作用的形式, 加上, 减掉, 等于某些权限
    r, w, x 或者多个权限一起, 比如 rx
     chmod u-r t2.py
     chmod g+x-w t3


     #!/usr/bin/python3        # 这句话是为了告诉你的电脑执行这个文件的时候用什么来加载