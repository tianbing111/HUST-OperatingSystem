# HUST-OperatingSystem
2017 fall, codes about Operating System.

## Experiment 1
    编写程序，演示多进程并发执行和进程软中断、管道通信。
* 父进程使用系统调用pipe( )建立一个管道,然后使用系统调用fork()创建两个子进程，子进程1和子进程2；
* 子进程1每隔1秒通过管道向子进程2发送数据:<br>
	I send you x times. (x初值为1，每次发送后做加一操作）<br>
	子进程2从管道读出信息，并显示在屏幕上。<br>
* 父进程用系统调用signal()捕捉来自键盘的中断信号（即按Ctrl+C键）；当捕捉到中断信号后，父进程用系统调用Kill()向两个子进程发出信号，子进程捕捉到信号后分别输出下列信息后终止：<br>
  Child Process l is Killed by Parent!<br>
  Child Process 2 is Killed by Parent!<br>
* 父进程等待两个子进程终止后，释放管道并输出如下的信息后终止:<br>
  Parent Process is Killed!<br>

## Experiment 2
    通过Linux多线程与信号灯机制，设计并实现计算机线程与I/O线程共享缓冲区的同步与通信。
* 程序要求:两个线程,共享公共变量a<br>
  * 线程1负责计算(1到100的累加，每次加一个数)<br>
  * 线程2负责打印（输出累加的中间结果)<br>
  
## Experiment 3
    利用多个共享内存（有限空间）构成的环形缓冲，将源文件复制到目标文件，实现两个进程的誊抄。

## Experiment 4
    编程实现目录查询功能：
* 功能类似ls -lR<br>
* 查询指定目录下的文件及子目录信息；<br>
  显示文件的类型、大小、时间等信息；<br>
* 递归显示子目录中的所有文件信息。<br>

