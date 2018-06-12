!> www端访问路径 域名/admin  账号密码 admin/admin
### 登录
```
 url: /admin/public/login 对应的是 app/controller/admin 目录下的 public控制器的 login 方法
 mothed为get时进入登录页面
 mothed为post时 参数：username || 用户名, password ||密码, verify||验证码
 登陆成功跳转到管理端首页，失败不跳转
 ```
 管理端其他请求与登录类似，不在说明


