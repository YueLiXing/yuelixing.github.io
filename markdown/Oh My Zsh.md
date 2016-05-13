---
title: mac 命令行 zsh
---


写在前面
切换命令行模式
```bash
chsh -s
```

```bash
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

git clone git://github.com/altercation/solarized.git
```

找到solarized/osx-terminal.app-colors-solarized，双击 Solarized Dark ansi.terminal 和 Solarized Light ansi.terminal

所谓zsh其实是Shell的一种，Shell是啥具体的就不给大家讲了，因为我也没往里面研究，因为毕竟我自己用Shell的场景并不多，所以只是稍微了解了一下皮毛。只给大家简单说一下，Shell对于在Linux与Unix平台上的开发者并不陌生，因为全靠它开发者才可以与机器进行交互，它是Linux与Unix的一个外壳，负责外界与其计算机内核进行交互，它接收用户或其他应用程序的命令，然后把这些命令转化成内核能理解的语言，然后传给内核，内核接收指令开始干活，干完活然后把结果返回给用户或者应用程序。

Linux/Unix有多种类型的Shell，比如bash、csh、ksh、zsh等等，你也可以用cat /etc/shells这个命令来看一下你的电脑中存在有几种Shell，至于为啥子有这么多种Shell，怪我咯，每个人习惯不同，然后用的功能或者啥的喜好也不同，这就好比你买房子，即使是一种户型的房子人不还是需要不同的室内设计嘛，一个道理。

zsh说实话真心的比较复杂，各种配置，但是配置出来功能绝对是6的一B，要么很多人都称其为终极Shell，为嘛，因为ABCDEFG…Z是最后一个，所以。。。初期的时候很少有人对它进行使用，由于这个原因，国外大神便对它进行了一系列的简化封装，最终形成了Oh-My-Zsh。

##Oh-My-Zsh

不要以为它只是个命令行，你可以看看他们[官方网站](http://ohmyz.sh)对它的描述，很多人对它报以非常高的评价，算了废话不多说，直接上干货吧。如何安装Oh-My-Zsh呢？

##安装Oh-My-Zsh

先将其[gitHub上的地址](https://github.com/robbyrussell/oh-my-zsh)发出来给大家参考。

其实说实话，gitHub上的README.markdown已经讲的非常清楚了，我建议大家可以自己看一下然后安装，但是也为了照顾一些想快速上手懒得看英语的同学们，我还是将其再说一下。
安装Oh-My-Zsh需要几个先决条件：

* 必须是基于Unix的操作系统（Mac OS X 或者 Linux）
* Zsh必须要首先安装（要求版本在4.3.9或者更高的），如果你不确定自己的电脑是否已经安装了Zsh，你可以用zsh --version这个命令来确定自己点是否已经安装了zsh。如果没有安装则运行sudo apt-get install zsh，然后在运行zsh --version这个命令，来检查是否安装成功。如果成功则继续。
* 电脑要安装curl或者wget（这个安装自己查）
* 电脑要安装git（这个我觉得开发的应该都会）
接下来就是安装了，你可以选择用curl或者wget。下面是两种方法，

```bash
//curl：
curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh
//wget：
wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O
```

## 使用Oh-My-Zsh

安装完成之后你可以通过编辑~/.zshrc这个文件中的一些参数来设置你的Shell，然后找到下面这一项ZSH_THEME="robbyrussel"，然后修改它的主题

Oh My Zsh 默认自带了一些默认主题，存放在 ~/.oh-my-zsh/themes 目录中。你可以查看这些主题。

而且最重要的是，如果你使用git等管理工具，在你使用终端时你可以清晰的看到自己项目所在的分支。而且我个人用的是Mac上的bash，有时候当cd一个文件时，有可能前几个字母或者啥的相同这时候得了，按Tab不管用了吧，哈哈哈，但是有了这个，就是6啊，效果自己测，我就不上了。


###总结

好了，说了这么多，你们自己试试效果吧。