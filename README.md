#GitHubÈëÃÅÖ¸ÄÏ#

**Ò»¡¢°²×°Git**  

Windows°æÏÂÔØµØÖ·£º[Git](http://windows.github.com/)  

Linux°æÏÂÔØµØÖ·£º[Git](http://git-scm.com/)

**¶ş¡¢×¢²áGitHubÓÃ»§**  

¹Ù·½ÍøÕ¾£º[GitHub](https://github.com)

**Èı¡¢Í¨¹ıGitHub´´½¨Repository**  

1. µÇÂ¼GitHub£¬Ñ¡Ôñ"Create a Repository"  

2. ÌîĞ´"Repository name"£¬µã»÷"Create repository"Íê³É´´½¨¡£

**ËÄ¡¢Ìí¼ÓÓÃÓÚ·ÃÎÊGitHubµÄ¹«Ô¿**  

1. Éú³É¹«Ô¿  

    ±¾µØ¿ØÖÆÌ¨ÊäÈë`ssh-keygen -t rsa -C "YourEmailAddress"`£¬¸ù¾İÌáÊ¾£¬ÕÒµ½¶ÔÓ¦µÄpubÎÄ¼ş£¬»ñÈ¡¹«Ô¿¡£  

2. Ìí¼Ó¹«Ô¿  

    µÇÂ¼Github£¬½øÈë"Account Settings"½çÃæ£¬Ñ¡Ôñ"SSH Keys"£»  

    µã»÷"Add SSH key"£¬ËæÒâÌîĞ´"Title",²¢½«¹«Ô¿ÌîÈë"Key"À¸£¬µã»÷"Add key"£¬ÔÙ´Î¾­¹ıGitHubÍøÕ¾µÇÂ¼ÃÜÂëÈ·ÈÏºó£¬Íê³É¹«Ô¿Ìí¼Ó¡£  

3. ÑéÖ¤  

    ±¾µØ¿ØÖÆÌ¨ÊäÈë`ssh git@github.com`£¬²é¿´ÊÇ·ñ¿ÉÒÔÍ¨¹ıGitHubÈÏÖ¤¡£  

**Îå¡¢Ê¹ÓÃGitHub´´½¨×Ô¼ºµÄRepository**  

¼ÙÈçÏÖÔÚGitHubÉÏ´´½¨ÁËÒ»¸öÃûÎªprinterµÄrepository£¬ÎÒÃÇ½«±¾µØµÄÎÄ¼şÉÏ´«ÖÁGitHub¡£  

1. ÅäÖÃGitÓÃ»§  

        $ git config --global user.name "GitHubÓÃ»§Ãû"  
        $ git config --global user.email you@example.com  

2. Ê¹ÓÃGit  

        $ mkdir printer  
        $ cd printer/  
        $ git init  
        $ touch A.java  
        $ git add A.java  
        $ git commit -m 'first commit'  
        $ git remote add origin git@github.com:GitHubÓÃ»§Ãû/printer.git  
        $ git push origin master  

**Áù¡¢²ÎÓëÆäËûÈËµÄRepository**

1. ÕÒµ½×Ô¼ºÏ£Íû²ÎÓëµÄrepository£¬µã»÷Ò³ÃæÓÒÉÏ½ÇµÄ"Fork"°´Å¥£¬´Ërepository¼´ÒÑÅÉÉúµ½×Ô¼ºµÄÕË»§ÃûÏÂ£¬²¢ÇÒ¿ÉÒÔÔÚ´Ë»ù´¡ÉÏ½øĞĞ¿ª·¢¡£

2. Èç¹ûÏ£Íû½«×Ô¼ºµÄĞŞ¸ÄºÏ²¢µ½Ô­×÷ÕßµÄ´úÂë¿â£¬µã»÷"Pull Request"£¬¼´¿ÉÏòÔ­×÷Õß·¢ËÍºÏ²¢ÇëÇó£¬Ô­×÷ÕßÔÚ½Óµ½ÇëÇóºó£×ÔĞĞ¾ö¶¨ÊÇ·ñ½ÓÊÜÇëÇó¡£
