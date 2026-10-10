# NEW000user 的个人博客

这是一个使用 Jekyll 的静态个人博客。文章写在 `_posts/*.md`，页面用 HTML 和 CSS 编写，GitHub Actions 负责构建并发布到 GitHub Pages。

## 仓库与网址

仓库：[NEW000user/NEW000user.github.io](https://github.com/NEW000user/NEW000user.github.io)

博客：[https://new000user.github.io/](https://new000user.github.io/)

注意：仓库里的 `index.html` 是 Jekyll 模板源码，不能靠双击本地文件看到最终页面；最终 HTML 会由 GitHub Actions 生成。本地不需要安装 Ruby、Jekyll、Node.js 或 npm。

## 写一篇新文章

在 `_posts/` 中复制示例文章，文件名使用：

```text
YYYY-MM-DD-title.md
```

文章开头保留 Front Matter：

```yaml
---
layout: post
title: 文章标题
date: 2026-10-08
excerpt: 一句话摘要
tags:
  - 学习
---
```

第二个 `---` 之后直接写 Markdown 正文：标题、段落、列表、链接、代码块都可以使用。

## 发布流程

Pages 已配置为 GitHub Actions。把变更提交并推送到 `main` 后，`.github/workflows/pages.yml` 会自动构建并发布网站；也可以在仓库的 **Actions** 页面查看运行结果。

## 需要学生理解的概念

```text
Markdown 文章
      ↓
Jekyll / GitHub Actions
      ↓
HTML 页面
      ↓
GitHub Pages URL
```

学生不需要在本地安装 Ruby、Jekyll、Node.js 或 npm。构建发生在 GitHub Actions 上。

## Agent 提示词

```text
/goal 这是一个 Jekyll 静态博客项目。请先读取 README、_config.yml、index.html、_layouts 和 _posts。
以后新增文章时，只在 _posts/ 中创建 YYYY-MM-DD-title.md，并使用现有 Front Matter 和 layout: post。
不要引入 React、Vue、Node.js、npm、外部 CDN 或新的构建工具。
修改前先列出文件和计划；修改后检查 Markdown Front Matter、文章链接、相对资源路径和 Git diff。
目标仓库是 https://github.com/NEW000user/NEW000user.github.io。提交和推送前先检查 git diff；只在我确认后执行 git commit 和 git push。
```
