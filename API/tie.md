#贴钱活动模块 

[1.用户申请发布贴钱活动](#1)

[2.用户申请发布贴钱活动后填写手机号码](#2)

---
##<a id="1">1.用户申请发布贴钱活动</a>

### URL
/tie/apply.json

### 请求方式
POST

### Header
Content-Type : application/json

### 请求参数
     参数      | 必选 	    | 类型及范围     |说明
-------------  | ---------- | -------------  |---------- 
uid            | true 	    | long(20)       |用户ID
title          | true 	    | string(100)    |活动名称
invited        | true 	    | int(1)            |活动是否有邀请机制,是1,否0
link           | false	    | string(500)    |活动邀请链接
code           | false	    | string(50)     |活动邀请码
brief          | false	    | string(500)    |活动简要描述
images         | false      | string['','']  |图片数组

### 请求Json示例
	{       
    "uid" : 100001,
    "title" : "只要你走路，就能按步数领钱",
    "invited" : 1,
    "link" : "http://www.qqqqqq.com/invite?code=dfasxxd",
    "code" : "fasfdsafa",
    "brief" : "简要说明该活动",
    "images" : [
      "http://www.qqqqqq.com/a.jpg",
      "http://www.qqqqqq.com/b.jpg"
    ]
	}

### 返回Json示例
#### 请求成功
	{
		"success":"true",
		"data" : {
		  "applyid" : 123421
		}
	}

#### 请求失败
	{
		"error_code":"10000",
		"error_message":"XXXXX"
	}

---
##<a id="2">2.用户申请发布贴钱活动后填写手机号码</a>

### URL
/tie/apply/fill_phone.json

### 请求方式
POST

### Header
Content-Type : application/json

### 请求参数
     参数      | 必选 	    | 类型及范围     |说明
-------------  | ---------- | -------------  |---------- 
applyid        | true 	    | long(20)       |申请id
phone          | true 	    | string(15)     |用户填写的手机号码

### 请求Json示例
	{       
		applyid : 1000001,
		phone : "15292422938"
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
