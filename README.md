#GitHub����ָ��#

**һ����װGit**  

Windows�����ص�ַ��[Git](http://windows.github.com/)  

Linux�����ص�ַ��[Git](http://git-scm.com/)

**����ע��GitHub�û�**  

�ٷ���վ��[GitHub](https://github.com)

**����ͨ��GitHub����Repository**  

1. ��¼GitHub��ѡ��"Create a Repository"  

2. ��д"Repository name"�����"Create repository"��ɴ�����

**�ġ�������ڷ���GitHub�Ĺ�Կ**  

1. ���ɹ�Կ  

    ���ؿ���̨����`ssh-keygen -t rsa -C "YourEmailAddress"`��������ʾ���ҵ���Ӧ��pub�ļ�����ȡ��Կ��  

2. ��ӹ�Կ  

    ��¼Github������"Account Settings"���棬ѡ��"SSH Keys"��  

    ���"Add SSH key"��������д"Title",������Կ����"Key"�������"Add key"���ٴξ���GitHub��վ��¼����ȷ�Ϻ���ɹ�Կ��ӡ�  

3. ��֤  

    ���ؿ���̨����`ssh git@github.com`���鿴�Ƿ����ͨ��GitHub��֤��  

**�塢ʹ��GitHub�����Լ���Repository**  

��������GitHub�ϴ�����һ����Ϊprinter��repository�����ǽ����ص��ļ��ϴ���GitHub��  

1. ����Git�û�  

        $ git config --global user.name "GitHub�û���"  
        $ git config --global user.email you@example.com  

2. ʹ��Git  

        $ mkdir printer  
        $ cd printer/  
        $ git init  
        $ touch A.java  
        $ git add A.java  
        $ git commit -m 'first commit'  
        $ git remote add origin git@github.com:GitHub�û���/printer.git  
        $ git push origin master  

**�������������˵�Repository**

1. �ҵ��Լ�ϣ�������repository�����ҳ�����Ͻǵ�"Fork"��ť����repository�����������Լ����˻����£����ҿ����ڴ˻����Ͻ��п�����

2. ���ϣ�����Լ����޸ĺϲ���ԭ���ߵĴ���⣬���"Pull Request"��������ԭ���߷��ͺϲ�����ԭ���߽��յ������ߵ��ʼ���
    * test

