## 分页结构
```
{
"resultCode": '0',
"data": {
"total": 19 // 总数(数据库总的全部记录数)
"pageNum": 4, // 当前页码
"pageSize": 5, // 每一页的数量
"pages": 4, // 总页数
"size": 4, // 当前页的数量
"firstPage": 1, // 第一页
"prePage": 3, // 上一页
"nextPage": 0, // 下一页, 0 表示没有下一页了
"lastPage": 4, //最后一页
"hasNextPage": false,
"hasPreviousPage": true,
"isFirstPage": false,
"isLastPage": true,

// 结果集数组
"list": [
{
// ...
},
{
// ...
},
{
// ...
}
// ...
]

"startRow": 1, // 数据库中的行号, 不用理会
"endRow": 1, // 数据库中的行号, 不用理会

//导航页, 不用理会
"navigatePages": 8,
"navigatepageNums": [
1
]
},
"resultMsg": "...成功"
}
```