---
title: node.js 版本控制 nvm 和 n 使用 及 nvm 重启终端失效的解决方法
---


nvm 重启后终端 node ,npm 失效的解决方案

如果你使用了上面的 brew 的安装方法 当安装成功后,请按照如下操作设置你的 shell 配置文件

```bash
brew info nvm
```







你会看到下面的输出帮助信息

```bash
nvm: stable 0.26.1 (bottled), HEAD
Manage multiple Node.js versions
https://github.com/creationix/nvm
/usr/local/Cellar/nvm/0.26.1 (3173 files, 56M) *
  Poured from bottle
From: https://github.com/Homebrew/homebrew/blob/master/Library/Formula/nvm.rb
==> Caveats
Add NVM's working directory to your $HOME path (if it doesn't exist):

  mkdir ~/.nvm

Copy nvm-exec to NVM's working directory

  cp $(brew --prefix nvm)/nvm-exec ~/.nvm/

Add the following to $HOME/.bashrc, $HOME/.zshrc, or your shell's
equivalent configuration file:

  export NVM_DIR=~/.nvm
  source $(brew --prefix nvm)/nvm.sh

Type `nvm help` for further information.

Bash completion has been installed to:
  /usr/local/etc/bash_completion.d
```




我们需要按照上面提供的方法,首先在用户更目录下 创建 .nvm 文件

```bash
mkdir ~/.nvm
```

然后把 nvm-exec 文件拷贝到你刚才新建的 .nvm 目录下 ```cp $(brew --prefix nvm)/nvm-exec ~/.nvm/```

然后去编辑你的 bash 配置文件 $HOME/.bashrc ,如果你 使用 zsh 那么编辑 $HOME/.zshrc 配置文件 nano ~/.bashrc 或

```bash
nano ~/.zshrc
```
把下面的内容粘贴进去

```bash
export NVM_DIR=~/.nvm
source $(brew --prefix nvm)/nvm.sh
```

最后让你的 shell 配置及时生效 ```source ~/.bashrc``` 或 ```source ~/.zshrc```

最后你就不会再出现关闭终端重启,或者重启机器发现 node ,npm 等系统环境变量失效的问题了.


[参考的链接](http://yijiebuyi.com/blog/b1328ffe88cdde6b4102894635cf8f11.html)
