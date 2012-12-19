#GitHub入门指南#

**一、安装Git**  

Windows版下载地址：[Git](http://windows.github.com/)  

Linux版下载地址：[Git](http://git-scm.com/)

**二、注册GitHub用户**  

官方网站：[GitHub](https://github.com)

**三、通过GitHub创建Repository**  

1. 登录GitHub，选择"Create a Repository"  

2. 填写"Repository name"，点击"Create repository"完成创建。

**四、添加用于访问GitHub的公钥**  

1. 生成公钥  

    本地控制台输入`ssh-keygen -t rsa -C "YourEmailAddress"`，根据提示，找到对应的pub文件，获取公钥。  

2. 添加公钥  

    登录Github，进入"Account Settings"界面，选择"SSH Keys"；  

    点击"Add SSH key"，随意填写"Title",并将公钥填入"Key"栏，点击"Add key"，再次经过GitHub网站登录密码确认后，完成公钥添加。  

3. 验证  

    本地控制台输入`ssh git@github.com`，查看是否可以通过GitHub认证。  

**五、使用GitHub创建自己的Repository**  

假如现在GitHub上创建了一个名为printer的repository，我们将本地的文件上传至GitHub。  

1. 配置Git用户  

        $ git config --global user.name "GitHub用户名"  
        $ git config --global user.email you@example.com  

2. 使用Git  

        $ mkdir printer  
        $ cd printer/  
        $ git init  
        $ touch A.java  
        $ git add A.java  
        $ git commit -m 'first commit'  
        $ git remote add origin git@github.com:GitHub用户名/printer.git  
        $ git push origin master  

**六、参与其他人的Repository**

1. 找到自己希望参与的repository，点击页面右上角的"Fork"按钮，此repository即已派生到自己的账户名下，并且可以在此基础上进行开发。

2. 如果希望将自己的修改合并到原作者的代码库，点击"Pull Request"，即可向原作者发送合并请求，原作者将收到请求者的邮件。
    * test

