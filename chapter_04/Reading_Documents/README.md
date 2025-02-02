### 阅读文档

传统上，UNIX和UNIX-like的操作系统会产生大量的文件，以供用户在某一时刻查阅。自然，会有很多读取文件的方法，我们在此展示几种最常见的。

早期，如果你想查看文件内容（任何文件，包括文本文件和二进制程序）你需要用到`cat(1)`. `cat`是个很简单的程序，能接受一个或多个文件，将其连接（连接，con**cat**enate, 因此得名）起来并输出到标准输出（一般是你的终端屏幕）。当文件不大不会刷屏时还好，但不适合阅览大型文件因为它没有内置的文件内跳转的功能，也不能逐段读取。今天，`cat`依然被广泛使用，但主要用在脚本里来合成文件。

```
darkstar:~$ cat /etc/slackware-version
Slackware 14.0
```

看到`cat`的缺点，一些聪明人士坐下来开发一个能一次只读取一页的程序。这种程序被称为"pagers". 最早的就是`more(1)`, 因为你能随时看到更多（more）文件内容而得名。

