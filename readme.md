#### 引入常见错误
* 未引入依赖
* 查看是否有多个文件，一般引入文件为结尾包含*.min.*

#### 前端向数据库添加数据常见错误
* 添加的数据长度等不符合规范
* 复制粘贴是否修改 _id,保证数据干净可用
	

#### js控制属性坑
* jQ 获取disable属性，少部分可以用prop()方法获取,大部分用attr()


#### 常见提交小错误
* 表单提交
```js
//阻止默认提交行为
//未阻止将发送get请求
return false
```
>注意变量是否书写真确！

#### 上传图片需要再ajax中添加的参数
```js
processData:false,
contentType:false
```

#### 带字符串的数字比较
```js
console.log("44">"4")//true
console.log("44">"5")//false
```
#### 一次发送多个Ajax
```js
//when()中间的Ajax请求以逗号分隔
$.when( , , ).done(function(){})
```

#### 三种声名变量方法的区别

|声名	|区别						|
|--	 |-- |
|var	|存在声名提前->预解析		|
|let	|无与解析，变量上方存在死区	|
|const	|无与解析，声名常量			|
	
#### 三种本地地址区别
|符号	|作用				|
|-- |-- |
|/		|绝对路径，根目录	|
|./		|相对路径			|
|../	|上一级目录			|

#### 阻止some()
* 用 `return true`

#### 解决编辑器终端运行yarn被禁止
1. 管理员身份运行编辑器
2. 在终端中执行get-ExecutionPolicy，显示Restricted，表示状态是禁止的；
3. 这时执行set-ExecutionPolicy RemoteSigned；
4. 此时再执行get-ExecutionPolicy，显示RemoteSigned，则表示状态解禁，可以运行
