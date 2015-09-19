
首先登录到https://github.com注册Github帐号，并且创建一个repository。

例如：注册的github帐号名为rombaby，创建的repository名称为TWRP_recovery_2870_baby，那么你的仓库名为rombaby在github上的地址为：

https://github.com/rombaby/TWRP_recovery_2870_baby.git

2、安装git 

sudo apt-get install git

3、生成ssh-key的私钥和公钥，注意保存。

ssh-keygen -t rsa      

//一路回车下来

注：Windows下使用git bash操作命令行。

4、 测试是否连接上github服务器

ssh -T git@github.com

这时一般会输出：

.........

Permission denied (publickey).

解决办法：将上面生成的public key(id_rsa.pub文件)拷贝到github服务器的SSH Keys中，具体操作，

登录后，点击右上角的Account settings——> SSH Keys。

5、将项目代码文件夹上传到github你的仓库内

1）在你的代码目录下执行以下命令：

git init

git add *

git commit -m 'Initial commit project'

git remote add origin https://github.com/rombaby/TWRP_recovery_2870_baby.git

git push origin master 

（如果没有配置用户名和邮箱，那么需要执行以下命令：

git config --global user.name "XXX"

git config --global user.email "XXX@XXX.com" ）

如果你的仓库中已经含有文件，那么执行这句会提示提交失败，用户需要先执行git pull命令

git pull origin master

ok，再次执行git push origin master，成功，到github网上擦看自己的仓库，发现项目已经提交上去了。

2）如果仅仅是clone仓库的代码，可以执行如下命令：

git clone https://github.com/rombaby/TWRP_recovery_2870_baby.git

