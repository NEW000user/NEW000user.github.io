---
layout: post
title: 这个博客如何写作与发布
date: 2026-10-08
excerpt: 文章以 Markdown 编写，由 Jekyll 和 GitHub Actions 构建，再通过 GitHub Pages 发布。
tags:
  - 学习
---

这个博客使用 Jekyll 模板生成静态网页。文章保存在 `_posts/` 目录中，以 Markdown 编写；每篇文章开头的 Front Matter 用来设置标题、日期、摘要和标签。

## 发布流程

将文章和页面修改提交到 `main` 分支后，GitHub Actions 会运行 Jekyll 构建，并把生成的网站发布到 GitHub Pages。

本地编辑只需要文本编辑器和 Git。页面使用 HTML 与 CSS，文章使用 Markdown；项目不依赖 Node.js、npm 或前端框架。

## 新建文章

在 `_posts/` 中新建 `YYYY-MM-DD-title.md` 文件，沿用现有 Front Matter 格式，然后写入 Markdown 正文。提交并推送后，Actions 会自动更新网站。
