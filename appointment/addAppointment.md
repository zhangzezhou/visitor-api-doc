# 新增预约接口

### 接口地址：`{{base_url}}/api/app/appointment`

### 请求方法：POST

### 请求头：

| 参数 | 参数值 | 是否必选 |
| --- | --- | --- |
| Content-Type | application/json | 是 |

### 请求参数:

| 参数 | 参数类型 | 描述 | 是否必选 |
| --- | --- | --- | --- |
| visitorName | String | 来访者姓名 | 是|
| visitorGender | Number | 来访者性别，1表示男，2表示女 |否|
| visitorCompanyName | String | 来访者企业名 |是|
| visitorCompanyId | String | 来访者企业id |是|
| visitorTel | String | 来访者手机号 |否|
| visitorLicencePlateNum | String | 来访者车牌号 |否|
| visitorCertificateNum| String | 来访者证件号 |是|
| visitorCertificateFrontUrl| String | 来访者证件正面 |是|
| visitorCertificateReverseUrl| String | 来访者证件反面 |是|
| visitorDepart | String | 来访者部门 |否|
| visitorPosition | String | 来访者职位 |否|
| visitorPortaitUrl | String | 来访者面部采样照片 |否|
| intervieweeName | String | 受访者姓名 |是|
| intervieweeDepart | String | 受访者部门 |是|
| intervieweeCompanyId | String | 受访者企业id |是|
| intervieweeQualificationCertificateUrl| String | 受访者职业资格证  |否|
| appointmentReason | String | 预约事由 |是|
| appointmentTime | Number | 预约时间,时间戳 |是|
| followerList | Arrary&lt;[Follower](/data-struct/data-struct.md#follower参数说明)&gt; | 同行人列表 |否|


### 响应参数:

| 参数 | 参数类型 | 描述 |
| --- | --- | --- |
| data | [Appointment](/data-struct/data-struct.md/#appointment参数说明) | 预约信息 |
| resultCode | string | [状态码](/data-struct/code.md) |
| resultMsg | string | 返回结果说明 |
| errorMsg | string | 异常信息 |

### 请求示例：

```
{{base_url}}/api/app/appointment
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



