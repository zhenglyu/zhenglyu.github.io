---
title:  "Python 从入门到放弃（1）"
date:   2017-03-26 15:14:23
categories: [Python]
tags: [Python]
---

开发环境：Windows 10 1703 + VS Code + Python 3.6

VS2017 Preview，Pycharm，VS Code，自带的IDLE都用了个遍。


首先VS2017 Preview挺好的，就是太大了，运行稍慢，感觉有点像杀鸡用牛刀的感觉。然后 Pycharm，据说是最好的IDE，但不是很会用。拿来学 Python，感觉有点复杂。自带的IDLE，功能太简陋，语法矫正，关键词提醒，行号等功能不是特别全。


最后的选择就是 VS Code。扩展好，简单易用，界面直观。简单调试后，直接上手。




先设置VSCode开发环境，依照[这里](http://jingyan.baidu.com/article/00a07f38503a2b82d028dc26.html "教程")大概设置一下。


然后发现拿来学Python，还不是很理想（可能我还是太菜了）。于是继续修改，先在【调试】里，运行改成CMD终端运行。第二个就是不断点。

【调试】修改，如下设置
```python
{
    "version": "0.2.0",
    "configurations": [

        {
            "name": "CMD终端运行",                   #名称
            "type": "python",
            "request": "launch",
            "stopOnEntry": false,                    #运行过程中不断点
            "pythonPath": "C:/Python3/python.exe",   #Python路径
            "program": "${file}",
            "cwd": null,
            "console": "externalTerminal",
            "env": null,
            "envFile": "${workspaceRoot}/.env",
            "debugOptions": [
                "WaitOnAbnormalExit",
                "WaitOnNormalExit"
            ]
        },

    ]
}
```


中文显示乱码问题，在第一行输入
```python
#encoding=utf8
```


终端里运行完程序后，程序直接退出，对于初学者来说看不到运行结果，于是我在最后加入了一句
```python
input()
```