# crawlChineseWeather
Python3.x
运行方法
```
python crawlChineseWeather.py
```
需要导入的库
```
import re
import requests
from bs4 import BeautifulSoup
```


crawlChineseWeather2.py使用方法,代码改动不多
将其上传服务器<br>
在服务器中安装mail服务 <br>
Centos7默认安装了mail <br>
Ubuntu16.04运行如下命令安装
```
sudo apt install mailutils
```
添加一个定时任务,每天7:00am发送天气信息到给定邮箱
```
0 7 * * * python3 crawlChineseWeather.py | mail -s subject email-Address
```
