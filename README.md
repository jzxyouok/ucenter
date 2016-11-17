# ucenter
## 用户中心demo
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




#### 用户登录验证接口



#### 修改密码接口



#### 设置信息接口 



#### 冻结接口



#### 解冻接口



