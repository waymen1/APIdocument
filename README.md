####*注意！当不能返回正确的数据时，接口都会返回:*
{
	status:"fail",
	errMsg:"相关错误的信息"
}
## 1.获取首页文章列表接口
#### 接口地址：http://域名/api/getIndexArticles/
#### 请求参数：
| 参数名   | 类型    | 必填  |描述 |
| :------:|:------:|:-----:|:---:|
| 无      | 无| 无 |无|
#### 请求示例：
http://localhost/api/getIndexArticles/
#### JSON返回示例：
{
	article:[
	    {
		    aid:3,
		    title:"xxxxxx",
		    image:"upload\/test.jpg",
		    categoryName: "猎物"
		},
	    {
		    aid:2,
		    title:"xxxxxx",
		    image:"upload\/test.jpg",
		    categoryName: "猎物"
		},
	    {
		    aid:1,
		    title:"xxxxxx",
		    image:"upload\/test.jpg",
		    categoryName: "推荐"
		}
	],	
	status:"sucess",
	errMsg:""
}



## 2.根据文章id获取某一篇文章的内容接口
#### 接口地址：http://域名/api/article/{aid}
#### 请求参数：
| 参数名   | 类型    | 必填  |描述 |
| :------:|:------:|:-----:|:---:|
| aid      | string | 是 |文章id|
#### 请求示例：
http://localhost/api/article/1
#### JSON返回示例：
{
	id:1,
	title:"xxxxxx",
	name:"author",
	image:"upload\/test.jpg",
	body:"\u003Cstrong\u003E我是正文\u003C\/strong\u003E",
	created_at: "2015-05-18 22:10:55",
	updated_at: "2015-05-18 22:10:55",
	tab:["霸气","酷炫","高大上"],
	status:"sucess",
	errMsg:""
}

## 3.查询用户拥有标签接口
#### 接口地址：http://域名/api/userTab/{uid}
#### 请求参数：
| 参数名   | 类型    | 必填  |描述 |
| :------:|:------:|:-----:|:---:|
| uid      | string | 是 |用户id|
#### 请求示例：
http://localhost/api/userTab/1
#### JSON返回示例：
{
	status:"success"，
	errMsg:"",
	uid:1,
	tab:[
	  {
	  	 "1":"猎物"
	  },
	  {
	  	 "2":"萌萌嗒"
	  }
	]
}

## 4.添加用户标签接口
#### 接口地址：http://域名/api/addUserTab/{uid}
#### 请求参数：
| 参数名   | 类型    | 必填  |描述 |
| :------:|:------:|:-----:|:---:|
| uid      | string | 是 |用户id|
| tabName  | string | 是 |用户id|
#### 请求示例：
http://localhost/api/userTab/1?tabName="猎物人"
#### JSON返回示例：
{
	status:"success"，
	errMsg:""
}

## 5.删除用户标签接口
#### 接口地址：http://域名/api/delUserTab/{uid}
#### 请求参数：
| 参数名   | 类型    | 必填  |描述 |
| :------:|:------:|:-----:|:---:|
| uid      | string | 是 |用户id|
| tabId  | string | 是 |标签id(通过查询用户标签接口获得)|
#### 请求示例：
http://localhost/api/userTab/1?tabId=1
#### JSON返回示例：
{
	status:"success",
	errMsg:""
}
