# sublime3 包管理工具的安装
1. 下载sublime3;(https://pan.baidu.com/s/1synTkEr8FQkQEBy3hxaVsw) 
2. 复制package control文件到perferences>Browse package目录下;复制channel_v3.json文件到一个不会随意删除的地方;修改package control setting-Default下的channels地址为channel_v3.json的绝对地址;
3. 重启sublime;
4. 或者直接下载破解版:https://pan.baidu.com/s/19uIpaQ9XemT997SFClJcvg

# stylus安装
1. node.js安装
        百度node.js下载安装
2. Stylus安装
        全局安装，安装之前你需要进行第一步安装 nodejs，然后打开cmd 输入"npm install stylus -g"。（如果出现windows_NT 6.1.7601...则先输入npm config set strict-ssl false和npm config set registry http://registry.cnpmjs.org （镜像，中国））。这样就算是安装完Stylus了，也可以正常使用Stylus。
3. 打开subline
        ctrl+shift+p调出控制台，然后输入"install package"回车（如果没有下载包管理工具Package Control则下载：http://pan.baidu.com/s/1hrp0anM 放到sublime3（在sublime的preference-Brows package）下的install packages目录下），再弹出的窗口中输入"stylus"然后回车安装，安装成功后在view中的Syntax可以选择stylus模式。
        
# 配置sublime php环境

  stp1: sublime安装sublimeLiner修改user-seting;

  stp2: 新建编译系统修改默认文件并改名php-sublime-build保存默认目录；

  stp3: 配置php环境变量高级系统设置-环境变量-编辑系统变量-新建把php.exe的目录填入；[可参阅](https://www.cnblogs.com/cisum/p/7999443.html)
        
# 使用github桌面版向github上传代码
### 在远程的git服务器上创建一个代码库
点击repositiories选在那个卡，右侧的new按钮，输入该代码库的基本信息，完成创建
### 将其克隆到本地
1. 在git shell命令行中使用git clone “代码仓库的地址（代码仓库url.git）”克隆至本地，默认是在命令行当前所在的文件夹中
### 作为npm项目的初始化
1. cd进入当前项目，然后在cmd命令行中使用npm init，很具体是步骤一步一步完成package.json的创建。其中git repository选项的值就应当为当前项目的git仓库地址
### 创建node_modules文件夹
后续通过npm install的依赖将会自动安装到这个文件夹中
### 配置产品环境以及开发环境的文件架构
### 创建并编辑.gitignore文件
忽略一些不必要提交到代码仓库中的开发者代码等，比如*node_modules*文件夹及开发者文件夹*develop*是不需要提交到代码仓库中的，则可以将这两个文件夹名称分别添加至*.gitignore*中
### 安装并使用构建工具gulp
1. `npm install gulp --save-dev`通过npm安装gulp工具，并添加为开发环境的依赖
2. 创建gulpfile.js文件到项目根目录，编辑图片压缩，js压缩及stylus编译及压缩和监听文件变化任务
3. `npm install 开发模块 --save-dev`安装gulpfile.js中所需要的开发模块的依赖
4. `npm install gulp -g`全局安装gulp使之成为一个被cmd执行的软件
5. cmd执行gulp
### 将本地初始化好的整个项目通过git推送至远程代码仓库
1. 打开git shell
2. `get pull`将远程代码仓库中修改的内容同步拉去至本地仓库
3. `git add *`经项目中所有未被。gitignore的文件添加至即将上传至本地仓库的缓冲区
4. `git status`查看即将被上传的文件
5. (\*)"git reset"如果发现"git add "操作有误，可以使用侧命令
6. `git commit -m "注释"`提交代码至本地并且必须书写注释
7. `git push`提交代码到远程仓库

# 搭建自己的网站(阿里云服务器)

	一. 购买阿里云服务器,一般双十一前后会有打折优惠
	
	  购买完成之后回有一个提货券,配置信息的时候最好选择华东1(杭州)地区,服务器操作系统最好是CentOS.(http://www.aliyun.com/act/aliyun/campus.html?spm=a2c4e.11153940.0.0.3f5d5a6dKxKwc6)
	
	二. 购买域名并备案(不备案是访问不了的。备案需要时间早点备着，然后去搭建环境)
	
	  1. 去万网挑选购买自己喜欢的域名(http://wanwang.aliyun.com/?spm=a2c4e.11153940.0.0.3f5d5a6dQ9HhNx)
	    购买之后一定要去实名认证一下
		
	  2. 域名申请备案
	    stp1: 申请备案服务号,购买阿里云服务器可以申请5个服务号
		登录阿里云-备案-备案服务号申请-申请-查看(查看备案服务号并保存,后面备案的时候会用到);
	    stp2: 登录备案系统进行备案(https://yq.aliyun.com/go/articleRenderRedirect?spm=a2c4e.11153940.0.0.3f5d5a6dQ9HhNx&url=https%3A%2F%2Fbeian.gein.cn%2Faccount%2Flogin.htm%3Fcallback%3Dhttp%3A%2F%2Faliyun.gein.cn)
		个人网站备案信息都写自己就好;(如果出现域名信息与你实名认证的信息不对照无法备案,有可能是你的实名信息还没传到后台服务器,需等个两天左右)填好基本信息之后,最后选择已有备案号申请,复制备案号提交申请就好;如果没什么问题初审很快就能过(一天左右),如果有问题会打电话,注意电话畅通;初审通过之后会提交通信管理局,这个过程说是要十几二十天;
		  
	三. 安装软件
	
		1. 下载'Linux一键安装web环境'安装包备用;下载Xshell和Xftp并安装。(https://pan.baidu.com/s/1e-kS6lZufWvLxh1IcWyhlw)
		
		2. 打开Xshell链接服务器
		  a. 弹出一个会话框;新建会话,名称写网站的名字,主机写购买的阿里云公网ip(点击服务器实例里边有ip地址);
		  b. 点击确定后,接受保存主机密匙,然后输入登录名必须是'root';
		  c. 确定之后会有'SSH用户身份验证'在这里生成密匙;记得一定要把公匙复制保存,然后去阿里云导入生成的公匙;
		  d. 打开 云服务ECS-网络与安全-密匙对-创建密匙对-导入已有密匙对(把复制的公匙放进去保存)-确定;然后再去绑定密匙对 绑定密匙对-找到ECS实例导入到'已选择'-确定(可以重启一下服务器);
		  e. 再去到Xshell填写SSH身份验证的密码然后确定就可以连上服务器了;
		  f. 文件-当前会话属性的连接-重新连接设为30s;终端-编码为utf-8避免乱码;
		  
		3. web环境的安装和选择
		  a. 打开Xftp找到下载的Linux一键安装web环境安装包sh-1.5.5然后拖到右侧等待完成;然后打开Xshell输入ll查看是否导入好;
		  b. 依次输入:'chmod -R 777 sh-1.5.5','cd sh-1.5.5/','./install.sh';
		     然后进入web服务器选择:1.'web'一定选择Apache;  2.'apache'选择最新版本即可;  3.'php'选择5.5.7;  4.'mysql'一定选择5.5.40其他有毛病;
		  c. 安装完之后可以'复制会话'在另外一个窗口输入top命令查看服务器情况;在原先会话输入netstat -tunpl可以查看运行的服务和端口号;
		  
		4. 修改ftp和mysql的密码
		   a. 输入 cat account.log 可以查看ftp和mysql的用户名和密码;
		   b. 输入 passwd www 命令修改ftp的密码;
		   c. 输入 mysqladmin -uroot -p旧密码 password 新密码 修改mysql的密码(-p与旧密码间没有空格);
		
	
	
	


