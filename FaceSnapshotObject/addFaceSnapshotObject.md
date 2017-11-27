# 新增预约接口

### 接口地址：`{{base_url}}/api/app/faceSnapshotObject`

### 请求方法：POST

### 请求头：

| 参数 | 参数值 | 是否必选 |
| --- | --- | --- |
| Content-Type | application/json | 是 |

### 请求参数:

| 参数 | 参数类型 | 描述 | 是否必选 |
| --- | --- | --- | --- |
| faceObjectId| String | 人脸对象id | 是 |
| faceObjectType| Number | 人脸对象类型,1是黑名单，2是员工，3是顾客，4是VIP顾客,5是陌生人 | 是  |
| firstSnapshotTime| Number | 第一次抓拍时间（时间戳） | 否 |
| lastSnapshotTime| Number | 最后一次抓拍时间（时间戳） | 否 |
| faceImageUrl| String | 抓拍人脸图片url| 是 |
| image| String | 来访者车牌号 | 否 |
| visitorCertificateNum | String | 来访者证件号 | 是 |
| visitorCertificateFrontUrl | String | 来访者证件正面 | 是 |
| visitorCertificateReverseUrl | String | 来访者证件反面 | 是 |
| visitorDepart | String | 来访者部门 | 否 |
| visitorPosition | String | 来访者职位 | 否 |
| visitorPortaitUrl | String | 来访者面部采样照片 | 否 |
| intervieweeName | String | 受访者姓名 | 是 |
| intervieweeDepart | String | 受访者部门 | 是 |
| intervieweeCompanyId | String | 受访者企业id | 是 |
| intervieweeQualificationCertificateUrl | String | 受访者职业资格证 | 否 |
| appointmentReason | String | 预约事由 | 是 |
| appointmentTime | Number | 预约时间,时间戳 | 是 |
| followerList | Arrary&lt;[Follower](/data-struct/data-struct.md#follower参数说明)&gt; | 同行人列表 | 否 |

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
    "visitorName":"zzz",
    "visitorCompanyName":"中软",
    "visitorTel":"13751733273",
    "visitorDepart":"荣耀交付部",
    "visitorPosition":"Java工程师",
    "intervieweeName":"张婧",
    "intervieweeDepart":"硬件交付部",
    "intervieweePosition":"PM",
    "intervieweeCompanyName":"中软",
    "intervieweeCompanyId":"59",
    "appointmentReason":"项目洽谈",
    "appointmentReasonId":"",
    "appointmentTime":1509185697,
    "followerList":[
            {
                "followerName":"zhangjing",
                "followerPhone":"13751733723",
                "followerPortraitUrl":""
            }
        ]
}
```

### 返回示例

```json
{
    "resultCode": 200,
    "resultMsg": "预约成功",
    "data": {
        "appointmentId": "d83fbd7dcaa011e78561b8aeed9e915f",
        "visitorId": null,
        "visitorName": "zzz",
        "visitorGender": null,
        "visitorCompanyName": "中软",
        "visitorTel": "13751733273",
        "visitorLicencePlateNum": null,
        "visitorDepart": "荣耀交付部",
        "visitorPosition": "Java工程师",
        "visitorPortraitUrl": null,
        "visitorCertificateNum": null,
        "visitorCertificateFrontUrl": null,
        "visitorCertificateReverseUrl": null,
        "intervieweeId": null,
        "intervieweeName": "张婧",
        "intervieweeDepart": "硬件交付部",
        "intervieweePosition": "PM",
        "intervieweeCompanyName": "中软",
        "intervieweeQualificationCertificateUrl": null,
        "intervieweeCompanyId": "59",
        "appointmentReason": "项目洽谈",
        "appointmentReasonId": null,
        "appointmentTime": 1509185697,
        "appointmentEndTime": null,
        "status": 1,
        "rejectReason": null,
        "inTrash": 1,
        "remark": null,
        "followerList": [
            {
                "followerId": "d8406d4acaa011e78561b8aeed9e915f",
                "followerPortraitUrl": "",
                "followerName": "zhangjing",
                "appointmentId": "d83fbd7dcaa011e78561b8aeed9e915f",
                "followerPhone": "13751733723"
            }
        ],
        "regionList": []
    },
    "errorMsg": null
}
```


