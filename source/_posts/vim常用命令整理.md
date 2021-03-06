---
title: vim常用命令整理
abbrlink: 51495
date: 2020-01-20 22:59:58
tags: 工具
categories: 技术
---

&emsp;&emsp;Vim是一个强大的文本编辑工具，然而刚开始使用的体验是极其痛苦的，因为各种命令实在太多，而且各种命令按键乍看之下完全没有规律，对于以往的输入方式，完全没有借鉴之处。这个体验让我想起了五笔输入法，使用体验是类似的，慢慢练习熟练之后就会大幅提高效率。

![vim keyboard](https://images20200326.oss-cn-hangzhou.aliyuncs.com/blog/vim-keyboard.png)

&emsp;&emsp;既然决定要开始学习Vim，那就开始定制学习计划。Vim命令那么多，想要一次性掌握几乎是不可能的，根据&lt;u&gt;**二八法则**&lt;/u&gt;，先掌握20%的命令就可以解决80%需求，按照这样的思路，我做出了以下的安排：

&emsp;&emsp;首先要先知道Vim有三种工作模式：`普通模式`、`插入模式`、`命令模式`。
- 普通模式进入插入模式，按下字母`i`
- 插入模式进入普通模式，按下`Esc`键
- 普通模式进入命令模式，先输入冒号`:`，然后输入相应的命令以回车结束

&emsp;&emsp;接下来就是先记忆常用的命令，别一眼看着好像也不少，但是是有规律的，移动类的是基础中的基础，如果掌握了，后面的命令记忆起来会非常快：
```bash
# 移动（普通模式）
h：向左
j：向下
k：向上
l：向右
8l： 向右移动 8 个字符

0：到行首
^：到行首第一个非空字符
$：到行尾
gg：到文件头
G：到文件尾
22G：跳转到第 22 行

Ctrl+F: 到上页
Ctrl+B: 到下页
```

```bash
# 复制（普通模式）
yy：复制一行
8yy：向下复制8行
# 字母y搭配移动命令
y0：复制到行首
y^：复制到行首第一个非空字符
y$：复制到行尾
```

```bash
# 剪切（普通模式）
x：向后剪切1个字符，如果是在行尾，则为向前剪切
8x：剪切8个字符
```

```bash
# 删除（普通模式）- 删除的内容会保存到粘贴板，可以配合下面的粘贴命令使用
dd：删除一行
100dd：删除100行
# 字母d搭配移动命令
d0：复制到行首
d^：复制到行首第一个非空字符
d$：复制到行尾
```

```bash
# 粘贴（普通模式）- 对应上面三种类型操作的粘贴功能，外部粘贴板的内容不识别
p：粘贴保存在粘贴板的内容
8p：将粘贴板的内容粘贴8次
```

```bash
# 撤销（普通模式）
u：撤销1次
3u：撤销3次
U：撤销当前行的所有修改
Ctrl+r：恢复到撤销前
```

```bash
# 查找（普通模式）- 按下/直接进入查找，输入相应的字符串按确定即可
n：查找下1个匹配
N：查找上1个匹配
3n：查找下面第3个匹配

```

```bash
# 退出（命令模式）- 普通模式进入命令模式，先输入冒号：
q： 不保存退出
q!： 不保存，强制退出
wq：保存当前文件并退出
```

```bash
# 排版（命令模式）
ce： 本行内容居中 #center单词简写
le： 本行内容居左 #left单词简写
ri： 本行内容居右 #right单词简写
```

&emsp;&emsp;我认为的基本常用命令就这些，别看上去好像也不少，但是很多都是类似的，只是组合了以下，实际精简一下也就10来种类型的命令。相信这些命令足以解决初学者绝大部分情况下的需求。
&emsp;&emsp;如果以上命令已经觉得烂熟于心了，那么就可以参照下面的这张总结图进行更全面的拓展了：

![vim command](https://images20200326.oss-cn-hangzhou.aliyuncs.com/blog/vim-command.png)