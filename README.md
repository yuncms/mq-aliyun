# Aliyun MNS Topic for YUNCMS

适用于 YUNCMS 的 Aliyun MNS Topic。使用了DI实现的，可自行继承扩展。

[![Latest Stable Version](https://poser.pugx.org/yuncms/broadcast-aliyun/v/stable.png)](https://packagist.org/packages/yuncms/broadcast-aliyun)
[![Total Downloads](https://poser.pugx.org/yuncms/broadcast-aliyun/downloads.png)](https://packagist.org/packages/yuncms/broadcast-aliyun)
[![License](https://poser.pugx.org/yuncms/broadcast-aliyun/license.svg)](https://packagist.org/packages/yuncms/broadcast-aliyun)

Installation
------------

Next steps will guide you through the process of installing  using [composer](http://getcomposer.org/download/). Installation is a quick and easy three-step process.

### Step 1: Install component via composer

Either run

```
composer require --prefer-dist yuncms/broadcast-aliyun
```

or add

```json
"yuncms/broadcast-aliyun": "~1.0.0"
```

to the `require` section of your composer.json.

### Step 2: Configuring your application

Add following lines to your main configuration file:

```php
'components' => [
    'broadcast' => [
        'class' => 'yuncms\broadcast\aliyun\Broadcast',
        'endPoint' => 'http://a13.mns.cn-hangzhou.aliyuncs.com/',
        'topicName' => 'abc',
        'accessId' => '',
        'accessKey' => '',
    ],
],
```

### Use 

使用方式非常简单

```php
$broadcast = Yii::$app->broadcast;


$res = $broadcast->send([
    'Key'=>'value',
    //etc ...
]);

var_dump($res);