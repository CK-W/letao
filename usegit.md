##使用git与github同步实现更新

##git的一般使用命令
    *1、git init -- 初始化git的仓库 
     2、git add . -- 把文件夹里面的文件临时添加到git仓库里
     3、git status -- 验证是否添加成功
     4、git commit -m "提交日志" -- 把文件确实的保存在git仓库中
     5、git log -- 查看当前提交了的所有信息，包括版本号等等



##使用SSH实现无密码提交到github上的方式
    1、在命令框输入 ssh-keygen -t rsa 一直回车 直到出现2408
    2、 找到生成的密钥
    C盘 》 用户 》 .ssh文件夹 》 打开id_rsa.pub 》复制里面的内容
    3、打开github用户设置 点击 左侧SSH and GPG keys
    4、点击右上角的new SSH key
    输入title 标题随便输入
    输入key  pub里面复制的乱码
    点击add key按钮
    5、创建一个项目
     git init
     git add .
     git commit -m '提交日志'
     指定远端地址注意远端地址要指定ssh地址
     git remote add origin git@github.com:zwxs/letao9.git
     git push -u origin master

     <!-- 这是第一次创建文件时的做法 -->

     <!-- 如果以后在本地更新自己的代码，可以使用以下方法 -->
## 修改了文件之后
1、在控制台里面输入 git add . 临时保存文件
2、git commit -m "提交日志"  永久保存文件
3、$ git push origin master  同步GitHub;
