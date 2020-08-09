## CSRF

跨站请求伪造(Cross-site request forgery,简称 CSRF)， 是一种挟制用户在当前已登录的 Web 应用程序上执行非本意的操作的攻击方法

#### CSRF 示例

- 其内容为

```
<!--仅用于演示，假设该点赞为 GET-->
<img src="https://segmentfault.com/api/article/1190000019050946/like?_=0faa0315ff95872d8b0f8da02e343ac7">
```

- 诱使目标用户访问页面P

如果你已经访问过 SF 网站，并且已经登录。可以看到在访问页面P之后，已经对 SF 文章进行点赞了

#### CSRF 防御

- 增加验证码(简单有效)
- 检查请求来源是否合法
- 增加随机 token