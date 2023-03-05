[English](README.md) | [中文](README_zh.md)

# 项目介绍
这是我的个人博客网站, 基于 Jekyll Minimal Mistakes 主题搭建的 Github Pages.

## 实现步骤
- 创建 '<Your-UserName>.github.io' 代码仓库.
- 将文章放在 _posts/ 目录，将图片放在 assets/images/ 目录，并将它们全部上传到仓库上.
- 在根目录下创建 _config.yml 文件，将主题指向远程 Github 的 Jekyll Minimal Mistakes 主题，并正确配置文章和图片的引用路径.
- 在根目录下创建 Gemfile 文件，用于安装 Jekyll 所需的 Ruby 环境和插件.
- 在 Mac M1 机器上安装必要的工具，并在本地从根目录启动并访问网站，确保一切正常.
- 新增文章后将代码推送到 Github 仓库即可，实现网站能够通过远程 URL 进行访问: https://<Your-UserName>.github.io.
我的博客地址: [https://VelocityLight.github.io](https://VelocityLight.github.io), 欢迎访问.

## 必要工具
我是 Mac, 安装以下工具：
```
# 安装 Ruby
brew install ruby

# 安装 Jekyll
gem install bundler jekyll
```

## 如何本地调试
```
# 安装依赖
bundle install

# 启动网站
bundle exec jekyll serve

# 访问网站
http://127.0.0.1:4000/
```

## 工程结构
```
.
├── Gemfile         # 项目依赖
├── README.md
├── _config.yml     # 主题配置
├── _data
├── _pages          # TAG & 目录等分类页面
├── _posts          # 个人博客
├── assets          # 静态文件, 包括图片等
└── index.html
```

## 联系作者
此项目中引用主题:
- https://github.com/mmistakes/minimal-mistakes
- 模版参考: https://github.com/mmistakes/mm-github-pages-starter

欢迎在 Github 上联系我，Have A Nice Day！
