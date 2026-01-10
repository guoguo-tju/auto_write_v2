# 用这个“黑科技”姿势，免费白嫖 Claude 4.5 和谷歌最强生图模型nbp


你想用最顶尖的 Claude 4.5 帮着写代码，或者想试试谷歌的最强生图模型 Nano Banana Pro ，结果一查API的价格，心凉了半截？


但我最近发现了一个近乎“白嫖”的姿势，只要一个Google 账号，配上一个叫 CLIProxyAPI 的神器，就能直接捅进谷歌的Antigravity “反重力” 通道。


## 第一步：搞定 Google 反重力账号

Google推出了自家的IDE开发工具 Antigravity - "反重力"，可以免费使用Gemini 3 Pro以及Claude Sonnet 4.5模型, 只要你的 Google 账号能正常登录谷歌服务，基本上就已经默认拿到了这张通往顶级模型的入场券。
官网: https://antigravity.google/
  
![[7.公众号/附件/反重力.png]]

## 第二步：下载并安装 CLIProxyAPI
有了账号，接下来就是工具。去 GitHub 搜 CLIProxyAPI。这玩意的开发者是个狠人，直接把各种复杂的 CLI 工具包装成了咱们熟悉的 API 格式, 即 他把 CLI 里的能力“偷”出来，给到所有支持 API 的软件里去用
CLIProxyAPI地址: https://github.com/router-for-me/CLIProxyAPI

里面有官方的文档安装也极其简单，macOS 的用户直接用 brew 一键搞定，Linux 或者 Windows 用户也都有对应的安装包，基本上就是几分钟的事。

![[7.公众号/附件/cliproxyapi快速开始.png]]

## 第三步：执行反重力 OAuth 登录

安装完别急着运行，咱们得把那个“反重力”的通道打开。

你要在终端里甩出那个带 \`--antigravity-login\` 后缀的命令。如果你对登录参数有疑问，可以参考这个官方说明：[反重力配置文档](https://help.router-for.me/cn/configuration/provider/antigravity.html)
![[7.公众号/附件/screenshot-20260110-160318.png]]


这时候会自动跳出一个 Google 授权页面。如果页面半天刷不出来，先别急，看看你的梯子是不是开了全局模式或者TUN模式。授权成功后，CLIProxyAPI 就会在本地帮你撬开那扇通往“反重力”通道的暗门。

  
  

## 第四步：验证成功，开启顶级模型体验

服务跑起来之后，有个web页面,  本地访问: http://localhost:8317/management.html#/system, 
可以看到可用的顶级模型
![[7.公众号/附件/哪些模型.png]]

然后打开 本地的Cherry Studio来验证，添加自定义供应商，key填你自己定义的; API地址填 \`http://localhost:8317`， 再验证是否联通

  ![[7.公众号/附件/cherry验证.png]]

试试生图模型 Nano Banana Pro。你直接甩给它一句话，直接出图成功, 大功告成!

![[7.公众号/附件/生图成功.png]]



## 最后

以上就是利用反重力来白嫖顶级模型的方法了，薅羊毛方法我摆在这儿了。别在那儿观望了，赶紧去占尝试吧。


如果文章对你有帮助可以帮忙**点个赞**, 帮助笔者有动力不断更新!

欢迎关注公众号: **"蝈蝈的AI笔记"** 里面有更多的干活内容。