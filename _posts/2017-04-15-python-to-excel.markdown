---
title:  "Python 从入门到放弃（2）Excel库"
date:   2017-04-15 15:04:23
categories: [Python]
tags: [Python,Excel]
---

Python中Excel库的比较内容（如下）

||XlsWriter|xlrd&xlwt|OpenPyXL|Microsoft Excel API|
|-|:-|:-|:-|:-|
|介绍|可以创建Excel 2007或更高版本的XLXS文件|即 python-excel,含xlrd,xlwt和xlutils三大模块，分别提供读、写和其他功能|可以读写Excel 2007 XLSX和XLSM文件|直接通过COM组件与Microsoft Excel进程通信调用其各种功能实现对Excel文件的操作|
|读|×|√|√|√|
|写|√|√|√|√|
|修改|×|×|!|√|
|.xls|×|√|×|√|
|.xlsx|√|!|√|√|
|大文件|√|×|√|×|
|功能|强|弱|一般|超强|
|速度|快|快|快|超慢|
|系统|无限制|无限制|无限制|Windows+Excel|
|适用场景|·要创建XLSX文件<br>·不需要读取已有文件<br>·数据量可能会很大<br>·需要跨平台|·要读取XLS或XLSX文件<br>·要生成XLS文件<br>·需要的功能不太复杂<br>·需要跨平台|·要处理XLSX文件<br>·需要修改已有文件，或者在写入过程中需要不断修改<br>·需要的功能比较复杂<br>·数据量可能会很大<br>·需要跨平台|·需要处理各种文件格式<br>·需要用到特别复杂的功能<br>·在修改文件时，不希望对原有信息造成任何意外破坏<br>·数据量很小，或者愿意等待<br>·尽在Windows中使用|