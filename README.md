# 使用github桌面版向github上传代码
## 在远程的git服务器上创建一个代码库
点击repositiories选在那个卡，右侧的new按钮，输入该代码库的基本信息，完成创建
## 将其克隆到本地
1. 在git shell命令行中使用git clone “代码仓库的地址（代码仓库url.git）”克隆至本地，默认是在命令行当前所在的文件夹中

## 作为npm项目的初始化
1. cd进入当前项目，然后在cmd命令行中使用npm init，很具体是步骤一步一步完成package.json的创建。其中git repository选项的值就应当为当前项目的git仓库地址

## 创建node_modules文件夹

后续通过npm install的依赖将会自动安装到这个文件夹中

## 配置产品环境以及开发环境的文件架构

## 创建并编辑.gitignore文件

忽略一些不必要提交到代码仓库中的开发者代码等，比如*node_modules*文件夹及开发者文件夹*develop*是不需要提交到代码仓库中的，则可以将这两个文件夹名称分别添加至*.gitignore*中

## 安装并使用构建工具gulp

1. `npm install gulp --save-dev`通过npm安装gulp工具，并添加为开发环境的依赖
2. 创建gulpfile.js文件到项目根目录，编辑图片压缩，js压缩及stylus编译及压缩和监听文件变化任务
3. `npm install 开发模块 --save-dev`安装gulpfile.js中所需要的开发模块的依赖
4. `npm install gulp -g`全局安装gulp使之成为一个被cmd执行的软件
5. cmd执行gulp

## 将本地初始化好的整个项目通过git推送至远程代码仓库

1. 打开git shell
2. `get pull`将远程代码仓库中修改的内容同步拉去至本地仓库
3. `git add *`经项目中所有未被。gitignore的文件添加至即将上传至本地仓库的缓冲区
4. `git status`查看即将被上传的文件
5. (\*)"git reset"如果发现"git add "操作有误，可以使用侧命令
6. `git commit -m "注释"`提交代码至本地并且必须书写注释
7. `git push`提交代码到远程仓库


# stylus安装
1. node.js安装
        百度node.js下载安装
2. Stylus安装
        全局安装，安装之前你需要进行第一步安装 nodejs，然后打开cmd 输入"npm install stylus -g"。（如果出现windows_NT 6.1.7601...则先输入npm config set strict-ssl false和npm config set registry http://registry.cnpmjs.org （镜像，中国））。这样就算是安装完Stylus了，也可以正常使用Stylus。
3. 打开subline
        ctrl+shift+p调出控制台，然后输入"install package"回车（如果没有下载包管理工具Package Control则下载：http://pan.baidu.com/s/1hrp0anM 放到sublime3（在sublime的preference-Brows package）下的install packages目录下），再弹出的窗口中输入"stylus"然后回车安装，安装成功后在view中的Syntax可以选择stylus模式。
        
# sublime3 包管理工具的安装；
1,下载sublime3;
2,复制package control文件到perferences>Browse package目录下;复制channel_v3.json文件到一个不会随意删除的地方;修改package control setting-Default下的channels地址为channel_v3.json的绝对地址;
3,重启sublime；就可以安装各种插件了
