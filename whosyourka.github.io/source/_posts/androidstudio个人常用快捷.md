---
title: android studio个人常用快捷
date: 2019-01-23 17:09:37
tags: android studio
categories: android studio
---

## 我的快捷（[参考](https://note.youdao.com/),[翻译](https://note.youdao.com/)）：

### IDE

Ctrl(Command)+Alt(Option)+S	打开设置对话框

Ctrl(Command)+Alt(Option)+Shift+S	打开当前项目/模块属性

Alt(Option)+Shift+C	查看文件的变更历史

### 编辑

Ctrl(Command)+C	复制当前行或选中的内容

Ctrl(Command)+D	粘贴当前行或选中的内容

Ctrl(Command)+X	剪切当前行或选中的内容

Ctrl(Command)+Y	删除行

Ctrl(Command)+Z	倒退

Ctrl(Command)+Shift+Z	向前

Alt(Option)+Enter	自动修正

Ctrl(Command)+Alt(Option)+L	格式化代码

Ctrl(Command)+Alt(Option)+I	将选中的代码进行自动缩进编排

Alt(Option)+Insert	得到一些Intention Action，可以生成构造器、Getter、Setter、将 == 改为 equals() 等

Ctrl(Command)+Shift+V	选最近使用的剪贴板内容并插入

Shift+Enter	在当前行的下面插入新行，并移动光标到新行

Ctrl(Command)+J	自动提示特殊代码如fori

Ctrl(Command)+Alt(Option)+T	把选中的代码放在 try{} 、if{} 、 else{} 里

Ctrl(Command)+ /	注释 //

F2/Shift+F2	跳转到下/上一个错误语句处

Ctrl(Command)+Shift+Back	跳转到上次编辑的地方

Ctrl(Command)+Alt(Option)+Space	类名自动完成

Ctrl(Command)+Shift+Up/Down	语句向上/下移动

Ctrl(Command)+Shift+U	大小写切换

Tab	代码标签输入完成后，按 Tab，生成代码

Ctrl(Command)+Backspace	按单词删除

Ctrl(Command)+Shift+Enter	语句完成

Ctrl(Command)+Alt(Option)+J	用动态模板环绕

### 文件

Ctrl(Command)+H	显示类继承结构图

Ctrl(Command)+Q	显示注释文档

Ctrl(Command)+P	方法参数提示

Ctrl(Command)+U	打开当前类的父类或者实现的接口

Alt(Option)+Up/Down	在方法间快速移动定位

Ctrl(Command)+W	选中代码，连续按会有其他效果

Ctrl(Command)+Shift+W	取消选择光标所在词

Ctrl(Command)+ - / +	折叠/展开代码

Ctrl(Command)+Shift+ - / +	折叠/展开全部代码

Ctrl(Command)+Shift+.	折叠/展开当前花括号中的代码

Ctrl(Command)+ ] / [	跳转到代码块结束/开始处

F2 或 Shift+F2	高亮错误或警告快速定位

Ctrl(Command)+Shift+C	复制路径

Ctrl(Command)+Alt(Option)+Shift+C	复制引用，必须选择类名

Ctrl(Command)+G	定位行

### 查找

Ctrl(Command)+F	在当前窗口查找文本

Ctrl(Command)+Shift+F	在指定环境下查找文本

F3	向下查找关键字出现位置

Shift+F3	向上一个关键字出现位置

Ctrl(Command)+R	在当前窗口替换文本

Ctrl(Command)+Shift+R	在指定窗口替换文本

Ctrl(Command)+B	查找变量的来源

Ctrl(Command)+Alt(Option)+B	快速打开光标处的类或方法

Ctrl(Command)+Shift+B	跳转到类或方法实现处

Ctrl(Command)+F7	查询当前元素在当前文件中的引用，然后按 F3 可以选择

Ctrl(Command)+Alt(Option)+F7	选中查询当前元素在工程中的引用

Ctrl(Command)+Alt(Option)+F7	查找某个方法的所有调用地方

### 重构

F6	移动

Ctrl(Command)+Alt(Option)+Shift+T	弹出重构菜单

Shift+F6	重构-重命名

Ctrl(Command)+Alt(Option)+M	提取代码组成方法

Ctrl(Command)+Alt(Option)+C	将变量更改为常量

Ctrl(Command)+Alt(Option)+V	定义变量引用当前对象或者方法的返回值

Ctrl(Command)+Alt(Option)+F	将局部变量更改为类的成员变量

Ctrl(Command)+Alt(Option)+P	将变量更改为方法的参数

### VCS

|Alt(Option)+ ~|

|VCS 操作菜单|

|Ctrl(Command)+K|提交更改|

|Ctrl(Command)+T|更新项目|

|Ctrl(Command)+Alt(Option)+Shift+D|显示变化|

### 其他

快速修复	Alt + Enter

删除光标所在行（选中行）	Ctrl + Y / Ctrl + X

复制光标所在的行（选中行）	Ctrl + D

格式化代码（java、xml）	Ctrl + Alt + L

重命名	Shift + F6

方法参数提示	Ctrl + P

打印输出	sout

快速定位到任意的文件	按两次shift

快速定位方法在哪里被调用	Ctrl + Alt + H

快速定位到当前类报错或警告的地方	F2 或Shift+F2

快速定位到类或方法的定义	Ctrl+B

代码助手，自动补全	Ctrl + Alt +空格：属性名、类名或接口名提示

Ctrl + Shift + 空格	方法提示

Ctrl + Alt + O	删除没用到的包。

搜索或替换	Ctrl + F / Ctrl + R

全局搜索或全局替换	Ctrl + Shift + F 在选中的文件目录里搜索

Ctrl + Shift + R	在选中的文件目录里替换

显示JavaDoc（注释文档）	Ctrl + Q

导入重载方法	Ctrl + O 输入方法名上下方向键选择后回车

生成 get/set方法、构造方法、toString()	alt + insert

撤销	Ctrl+Z

恢复	Ctrl+Shift+Z

注释	同左

回车换行	Ctrl + Alt + Enter

复制类的全局路径（包名加类名）	Ctrl + Shift + Alt + C (右击--> Copy Reference)

大写/小写	Ctrl + Shift + U

回到上一次编辑的位置	Ctrl + Shift + Backspace



### 自定义快捷

alt ` 显示版本(vcs operation popup)

ctrl alt shift ` 和某一个版本比较（compare with...）

ctrl alt ` （Main menu | VCS | Subversion | Compare with Latest Repository Version） 和前一个版本比较

alt ctrl 1 自己注释方法（fix doc comment）

Ctrl + J 动态模板（Main menu | Code | Insert Live Template...）

ctrl alt q 为翻译软件专用（Plug-ins | ECTranslation | Translate）

[工具库](https://github.com/vondear/RxTool)