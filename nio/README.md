# 蔚来
## 配置 (QuanX)

```properties
[MITM]
app.nio.com

[rewrite_local]
^https:\/\/app\.nio\.com\/api\/1\/app\/daily_checkin url script-request-header https://raw.githubusercontent.com/makereleven/QuantX-scripts/master/nio/nio.cookie.js

[task_local]
1 0 * * * https://raw.githubusercontent.com/makereleven/QuantX-scripts/master/nio/nio.js
```

## 说明

3. 打开 APP[蔚来](https://apps.apple.com/cn/app/%E8%94%9A%E6%9D%A5/id1116095987) 然后手动签到 1 次, 系统提示: `获取Cookie: 成功`
4. 最后就可以把第 1 条脚本注释掉了
5. 运行一次脚本, 如果提示重复签到, 那就算成功了!

> 第 1 条脚本是用来获取 cookie 的, 用浏览器访问一次获取 cookie 成功后就可以删掉或注释掉了, 但请确保在`登录成功`后再获取 cookie.

> 第 2 条脚本是签到脚本, 每天`00:00:10`执行一次.

## 感谢

[@chavyleung](https://github.com/chavyleung)