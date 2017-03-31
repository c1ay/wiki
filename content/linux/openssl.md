---
title: "openssl 解密有密码的密钥"
date: 2017-03-31 15:22
---


用openssl 解密有密码的密钥，解密后用密钥登陆不用输入密码

`openssl rsa -in rsa.pem -out rsa_pri.pem`
> rsa.pem 为有密码的密钥，rsa_pri.pem 为解密后的密钥

