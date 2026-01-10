
先介绍下Claude Code是什么, 为什么要用Claude Code, 他有什么优势?
  

## **第一步：准备工作**

### **1.1 安装 Claude Code**

### 方案一（Claude code 官方推荐方式）

如果你按照我下面推荐的安装方式（Mac 的 curl 命令或 Windows 的 PowerShell 命令），不需要提前安装 Node.js。



**Mac 用户**：

1. 打开「终端」（Terminal）- 在启动台里搜索就能找到。终端是一个使用命令让电脑干活的方式，只需要会复制粘贴，按回车，就可以用。
    
2. 复制这行命令，粘贴进去，回车：
    

```Bash
curl -fsSL https://claude.ai/install.sh | bash
```

  

**Windows 用户**：

3. 点击开始菜单，搜索「PowerShell」，右键选择「以管理员身份运行」
    
4. 复制这行命令，粘贴进去，回车：
    

```PowerShell
irm https://claude.ai/install.ps1 | iex
```

  

安装过程会自动下载，等个 1-2 分钟就好。

**安装完成的标志**：会提示「Claude Code installed successfully」。

---

  

### **1.****2****你需要一个 Claude 账号**

唯一的门槛，就是搞定一个能在 Claude code 里用的账号。

可以这样理解 Claude code：它是一个工具，Claude code 和大模型的关系，就像手机和运营商的关系。你的手机可以选电信、联通、移动，都能打电话上网， Claude code 就相当于手机，大模型就相当于运营商，你可以在 Claude code 使用各种模型，你只需要为大模型付费。

Claude 官方会直接封中国用户的账号，所以使用官方账号门槛很高。

推荐使用中转方案，或者用国产大模型平替。

如何选择？如果追求效果最好，选中转；如果追求简单方便，选国产大模型。

|方案类型|名称|链接|
|---|---|---|
|中转<br><br>（中转的意思是，你的请求会发送到中转服务商那里，然后它再请求 Claude 官方，所以你不用担心封号、梯子之类的问题）|GACcode|[购买 Claude Code 账号-手把手教程](https://larkcommunity.feishu.cn/docx/Trszd77MEoEM9lxcnJKcf4Gxn3c)|
|Lion CC|Claude code、codex 拼车：https://codecodex.ai （下单备注 ben 即可）|
|AIcodewith|https://aicodewith.com/?invitation=Q71I6P|
|国产大模型|DeepSeek|Deepseek 官方教程：https://api-docs.deepseek.com/zh-cn/guides/anthropic_api|
|智谱 GLM|智谱 AI 编程套餐： https://www.bigmodel.cn/claude-code?ic=U5NGPIMKRG|
|Kimi K2|https://zhuanlan.zhihu.com/p/1965040472201335898|
|MiniMax|https://platform.minimaxi.com/docs/guides/text-ai-coding-tools#%E5%9C%A8-claude-code-%E4%B8%AD%E4%BD%BF%E7%94%A8-minimax-m2%EF%BC%88%E6%8E%A8%E8%8D%90%EF%BC%89|


用 DeepSeek 给大家做一个简单的演示 (todo: 演示改成用智谱GLM的)：

|   |   |   |
|---|---|---|
|步骤|描述|截图|
|第一步|- 打开 DeepSeek 开放平台：https://platform.deepseek.com<br>    <br>- 注册 DeepSeek 账号并登录|![](https://waytoagi.feishu.cn/space/api/box/stream/download/asynccode/?code=ZWYzYTA2NzUyODdkYTkyYzgyNzI0YWZmYjYyZjhlZmZfaElsaGUxbnQ0U2ZIUVpNQWxCWHpjOEtQbHM0aVdHWlJfVG9rZW46SWFKZWJFUTlYb210V0J4eGlaUmNtYmFMbkdlXzE3NjU5NzI1NTA6MTc2NTk3NjE1MF9WNA)|
|第二步|- 获取 API：https://platform.deepseek.com/api_keys<br>    <br>- 新建一个 APIkey，名字随便取<br>    <br>- 复制 API key|![](https://waytoagi.feishu.cn/space/api/box/stream/download/asynccode/?code=ZDBmZDdhYzk0MzI2NThiOWY3ODhmNDc5ZDRlMjk0Y2ZfTXV5TVVlcmxoS3JzZGFmVzI2SVBNaVBNNXFKajdwdmRfVG9rZW46U3VqaWJuaUYyb2JVc2N4UlNnWmMzbHdjbmloXzE3NjU5NzI1NTA6MTc2NTk3NjE1MF9WNA)<br><br>![](https://waytoagi.feishu.cn/space/api/box/stream/download/asynccode/?code=MTFhM2VjN2I0MmJmODVmZmY5Y2RmZTE0ZGE2ODc4NmVfNUlxRDZtamJkendqdUZlTVZ4WmFMQXdHOWFzeDBhbEdfVG9rZW46SW9EWWJCa3RJb3ZzUWx4OHdVMWN2Y2VvbldnXzE3NjU5NzI1NTA6MTc2NTk3NjE1MF9WNA)|
|第三步|在 Claude code 里使用：<br><br>- 复制以下所有的内容，把第二行里的 `DEEPSEEK_API_KEY` 换成你上一步生成的 APIkey，其他不要动<br>    <br><br>```Bash<br>export ANTHROPIC_BASE_URL=https://api.deepseek.com/anthropic<br>export ANTHROPIC_AUTH_TOKEN=DEEPSEEK_API_KEY<br>export API_TIMEOUT_MS=600000<br>export ANTHROPIC_MODEL=deepseek-chat<br>export ANTHROPIC_SMALL_FAST_MODEL=deepseek-chat<br>export CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC=1<br>```<br><br>- 粘贴到命令行里，然后按回车键。按回车<br>    <br>- 之后，不会有任何反馈，这是正常的。<br>    <br>- 然后输入 Claude，按回车，就可以进入 Claude code 了！（中间会有一些让你确认的，选 yes，继续就 OK）<br>    <br>- 左上角如果能看到 DeepSeek-chat，就说明用的就是 DeepSeek。|![](https://waytoagi.feishu.cn/space/api/box/stream/download/asynccode/?code=NzY2ZjY2ZjU4MmYwM2VmNzQ5MTAzYTlkY2YxZGQ3ZDRfZkpqcUxjbkRSMURWcHo5eWxta1FRWmhXUHlRbGlxV1JfVG9rZW46TVdNSWJmM2hlbzF3aVh4TmxEQmNhNXRybkxkXzE3NjU5NzI1NTA6MTc2NTk3NjE1MF9WNA)<br><br>![](https://waytoagi.feishu.cn/space/api/box/stream/download/asynccode/?code=MjQzMGRhZGUyYjQzNWUwYjFlZDY1YzE0NTBhZTg0ZDJfdkxaMUdKa1M5RXhYQ3BhS1ZpdkNVSVVnanFpMWtxWTNfVG9rZW46WDY1eWIxbUlmb3Zld0d4Y3FZUmNDOENGbjdnXzE3NjU5NzI1NTA6MTc2NTk3NjE1MF9WNA)|

其他大模型，也是类似于这样的流程去获取 API key 使用。

todo: 这里单独起一小节介绍下 cc Switch

如果需要多个大模型来回切换，可以使用 cc Switch：https://github.com/farion1231/cc-switch



### 1.3 降低上手门槛：安装 Claude code for vs code 插件

使用终端、命令行还是挡住了非常多的朋友，这个时候，有个界面很重要！

Claude code、Codex 官方也都推出了插件，安装即可使用。

#### 第一步：安装 vs code / 或者trae / cursor

https://code.visualstudio.com/

在 vs vode 官网下载安装，免费的

  

#### 第二步：安装插件

点击链接：https://marketplace.visualstudio.com/items?itemName=anthropic.claude-code，会自动跳转到 vs code 安装。

或者在 vs code 插件市场搜索「Claude code」，即可安装

![](https://waytoagi.feishu.cn/space/api/box/stream/download/asynccode/?code=OWE3ZmNmMmQxNzdiNGNiZDRlNzZmMWYxNjM0OTI3Y2ZfU2tKWnlVd005Wmc0UkxlN3VmT3pPZVRRRzFqUWtlTGJfVG9rZW46R28yQWJLNGNFb2ZKZkx4UmdWU2NXbVI1bkxOXzE3NjU5NzI1NTA6MTc2NTk3NjE1MF9WNA)

#### 如何使用

安装完之后，点击 Claude code 图标，即可使用。

![](https://waytoagi.feishu.cn/space/api/box/stream/download/asynccode/?code=M2Q2NzNhZjAzYjViMWU4ZjM5ZDMzN2ZhM2FiNDg0ODlfWVJqR0JjeHJmMm1XSnVWMVpOVUs3WTRHQ3NzbDhrR3FfVG9rZW46RlJjUmJHMmdPbzFEd014c0RvYmNMQVlmbmNnXzE3NjU5NzI1NTA6MTc2NTk3NjE1MF9WNA)

这个时候配置base url 和 api key 比较麻烦，可以用 cc [Switch](https://waytoagi.feishu.cn/wiki/WZZRwjxAbiNow5ki0s6clQNLnsb#share-HJv3dKW7Co1mMcx1tp4cNA75nme) 去配置：

- 在 cc Switch 里勾选应用到 Claude code 插件，然后重新启动 vs code。
    

![](https://waytoagi.feishu.cn/space/api/box/stream/download/asynccode/?code=MmFlMTZhNzg5ZjNmYTgyZTViYzQ0YTg5ZjNkZmViYzJfOUtITHVrZHJLSjZlS01hY28wZmJkdW80YmU1c0pwcmhfVG9rZW46RDRLZGJiWndvb1k2T1R4Yzlrc2N3ZlprbjJkXzE3NjU5NzI1NTA6MTc2NTk3NjE1MF9WNA)![](https://waytoagi.feishu.cn/space/api/box/stream/download/asynccode/?code=ODc0MWQ3YzU0Y2U3ZjZmNmIwYzZiODYwNDBlYjQ4NmNfdElwSHoyelJSbnFkRUh3WVNIWjVEakRsbk9OMllFZlBfVG9rZW46RGFqRWJnSzhib0JGUFR4MXVBZmM4Y3V2bkxmXzE3NjU5NzI1NTA6MTc2NTk3NjE1MF9WNA)

#### 开启 Claude code 全自动模式

默认状态下，Claude code 只能在 plan、手动确认、自动编辑三种模式选择，可以在 cc 插件里开启「Allow Dangerously Skip Permissions」，这样能开启全自动模式，cc 能自动运行命令，无需二次确认。下面的选项里，也可以把全自动模式配置为默认模式。

![](https://waytoagi.feishu.cn/space/api/box/stream/download/asynccode/?code=NGM5ZDhlNjdkZjhlODdjMmQyZTQ3ODgzODQ4NjY4ZDRfdXd2enBvZEx1QmI0STdmUzB6OWN6UFFOVWhSaXJ2aGVfVG9rZW46TzA0N2JVMEc2bzVQcXR4b1RNQWNOcmVrblNnXzE3NjU5NzI1NTA6MTc2NTk3NjE1MF9WNA)

plan mode - 讨论, 不会写代码, 做调研和计划, 写文档可以用
bypass permission - 全自动模式, 写代码运行命令删除文件 会自动执行
ask before edits - 写代码和运行命令要你二次确认
edit automatically - 写代码自动, 运行命令要二次确认


#### 开启 Claude code 的常用指令
  

# _启动_

claude

  

# _创建项目_

mkdir project-name

cd project-name

claude

  

# _常用命令_

/help _# 查看帮助_

/rewind _# 回退版本_

/clear _# 清空对话_

/exit _# 退出_

  

todo: 上面就是第一篇文章的部分了; 下面的实操放在第二篇文章


## **第二步：做你的第一个作品**

  

### **2.1 我们要做什么？**

  

我建议第一个项目做「待办清单」。

为什么？

  

- 够简单，15 分钟能完成
    
- 够实用，做完了真的能用
    
- 够完整，该有的功能都有（增删改查）
    

**最终效果是什么样？**

  

一个网页，你可以：

- 添加任务
    
- 标记任务完成
    
- 删除任务
    
- 界面干净好看
    

### **2.2 创建项目文件夹**

  

还是在刚才的终端里，输入：

```Bash
mkdir my-todo-app
cd my-todo-app
claude
```

  

解释一下：

- `mkdir my-todo-app`：创建一个叫「my-todo-app」的文件夹
    
- `cd my-todo-app`：进入这个文件夹
    
- `claude`：启动 Claude Code
    

现在你在 Claude Code 里了，可以开始对话。

  

### **2.3 最重要的一步：先规划再动手**

  

直接让 AI 写代码，容易一团乱。

聪明的做法是先让它给你一个计划，看清楚要做什么，再开始写代码。

  

**复制这段话，发给 Claude**：

  

```Plain
我想做一个待办清单网页，要求：
1. 可以添加新任务（输入框+添加按钮）
2. 可以点击任务标记为完成（会有划线效果）
3. 可以删除任务（每个任务旁边有删除按钮）
4. 界面要简洁美观，用现代化的设计

请先给我一个实现计划，包括用什么技术、分几个文件、大概的实现步骤，等我确认后再开始写代码。
```

  

**Claude 会回复类似这样**：

  

```Plain
好的，我来规划这个待办清单应用：

## 技术选择
- HTML：页面结构
- CSS：样式设计（使用 Flexbox 布局）
- JavaScript：交互逻辑

## 文件结构
1. index.html - 主页面
2. style.css - 样式文件
3. script.js - 功能代码

## 实现步骤
1. 创建 HTML 基础结构（输入框、按钮、任务列表区域）
2. 编写 CSS 样式（现代卡片设计+渐变背景）
3. 实现 JavaScript 功能（添加、完成、删除）
4. 添加本地存储，刷新页面后数据不丢失

准备好了吗？我可以开始实现。
```

  

**你只需要回复**：「好的，开始吧」

  

### **2.4 看着代码自己写出来**

  

这是最神奇的部分。

  

你会看到 Claude 开始自己工作：

- 创建 `index.html` 文件
    
- 写入 HTML 代码
    
- 创建 `style.css` 文件
    
- 写入样式代码
    
- 创建 `script.js` 文件
    
- 写入交互逻辑
    

整个过程你什么都不用做。就像看着一个程序员在你的电脑上工作。

每创建一个文件，Claude 都会告诉你它在做什么。比如：

  

```Plain
创建 index.html...
添加了页面基础结构，包括标题、输入区域和任务列表容器

创建 style.css...
使用了现代化的卡片设计，添加了渐变背景和阴影效果

创建 script.js...
实现了添加、完成、删除功能，并加入了本地存储
```

  

大概 2-3 分钟，所有代码就写完了。

  

### **2.5 打开浏览器看效果**

  

代码写完后，Claude 会告诉你怎么运行。通常会说：

```Plain
已完成！你可以直接用浏览器打开 index.html 查看效果。

或者在终端运行：
python3 -m http.server 8000

然后在浏览器访问 http://localhost:8000
```

  

**Mac 用户**：直接在 Finder 里找到 `my-todo-app` 文件夹，双击 `index.html`

  

**Windows 用户**：在文件资源管理器里找到这个文件夹，双击 `index.html`

  

**浏览器会打开，你会看到**：

- 顶部有个大标题「我的待办清单」
    
- 一个输入框，旁边有「添加」按钮
    
- 下面是任务列表区域
    

试试添加一个任务：「学会用 Claude Code」，点击添加。

  

你的第一个任务出现了！

  

点击任务可以标记完成（会有划线），旁边的删除按钮可以删掉它。

  

**恭喜，这就是你用 AI 做出的第一个作品。**

  

## **第三步：加一个新功能**

  

现在你可能会想：能不能改改？

  

当然可以，而且超级简单。

  

### **3.1 提一个新需求**

  

假设你想给每个任务加上时间戳，显示是什么时候添加的。

  

直接在 Claude Code 里说：

  

```Plain
我想给每个任务加上创建时间，格式是「2025-11-10 15:30」，显示在任务文字的下面，用小字灰色显示
```

  

### **3.2 Claude 会自动修改**

  

Claude 会：

1. 告诉你需要改哪些地方
    
2. 自动修改 `script.js` 添加时间记录逻辑
    
3. 自动修改 `style.css` 添加时间显示的样式
    

**你只需要刷新浏览器**，新功能就生效了。

  

这就是 AI 协作的感觉：你提需求，它写代码，你验收效果。

  

不满意？继续对话调整。

  

### **3.3 试试其他功能**

  

你还可以尝试：

- 「加一个优先级标签，重要的任务显示红色」
    
- 「加一个全部删除按钮」
    
- 「换一个配色方案，我想要蓝色系」
    

每次 Claude 都会理解你的意思，自动改代码。

  

## **第四步：新手常见问题**

  

在过去半年教学员用 Claude Code 的过程中，我发现新手最常问这些问题：

  

### **Q1：改错了怎么办？**

  

别慌，Claude Code 有「时光机」功能。

  

**方法一：按 ESC 两次**

快速回退到上一个版本

  

**方法二：输入命令**

```Plain
/rewind
```

Claude 会列出历史版本，你可以选择回到哪个时间点

  

**方法三：直接说**

「刚才那个改动我不喜欢，还原回去」

  

### **Q2：我完全不懂代码，怎么知道 Claude 做的对不对？**

  

答案：**你不需要懂代码，你只需要测试功能**。

  

就像你不需要懂汽车发动机，也能知道车能不能开。

  

- 添加任务试试，能加上吗？
    
- 标记完成试试，有划线吗？
    
- 删除试试，真的删掉了吗？
    
- 刷新页面，数据还在吗？
    

**功能对了，代码就是对的。**

  

有问题？直接告诉 Claude：「删除按钮点了没反应」，它会自己检查和修复。

  

### **Q3：为什么有些教程说要装 Node.js？**

这是个好问题，说明你真的在学习。

**简单回答**：如果你用的是我推荐的安装方式（curl 或 PowerShell 一键安装），就不需要 Node.js。

**完整解释**：Claude Code 有多种安装方式。如果用 NPM 方式（`npm install -g @anthropic-ai/claude-code`），需要先装 Node.js。但一键安装方式（curl/PowerShell）已经把所有依赖打包好了，直接用就行。

**对新手来说**：跟着我这篇教程的步骤走，别去碰 NPM 安装，就不会遇到 Node.js 的问题。

  

### **Q4：我应该从这个开始学编程吗？**

  

这取决于你的目标。

  

**如果你想快速做出东西**（做个工具、验证个想法、自动化工作）：

- 从 Claude Code 开始是对的
    
- 边做边学，有问题就问 Claude
    
- 遇到不懂的概念，让 Claude 解释
    

**如果你想成为专业开发者**：

- Claude Code 是很好的辅助，但不能替代系统学习
    
- 建议路径：用 AI 做出第一个项目（建立信心）→ 系统学习基础（CS50、FreeCodeCamp）→ 再用 AI 加速开发
    

**我在 WaytoAGI 社区的观察**：很多人就是通过 Claude Code 找到了编程的乐趣，然后主动去学了 JavaScript、Python。

  

因为当你做出东西的时候，学习的动力完全不一样。


  

## **下一步：你可以做什么？**

  

完成了这 15 分钟的教程，你已经掌握了：

- ✅ 安装和认证 Claude Code
    
- ✅ 先规划再动手的方法
    
- ✅ 让 AI 写代码并运行
    
- ✅ 迭代修改功能
    
- ✅ 解决常见问题
    

**接下来试试这些**：

  

1. **做个你真正需要的工具**

- 记账页面？
    
- 倒计时器？
    
- 个人简历网站？
    

2. **挑战：给待办清单加功能**

- 加一个「优先级」分类（高/中/低）
    
- 加一个搜索功能
    
- 换成你喜欢的配色
    
    

## **最后说两句**

  
2025 年的 AI 编程工具，本质上是降低了「想法」到「实现」的门槛。

以前你得先学几个月代码才能做出东西，现在你可以先做出东西，再慢慢理解背后的原理。

**这不是说传统学习不重要，而是学习的路径变了。**

先用 AI 做出第一个作品，建立信心和兴趣，然后再去系统学习底层知识。

这个顺序，反而让很多人坚持下来了。

所以，别担心自己「不会编程」。

打开 Claude Code，用 15 分钟试一试，你可能会发现一个新世界。

  

---

  
  

# _启动_

claude

  

# _创建项目_

mkdir project-name

cd project-name

claude

  

# _常用命令_

/help _# 查看帮助_

/rewind _# 回退版本_

/clear _# 清空对话_

/exit _# 退出_

## **推荐提示词模板**

  

```Plain
做一个[项目类型]，需要：
1. [功能1]
2. [功能2]
3. [功能3]
界面要[风格要求]

请先给我一个实现计划，等我确认后再开始写代码。
```