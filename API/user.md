#用户模块 

[1.绑定手机号](#1)

---
##<a id="1">1.绑定手机号</a>

### URL
/user/phone/bind.json

### 请求方式
POST

### Header
Content-Type : application/json

### 请求参数
     参数      | 必选 	    | 类型及范围     |说明
-------------  | ---------- | -------------  |---------- 
phone          | true	    | string(15)     |手机号码
uid            | true	    | long           |用户ID

### 请求Json示例
	{       
	    "phone" : "13927450239",
	    "uid" : 11232434	
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
