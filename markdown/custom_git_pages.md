###Setting up your GitHub Pages site locally with Jekyll

####一.环境准备

1. 首先确定 ruby 环境，如果没有，自行安装
	```bash
	ruby --version
	```

2. 安装 bundler 

	```bash
	// 优先使用
	sudo gem install bundler
	// 如果 mac 系统版本过高，会报错，那就需要下面的命令来安装 bundler
	sudo gem install -n /usr/local/bin bundler
	```

####二.创建对应的 git 仓库

1. 要有一个可用的 git，如果没有自行安装
2. 打开 Terminal
3. 创建对应的代码仓库
	```bash
	git init my-project
	cd my-project
	```
4. 进入对应的目录下，并切换到分支 gh-pages
	```bash
	git checkout -b gh-pages
	```
	
####三.Install Jekyll using Bundler

1. 创建 Gemfile

	创建一个名为 Gemfile 的文件，并写入下面的内容
	
	```bash
	# source 'https://ruby.taobao.org'
	# 因为万能的墙，如果不翻墙的话需要换成淘宝的镜像
	source 'https://ruby.taobao.org'
gem 'github-pages', group: :jekyll_plugins
	```
2. Install Jekyll and other dependencies from the GitHub Pages gem:
	
	```bash
	$ bundle install
	Fetching gem metadata from https://rubygems.org/............
	Fetching version metadata from https://rubygems.org/...
	Fetching dependency metadata from https://rubygems.org/..
	Resolving dependencies...
	...
	
	# 如果你的mac 系统版本过高，需要使用下面的命令来安装
	bundle install --path /usr/local/bin
	
	```

####四.Generate Jekyll site files

1. 如果你本地没有 Jekyll 站点，可通过下面的命令创建
	
	```bash
	$ bundle exec jekyll new . --force
	New jekyll site installed in /Users/octocat/my-site.
	```
	
####五. Build your local Jekyll site

1. Navigate into the root directory of your local Jekyll site repository.
Run your Jekyll site locally:

```bash
bundle exec jekyll serve
Configuration file: /Users/octocat/my-site/_config.yml
           Source: /Users/octocat/my-site
      Destination: /Users/octocat/my-site/_site
Incremental build: disabled. Enable with --incremental
     Generating...
                   done in 0.309 seconds.
Auto-regeneration: enabled for '/Users/octocat/my-site'
Configuration file: /Users/octocat/my-site/_config.yml
   Server address: http://127.0.0.1:4000/
```
Server running... press ctrl-c to stop.
Preview your local Jekyll site in your web browser at [http://localhost:4000](http://localhost:4000).

####Keeping your site up to date with the GitHub Pages gem
Jekyll is an active open source project and is updated frequently. As the GitHub Pages server is updated, the software on your computer may become out of date, resulting in your site appearing different locally from how it looks when published on GitHub.

1. Open Terminal.

2. Run this update command:

If you followed our setup recommendations and installed Bundler, run ```bundle update github-pages``` or simply ```bundle update``` and all your gems will update to the latest versions.
If you don't have Bundler installed, run ```gem update github-pages```

