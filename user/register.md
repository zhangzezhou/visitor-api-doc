# app用户注册
### 接口地址：``{{base_url}}/api/app/appUser ``
### 请求方法：POST
### 请求头：
参数 | 参数值 | 是否必选
---|---|---
Content-Type | application/json | 是
appToken | {appToken}（app调用接口的token） | 是 
### 请求参数:&nbsp; 
参数 | 参数类型 | 描述 | 是否必选
---|---|---|---
account  | string | 用户账号| 是
password  | string | 密码| 是
userName |string|用户名|是
### 响应参数:&nbsp; 
参数 | 参数类型 | 描述 
---|---|---
data  | [AppUser](/data-struct/data-struct.md/#appuser参数说明) | 用户基本信息
resultCode  | string | [状态码](data-struct/code.md)
resultMsg | string | 返回结果说明
errorMsg | string | 异常信息
### 请求示例：
```  
{{base_url}}/api/app/appUser
```  
##### Header：
```
"Content-Type":"application/json"
```
##### Body：
```json
{
	"account":"admin_nova",
	"password":"admin_nova"
}
```
### 返回示例
```json
    "resultCode": 200,
    "resultMsg": "创建成功",
    "data": {
        "userId": "952535f6bb2111e78561b8aeed9e915f",
        "account": "sunpengwei",
        "password": "2a16a2203188ee8d3860aa6dc9c8f4088d5c9e632d8d8b36f6d083b5f6067f70",
        "userName": "孙朋维",
        "companyId": "1"
    },
    "errorMsg": null
```