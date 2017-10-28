# 根据条件查询app用户列表

### 接口地址：`{{base_url}}/api/app/appUser`

### 请求方法：GET

### 请求头：

| 参数 | 参数值 | 是否必选 |
| --- | --- | --- |
| appToken | {appToken}（app调用接口的token） | 是 |

### 请求参数:

| 参数 | 参数类型 | 描述 | 是否必选 |
| --- | --- | --- | --- |
| userName | string | 用户名 | 否 |
| pageNum | number | 页码，默认第一页 | 否 |
| pageSize | number | 每页几条，默认5条 | 否 |

### 响应参数:

| 参数 | 参数类型 | 描述 |
| --- | --- | --- |
| accessToken | string | 令牌 |
| data | PageInfo&lt;List&lt;[AppUser](/data-struct/data-struct.md/#appuser参数说明)&gt;&gt; | 用户基本信息 |
| resultCode | string | [状态码](data-struct/code.md) |
| resultMsg | string | 返回结果说明 |
| errorMsg | string | 异常信息 |
> PageInfo表示分页结构，具体参数说明查看[分页结构参数说明](data-struct/page.md)
### 请求示例：

```
{{base_url}}/api/app/appUser
```

##### Header：

```
"appToken ":"asdfgghhh"
```

##### Body：



### 返回示例

```json
{
    "resultCode": 200,
    "resultMsg": "查询成功",
    "data": {
        "pageNum": 1,
        "pageSize": 5,
        "size": 2,
        "orderBy": null,
        "startRow": 1,
        "endRow": 2,
        "total": 2,
        "pages": 1,
        "list": [
            {
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
            {
                "userId": "85cadff3bb2111e78561b8aeed9e915f",
                "account": "zhangjing",
                "password": "6a22aa783f90a73b27e45e80aac5f89b2faf4485701f6103254e9c0f3bce77a3",
                "userName": "张婧",
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
            }
        ],
        "firstPage": 1,
        "prePage": 0,
        "nextPage": 0,
        "lastPage": 1,
        "isFirstPage": true,
        "isLastPage": true,
        "hasPreviousPage": false,
        "hasNextPage": false,
        "navigatePages": 8,
        "navigatepageNums": [
            1
        ]
    },
    "errorMsg": null
}
```



