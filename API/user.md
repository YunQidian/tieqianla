#用户模块 

[1.批量添加社区信息](#1)

---
##<a id="1">1.批量添加社区信息</a>

### URL
/v1/user/user.json

### 请求方式
POST

### Header
Content-Type : application/json

### 请求参数
     参数      | 必选 	    | 类型及范围     |说明
-------------  | ---------- | -------------  |---------- 
phone          | false	    | string(15)     |手机号码
username       | false	    | string(30)     |用户名
nickname       | false	    | string(20)     |昵称
email          | false	    | string(30)     |邮箱
qq             | false	    | long(15)       |qq号
sex            | false	    | string(1)      |性别,1男2女0未知
country        | false	    | string(10)     |国家
province       | false	    | string(15)     |省份
city           | false	    | string(15)     |城市 
portrait       | false	    | string(500)    |头像地址

### 请求Json示例
	{       
    "phone" : "13927450239",
    "province" : "湖北省"
	}

### 返回Json示例
#### 请求成功
	{
		"success":"true",
		"data" : {
		  "uid" : 123421
		}
	}

#### 请求失败
	{
		"error_code":"10000",
		"error_message":"XXXXX"
	}
[错误码详见错误码对照表](错误码对照表.md)
