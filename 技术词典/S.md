## Symbol Link ##
### 符号链接 ###
*nix 系统的文件连接可分为硬连接(Hard Link)和软连接(Symbol Link)，其中硬链接和原文件名共享一个文件编号(Inode Index)。硬连接的作用是允许一个文件有多个有效路径，这样可以防止误删，删除一个连接并不影响文件本身及其它连接。只有当最后一个连接被删除时，文件才会被释放。

软连接则类似于快捷方式，其文件编号与原文件不同，实际上是一个文本文件，其中包含所指向文件的位置信息。

建立硬连接命令：`ln file1 f2`  
建立软连接命令：`ln -s file1 file2`

软连接常用于设置环境变量，尤其是当安装有不同的程序版本时，如JDK，Maven等。  

参考：http://www.cnblogs.com/itech/archive/2009/04/10/1433052.html  

## Static Import ##
### 静态导入 ###
JDK1.5引入的新特性，即导入静态的方法和变量。作用是使导入的静态类对当前类直接可见，无需给出类名即可调用方法。经常用于单元测试中导入测试框架的Assert方法。  

`import static org.junit.Assert.*;'`  

参考：http://www.cnblogs.com/mengdd/archive/2013/01/23/2873312.html