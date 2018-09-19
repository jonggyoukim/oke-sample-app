# Node-MySQL sample for Kubernetes

쿠버네티스를 위한 샘플입니다.

node 와 mysql 을 사용한 게시판입니다.

## MySQL 설정
~~~
create user 'test'@'%' identified WITH mysql_native_password by 'password';
grant all privileges on 'test'.* to 'test'@'%';
CREATE DATABASE sample;
use sample;
CREATE TABLE IF NOT EXISTS `players` (
  `id` int(5) NOT NULL AUTO_INCREMENT,
  `first_name` varchar(255) NOT NULL,
  `last_name` varchar(255) NOT NULL,
  `position` varchar(255) NOT NULL,
  `number` int(11) NOT NULL,
  `user_name` varchar(20) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB  AUTO_INCREMENT=1;
~~~
## 실행
~~~
$ npm install
$ node app.js
~~~
