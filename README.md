# selenium

分享自写源码，希望对大家有帮助

本人配置

- jdk13.0.2 （jdk1.7以上均可）
- Maven 3.6.3 
- selenium  4.1.3
- chrome 98.0.4758.102 (正式版本) （64 位）
- chromedriver 

## selenium:

- chrome浏览器驱动路径
使用Chrome做测试时，报了如下错误:

The path to the driver executable must be set by the webdirver.chrome.driver system properity

解决方案：

系统设置Chrome驱动文件的路径

System.setProperty("webdriver.chrome.driver", "xxx");
- chrome浏览器与chromeDriver匹配问题
使用chrome浏览器去完成自动化测试时，chrome浏览器停止运行

chromedriver.exe 已停止工作

错误总结：

chrome浏览器版本过高，虽然根据官网上的信息，2.33的chrome驱动支持60-62的谷歌。但是60根本不行

解决办法：

降级chrome

- Chrome与ChromeDriver版本对照表
ChromeDriver 版本	支持的 Chrome 版本

v2.41	v67-69

v2.40	v66-68

v2.39	v66-68

v2.38	v65-67

v2.37	v64-66

v2.36	v65-67

v2.35	v62-64

v2.34	v61-63

v2.33	v60-62

v2.32	v59-61

v2.31	v58-60

v2.30	v58-60

v2.29	v56-58

chrome浏览器各版本
http://www.chromedownloads.net/chrome64win/

禁止谷歌浏览器更新
https://jingyan.baidu.com/article/76a7e409f2137afc3b6e15be.html

ChromeDriver 镜像 http://npm.taobao.org/mirrors/chromedriver

Selenium 镜像 http://npm.taobao.org/mirrors/selenium

JDK版本问题
使用3.x的selenium来完成自动化测试时，代码报了如下错误:

Exception in thread "main" java.lang.UnsupportedClassVersionError:

错误总结：

3.x的selenium需要1.8的jdk，可能jdk版本过低

解决办法：

降级selenium版本，或提高jdk的版本为1.8
