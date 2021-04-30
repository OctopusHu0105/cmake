第一部分：
Makefile 里主要包含了五个东西:显式规则、隐晦规则、变量定义、文件指示和注释。
1. 显式规则说明了,如何生成一个或多的的目标文件。
2. 由于我们的 make 有自动推导的功能,所以隐晦的规则可以让我们比较粗糙地简略地书写 Makefile,这是由 make 所支持的。
3. 在 Makefile 中我们要定义一系列的变量,变量一般都是字符串,这个有点你 C 语言中的宏,当 Makefile 被执行时,其中的变量都会被扩展到相应的引用位置上。
4. 文件指示。其包括了三个部分,一个是在一个 Makefile 中引用另一个 Makefile,就像 C 语言中的include 一样;另一个是指根据某些情况指定 Makefile 中的有效部分,就像 C 语言中的预编译#if 一样;还有就是定义一个多行的命令。
5. 注释是用“#”字符。

### 引用其它的 Makefile

include foo.make *.mk $(bar)
等价于:
include foo.make a.mk b.mk c.mk e.mk f.mk


## make 寻找的目录

1. [200~如果 make 执行时,有“-I”或“--include-dir”参数,那么 make 就会在这个参数所指定的目录下去寻找。
2. 如果目录<prefix>/include(一般是:/usr/local/bin 或/usr/include)存在的话, make 也会去找

## make 的基本工作步骤

1、读入所有的 Makefile。
2、读入被 include 的其它 Makefile。
3、初始化文件中的变量。
4、推导隐晦规则,并分析所有规则。
5、为所有的目标文件创建依赖关系链。
6、根据依赖关系,决定哪些目标要重新生成。
7、执行生成命令。

### 书写规则

targets : prerequisites
command

targets 是文件名,以空格分开,可以使用通配符。一般来说,我们的目标基本上是一个文件,但也有可能是多个文件。
command 是命令行,如果其不与“target:prerequisites”在一行,那么,必须以[Tab键]开头,如果和 prerequisites 在一行,那么可以用分号做为分隔。






