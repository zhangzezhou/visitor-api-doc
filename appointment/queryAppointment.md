# 根据条件预约接口

### 接口地址：`{{base_url}}/api/app/appointment`

### 请求方法：GET

### 请求头：

| 参数 | 参数值 | 是否必选 |
| --- | --- | --- |
| accessToken| | 否|
### 请求参数:

| 参数 | 参数类型 | 描述 | 是否必选 |
| --- | --- | --- | --- |
| status| String | 按审核状态查询 | 否|
| pageNum| Number | 分页查询，页码 |否|
| pageSize | String | 分页查询，每页多少条 |否|

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



