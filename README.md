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

2. 使用Git进行代码版本控制  

        $ mkdir printer  
        $ cd printer/  
        $ git init  
        $ touch A.java  
        $ git add A.java  
        $ git commit -m 'first commit'  
        $ git remote add origin git@github.com:GitHub用户名/printer.git  
        $ git push origin master  

3. 处理其他开发者的代码合并请求

    当有其他开发者提起合并请求时，GitHub网页及个人邮件中都会收到消息。
    * 可以直接在网页中点击"Merge pull request"进行合并  
    * 可以通过获得将请求者repository的url进行代码合并  
      1) 打开个人邮件，取得url  
      2) 本地进行代码合并：`git pull https://github.com/zhyl/Tutorials master`  
      3) 推送至GitHub：`git push origin master`  
    * 可以通过补丁包的方式进行代码合并  
      1) 打开个人邮件，取得补丁包url  
      2) 本地进行代码合并：`curl -k https://github.com/zhyl/Tutorials/pull/2.patch | git am`  
      3) 推送至GitHub：`git push origin master`  

**六、参与其他人的Repository**

1. 找到自己希望参与的repository，点击页面右上角的"Fork"按钮，此repository即已派生到自己的账户名下，并且可以在此基础上进行开发。

2. 如果希望将自己的修改合并到原作者的代码库，点击"Pull Request"，即可向原作者发送合并请求，原作者在收到请求后自行决定如何处理。

3. 当原作者修改了代码，我们希望将修改内容合并到自己的repository中时，可以进行如下操作：
    * 创建原始repository别名，方便跟踪：`git remote add upstream git://github.com/zyl54586/Tutorials.git`
    * 获取原始代码：`git fetch upstream`
    * 合并到自己的repository：`git merge upstream/master`

**七、常见问题（FAQ）**

1. 如何修改repository路径别名？
    * 直接：`git remote set-url origin git@github.com:username/reponame.git`
    * 或者：  
     `$ git remote rm origin`  
     `$ git remote add origin git@github.com:username/reponame.git`
