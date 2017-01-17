# linux环境变量配置
### 1. /etc/profile 
此文件中增加环境变量时即使执行了source /etc/profile也只能在当前的会话中有用，重新连接或重新开机又需要重新执行
```
    vim /etc/profile
    source /etc/profile
```
### 2. ~/.bashrc
此文件中指定了设置全局变量文件的位置,可以修改来改变
，在该指定文件中添加就可以实现解决每次1.中都要输入source的问题
```
# .bashrc

# User specific aliases and functions

alias rm='rm -i'
alias cp='cp -i'
alias mv='mv -i'

# Source global definitions
if [ -f /etc/profile ]; then
	. /etc/bashrc # 这里指定了环境变量文件的位置
fi
```


###网上参考摘录
环境变量设置方法：
1. /etc/profile:在登录时,操作系统定制用户环境时使用的第一个文件,此 文件为系统的每个用户设置环境信息,当用户第一次登录时,该文件被执行。
2. /etc/environment:在登录时操作系统使用的第二个文件,系统在 读取你自己的profile前,设置环境文件的环境变量。
3. ~/.bash_profile:在登录时用到的第三个文件是.profile文 件,每个用户都可使用该文件输入专用于自己使用的shell信息,当用 户登录时,该 文件仅仅执行一次!默认情况下,他设置一些环境变游戏量,执 行用户的.bashrc文件。/etc/bashrc:为每一个运行bash shell的用户执行此文件.当bash shell被打开时,该 文件被读取.
4. ~/.bashrc:该文件包含专用于你的bash shell的bash信 息,当登录时以及每次打开新的shell时,该该文件被读取。
几个环境变量的优先级1>2>3

设置永久环境变量

1. 环境变量配置中，要先删除.bash_profile中的三行关于.bashrc的 定义，然后把环境变量配置在.bashrc中
2. 选择要使用的java环境：update-alternatives –config java
3. 要使得刚修改的环境变量生效：source .bashrc
4. 查看环境变量：env

可以放到/etc/bashrc，这样就是系统级的
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
