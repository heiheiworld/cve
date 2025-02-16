# blood-bank-system-in-php has Cross Site Scripting vulnerability

## supplier 
https://code-projects.org/blood-bank-system-in-php-with-source-code/
## Vulnerability file
/BBfile/prostatus.php
## describe
There is an  Cross Site Scripting vulnerability in blood-bank-system-in-php  in /BBfile/prostatus.php. Control parameter: $message

A malicious attacker can use this vulnerability to obtain administrator login credentials or phishing websites

## code analysis

echo $row['message'] in no filter.

![Image](https://github.com/user-attachments/assets/064edeb1-9889-47d4-9afd-7b74f65e5358)

## POC

```
GET /prostatus.php HTTP/1.1
Host: bloodbankmgmtsystem
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.6261.112 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Accept-Encoding: gzip, deflate, br
Accept-Language: zh-CN,zh;q=0.9
Cookie: PHPSESSID=3lgrau18ka280ntnhqf9et3ud3
Connection: close


```

**Result**

![Image](https://github.com/user-attachments/assets/c6bfd55a-afcf-4f02-b648-8d9ed5766cf6)



![Image](https://github.com/user-attachments/assets/1ff37299-7482-4083-a51b-e69f0ba08a9d)