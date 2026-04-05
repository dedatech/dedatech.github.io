# CLAUDE.md

本文件为 Claude Code (claude.ai/code) 在此代码仓库中工作时提供指导。

## 项目概述

这是一个基于 Jekyll 的 GitHub Pages 站点（debao.wang），个人技术博客。当更改推送到 main 分支时，GitHub Pages 会自动部署。

## 关键信息

- **域名**: debao.wang（通过 CNAME 文件配置）
- **平台**: GitHub Pages（Jekyll 主题）
- **语言**: 内容主要为中文
- **仓库**: dedatech/dedatech.github.io

## 开发工作流

### 本地开发

在本地运行站点进行测试：

```bash
# 首次运行时安装 Jekyll 和依赖
bundle install

# 启动本地开发服务器
bundle exec jekyll serve

# 或指定主机和端口
bundle exec jekyll serve --host 0.0.0.0 --port 4000
```

站点将在 `http://localhost:4000` 访问

### 构建站点

```bash
# 构建生产环境站点
bundle exec jekyll build
```

生成的文件将位于 `_site` 目录中（该目录已被 gitignore）。

### 发布更改

只需提交并推送到 main 分支。GitHub Pages 将自动构建和部署：

```bash
git add .
git commit -m "更改说明"
git push origin main
```

## 架构

这是一个使用 GitHub Pages 默认主题的极简 Jekyll 站点。主要配置在 `_config.yml` 中：

- `title`: 站点标题
- `description`: SEO 站点描述

### 站点结构

- `_config.yml` - Jekyll 配置文件
- `README.md` - 项目文档
- `build_site.md` - 站点搭建文档
- `todolist.md` - 项目路线图和待办事项
- `CNAME` - debao.wang 自定义域名配置
- `1fe14807cf8678f72a0af022f64fa20b.txt` - GitHub 所有权验证文件

### 添加内容

添加新博客文章：
1. 在 `_posts` 目录中创建新的 markdown 文件（如果该目录存在），格式：`YYYY-MM-DD-title.md`
2. 在顶部添加 Jekyll front matter：
```yaml
---
layout: post
title: "文章标题"
date: YYYY-MM-DD
---
```

## 项目状态

当前待办事项（来自 todolist.md）：
- [ ] 使用 Jekyll 维护网站内容（进行中）
- [ ] 博客与微信公众号同步

## 注意事项

- 站点使用 GitHub Pages 内置的 Jekyll 主题 - 仓库中没有自定义主题文件
- 不需要构建脚本或 npm 配置
- GitHub Pages 自动处理所有构建和部署
- 内容语言为中文
