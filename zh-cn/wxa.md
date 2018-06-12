## 小端数据请求与接口说明

### 首页
```
    url: /wxa/index/index  对应的是 app/controller/wxa 目录下的 index控制器的 index 方法
    method:get
    返回值  data:{adslist:[{id: 7, position_id: 3, name: "全球尖货", sub: "", file_id: 674,…}],hot:[{id: 184, category_id: 44, albums_id: "1814", labels_id: ",3,", file_id: 1814, name: "马利宝",…}],product:[{id: 184, category_id: 44, albums_id: "1814", labels_id: ",3,", file_id: 1814, name: "马利宝",…}]}
```

### 搜索
```
    搜索：/wxa/product/index 对应的是 app/controller/wxa 目录下的 product控制器的 index 方法
    类型：get
    搜索传值：? name = '苹果'
    商品分类：? menu_id＝'1'
    排序字段：? sort  = 'rank'
    排序类型：? type = 'desc'        或者       ' asc'
```    

### 菜单接口
```  
  url：/wxa/menu/index 
  method:get
```  


### 详情 

```
    url: /wxa/product/detail
    method：get
    参数：?id = '商品id'
```    
、
### 添加购物车接口

```
    url：/wxa/user/addToCart 
    method： post
    params： goods_id：4 (商品id) number:2(商品数目) ids: 4-5-6(商品sku的id集合)
    返回值：{data: 3, msg: "操作成功", code: 1}
```


### 获取购物车的接口

```
    url：/wxa/cart/index 
    method:get
```
### 更新购物车数据 

```
    url：/wxa/cart/changeGoodsNumber
   	method： post
    params：goods_number:"7" (数目) rec_id:235(数据id)
    return：{data:18，msg:"359.20"}   
```       

### 获取商品评论列表

```
    url /wxa/product/comment 
    method: get
```
### 新增或修改收货地址
 
 ```
    url: /wxa/user/addcontact
    method：get
    params：?id='contact_id'
    method：post
    params：province、city、district、address
```    
### 删除购物车 
``` 
    url:/wxa/cart/del 
    method:get
    params:?id='id'
```
### 地址列表
```
    url:/wxa/user/contactlist
    method：get
 ```  
### 小程序登录 
```  
    url:/wxa/public/wxaLogin
    method:post
    params:{code:"011umq44056SwC1VF25401do440umq4e",encryptedData:"Iq1M1i7pDrOXAGmLTMpJi/+D3iZLHk3sFH02WsfrLFSzQVCfrHZxxzvTbwlqwkrt4DhY+HVyJdemYlzobTaj1ZIYw4hf4f9Zbq9qEDVhJr/fwRCjF4hJfODgPBMc4pXq82nut1Do+/w+0Op4DWsX9ifqj8pAcNnCoIqPKcWZblZ4WKmcpzy+A004dgO1CQEIjFE8rDEMrlm2esUmqnYpWtHwIm8VY0dmt+VexLckt+Lr9I/aIrhfyKYRssJHRC2C4NHtehOcettl/cOkHEkyYnA+/sfMwwpeifCZ+l+vYH6GsoJ9pKUkbKu9U1HMLUNtxDPTHvZ5CwiiApaf1RAWgRX6CMotd2jqMXw6l0yzLj4e5n+/pKFJmzYdxkQiaHwcb/euF4HqVrpCujvUEJSMH91xamMEygAzs/Kh29/DNM9FJ/r5+RfACbaBaRohAJ+zXio4Z76TPiQSYzeH4dDbI8hdBiW8m/k/ZcmAIbs+MjE=",iv:"Y1+BeXX+ydrLM53HsbB+iw=="}

    返回值： {token:"jwt用于验证的token",user:"用户信息"} 
```
### 订单支付
```
  url:/wxa/pay/wxpay/index
  method:get
  params:'?id=订单id'
  返回值 {timeStamp:"时间戳",nonceStr:"",package:"",signType:"MD5",paySign:"签名"}


``` 
### 订单详情
```
    /wxa/order/detail
        类型：get
        接收参数：?id=''
``` 

### 取消订单
```
/wxa/order/cancel
    类型：get
    接收参数： ?id='订单id'
```
### 下订单接口
```
 /wxa/order/add
    类型：
    接收参数：        
    const cart = [{id:1,num:1},{id:2,num:2}];商品
        const payment_id = 1;付款方式
        const contact_id = 10;配送地址

```

### 完成订单
```
  /wxa/order/finish
    类型：get 
    接收参数：?id='订单id'
```   

### 订单列表
```
    /wxa/order/index
    类型：get带分页
    接收参数：?status=''&page=''
```   