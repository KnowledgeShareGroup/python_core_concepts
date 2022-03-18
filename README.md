# python_core_concepts
important concepts and notations in language python

## 1.参考书籍
- [1] [Think Python](https://greenteapress.com/wp/think-python-2e/)

## 2.Tips
### 1.多线程的优点
1. 使用线程可以把占据长时间的程序中的任务放到后台去处理。
2. 程序的运行速度可能加快
3. 在一些等待的任务实现如，<用户输入><文件读写><网络收发数据>
### 3.构成：
* 每个独立的线程都有一个程序运行的入口，顺序执行序列和程序的出口
*（线程无法独立执行，必须依存在应用程序中（此处看线程和进程之间的关系），由应用程序提供多个线程执行控制）
* 每个线程都有他自己的一组CPU寄存器，称为线程的上下文，这反映了线程上次运行该线程的CPU寄存器状态
* 指令指针和堆栈指针寄存器是线程上下文最重要的两个寄存器，这些地址都用于标志
拥有线程的进程地址空间中的内存。
### 4.python的命名
1 虚数不能单独存在，它们总是和一个值为 0.0 的实数部分一起来构成一个复数。
2复数由实数部分和虚数部分构成
3表示虚数的语法： real+imagj
4 实数部分和虚数部分都是浮点数
5 虚数部分必须有后缀 j 或 J
### 5.python中主要存在四种命名方式：
- [1].object #公用方法
- [2]._object #半保护被看作是“protect”，意思是只有类对象和子类对象自己能访问到这些变量，在模块或类外不可以使用，不能用’from module import *’导入。
- [3].__object 是为了避免与子类的方法名称冲突， 对于该标识符描述的方法，父类的方法不能轻易地被子类的方法覆盖，他们的名字实际上是_classname__methodname。
__object  #全私有，全保护
私有成员“private”，意思是只有类对象自己能访问，连子类对象也不能访问到这个数据，不能用’from module import *’导入。
- [4].__object__内建方法，用户不要这样定义
