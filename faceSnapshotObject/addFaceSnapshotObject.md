# 人脸抓拍推送接口

### 接口地址：`{{base_url}}/api/app/faceSnapshotObject`

### 请求方法：POST

### 请求头：

| 参数 | 参数值 | 是否必选 |
| --- | --- | --- |
| Content-Type | application/json | 是 |
| appToken | d83fbd7dcaa011e78561b8aeed9e915f | 是 |
### 请求参数:

| 参数 | 参数类型 | 描述 | 是否必选 |
| --- | --- | --- | --- |
| faceObjectId| String | 人脸对象id | 是 |
| faceObjectType| Number | 人脸对象类型,1是黑名单，2是员工，3是顾客，4是VIP顾客,5是陌生人 | 是  |
| firstSnapshotTime| Number | 第一次抓拍时间（时间戳） | 否 |
| lastSnapshotTime| Number | 最后一次抓拍时间（时间戳） | 否 |
| faceImageUrl| String | 抓拍人脸图片url| 是 |

### 响应参数:

| 参数 | 参数类型 | 描述 |
| --- | --- | --- |
| resultCode | string | [状态码](/data-struct/code.md) |
| resultMsg | string | 返回结果说明 |
| errorMsg | string | 异常信息 |

### 请求示例：

```
{{base_url}}/api/app/faceSnapshotObject
```

##### Header：

```
"Content-Type":"application/json"
```

##### Body：

```json
{
    "faceObjectId":"d83fbd7dcaa011e78561b8aeed9e915f",
    "faceObjectType":1,
    "firstSnapshotTime":"1509185697",
    "lastSnapshotTime":"1509185697",
    "faceImageUrl":"http://a.hiphotos.baidu.com/image/pic/item/00e93901213fb80e3b0a611d3fd12f2eb8389424.jpg"
}
```

### 返回示例

```json
{
    "resultCode": 200,
    "resultMsg": "接收抓拍信息成功",
    "data": null,
    "errorMsg": null
}
```



