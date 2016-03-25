#消息相关模块

[1.发送手机验证码](#1)

[2.验证手机验证码](#2)

---
##<a id="1">1.发送手机验证码</a>

### URL
/message/phone/verify_code.json

### 请求方式
POST

### Header
Content-Type : application/json

### 请求参数
     参数      | 必选 	    | 类型及范围     |说明
-------------  | ---------- | -------------  |---------- 
uid            | false 	    | long(20)       |用户ID
phone          | true 	    | string(15)     |手机号码

### 请求Json示例
	{       
    "uid" : 100001,
    "phone" : "15823679287"
	}

### 返回Json示例
#### 请求成功
	{
		"success":"true",
		"data" : {
		  "codeid" : 123421 //数据库中验证码表的记录ID  
		}
	}

#### 请求失败
	{
		"error_code":"10000",
		"error_message":"XXXXX"
	}
	
---
##<a id="2">2.验证手机验证码</a>

### URL
/message/phone/verify.json

### 请求方式
POST

### Header
Content-Type : application/json

### 请求参数
     参数      | 必选 	    | 类型及范围     |说明
-------------  | ---------- | -------------  |---------- 
codeid         | true 	    | long(20)       |记录ID
code           | true 	    | string(6)      |验证码

### 请求Json示例
	{       
    "codeid" : 100001,
    "code" : "345987"
	}

### 返回Json示例
#### 请求成功
	{
		"success":"true"
	}

#### 请求失败
	{
		"error_code":"10000",
		"error_message":"XXXXX"
	}
[错误码详见错误码对照表](错误码对照表.md)
