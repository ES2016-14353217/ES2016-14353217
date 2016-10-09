# Lab1: DOL开发环境配置

## 1.下载文件

 sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz

 sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip

## 2.解压文件

#### 2.1 新建dol的文件夹

​	$ mkdir dol

#### 2.2 将dolethz.zip解压到 dol文件夹中

​	$ unzip dol_ethz.zip -d dol

#### 2.3 解压systemc$

​	$ tar -zxvf systemc-2.3.1.tgz

## 3.编译systemc

#### 3.1 解压后进入systemc-2.3.1的目录下

​	$ cd systemc-2.3.1

#### 3.2 新建一个临时文件夹objdir

​	$ mkdir objdir

#### 3.3 进入该文件夹objdir

​	$ cd objdir

#### 3.4 运行configure

​	$ ../configure CXX=g++ --disable-async-updates

​	运行configure之后的截图如下

![](http://ww4.sinaimg.cn/mw690/a16d1d95gw1f8mibg71g2j20hk0ck0x5.jpg)

#### 3.5 编译$ sudo make install

#### 3.6 记录当前的工作路径(会输出当前所在路径，记下来，待会有用)

​	$ pwd

​	编译完后文件目录如下
![](http://ww3.sinaimg.cn/mw690/a16d1d95gw1f8mibgcn4hj20iz02ht9n.jpg)

## 4.编译dol

#### 4.1 进入刚刚dol的文件夹

4.1 进入刚刚dol的文件夹

​	$ cd ../dol

#### 4.2 修改build_zip.xml文件

​	找到下面这段话，就是指明上面编译的systemc位置在哪里
​	**<property name="systemc.inc" value="YYY/include"/>**
​	**<property name="systemc.lib" value="YYY/lib-linux/libsystemc.a"/>**
​	把YYY改成上页pwd的结果（注意，对于  64位 系统的机器，lib-linux要改成lib-linux64）

#### 4.3 编译$ ant -f build_zip.xml all

​	若成功会显示build successful
![](http://ww4.sinaimg.cn/mw690/a16d1d95gw1f8micjqz9nj20iz0bg42m.jpg)

![](http://ww4.sinaimg.cn/mw690/a16d1d95gw1f8micje27rj20gg0chadr.jpg)

## 5.接着可以试试运行第一个例子

#### 5.1 进入build/bin/mian路径下

​	$ cd build/bin/main

#### 5.2 然后运行第一个例子

​	$ ant -f runexample.xml -Dnumber=1
​	成功结果如图

![](http://ww2.sinaimg.cn/mw690/a16d1d95gw1f8mibhroybj20fn0c0n0u.jpg)