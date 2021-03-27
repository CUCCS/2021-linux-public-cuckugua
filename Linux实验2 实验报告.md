## 软件环境

Virtualbox

Ubuntu 20.04 Server 64bit

asciinema

## 实验目的

学习使用vimtutor

## 实验要求

确保本地已经完成asciinema auth，并在asciinema成功关联了本地账号和在线账号

上传本人亲自动手完成的vimtutor操作全程录像

在自己的github仓库上新建markdown格式纯文本文件附上asciinema的分享URL

## 实验步骤

1.打开安装了Ubuntu 20.04 Server 64bit的虚拟环境

2.用ssh从主机远程连接到虚拟环境

3.安装asciinema

4.进行学习并授权登录，上传录屏

## 过程录屏

Lesson1

[![asciicast](https://asciinema.org/a/psIgGxilON3SzeQaJOGV6tdWO.svg)](https://asciinema.org/a/psIgGxilON3SzeQaJOGV6tdWO)

Lesson2

[![asciicast](https://asciinema.org/a/601SOOg7m35OQHCifuu4vLOPN.svg)](https://asciinema.org/a/601SOOg7m35OQHCifuu4vLOPN)

Lesson3

[![asciicast](https://asciinema.org/a/hZvipBQry8R01YAqWhykiTeKK.svg)](https://asciinema.org/a/hZvipBQry8R01YAqWhykiTeKK)

Lesson4

[![asciicast](https://asciinema.org/a/M15ZR0uxKK8l6qSReHifclRRG.svg)](https://asciinema.org/a/M15ZR0uxKK8l6qSReHifclRRG)

Lesson5

[![asciicast](https://asciinema.org/a/Tplmku0OsJYVmyDrjOATPCOpa.svg)](https://asciinema.org/a/Tplmku0OsJYVmyDrjOATPCOpa)

Lesson6

[![asciicast](https://asciinema.org/a/fYXTtgD94xcIND6Lp4VDvVjkq.svg)](https://asciinema.org/a/fYXTtgD94xcIND6Lp4VDvVjkq)

Lesson7

[![asciicast](https://asciinema.org/a/mSIv5OfWwDgEGSsICtP0kRpRW.svg)](https://asciinema.org/a/mSIv5OfWwDgEGSsICtP0kRpRW)


## 自查清单

- 你了解vim有哪几种工作模式？

命令模式(command-mode)：操作文件

插入模式(insert-mode)：在文本中插入内容

可视模式(visual-mode)：通过v进入，可选区文本

选择模式(Select-mode)：在visual模式下Ctrl+G进入和退出模式，直接输入文字会进入inster模式并替换内容

EX模式(Ex-mode)：ex进入，:vi离开

- Normal模式下，从当前行开始，一次向下移动光标10行的操作方法？如何快速移动到文件开始行和结束行？如何快速跳转到文件中的第N行？

向下移动光标10行：10j

移动到文件开始行：1G/gg

移动到文件结束行：G

跳转到文件第N行：NG/Ngg

- Normal模式下，如何删除单个字符、单个单词、从当前光标位置一直删除到行尾、单行、当前行开始向下数N行？

除单个字符：x

删除单个单词：dw

从光标位置一直删除到行尾：d$

删除单行：dd

删除当前行开始向下数N行：Ndd

- 如何在vim中快速插入N个空行？如何在vim中快速输入80个-？

插入N个空行：

向下插入：No

向上插入：NO ESC

输入80个-： 80i/a- ESC

- 如何撤销最近一次编辑操作？如何重做最近一次被撤销的操作？

撤销最近一次编辑操作：u

重做最近一次倍撤销的操作：Ctrl+R

- vim中如何实现剪切粘贴单个字符？单个单词？单行？如何实现相似的复制粘贴操作呢？

剪切粘贴单个字符：x，p

剪切粘贴单个单词：dw，p

剪切粘贴单行:d$/D,p

实现相似的复制粘贴操作：v进入可视模式,移动对文本进行选中,y复制,p粘贴

- 为了编辑一段文本你能想到哪几种操作方式（按键序列）？

a键在光标后插入内容，A在行尾插入内容

ce删除单词/行以更改内容

dd、dw删除行/单词/光标到行末

G移动至文件尾，gg移动至文件首，Ctrl+G查看行号，<行号>+shift+G跳转行号

i键进入插入模式

O键在光标上方打开新的一行进入插入模式，o键在光标下方打开新的一行进入插入模式

r替换文字

u撤销操作，U恢复某行原始状态，Ctrl+R撤销刚才的撤销操作

v进入可视模式，y复制，p粘贴

x删除文字

/<word> + n键 可查找单词

- 查看当前正在编辑的文件名的方法？查看当前光标所在行的行号的方法?

Ctrl+G

- 在文件中进行关键词搜索你会哪些方法？如何设置忽略大小写的情况下进行匹配搜索？

关键词搜索：

\word 用n向后搜索，N向前搜索

?word 用n向前搜索，N向后搜索

设置忽略大小写的情况下进行匹配搜索：

:set ic


- 如何将匹配的搜索结果进行高亮显示？如何对匹配到的关键词进行批量替换？

将匹配的搜索结果进行高亮显示：

:set hls

对匹配到的关键词进行批量替换：

:s/old/new在一行内替换头一个字符串 old 为新的字符串 new

:s/old/new/g 在一行内替换所有的字符串 old 为新的字符串 new

:#,#s/old/new/g替换两行之间的关键词

:%s/old/new/g在文件内替换所有的字符串 old 为新的字符串 new

:%s/old/new/gc进行全文替换时询问用户确认每个替换

- 在文件中最近编辑过的位置来回快速跳转的方法？

Ctrl+O向前跳转

Ctrl+I向后跳转

- 如何把光标定位到各种括号的匹配项？例如：找到(, [, or {对应匹配的),], or }

光标位于(,[,{时，键入%，再按%可跳回

- 在不退出vim的情况下执行一个外部程序的方法？

:!<command>

- 如何使用vim的内置帮助系统来查询一个内置默认快捷键的使用方法？如何在两个不同的分屏窗口中移动光标？

查询一个内置默认快捷键的使用方法：

:help <shortcut>查询normal模式下的快捷键

:help i_<shortcut>查询insert模式下的快捷键

:help c_<shortcut>查询command-line模式下的快捷键

:help v_<shortcut>查询Visual模式下的快捷键

在两个不同的分屏窗口中移动光标：(Ctrl+W)+W


