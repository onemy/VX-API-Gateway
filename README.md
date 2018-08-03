# VX-API-Gateway (JWT Token Plugin)
![logo](https://raw.githubusercontent.com/shenzhenMirren/MyGithubResources/master/image/VX-API-Gateway-Logo_small.png)<br/>
VX-API-Gateway是基于Vert.x(java)开发的API网关,是一个分布式,全异步,高性能,可扩展 ,轻量级的API网关<br/>
VX-API-Gateway的部分流程与页面设计灵感来自阿里云的API网关<br/>
QQ交流群 : 440306757<br/>
### JWTTokenPlugin使用说明

一、发布JWT鉴权服务
1、选择jwtTokenAuth
2、认证配置文件说明
需使用JSON对象描述

{
"apiTokenName":"apiToken",			//非必须，请求头使用的KEY，值为加密token串，默认apiToken
"userTokenName":"apiName",			//非必须，请求头使用的KEY，值为用户名，默认apiName
"secretKeys":[{"admin":"secret"},{"test":"123456"}]	,	//必须，用户名及密钥数组
"userTokenScope":"HEADER",			// 非必须，用户请求token存放的位置,默认为header
"authFailContentType":"HTML_UTF8",		// 非必须，认证失败返回结果的contentType,默认json-utf8
"authFailResult":"Unauthorized"			// 非必须，认证失败返回结果
}

