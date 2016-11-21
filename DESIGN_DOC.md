# ucenter 开发设计文档
### 用户表数据库设计
``` sql
CREATE TABLE `user` (
  `uid` int(11) unsigned NOT NULL AUTO_INCREMENT,
  `phone_no` varchar(100) NOT NULL DEFAULT '',
  `user_name` varchar(100) NOT NULL DEFAULT '',
  `avatar` varchar(100) NOT NULL,
  `email` varchar(100) NOT NULL DEFAULT '',
  `password` char(64) NOT NULL,
  `status` int(10) NOT NULL DEFAULT '0',
  `birth_date` date DEFAULT NULL,
  `sex` tinyint(4) unsigned NOT NULL DEFAULT '0',
  `create_time` int(11) unsigned NOT NULL,
  `update_time` timestamp NOT NULL DEFAULT '0000-00-00 00:00:00' ON UPDATE CURRENT_TIMESTAMP,
  PRIMARY KEY (`uid`)
) ENGINE=InnoDB AUTO_INCREMENT=1000 DEFAULT CHARSET=utf8;
```
### 接口设计
#### 注册接口
uri:user/register
Request:
``` json
{
    "phone_no":13200000000,
    "password":"xxxxxxx"
}
```
Response:
``` json
{
    "statusCode":0,
    "msg":"",
    "uid":'100001'
}
```
#### 用户登录验证接口
uri:user/verify
Request:
``` json
{
    "phone_no":13200000000,
    "password":"xxxxxxx"
}
```
Response:
``` json
{
    "statusCode":0,
    "msg":"",
    "data":{
	"uid":'100001'
     }
}
```

### 修改密码接口
uri:user/modifyPwd
Request:
``` json
{
    "uid":13200000000,
    "password":"xxxxxxx"
}
```
Response:
``` json
{
    "statusCode":0,
    "msg":"",
    "uid":'100001'
}
```

#### 设置信息接口 
uri:user/updateInfo
Request:
``` json
{
    "uid":13200000000,
    "user_name":"xxxxxxx",
    "avatar":"xxxxxxx.png",
    "email":"xxxxxxx@qq.com",
    "birth_date":'1993-10-10',
    "sex":1,
}
```
Response:
``` json
{
    "statusCode":0,
    "msg":"",
    "uid":'100001'
}
```

#### 冻结接口
uri:user/lock
Request:
``` json
{
    "uid":13200000000,
}
```
Response:
``` json
{
    "statusCode":0,
    "msg":"",
    "uid":'100001'
}
```

#### 解冻接口
uri:user/unLock
Request:
``` json
{
    "uid":13200000000,
}
```
Response:
``` json
{
    "statusCode":0,
    "msg":"",
    "uid":'100001'
}
```


