1.Linux 系统
    * C编程语言中的malloc、calloc函数和C++的 new 运算符都是在动态存储区(heap)上申请内存空间。
    * cat 将两个文件拼接在一起，cat file1 file2 > file3
      grep 命令可以从一个或者多个文件中搜索特定的字符串模式
      awk 是在文件或字符串中基于指定规则浏览和抽取信息
      cut 从数据文件或者命令的输出中截取各种各样的数据域
    * 路由信息是由[ 目的主机所在的网络地址，下一跳地址，子网掩码]组成
    * crontab 中*****分别是"分时日月周"
    * 硬链接：一个inode号对应多个文件名，则称这些文件为硬链接（同一个文件使用了多个别名）
      软链接：若文件用户数据块中存放的内容是另一文件的路径名的指向，则该文件就是软链接。
    * TCB：线程控制块
      PCB：进程控制块
      MMU：内存管理单元，是中央处理器用来管理虚拟内存和物理内存寄存器的控制线路，也负责虚拟内存映射为物理内存。
      CACHE：高速缓冲存储器
      DMA：直接内存存储，传输数据从一个地址空间到另一个地址空间。
    * tcpdump 是简单可靠网络监控的使用工具。
      top：显示活动进程方面的情况。
      netstat：显示网络有关信息，比如套接口使用情况、路由、接口、协议等。
      ifconfig：查看活动的网卡信息。
    * setuid位是让普通用户可以以root用户的角色运行只有root帐号才能运行的程序或命令。
      因此当程序设置了setid权限位时，普通用户会临时变成root权限，但实际用户任然是原来的用户。
    * /etc/mtab文件的作用：记载的是现在系统已经装载的文件系统，包括操作系统建立的虚拟文件等；而/etc/fstab是系统准备装载的
      /etc/fstab文件的作用 ：记录了计算机上硬盘分区的相关信息，启动 Linux 的时候，检查分区的 fsck 命令，和挂载分区的 mount 命令，都需要 fstab 中的信息，来正确的检查和挂载硬盘。
    * Linux进程间通信：管道、信号、消息队列、共享内存、信号量、套接字(socket)
      Linux线程间通信：互斥量（mutex），信号量，条件变量
      Windows进程间通信：管道、消息队列、共享内存、信号量 （semaphore） 、套接字(socket)
      Windows线程间通信：互斥量（mutex），信号量（semaphore）、临界区（critical section）、事件（event）
    * Linux下通过 cat /proc/interrupts 命令查看中断
      /proc/ioports 当前使用的I/O端口
      /proc/kcore 系统物理内存映像。与物理内存大小完全一样，但不实际占用这么多的内存。
      /proc/kmsg  内核输出的消息，也被送到syslog
    * sed 流编辑器,处理时，把当前处理的行存储在临时缓冲区中，称为"模式空间"（pattern space），接着用sed命令处理缓冲区中的内容，处理完成后，把缓冲区的内容送往屏幕。接着处理下一行，这样不断重复，直到文件末尾。文件内容并没有 改变，除非你使用重定向存储输出。
      sed [options] 'command' file(s)
      -n或--quiet或--silent：仅显示script处理后的结果；
      g 表示行内全面替换  
      p 表示打印行  
      s 替换指定字符
    *tar
      -c: 建立压缩档案
      -x：解压
      -t：查看内容
      -r：向压缩归档文件末尾追加文件
      -u：更新原压缩包中的文件
      
      这五个是独立的命令，压缩解压都要用到其中一个，可以和别的命令连用但只能用其中一个。下面的参数是根据需要在压缩或解压档案时可选的。
      
      -z：有gzip属性的
      -j：有bz2属性的
      -Z：有compress属性的
      -v：显示所有过程
      -O：将文件解开到标准输出
      
      压缩
      
      tar -cvf jpg.tar *.jpg //将目录里所有jpg文件打包成jpg.tar 
      
      tar -czf jpg.tar.gz *.jpg   //将目录里所有jpg文件打包成jpg.tar后，并且将其用gzip压缩，生成一个gzip压缩过的包，命名为jpg.tar.gz
      
       tar -cjf jpg.tar.bz2 *.jpg //将目录里所有jpg文件打包成jpg.tar后，并且将其用bzip2压缩，生成一个bzip2压缩过的包，命名为jpg.tar.bz2
      
      tar -cZf jpg.tar.Z *.jpg   //将目录里所有jpg文件打包成jpg.tar后，并且将其用compress压缩，生成一个umcompress压缩过的包，命名为jpg.tar.Z
      
      rar a jpg.rar *.jpg //rar格式的压缩，需要先下载rar for linux
      
      zip jpg.zip *.jpg //zip格式的压缩，需要先下载zip for linux
      
      解压
      
      tar -xvf file.tar //解压 tar包
      
      tar -xzvf file.tar.gz //解压tar.gz
      
      tar -xjvf file.tar.bz2   //解压 tar.bz2
      
      tar -xZvf file.tar.Z   //解压tar.Z
      
      unrar e file.rar //解压rar
      
      unzip file.zip //解压zip
      
      总结
      
      1、*.tar 用 tar -xvf 解压
      
      2、*.gz 用 gzip -d或者gunzip 解压
      
      3、*.tar.gz和*.tgz 用 tar -xzf 解压
      
      4、*.bz2 用 bzip2 -d或者用bunzip2 解压
      
      5、*.tar.bz2用tar -xjf 解压
      
      6、*.Z 用 uncompress 解压
      
      7、*.tar.Z 用tar -xZf 解压
      
      8、*.rar 用 unrar e解压
      
      9、*.zip 用 unzip 解压
    * 列模式
      删除列
      1.光标定位到要操作的地方。
      2.CTRL+v 进入"可视 块"模式，选取这一列操作多少行。
      3.d 删除。
       
      插入列
      插入操作的话知识稍有区别。例如我们在每一行前都插入"() "：
      1.光标定位到要操作的地方。
      2.CTRL+v 进入"可视 块"模式，选取这一列操作多少行。
      3.SHIFT+i(I) 输入要插入的内容。
      4.ESC 按两次，会在每行的选定的区域出现插入的内容。
    * 死锁
      产生死锁的原因主要是： 
      （1） 因为系统资源不足。 
      （2） 进程运行推进的顺序不合适。 
      （3） 资源分配不当等。 
      
      产生死锁的四个必要条件： 
      （1） 互斥条件：一个资源每次只能被一个进程使用。 
      （2） 请求与保持条件：一个进程因请求资源而阻塞时，对已获得的资源保持不放。 
      （3） 不剥夺条件:进程已获得的资源，在末使用完之前，不能强行剥夺。 
      （4） 循环等待条件:若干进程之间形成一种头尾相接的循环等待资源关系。 
    * tail
      tail -n +K是输出从第K行开始的内容。
      tail -n K是输出最后K行的内容。
    * 僵尸进程 & 孤儿进程
      僵尸进程：一个子进程在其父进程还没有调用wait()或waitpid()的情况下退出。这个子进程就是僵尸进程。
      孤儿进程：一个父进程退出，而它的一个或多个子进程还在运行，那么那些子进程将成为孤儿进程。孤儿进程将被init进程(进程号为1)所收养，并由init进程对它们完成状态收集工作。
      僵尸进程将会导致资源浪费，而孤儿则不会。
      
      正常情况下， 当一个 进程完成它的工作终止之后，它的父进程需要调用wait()或者waitpid()系统调用取得子进程的终止状态。
      孤儿进程的存在 是因为 父进程先于子进程退出，那么子进程会变成孤儿进程
      僵尸进程的存在 是因为 子进程退出后，父进程并没有调用wait（）或者 waitpid（），子进程的描述符还保留在系统中
    * 内核分为进程管理子系统，内存管理子系统，io管理子系统，文件管理子系统
    * rsync
    * 文件描述符
      0 ,1,2叫文件描述符；Linux中，每打开一个文件都有一个小的整数与之对应，就是文件描述符！
      0 是标准输入的 （stdin）
      1 是标准输出的 （stdout）
      2 是标准报错输出的 （stderr）
      '<'是输入重定向符
      '>'是输出重定向符
    * fg：将后台中的命令调至前台继续运行
      bg：将一个在后台暂停的命令，变成继续执行
      ctrl + z：可以将一个正在前台执行的命令放到后台，并且暂停
    * /etc/hosts 设定用户自已的IP与名字的对应表
      /etc/HOSTNAME   设定用户的节点名 
      /etc/resolv.conf    设置DNS  
      /etc/gateways 设定路由器 
    * 用户态切换到内核态的  3  种方式
      a.  系统调用
      b.  异常
      c.  外围设备的中断 
    * fstab
      /etc/fstab是用来存放文件系统的静态信息的文件。位于/etc/目录下，可以用命令less /etc/fstab 来查看，如果要修改的话，则用命令 vi /etc/fstab 来修改。
      当系统启动的时候，系统会自动地从这个文件读取信息，并且会自动将此文件中指定的文件系统挂载到指定的目录。
    * 
      ctrl+z把正在运行的程序调到后台,暂停一个前台的作业，即挂起 。
      ctrl+x在某些文字处理程序中，这个控制字符将会剪切高亮的文本并且将它复制到剪贴板中。
      ctrl+v在输入文本的时候，按下之后，可以插入控制字符。
      ctrl+c中断，终结一个前台作业。



2.开源软件
Nginx(ngx_lua、openresty）
LVS
HAProxy
RabbitMQ
Kafka
ZooKeeper
Bind
Puppet
ELK
3.编程语言
Python
4.软素质
分析问题的思路、解决问题的能力、自驱性
5.系统
消息队列、分布式系统
6.网络协议