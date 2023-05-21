---
title: 云 · ChatGPT · 开源：Azure OpenAI 上一些有趣场景的应用实践与源码
last_modified_at: 2023-05-21 21:30:00
tags:
- 工程
categories:
- 技术分享
---
Azure 在 5.11 举办了 App Innovation with Azure Openai In-A-Day Workshop 活动，利用一天时间与客户一起交流 OpenAI 技术及解决方案，并在活动中演示了基于创新应用场景的 OpenAI Demo。我们来看看本次活动上的分享内容和应用实践【全部均已开源 & 附源码】。

# Azure OpenAI & OpenAI 
先做一下内容的简单回顾，了解一些云上 OpenAI 的基础能力：
## 合作
<img src="/assets/images/Azure-OpenAI/1.png"/>

## 异同
| 特性 | OpenAI | Azure OpenAI |
| ---- | ---- | ---- |
| 模型种类 | 语言、视觉、语音… |
| 价格 | 按标记 (token) 数量进行收费 |
| 最新模型 | 首先发布 | 延后一段时间发布，完善安全性，合规性等 |
| 安全性及数据隐私 | 基本安全性 | 企业级安全性、RBAC、客户管理密钥 |
| 合规 | 不提供 | SOC2, ISO, HIPAA, CSA STAR |
| 可靠性 | 目前还不提供 SLA | Azure SLA, 专属容量选项 (即将发布) |
| Responsible AI | 单独的安全分类器（增加延迟） | 内置企业级低延迟审核和伤害预防 |
| 解决方案 | 先进的大语言模型 (LLM) 和图片生成技术，基础语音技术 | OpenAI 模型，完整的 AI 解决方案和完整的 PaaS 服务 |

## GPT 最新版本信息
<img src="/assets/images/Azure-OpenAI/2.png"/>

<img src="/assets/images/Azure-OpenAI/3.png"/>

# 创新场景的应用实践 & 源码
云上有很多构建企业 AI 应用的云服务，通过它们的组合可以生成很多很有趣的创新场景：
<img src="/assets/images/Azure-OpenAI/4.png"/>

下面给出一些场景示例 & 开源代码：

## Chat Your Data
针对企业现有数据提供基于自然语言实现零代码的数据自服务查询，例如如下的示例：关系型数据 SQL 智能交互。
- 开源代码：https://github.com/teo-ma/AzureSQLChatGPTDemo
- Demo 网站地址：https://sqlchatteo.azurewebsites.net/
- 使用指南：点击左侧“+”号图表 Create Connection，连接到默认 MySql 数据库或您自己的 MySql 数据库，然后通过自然语言查询数据，如下图：

<img src="/assets/images/Azure-OpenAI/5.png"/>

## Chat Your Doc
针对特定文章做内容检索、摘要生成、自然语言答复，做企业内部的搜索引擎。例如如下的示例：多模态企业数据知识库智能搜索。
- 开源代码：https://github.com/teo-ma/azure-open-ai-embeddings-qna
- Demo 网站地址：https://oaiembedding0410-site.azurewebsites.net/
- 使用指南：通过 "Add Document" 加载您自己的文本或图片，进行问答式搜索，如下图：

<img src="/assets/images/Azure-OpenAI/6.png"/>

- 云上搭建应用的解决方案：主要用到 OpenAI Embedding + Azure Form Recognizer，整体如下：

<img src="/assets/images/Azure-OpenAI/7.png"/>

## Chat Your Vedio
从电话记录中提取大量见解，例如如下的示例：企业客服语音数据分析。
- 开源代码：https://github.com/amulchapla/AI-Powered-Call-Center-Intelligence
- Demo 网站地址：https://www.microzure.com/
- 使用指南：选择语言之后，点击 START Converstation，对话结束点击 END Conversation，按照自定义提示进行对话的总结。

<img src="/assets/images/Azure-OpenAI/8.png"/>

- 云上搭建应用的解决方案：主要用到 OpenAI + Azure Speech Cognitive Service，整体如下：

<img src="/assets/images/Azure-OpenAI/9.png"/>

## 更多应用场景
更多创新场景的应用实践 & 源代码访问：https://agreeable-flower-0968eb610.2.azurestaticapps.net/

<img src="/assets/images/Azure-OpenAI/10.png"/>

# 参考资料
本文查阅的开源文档及代码如下：
- In-A-Day Workshop：https://github.com/microsoft/gpscsa-china-openai-in-a-day
- OpenAI 官方 Cookbook：https://github.com/openai/openai-cookbook
- Azure OpenAI 官方文档：https://learn.microsoft.com/zh-cn/azure/cognitive-services/openai/
- 探索 Azure OpenAI 服务嵌入和文档搜索：https://learn.microsoft.com/zh-cn/azure/cognitive-services/openai/tutorials/embeddings?tabs=command-line
- 使用语音与 Azure OpenAI 对话：https://learn.microsoft.com/zh-cn/azure/cognitive-services/speech-service/openai-speech
- 快速入门：体验 ChatGPT 并通过程序调用它的API：https://learn.microsoft.com/zh-cn/azure/cognitive-services/openai/chatgpt-quickstart?tabs=command-line&pivots=programming-language-studio
- 部署企业自己的 ChatGPT - OpenAI 官方 ChatGPT 的最小克隆：https://github.com/teo-ma/cosmosdb-chatgpt
- 使用 OpenAI API 构建智能聊天机器人并部署到 Azure App Service 和 Microsoft Teams App：https://github.com/microsoft/gps-csa-tech-stack/tree/main/Create-A-ChatGPT-Bot-APP-and-Deploy-To-Azure-APP-Service-or-Teams-APP
