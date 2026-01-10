# Cherry Studio + Nano Banana Pro，在本地就能制作爆火的AI图


前段时间 Nano Banana Pro 火得一塌糊涂，其中"穿搭拆解图"在小某书上爆火 (见下图), 效果确实惊艳。
![[7.公众号/附件/小红书爆款.png]]
  
但是国内根本用不了 Google 的 Gemini 系列，需要科学上网。更烦的是，就算能连上 Google，还要解决账号、支付、额度一堆问题。

后来我发现了一个解决方案：通过 国内的API 中转站，就能在本地的 Cherry Studio 里就能直接用，全程不需要科学上网，配置也很简单。

  

## 三步搞定配置



### 第一步：下载 Cherry Studio

  

Cherry Studio 是国产开源的 AI 工具，完全免费、功能强大、持续更新。它支持接入各种主流的 AI 模型，包括大语言模型和生图模型。
官网：https://cherry-ai.com/
直接下载安装就行，Windows、macOS、Linux 全平台支持。

![[7.公众号/附件/官网介绍 1.png]]

### 第二步：注册 中转站注册API

  

打开 中转 API 站 注册账号。中转 API 站提供了很多主流模型的接口，包括 Google 的 Gemini 系列(包含了nano banana pro)、OpenAI 的 GPT 系列、Anthropic 的 Claude 系列等等。
ps: 我用的是 https://vibecodingapi.ai/register?aff=4zI3
![[7.公众号/附件/中转站模型.png]]


注册后进入控制台，找到 API Key 管理页面，创建一个新的 Key 并复制保存好。这个 Key 就是你的通行证，千万别泄露给别人。
ps: 中转站这里有个导入快捷方式: 按图中所示，点击聊天下面的按钮，选择cherry studio, 会一键将key导入cherry studio中。

![[7.公众号/附件/中转站模型配置.png]]

  

### 第三步：在 Cherry Studio 里配置


1. 打开 Cherry Studio，点击右上角的「设置」图标

2. 选择「模型服务」→ 在搜索框输入「VibeCodingAPI」

3. 填入刚才复制的 API Key

4. 在右下角点击「添加模型」，模型 ID 输入：`gemini-3.0-pro-image-preview`

5. 点击 API 密钥右侧的「检测」按钮，选择要检测的模型，等待 10 秒左右，显示「连接成功」就说明配置对了

6. 返回首页，在顶部模型栏选择 `gemini-3.0-pro-image-preview|New API`，就可以开始生图了

  ![[7.公众号/附件/香蕉模型配置.png]]


## 实测效果分享


### 穿搭拆解 实测

输入穿搭拆解的提示词, 然后我们上传一张原神中"胡桃"的角色图片, 香蕉模型开始执行
![[7.公众号/附件/生图前-胡桃.png]]

大约30s, "胡桃"的穿搭拆解图 就能生成完成了!
![[7.公众号/附件/生图效果-胡桃.png]]

  

## 更多提示词灵感

  

想找更多有趣的提示词？

  

1. 在各大社交媒体搜索「nano banana 提示词」，能看到很多网友分享的案例

2. 可以参考我往期 常用生图提示词库的文章：https://mp.weixin.qq.com/s/JNde7HzgW1PmNrLc2x-JTw

  
  

## 你学会了什么

  

- 如何在 Cherry Studio 中配置 Nano Banana Pro 的API

- 使用 Nano Banana Pro 生成高质量图片

- 生成穿搭拆解图

  

**下一步建议**：用自己喜欢的角色人物做穿搭拆解试试看呢

  
---

  

**小贴士**：中转站API 还支持很多其他模型，比如 GPT-5、Claude 4.5 系列（Opus、Sonnet、Haiku）、Grok 等，配置方法完全一样，只是模型 ID 不同。

如果文章对你有帮助可以帮忙**点个赞**, 帮助笔者有动力不断更新!
欢迎关注公众号: "蝈蝈的AI笔记" 里面有更多的干活内容