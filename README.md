# atricfox-vims

> 我的Vim插件管理版本库，采用pathogen进行管理.

---
## 版本库管理
- 需要事先在github建立一个vim插件管理的版本库，使用submodule管理
- 本地初始化版本库，在~/.vim目录下运行：git init
- 建立与远程的版本库连接：git remote add origin  <REMOTE_URL>

---
## 插件安装
在~/.vim目录下执行命令：

	git submodule add 插件的giturl bundle/插件名称
	例如：git submodule add https://github.com/tpope/vim-git.git bundle/vim-git

	然后提交到git版本库即可。

---
## 插件移除
运行命令：

	git rm bundle/插件名称

---
## 插件更新
### 更新全部插件

	cd ~/.vim
	git submodule foreach git pull origin master

### 更新单个插件
进入某个插件文件夹下，git pull origin master

---
## 配置迁移

	git clone http://github.com/username/dotvim.git ~/.vim
	ln -s ~/.vim/vimrc ~/.vimrc
	cd ~/.vim
	git submodule init
	git submodule update

---
## 插件库
- github搜索
- 网站：https://vimawesome.com vim插件搜索引擎，内有大量优质vim插件
