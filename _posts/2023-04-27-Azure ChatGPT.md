---
title: 薅羊毛！微软 Azure 200 美元免费额度，云上 ChatGPT 使用指南！
last_modified_at: 2023-04-27 17:00:00
tags:
- 工程
categories:
- 技术分享
---
## 背景
微软 Azure Cloud 针对新用户，提供了 200 美元热门云服务使用的免费额度，可使用于计算实例、存储等资源，其中还包括最近大热门的 OpenAI ChatGPT (支持 gpt-3.5 & gpt-4 等最新 API 版本) 服务。

本文主要介绍 Azure 注册 & 免费额度使用指南，同时以 ChatGPT 服务为例介绍使用过程，让我们薅秃 Azure 羊毛！

## 登陆 Azure
首先我们先登陆 Azure ，网站地址如下（拷贝后粘贴到浏览器打开）：
```
https://login.microsoftonline.com/organizations/oauth2/v2.0/authorize?redirect_uri=https%3A%2F%2Fportal.azure.com%2Fsignin%2Findex%2F&response_type=code%20id_token&scope=https%3A%2F%2Fmanagement.core.windows.net%2F%2Fuser_impersonation%20openid%20email%20profile&state=OpenIdConnect.AuthenticationProperties%3DmcnNU3oK5Ms-Yt4fM3p9DTXASEj7LPxN6sX6HRHiATDIt7ByMvI0FZF489VmLpXta5fQbtGC34dh2uwZ1mfN_3c-jKt6183YfdfPP2vhqintzRIbKPnvKi2EO5pLuK8Oz2Ucp9-5kxX4_HkX66CX6-yGTBTUQQq-9cm68o-w6Mn7bHEoD4ibUEnICRtyiCevg7jojN0HRNae6J37q-_UgClkgOC9Ac5-VMpmJ4CtlIY5-7R-E2jRrTvcW_0TNg1I9agBDpmRFN6dQc9xNEiaO_dy0a8Dh4W6fxH9HDmkGHobyj-_z-kGleLAiqU-XNQdjyyu4wEuD2P7h6Ctcs9XUqPwIrhsG9vWoKWJmK1y3hIndOqai7k-zagvMdc3Ubg5bxeCP03-JkcjOHQUH04mfs6zbTX-fQ8xQYFaQOPDgYZ-nxtkh2b9Zl0cu-MSyzNJteCSR3gGdxk4lEc-FZDUkxB8dQENikDYyDywOz2e42Y&response_mode=form_post&nonce=638186935030121164.MzVmMGRiNmMtOWJmMC00N2MzLWE0NmEtNTM2NzUxNGIyZTI1Y2UyMjliNGUtYTkzNS00YjdjLWJlNzgtYzg3Njc5YzQzOGY4&client_id=c44b4083-3bb0-49c1-b47d-974e53cbdf3c&site_id=501430&client-request-id=f9a287d6-6251-4169-8425-5d95b7e803b0&x-client-SKU=ID_NET472&x-client-ver=6.27.0.0
```

如果没有微软账号可以快速用个人邮箱注册一个，已有账号（可以用自己常用 Windows 系统微软账号）直接登陆即可。登陆后进入如下页面：
![](https://mmbiz.qpic.cn/sz_mmbiz_png/GI9iaFcKKibicUpMjGjORPrz13RkGzn8xKHfyNFSWO0b0pic8Fqo6ic85JaFF95wKwFVic8ibWMx0P43mpWicibYY8umI7g/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

可以看到 “从 Azure 免费使用版开始”，点击 “开始” 即可看到支持的免费服务了。
![](https://mmbiz.qpic.cn/sz_mmbiz_png/GI9iaFcKKibicUpMjGjORPrz13RkGzn8xKHKOI5WydBsLeDV91UzfsicGPZKmczFtpNv0bXx5Pdzn5Lpw62q3CNPEg/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

点击 “免费开始使用”，输入姓名 & 电话 & 地址，完成短信验证码验证：
![](https://mmbiz.qpic.cn/sz_mmbiz_png/GI9iaFcKKibicUpMjGjORPrz13RkGzn8xKHKBvXtWNsglWfF7V1PPzbLMiaqvM9icIUuGMTJMMabAqqp2XDcib6gBOuA/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

输入 Visa 或万事达的信用卡或借记卡相关信息，即可开始免费使用 (在赠金 200 美元用完后，Azure 将询问是否想要继续使用即用即付模式，不用担心免费额度外还有其它费用问题) ：
![](https://mmbiz.qpic.cn/sz_mmbiz_png/GI9iaFcKKibicUpMjGjORPrz13RkGzn8xKHtcpPUStytTAiciatrlheuEkoiaqyUeUeO3KKJUHAjwwQlDm5O7TR8VvHw/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

下面我们以 ChatGPT 服务为例展示云服务的使用过程。

## 创建 ChatGPT 云资源
在搜索栏搜索 “OpenAI” 进入云服务，找到 “创建”：
![](https://mmbiz.qpic.cn/sz_mmbiz_png/GI9iaFcKKibicUpMjGjORPrz13RkGzn8xKHlz2dMxmQyZFE7qk47FlXff88qVyfls8x0j9EibbES5bk0UCiazefQCibw/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

按提示填写：基本信息、网络等配置，即可完成资源创建：
![](https://mmbiz.qpic.cn/sz_mmbiz_png/GI9iaFcKKibicUpMjGjORPrz13RkGzn8xKHFLucqF7zAGLlgrpqCkFMMkoxJSYCuysSRC9Rh0oqhy6kXB3ZYNnC0w/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

稍等三分钟后创建完毕，再进入资源，可以看见如上操作引导了：
![](https://mmbiz.qpic.cn/sz_mmbiz_png/GI9iaFcKKibicUpMjGjORPrz13RkGzn8xKHVnGKINg1icSJ6XUcWibjssIMudtg3jx6oSn4rJOcfTJ1oxCicaZQ1JOLw/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

首先点击进入 OpenAI Studio 页面，找到 “部署”，部署一个你所需的模型，包括 gpt-3.5-turbo 等 OpenAI 已支持的模型列表，这过程只需几秒钟完成：
![](https://mmbiz.qpic.cn/sz_mmbiz_png/GI9iaFcKKibicUpMjGjORPrz13RkGzn8xKHZTFImUb2pzNgffBTELiajcnN85gpta57r2MLXFBEE2m61rLrFiacksAw/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

而后就可以直接开始使用了，进入 “聊天”，开始愉快的和 ChatGPT 聊天吧～ 支持动态调整参数，示例如下：
![](https://mmbiz.qpic.cn/sz_mmbiz_png/GI9iaFcKKibicUpMjGjORPrz13RkGzn8xKHEpCQNRdAwXHRPR9cIJF9GYNwibkocJrfyXuEZJ1dNnyZ53iaNcnZJddw/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

## 代码调用 API
如果你想通过代码调用 Azure OpenAI ChatGPT，下面以 Golang 为例展示通过代码连接 & 测试过程。

其实 Azure 连接和 OpenAI api-key 连接方法非常类似，仅是多了一些参数（重点是 InitGPTAzure 方法，至于 configYaml 配置大家定义一个 struct 即可）。代码示例如下：
```
package openai

import (
  "context"

  openai "github.com/sashabaranov/go-openai"

  "github.com/VelocityLight/go-template/pkg/configs"
)

var (
  c *openai.Client
)

const (
  AISystemMessage = "You are an AI assistant, You can talk and help to the user."
)

type Params struct {
  MaxTokens   int      `json:"max_tokens"`
  Model       string   `json:"model"`
  TopP        float32  `json:"top_p"`
  Temperature float32  `json:"temperature"`
  N           int      `json:"n"`
  Stop        []string `json:"stop"`
}

func InitGPT(APIKey string) {
  c = openai.NewClient(APIKey)
}

func InitGPTAzure(config *configs.ConfigYaml) {
  cfg := openai.DefaultConfig(config.AzureAI.Token)
  cfg.BaseURL = config.AzureAI.BaseURL
  cfg.OrgID = config.AzureAI.OrgID
  cfg.APIType = openai.APIType(config.AzureAI.APIType)
  cfg.APIVersion = config.AzureAI.APIVersion
  cfg.Engine = config.AzureAI.Engine

  c = openai.NewClientWithConfig(cfg)
}

func buildRequest(prompt string, params Params) openai.ChatCompletionRequest {
  req := openai.ChatCompletionRequest{
    Model:       params.Model,
    MaxTokens:   params.MaxTokens,
    Temperature: params.Temperature,
    TopP:        params.TopP,
    N:           params.N,
    Stream:      false,
    Stop:        params.Stop,
    Messages: []openai.ChatCompletionMessage{
      {
        Role:    openai.ChatMessageRoleSystem,
        Content: AISystemMessage,
      },
      {
        Role:    openai.ChatMessageRoleUser,
        Content: prompt,
      },
    },
  }

  if req.Model == "" {
    req.Model = "gpt-3.5-turbo"
  }
  if req.TopP == 0.0 {
    req.TopP = 0.7
  }
  if req.MaxTokens == 0 {
    req.MaxTokens = 256
  }

  return req
}

func AskOpenAI(ctx context.Context, promptText string, params Params) (string, error) {
  req := buildRequest(promptText, params)
  resp, err := c.CreateChatCompletion(ctx, req)
  if err != nil {
    return "", err
  }

  line := resp.Choices[0].Message.Content
  return line, nil
}
```

注意上面 33 ~ 38 行的几个关键参数：

cfg.Token 即 “资源密钥” (密钥 1 或 密钥 2 均可)，cfg.BaseUrl 即 “终结点”，你可以在资源列表页找到。

cfg.APIType 默认值是 “Azure”，cfg.APIVersion 默认值是 “2023-03-15-preview” （如果你用的也是 gpt-3.5-turbo）, cfg.Engine 是前面你部署的模型自己设定的名字。

![](https://mmbiz.qpic.cn/sz_mmbiz_png/GI9iaFcKKibicUpMjGjORPrz13RkGzn8xKHZ5xrRNpaiaibSJlelt6OTI1AwQsxgtP0oPw42ndZzIsRW4NByajLeutw/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

发起测试看看，让 ChatGPT 给我们写首诗：
![](https://mmbiz.qpic.cn/sz_mmbiz_png/GI9iaFcKKibicUpMjGjORPrz13RkGzn8xKH3lJ7wBNZ9o8ibz1iaqKXEc2ZDJxyOYht9mFJY3amiaA8sQ8vgRBTVgicWw/640?wx_fmt=png&wxfrom=5&wx_lazy=1&wx_co=1)

这首诗感觉如何？哈哈哈哈。

## 总结
本文介绍了薅 Azure 云服务羊毛的方法，并且以 OpenAI ChatGPT 为例展示了服务使用、代码连接&测试实战过程。

希望本文可以对你有所帮助，要是觉得文章还不错，希望帮忙点个赞、分享和关注 (微信公众号：FinOps 实战)（Github: [Github](https://github.com/VelocityLight)），您的支持和鼓励是持续更新的最大动力，公众号内持续有实战分享，欢迎一起探讨和发现。
