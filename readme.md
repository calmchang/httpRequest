

# 常见ajax请求

预览地址:https://m.vuedata.cn/httpRequest

## 目录  
1. Get请求   
2. Content-Type为`application/json`的Post请求    
3. Content-Type为`application/x-www-form-urlencoded`的Post请求
4. Content-Type为`text/plain`的Post请求  
5. Content-Type为`multipart/form-data`的Post请求
6. 上传文件
7. Content-Type为`text/xml`的Post请求    


## HOST
案例中使用的测试接口地址：https://m.vuedata.cn/ndapp/httpTest

## 请求参数
所有案例request数据以下面为测试数据：  

```json
let params={
  name:'tom',
  arr:['a','b','1']
};
```

## 常规GET请求  
URL:/get  
Method:GET  

## 常规post调用,包括`application/json`、`application/x-www-form-urlencoded`、`text/plain`  
URL:/post    
Method:POST    



## formdata数据  
URL:/postform  
Method:POST  
RequestParams:  
let form = new FormData();  
form.append('name','tom');  
form.append('city','shanghai');  


## 上传文件    
URL:/postform  
Method:POST  
RequestParams:  
let form = new FormData();  
form.append('name','tom');  
form.append(file,文件数据);

## XML数据    
URL:/xml  
Method:POST  
RequestParams:    
```xml
<xml> 
  <ToUserName><![CDATA[gh_7f089789a]]></ToUserName>  
  <FromUserName><![CDATA[oia2TjuNoeX76QEjQNrcURxG8]]></FromUserName>  
  <CreateTime>1395620</CreateTime>  
  <MsgType><![CDATA[event]]></MsgType>  
  <Event><![CDATA[TEMPLATESENDJOBFINISH]]></Event>  
  <MsgID>200163836</MsgID>  
  <Status><![CDATA[success]]></Status> 
</xml>
```

## Response
请求成功后，返回的数据将包含请求的内容以及服务端解析后的数据内容

## 要求
1、创建一个index.html页面
2、在页面中使用js原始XMLHttpRequest对象完成接口正确调用,
3、关键字`XMLHttpRequest`、`<input>`、`FormData`

axios：https://www.npmjs.com/package/axios


