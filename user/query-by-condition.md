# 根据条件查询app用户列表
### 接口地址：``{{base_url}}/api/appUser ``
### 请求方法：POST
### 请求头：
参数 | 参数值 | 是否必选
---|---|---
appToken | {appToken}（app调用接口的token） | 是
### 请求参数:&nbsp; 
参数 | 参数类型 | 描述 | 是否必选
---|---|---|---
user| string | 用户账号| 是
password  | string | 密码| 是
### 响应参数:&nbsp; 
参数 | 参数类型 | 描述 
---|---|---
accessToken  | string | 令牌
data  | [AppUser](/data-struct/data-struct.md/#appuser参数说明) | 用户基本信息
resultCode  | string | [状态码](data-struct/code.md)
resultMsg | string | 返回结果说明
errorMsg | string | 异常信息
### 请求示例：
```  
{{base_url}}/api/app/accessToken
```  
##### Header：
```
"Content-Type":"application/json"
```
##### Body：
```json
{
	"account":"zhangzezhou",
	"password":"asdqwe123"
}
```
### 返回示例
```json
{
    "data": {
        "userId": "098cddddbac811e78561b8aeed9e915f",
        "account": "zhangzezhou",
        "password": "20504cdfddaad0b590ca53c4861edd4f5f5cf9c348c38295bd2dbf0e91bca4c3",
        "userName": "张泽洲",
        "companyId": "1",
        "phone": null,
        "idCard": null,
        "certificateName": null,
        "certificateNum": null,
        "gender": null,
        "faceImageUrl": null,
        "departId": "2",
        "depart": {
            "departId": "2",
            "departName": "云服务与荣耀交付部",
            "parentId": "1",
            "parentDepart": {
                "departId": "1",
                "departName": "硬件交付部",
                "parentId": null,
                "parentDepart": null
            }
        },
        "position": null,
        "email": null
    },
    "resultCode": 200,
    "accessToken": "098cddddbac811e78561b8aeed9e915f_ee8096ea42844b36980ddc1cc85326ed",
    "resultMsg": "登录成功"
}
```