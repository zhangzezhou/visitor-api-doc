# 数据结构

## Appointment参数说明

| 参数 | 类型 | 描述 |
| --- | --- | --- |
| appointmentId | String | 预约id |
| visitorId | String | 来访者用户id |
| visitorName | String | 来访者姓名 |
| visitorGender | Number | 来访者性别，1表示男，2表示女 |
| visitorCompanyName | String | 来访者企业名 |
| visitorCompanyId | String | 来访者企业id |
| visitorTel | String | 来访者手机号 |
| visitorLicencePlateNum | String | 来访者车牌号 |
| visitorDepart | String | 来访者部门 |
| visitorPosition | String | 来访者职位 |
| visitorPortaitUrl | String | 来访者面部采样照片 |
| intervieweeName | String | 受访者姓名 |
| intervieweeDepart | String | 受访者部门 |
| intervieweeCompanyId | String | 受访者企业id |
| appointmentReason | String | 预约事由 |
| appointmentTime | Number | 预约时间,时间戳 |
| deliveryOrderNum | String | 提货单号 |
| status | Number | 审核状态，1是审核中，2是审核成功，3是审核失败 |
| followerList | Arrary&lt;[Follower](/data-struct/data-struct.md#follower参数说明)&gt; | 同性人列表 |
| createTime | Number | 创建时间 |
| updateTime | Number | 更新时间 |

## SignInfo参数说明

| 参数 | 类型 | 描述 |
| --- | --- | --- |
| signInfoId | String | 签到id |
| userId | String | 签到用户id\(app\_user\_id\) |
| longitude | String | 经度 |
| latitude | String | 纬度 |
| faceImageUrl | String | 签到照片url |
| companyId | String | 签到者企业id |
| signTime | Number | 签到时间（时间戳） |

## Follower参数说明
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| followerId| String | 签到id |
| userId | String | 签到用户id\(app\_user\_id\) |
| longitude | String | 经度 |
| latitude | String | 纬度 |
| faceImageUrl | String | 签到照片url |
| companyId | String | 签到者企业id |
| signTime | Number | 签到时间（时间戳） |




