#官方中文地址

中文手册地址<br>
https://phpunit.de/manual/5.6/zh_cn/index.html

主要

* 阅读安装
* 覆盖率
* 对异常进行测试
* assertTrue()
* assertEquals() 能预期的精确的返回比较
* @expectedException 对异常的测试,后面跟上异常的全路径

#配置文件 phpunit.xml

一个配置模板
里面的路径都是相对于phpunit.xml的路径

```
<?xml version="1.0" encoding="UTF-8"?>
<phpunit backupGlobals="false"
         backupStaticAttributes="false"
         bootstrap="./vendor/autoload.php"
         colors="true"
         convertErrorsToExceptions="true"
         convertNoticesToExceptions="true"
         convertWarningsToExceptions="true"
         processIsolation="false"
         stopOnFailure="false"
         syntaxCheck="true"
         verbose="true"
>

    <testsuites>
        <testsuite name="ormtest">
            <directory suffix=".php">./test/</directory>
        </testsuite>
    </testsuites>

    <filter>
        <whitelist addUncoveredFilesFromWhitelist="true">
            <directory suffix=".php">./src/</directory>
        </whitelist>
    </filter>


    <logging>
        <log type="coverage-text" target="php://stdout" showUncoveredFiles="true"/>
        <log type="coverage-html" target="coverage" showUncoveredFiles="true"/>
        <log type="coverage-clover" target="coverage.xml" showUncoveredFiles="true"/>
    </logging>


</phpunit>
```
#运行方式
在phpunit.xml目录下，命令行运行phpunit即可
