## app端接口
>在app的代码中,将 app/util/config.json中的路径替换为自己的url

### 首页接口
```
 /api/index/index
``` 
### 菜单接口：
```
    /api/menu/index
```    
### 商品列表，带搜索
```
 /api/product/index
    类型：get
    搜索传值：? name = '苹果'
    商品分类：? menu_id＝'1'
    排序字段：? sort  = 'rank'
    排序类型：? type = 'desc'        或者       ' asc'
```    
### 商品详情：
```
    /api/product/detail
    类型：get
    接收参数：?id = '商品id'
```    
### 商品收藏：
```
  /api/user/addcollect
    类型：get
    接收参数：?id = '商品id'
```    
### 取消收藏
```
  /api/user/delcollect
    类型：get
    接收参数：?id = '收藏id'
```    
### 搜索页面
```
 /api/product/searchlist
    //热门搜索hot
    //我的最近搜索my
```    
### 获取商品评论列表
```
/api/product/comment
    类型：get
    接收参数：?id='商品id' & star='星星数' 
```    
### 获取购物车列表
```
/api/cart/index
```
### 直接添加到购物车
```
/api/cart/add
    类型：get
    接收参数：商品id
```    
### 清空购物车
```
/api/cart/del
    类型：get
    接收参数：购物车id，不传参数全部清空
```    
### 发送短信验证码接口
```
/api/public/sendsms
    类型：get
    接收参数：phone
    返回数据：{uuid:'',msg:"发送成功"}
```    
### 用户注册接口
```
/api/public/register
    类型：post
    接收参数：phone、password、uuid、code
```    
### 用户重置密码接口
```
   /api/public/resetpassword
    类型：post
    接收参数：phone、password、uuid、code
```    
### 订单列表
```
    /api/order/index
    类型：get带分页
    接收参数：?status=''&page=''
```    
### 订单详情
```
    /api/order/detail
        类型：get
        接收参数：?id=''
```        
### 个人中心
```
  /api/user/index
    类型：
    返回参数：
    user: 用户信息
    collection_count: 2,收藏数
    msg_count: 0,信息数
    history: 历史
    to_recieve: 3,待收货
    to_comment: 0待评论
```    
### 消息中心
 ```  
   /api/user/message
    类型：get
 ```   
### 商品收藏列表
```
   /api/user/collect
    类型：get
```    
### 下订单接口
```
 /api/order/add
    类型：
    接收参数：        
    const cart = [{id:1,num:1},{id:2,num:2}];商品
        const payment_id = 1;付款方式
        const contact_id = 10;配送地址
```
### 取消订单
```
/api/order/cancel
    类型：get
    接收参数： ?id='订单id'
```
### 取消订
```
 /api/order/exchange
    类型：get
    接收参数： ?id='订单id'&product_id＝'商品id'
    类型：post
    接收参数： order_id='订单id'
              product_id＝'商品id'
              reason_id＝'原因'
              remark＝'理由'
```              
### 设置个人资料
```
   /api/user/personaldata
    类型：get
    接收参数： 
    类型：post
    接收参数： phone='手机号'
```    
### 商品评价
```
   /api/user/comment
    类型：post
    接收参数： order_id='订单id'
              rank＝'星星'
                  content＝'内容'
```                  
### 确认订单页面
```
  /api/order/confirm
    类型：get
    接收参数：
```    
### 地址列表
```
 /api/user/contactlist
    类型：get
    接收参数：
```    
### 设置默认地址
```
  /api/user/setcontact
    类型：get
    接收参数：?contact_id=''
```    
### 新增或修改收货地址
```
  /api/user/addcontact
    类型：get
    接收参数：?id='contact_id'
    类型：post
    接收参数：province、city、district、address
```
### 删除收货地址
```
/api/user/delcontact
    类型：get
    接收参数：?id='contact_id'
```    
### 支付接口
```
/api/order/pay
    类型：get
    接收参数：?id='order_id'
```    
### 头像上传接口
```
/api/user/set_avater
    类型：
    接收参数：
```    
### 登陆后修改密码
```
   /api/user/resetpassword
    类型：post
    接收参数：password、repassword
```    
### 申请提现
 ```
 /api/user/withdrawals
    类型：get 获取提现金额
    接收参数：
    类型：post
    接收参数：money、account
```    
### 账户明细
```
    /api/user/detail
        类型：get 
        接收参数：
```        
### 申请记录
```
    /api/user/apply
        类型：get 
        接收参数：
```        
### 完成订单
```
  /api/order/finish
    类型：get 
    接收参数：?id='订单id'
```    
### 支付宝充值
 ```
 /api/user/recharge
    类型：post
    接收参数：money、payment_id(2微信3支付宝)
```    