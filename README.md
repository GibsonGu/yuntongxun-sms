# ucpaas-sms
云之讯 短信Api

#安装 
在composer.json 添加 
```json
hardywen/ucpaas-sms: '~v1.0'
```

运行 ```composer update```

在 ```app/config/app.php```的providers数组里加入
```php
'Hardywen\UcpaasSms\UcpaasSmsServiceProvider',
```
aliases 数组里加入
```php
'UcpaasSms' =>'Hardywen\UcpaasSms\Facade\UcpaasSms',
```

运行
```php 
artisan config:publish hardywen/ucpaas-sms
```

去 ```app/config/packages/hardywen/ucpaas-sms/config.php``` 配置

#使用
发送手机短信
```php
UcpaasSms::templateSMS('9635', '123456,3', '138xxxxxx')
```

发送语音验证码
```php
UcpaasSms::voiceCode('123123','138xxxx')
```