# 文浩的技术博客

这是我的个人技术博客仓库，网站地址：[https://wenhao-in-chengdu.github.io](https://wenhao-in-chengdu.github.io)

## 博客内容

- 网络架构设计经验
- 网络运维与安全实践
- 网站开发与维护心得
- 自动化脚本与工具分享

## 技术栈

本博客使用GitHub Pages + Hugo搭建，主要技术包括：

- Hugo静态网站生成器
- Markdown文档编写
- Go模板语言
- CSS样式

## 本地开发

1. 安装Hugo环境（推荐版本0.134.0或更高）
2. 克隆仓库：`git clone https://github.com/wenhao-in-chengdu/wenhao-in-chengdu.github.io.git`
3. 本地运行：`hugo server -D`
4. 浏览器访问：`http://localhost:1313`

## 文章归档

所有博客文章按年份和分类归档：
- 年份归档：`/year/YYYY/`（如`/year/2025/`）
- 分类归档：`/categories/分类名/`（如`/categories/网络架构/`）
- 文章URL格式：`/posts/:year/:slug/`（如`/posts/2025/network-design/`）

## 文章编写

所有博客文章放在`content/posts`目录下，文件名格式为`YYYY-MM-DD-title.md`。

文章头部需要包含以下Front Matter信息：

```yaml
---
title: "文章标题"
date: YYYY-MM-DDT00:00:00+08:00
categories: ["分类名称"]
tags: ["标签1", "标签2"]
year: "YYYY"  # 年份，用于年份归档
slug: "article-slug"  # 文章URL路径
---
```

## GitHub Pages设置

在GitHub仓库中，需要进行以下设置：

1. 进入仓库的 `Settings` > `Pages`
2. 在 `Build and deployment` 部分：
   - 将 `Source` 设置为 `GitHub Actions`
3. 提交代码后，GitHub Actions会自动构建并部署网站

## 问题排查

如果网站只显示README.md内容而非博客内容，请检查：

1. 确认GitHub Pages设置为通过GitHub Actions部署
   - 进入 Settings > Pages
   - Source 应设置为 "GitHub Actions"

2. 查看Actions页面中的工作流是否执行成功
   - 进入 Actions 标签页
   - 查看最新的工作流执行情况
   - 如果有错误，根据错误信息排查问题

3. 确认`hugo.yml`工作流文件存在于`.github/workflows`目录中

4. 如果网站返回404错误：
   - 检查仓库名称是否正确为 `username.github.io` 格式
   - 确保 `baseURL` 在 `config.toml` 中设置正确
   - 确认 Hugo 构建成功生成了 public/index.html 文件

5. 网站空白或样式错误：
   - 检查CSS路径是否正确
   - 确保主题文件存在且正确配置
