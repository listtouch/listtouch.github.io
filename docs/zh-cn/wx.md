## 微信端数据请求与接口说明
### 首页
```
 url: /app/index/index 对应的是 app/controller/app 目录下的 index控制器的 index 方法
 
 ``` 
 ### 搜索
 ```
 url: /app/product/index 对应的是 app/controller/app 目录下的 product控制器的 index 方法
 mothed:get
 params: name||输入的关键字  
 
 ``` 
 ### 商品详情
  ```
 url: /app/product/detail 对应的是 app/controller/app 目录下的 product控制器的 detail 方法
 mothed:get
 params: id||商品id  
 
 ``` 
 ### 获取分类
   ```
 url: /app/menu/index 对应的是 app/controller/app 目录下的 menu控制器的 index 方法
 mothed:get
 
 ``` 
 ### 加入购物车
   ```
 url: /app/user/addToCart 对应的是 app/controller/app 目录下的 user控制器的 addToCart 方法
 mothed:POST
 params: id||商品id,num||数目
 返回值  {data: 2, msg: "操作成功", code: 1}
 
 ``` 
### 获取分类下的商品
   ```
 url: /app/product/index 对应的是 app/controller/app 目录下的 product控制器的 index 方法
 mothed:get
 params: menu_id||分类id
 ``` 
 ### 商品排序
    
 ```
    url: /app/product/index 对应的是 app/controller/app 目录下的 product控制器的 index 方法
    mothed:get
    params: menu_id||分类id,sort||visit_desc(人气倒序)visit_asc(人气正序)sale_asc(销量正序)sale_desc(销量倒序)
 ``` 
 ### 获取购物车列表
  ```
    url:/app/cart/index 对应的是 app/controller/app 目录下的 cart控制器的 index 方法
    mothed:get
 ``` 
### 购物车中增加商品的数目
```
 url:/app/cart/index 对应的是 app/controller/app 目录下的 cart控制器的 index 方法
 mothed:get
 params: rec_id(购物车数据的id) goods_number(该条数据商品的数目)
 返回值 {data: 3, msg: "76.01"}  (data为商品总数目，msg为总价格)
 ``` 

 ### 删除购物车中商品
 ```
 url:/app/cart/del 对应的是 app/controller/app 目录下的 cart控制器的 del 方法
 mothed:get
 params: id(商品的id) 
```
### 商品收藏
```
 url:/app/user/addeCollection 对应的是 app/controller/app 目录下的 user控制器的 addeCollection 方法
 mothed:get
 params: id(商品的id) 
 返回值 {data: "data", msg: "取消收藏成功", code: 0}
```
### 立即结算
```
 url:/app/user/addeCollection 对应的是 app/controller/app 目录下的 order控制器的 confirm 方法
 mothed:get
```
### 订单提交

```
 url:/app/order/submission 对应的是 app/controller/app 目录下的 order控制器的 submission 方法
 mothed:get
```

### 个人中心

```
 url:/app/user/index 对应的是 app/controller/app 目录下的 user控制器的 index 方法
 mothed:get
```
### 全部订单


```
 url:/app/order/index 对应的是 app/controller/app 目录下的 order控制器的 index 方法
 mothed:get
```
### 订单详情
```
 url:/app/order/detail 对应的是 app/controller/app 目录下的 order控制器的 detail方法
 mothed:get  
 params:id(订单id)

```
### 订单取消
```
 url:/app/order/cancel 对应的是 app/controller/app 目录下的 order控制器的 cancel方法
 mothed:get  
 params:id(订单id)
 返回值 {data: "", msg: "", code: 0}
```
### 余额·订单支付
```
 url:/app/order/pay 对应的是 app/controller/app 目录下的 order控制器的 pay方法
 mothed:get  
 params:id(订单id)
 返回值 支付成功 {data: "", msg: "", code: 0} 失败:{data: "", msg: "", code: 1}

```
### 支付宝支付 与用户充值
```
 url:/app/pay/alipay/index 对应的是 app/controller/app/pay 目录下的 alipay控制器的 index方法
 mothed:get  
 params:id(订单id),type(1支付，2充值)
 
```

### 微信支付 与用户充值
```
 url:/app/pay/wxpay/index 对应的是 app/controller/app/pay 目录下的 wxpay控制器的 index方法
 mothed:get  
 params:id(订单id),type(1支付，2充值)
```

### 收藏列表

```
 url:/app/user/collection 对应的是 app/controller/app 目录下的 user控制器的 collection方法
 mothed:get  
```

### 不同状态的订单
```
 url:/app/order/index 对应的是 app/controller/app 目录下的 order控制器的 index 方法
 mothed:get  
 params: status(-1已取消，0待发货，2已完成)
```
### 提交评论
```
  url:/app/user/comment 对应的是 app/controller/app 目录下的 user控制器的 comment 方法
 mothed:post  
 params: content(内容) order_id（订单id） rank(星级)
```
### 申请提现
```
    url:/app/user/withdrawals 对应的是 app/controller/app 目录下的 user控制器的 withdrawals 方法
  mothed:post
  params:money(金额) account(内容)
```
### 新增收货地址
```
    url:/app/user/editconsignee 对应的是 app/controller/app 目录下的 user控制器的 editconsignee 方法
  mothed:post
  params:name(名称) phone(手机号) province(省) district(市) address（地址）
```
### 收货地址列表
```
    url:/app/user/consignee 对应的是 app/controller/app 目录下的 user控制器的 consignee 方法
  mothed:get
  params: consignee_back
```
### 收货地址设为默认
```
    url:/app/user/setDefaultConsignee 对应的是 app/controller/app 目录下的 user控制器的 setDefaultConsignee 方法
  mothed:get
  params: id(地址id)
```
### 删除地址
```
    url:/app/user/delconsignee 对应的是 app/controller/app 目录下的 user控制器的 delconsignee 方法
  mothed:get
  params: id(地址id)
```
### 退出
```
    url:/app/public/logout 对应的是 app/controller/app 目录下的 public控制器的 logout 方法
  mothed:get
```
### 登录
```
    url:/app/public/login 对应的是 app/controller/app 目录下的 public控制器的 login 方法
  mothed:post
  params: username password
```
### 获取验证码
```
 url:/app/public/send_sms 对应的是 app/controller/app 目录下的 public控制器的 send_sms 方法
  mothed:get
  params: phone
  返回值 失败 {data: "发送失败", code: 0} 成功{data: "发送失败", code: 1}
```
### 注册
```
  url:/app/public/register 对应的是 app/controller/app 目录下的 public控制器的 register 方法
  mothed:post
  params: username password phone verify
```