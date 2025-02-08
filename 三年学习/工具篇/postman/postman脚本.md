## 场景1：提取响应体中json的数据，保存到全局变量

给定的条件：响应体中的数据是文本形式保存的json数据  



```javascript
var result=Json.parse(responseBody) //将字符类型转化为Json格式  
pm.globals.set("access_token",results.access_token) //将result中的access_token的住保存到名为access_token的全局变量中
```

使用正则表达式  

```javascript
var result=responseBody.match(new RegExp(正则表达式))  
pm.globals.set("access_token",results[1])
```

# 场景2：提取响应头中的数据

```js
var result=pm.reponse.headers.get("key")  
```

# 场景3：某些参数需要到随机数

## 内置动态参数

{{$timestamp}} 当前时间的时间戳  

{{$randomInt}} 返回1-1000的随机整数  

{{$guid}} 随机的很长的字符串  

## 自定义的动态参数

在pre-request script 模块去定义-》设置成全局变量  

js脚本

# 场景4：参数化  全部运行时选择数据文件






