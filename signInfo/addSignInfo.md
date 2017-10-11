# 新增签到接口

接口地址：`{{base_url}}/api/app/signInfo`

请求方法：POST

请求头：

| 参数 | 参数值 | 是否必选 |
| --- | --- | --- |
| Content-TypeE | application/json | 是 |
| accessToken | ${accessToken} | 是 |

### 请求参数:

| 参数 | 参数类型 | 描述 | 是否必选 |
| --- | --- | --- | --- |
| account | string | 用户账号 | 是 |
| password | string | 密码 | 是 |

### 响应参数:

| 参数 | 参数类型 | 描述 |
| --- | --- | --- |
| data | [S](/appointment)ignInfo | 预约信息 |
| resultCode | string | [状态码](/data-struct/code.md) |
| resultMsg | string | 返回结果说明 |
| errorMsg | string | 异常信息 |

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
    "account":"admin_nova",
    "password":"admin_nova"
}
```

### 返回示例

```json
{
    "accessToken": "002baaaac60a1838781aa8c53bc82516",
    "expiresIn": 622080000,
    "data": {
        "userId": 82,
        "account": "admin_nova",
        "userName": "admin_nova",
        "phone": "15217297145",
        "email": "13751733273@qq.com",
        "password": "6cc2cd573cae23d40529b907e6488120",
        "userRole": 1,
        "company": {
            "companyId": 48,
            "companyName": "南凌",
            "email": "huangyuhua@nova.net.cn",
            "address": "深圳",
            "legalPerson": "南凌管理员"
        }
    },
    "resultCode": "0"
}
```



