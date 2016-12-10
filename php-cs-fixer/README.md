#代码格式化工具

>更多时候，我们可以通过配置文件来自定义格式化选项以及搜索的目录和文件。
自定义配置通过在项目根目录添加一个 .php_cs 文件的方式实现。

#相关入门文档

(http://0x1.im/blog/php/php-cs-fixer.html)

```php
<?php

$finder = PhpCsFixer\Finder::create()
    ->in(__DIR__)
;

return PhpCsFixer\Config::create()
    ->setRules(array(
        '@PSR2' => true,
        '@Symfony' => true,
        'phpdoc_order'=>true,
        'array_syntax' => array('syntax' => 'short'),
    ))
    ->setFinder($finder)
;
```