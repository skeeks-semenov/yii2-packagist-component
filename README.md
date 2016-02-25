Packagist API wrapper component extension for Yii2
======================

Component extension wrapper for [Packagist API](http://packagist.org/)

Installation
------------
The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require "skeeks/yii2-packagist-component" "*"
```
or add

```json
"skeeks/yii2-packagist-component" : "*"
```

to the require section of your application's `composer.json` file.

Usage
-----

```
use dosamigos\packagist\Packagist;

$api = new Packagist;

// get a package information  
$response = $api->package('yiisoft/yii2`)->getResponse();  
// dump response  
var_dump($response->body);

// get a filtered list  
$response = $api->all(['vendor' => '2amigos'])->getResponse();
if($response->isSuccessFul) {
    var_dump($response->body);
} else {
    var_dump($response->error);
}

// search packages
$response = $api->search('yii2')->getResponse();  
var_dump($response->body);  
```


___

> [![skeeks!](https://gravatar.com/userimage/74431132/13d04d83218593564422770b616e5622.jpg)](http://skeeks.com)
<i>SkeekS CMS (Yii2) — fast, simple, effective!</i>
[skeeks.com](http://skeeks.com) | [cms.skeeks.com](http://cms.skeeks.com) | [marketplace.cms.skeeks.com](http://marketplace.cms.skeeks.com)