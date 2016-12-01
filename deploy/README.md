每个项目，从本地部署到服务器上面

+ composer require --dev deployer/deployer
+ 把当前最新tag/head部署到服务器上面
+ composer 更新代码
+ 拷贝到目标目录

全程要求不能登录服务器，否则就不是自动化，会有人为差别，导致可能错误

工具：deployer/deployer<br>
相关文章：https://www.sitepoint.com/deploying-php-applications-with-deployer/