## 一.Get请求

​	//获取所有用户信息

​	http://localhost:3000/users

​	//获取id为1的用户信息

​	http://localhost:3000/users/1

​	//获取公司的所有信息

​	http://localhost:3000/companies

​	//获取公司为1的用户信息

​	http://localhost:3000/companies/3/users

​	//根据公司名字获取信息

​	http://localhost:3000/companies?name=Microsoft

​	//根据多个名字获取公司信息

​	http://localhost:3000/companies?name=Microsoft&name=Apple

​	//获取一页中只有两条数据

​	http://localhost:3000/companies?_page=1&_limit=2

​	//升序排序 asc（desc降序）

​	http://localhost:3000/companies?_sort=name&_order=asc

​	//获取年龄30及以上40以下的

​	http://localhost:3000/user?_age_gte=30&age_lte=40
​	//搜索用户信息

​	http://localhost:3000/user?q=h

## 二.监听jsonserver

##### 	2.1 Install JSON Server

```json
npm install -g json-server
```

##### 	2.2 Create a `db.json` file with some data

```json
{
  "posts": [
    { "id": 1, "title": "json-server", "author": "typicode" ,"title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
      "body": "quia et suscipit\nsuscipit recusandae consequuntur expedita et cum\nreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem sunt rem eveniet architecto"}
  ]
```

##### 	2.3 Start JSON Server

```json
json-server --watch db.json
```

##### 	2.4 启动本地网址

​	http://localhost:3000/posts