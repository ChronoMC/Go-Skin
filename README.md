# authlib-skin
轻量级的 Yggdrasil 服务端实现，后端 Go，前端 react。

适合于只需要用于 [authlib-injector](https://github.com/yushijinhun/authlib-injector) 的验证服务器的情况，部署简单。

实现了 [Yggdrasil](https://github.com/yushijinhun/authlib-injector/wiki/Yggdrasil-%E6%9C%8D%E5%8A%A1%E7%AB%AF%E6%8A%80%E6%9C%AF%E8%A7%84%E8%8C%83) 规范，可用于一些启动器中的外置登录，和服务器的外置登录。

## 特性
- 支持用于聊天签名的 /player/certificates 接口
- 支持于离线模式相同的方式生成用户 uuid（开启后不可更改用户名）
- 基本的用户管理
- Cloudflare Turnstile 支持

## 运行
`./authlibskin` 运行，`-c` 指定配置文件位置，若找不到配置文件，则会生成示例配置文件，其中带有注释。

## 编译 
`redis` 和 `sqlite` tag 控制是否开启 redis 和 sqlite 支持，使用 `sqlite` tag 需要 c 语言工具链。

请使用 build.sh 编译，会依次对前端和后端源码进行编译打包。
## 下载
https://github.com/xmdhs/authlib-skin/releases

## demo
https://skin.xmdhs.com

## todo

- 削减为仅一个非正版皮肤，允许绑定和导入正版皮肤（暂时不做）
- 披风？
- 使用日冕用户数据库认证，本地通过某独立服务向日冕请求认证（绑定并自动创建账户）
- 日冕注册邮箱查询皮肤站注册状态
- 关键的两方认证：日冕、微软（暂时不做）、QQ（异想天开）
- 。。。
