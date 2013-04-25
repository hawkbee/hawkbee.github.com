---
layout: default
title: 查看Linux版本号及其来源
---

通常可以通过`uname`命令来获取操作系统的基本信息。当前的电脑上，`uname -a`的返回值为：`Linux Hiker 3.8.7-1-ARCH #1 SMP PREEMPT Sat Apr 13 12:52:41 CEST 2013 i686 GNU/Linux`,而`uname -r`返回的是`3.8.7-1-ARCH`。

但是在开发进行中的版本，调用`uname -r`返回的字符串却是`2.6.32.60-00013-g233d67a-svn336`，除了真正的版本号`2.6.32.60`外，还有另外的字符串`-00013-g233d67a-svn336`。这部分是代表什么意思呢？

首先来看几个重要的文件。

  >1. Makefile
  2. include/config/kernel.release
  3. include/config/auto.conf
  4. scripts/setlocalversion
