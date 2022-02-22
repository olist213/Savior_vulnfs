# Savior_vulnfs
Savior漏洞修复建议更新，添加一些其他的漏洞，补充原先的漏洞模版。



项目地址：https://github.com/Mustard404/Savior



漏洞修复建议导出参考官方。

```bash
docker exec -it b9d9472f9ab5 /bin/bash

mysqldump -u root -p  savior api_program > api_program.sql; 
#输入密码，默认Savior@404 

exit 
docker cp b9d9472f9ab5:/api_program.sql ~ 
```

漏洞修复建议导入

```
docker cp Demo/api_program.sql b9d9472f9ab5:/
docker exec -it b9d9472f9ab5 /bin/bash 
mysql -u root -p 
#输入密码，默认Savior@404 
use savior; 
source /api_program.sql; 
```
