# sms-code

[![NPM](https://nodei.co/npm/sms-code.png?downloads=true&downloadRank=true&stars=false)](https://nodei.co/npm/sms-code/)

## Installation
Using npm:
```shell
$ npm i sms-code
```
Note: add `--save` if you are using npm < 5.0.0

## Usage
0.快速开始
```javascript
    // nodejs 运行环境
    const smsCode = require('sms-code')
    // es6
    import smsCode from 'sms-code'

    const code = smsCode.getCode('188888888888')     // 随机数 如：3333
    smsCode.verifyCode('18888888888', code)   // 验证结果 true/false
```


1.用于生成随机验证码以及验证验证码

```javascript
    smsCode.getCode('188888888888')     // 随机数 如：3333
    smsCode.verifyCode('18888888888', '3333')   // 验证结果 true/false
```

2.每个手机号对应的验证码只能被验证一次且可自定义有效期

3.可以设置验证码过期时间以及验证码长度

```javascript
    smsCode.setOptions({
        age: 5, // 默认有效时间为五分钟
        length: 4   // 默认长度为四位
    })
```
