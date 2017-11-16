# 数据结构
## AppUser 参数说明
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| userId| String | 用户id |
| account| String | 账户 |
| password| String | 密码 |
| userName | String| 用户名 |
| companyId| String | 企业Id |
| phone| String | 联系方式 |
| idCard| String | 身份证号|
| certificateName | String |资格证书名称 |
| certificateNum| String | 资格证书号码 |
| gender| Integer| 性别，1表示男，2表示女 |
| faceImageUrl| String | 面部采样图片url |
| departId | String | 部门id |
| depart| [Depart](data-struct/data-struct.md/#depart参数说明)| 部门信息 |
| position| String | 职位|
| email| String | 邮箱 |

## Depart参数说明
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| departId| String | 部门id |
| departName| String | 账户 |
| parentId| String | 父级部门ID|
| parentDepart| Depart| 父级部门信息 |


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
| visitorCertificateNum| String | 来访者证件号 |
| visitorCertificateFrontUrl| String | 来访者证件正面 |
| visitorCertificateReverseUrl| String | 来访者证件反面 |
| visitorDepart | String | 来访者部门 |
| visitorPosition | String | 来访者职位 |
| visitorPortaitUrl | String | 来访者面部采样照片 |
| intervieweeName | String | 受访者姓名 |
| intervieweeDepart | String | 受访者部门 |
| intervieweeCompanyId | String | 受访者企业id |
| intervieweeQualificationCertificateUrl| String | 受访者职业资格证  |
| appointmentReason | String | 预约事由 |
| appointmentTime | Number | 预约时间,时间戳 |
| deliveryOrderNum | String | 提货单号 |
| status | Number | 1是待审核，2是审核成功，3是审核失败,4是审核中，5是取消预约 |
| followerList | Arrary&lt;[Follower](/data-struct/data-struct.md#follower参数说明)&gt; | 同性人列表 |
| followerList | Arrary&lt;[Follower](/data-struct/data-struct.md#follower参数说明)&gt; | 同性人列表 |
| appointmentReason | String | 预约事由 |

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
| followerId| String | 随行id |
| followerPortaitUrl| String | 随行人头像url |
| followerName| String | 随行人姓名|
| appointmentId| String | 预约id|

## Company参数说明
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| companyId| String | 企业id|
| companyName| String | 公司名 |
| address| String | 地址|
| legalPerson| String | 负责人|
| email| String | 邮箱|
| contacts| String | 联系人|
| companyDomain| String | 公司域名|
| createTime | Number | 创建时间 |
| updateTime | Number | 更新时间 |
## CompanyAuth参数说明
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| appid| String | 应用id|
| appkey| String | 应用秘钥 |
| companyId| String | 企业id|
| createTime | Number | 创建时间 |
| updateTime | Number | 更新时间 |
## NoticeReceiver参数说明
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| noticeReceiverId| String | 消息通知id|
| senderId| String | 发送者id |
| title| String | 消息标题|
| summary| String | 消息摘要|
| contentId| String | 内容id|
| content| T | 内容的类型根据contenType确定|
| contentType| String | 消息通知类别|
| read| Boolean| 是否已读|
| inTrash| Boolean| 是否已删除|
| createTime | Number | 创建时间 |
| updateTime | Number | 更新时间 |












































