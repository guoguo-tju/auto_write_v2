# 为什么大家都在用Claude Code？用完之后你就懂了

---

最近朋友圈大家都在用的Claude Code，是不是感觉自己又落伍了？


别慌。让我先说清楚**Claude Code到底是什么**。


---



### Claude Code是什么？


简单说，Claude Code是一个**AI助手工具**，就像你的私人秘书。


>>> 🖼️ IMAGE: Claude Code是一个AI助手工具，就像你的私人秘书 <<<


它的核心能力包括：

- **写代码**：你告诉它想做什么，它自动写代码

- **改代码**：代码有bug，它帮你改

- **写文章**：写博客、写报告、写教程，都能帮忙

- **做调研**：搜集资料、整理信息、分析数据

- **运行命令**：在终端执行各种操作

- **文件管理**：读写文件、搜索内容、批量处理


**所以它不只是写代码的，更像一个万能AI助手。**



---



### 为什么要用Claude Code？

**优势1：Skills和Subagent，能力无限扩展**

  这是Claude Code最强大的地方，也是它和其他AI工具(如cursor)最大的不同。

**什么是Skills？**
Skills就是**自定义技能**。你可以写一些脚本/md文件，让Claude Code使用新的能力。



举个例子：

- 你经常需要批量处理Excel？写个Skill让它一键完成

- 你需要自动生成周报？写个Skill读取项目数据自动生成

- 你需要批量改图片？写个Skill调用ImageMagick帮你处理



**就像是给Claude Code装插件，想加什么功能就加什么功能。**




**什么是Subagent？**


Subagent是**子代理能力**。遇到复杂任务，Claude Code可以启动专门的子AI来处理。



>>> 🖼️ IMAGE: Subagent子代理能力，Claude Code可以启动专门的子AI来处理复杂任务，就像有个AI团队在帮你干活 <<<


比如你让它"做个网站分析竞品"，它会：

1. 启动一个**浏览子代理**去爬取网站内容

2. 启动一个**分析子代理**去处理数据

3. 启动一个**写作子代理**去生成报告



每个子代理都专注做一件事，多线程并行，效率比单个AI高多了。



**就像有个AI团队在帮你干活，而不是只有一个AI助手。**





**优势2：不绑定任何IDE，想在哪用就在哪用**


>>> 🖼️ IMAGE: Claude Code不绑定任何IDE，可以在VS Code、JetBrains、Vim或终端中使用 <<<


这是Claude Code最大的优势。

Cursor？你必须用它的编辑器。你习惯了VS Code？对不起，换工具吧。


Claude Code不一样：

- **喜欢用VS Code/ JetBrains全家桶** ？装个插件就行，还是你熟悉的界面

- **喜欢用Vim？命令行里启动，无缝集成

- **不想装任何编辑器**？直接在终端用，最轻量


**你不需要改变工作习惯，它来适应你。**



---



### 它能解决什么问题？




**痛点1：想做东西但不会编程**


以前你得学几个月才能做个网站。现在？告诉Claude Code你的需求，它自己写。



**痛点2：写作没思路**


卡文了？让Claude Code给你10个标题方向。写完了？让它帮你润色、改错别字、优化结构。



**痛点3：重复性工作太多**


>>> 🖼️ IMAGE: Claude Code能自动化处理重复性工作，如批量改文件名、整理Excel、写重复性报告等


批量改文件名、整理Excel、写重复性的报告...Claude Code都能自动化。



---



## 安装Claude Code：5分钟搞定



安装超简单，跟着我做就行。



### Mac用户



**步骤1：打开终端**


在启动台里搜索"终端"，打开它。终端就是一个用命令控制电脑的工具，你只需要会复制粘贴就行。



**步骤2：复制这行命令，粘贴到终端，按回车**



```bash

curl -fsSL https://claude.ai/install.sh | bash

```



**步骤3：安装完成后再命令行输入claude, 即可启动claude code

### Windows用户



**步骤1：打开PowerShell**


点击开始菜单，搜索"PowerShell"，右键选择"以管理员身份运行"



**步骤2：复制这行命令，粘贴进去，按回车**



```powershell

irm https://claude.ai/install.ps1 | iex

```





等个1-2分钟，看到"Claude Code installed successfully"就装好了。



---



## 搞定账号：唯一的小门槛




Claude Code需要配合大模型使用, Claude官方会封中国用户账号，所以推荐用中转方案或国产大模型。




**两种方案：**




- **中转方案**（推荐）：效果最好，但需要付费。比如88code (评价好, 我自用的付费站)
- 链接: https://www.88code.org/register?ref=KWW7JB

- **国产大模型**：简单方便，性价比高。推荐: 智谱GLM-4.7 、DeepSeek 、Kimi K2
- 智谱GLM链接：https://www.bigmodel.cn/glm-coding?ic=1HVEGRP0BR




我用DeepSeek给你演示一下：



**步骤1：注册DeepSeek**

打开 https://platform.deepseek.com ，注册账号并登录


**步骤2：获取API Key**

访问 https://platform.deepseek.com/api_keys ，点击"新建API Key"，复制它



**步骤3：用cc Switch一键配置**

cc Switch是一个配置Claude code apikey,切换管理配置的工具,推荐下载使用。
安装链接: https://github.com/farion1231/cc-switch

新增deepseek模型ak配置


在cc Switch里勾选"应用到Claude Code插件"，然后重启Claude Code，配置就自动同步好了。



注意： 修改配置后记得重启VS Code才能生效



---



## 命令行不方便? 安装Claude code插件：有个界面更方便




如果你不想用黑乎乎的终端，可以装个Claude code插件，有图形界面更好用。



**步骤1：安装VS Code**



访问 https://code.visualstudio.com/ ，下载并安装，免费的



**步骤2：安装Claude Code插件**



打开VS Code，点击左侧扩展图标，搜索"Claude Code"，点击安装


  安装完成后即可页面化操作

---



## 常用命令：记住这几个就够了

```bash

claude # 启动Claude Code

/help # 查看帮助

/rewind # 回退版本（改错了很有用）

/clear # 清空对话

/exit # 退出

/compact #压缩上下文

```



---



希望这篇安装指南能帮你快速上手Claude Code。

如果有帮助，可以帮忙**点个赞**，让我有动力继续更新下一篇实操教程。

欢迎关注公众号：**"蝈蝈的AI笔记"**，下一期我们会用Claude Code做出第一个应用。
