# GitHub AI 技术简报

面向工程师的 GitHub AI 项目观察，每天三次由 Claude 定时任务自动生成并推送到本仓库。

- **09:00** 新星爆发 — 近 30 天内新建、已积累关注度的项目
- **15:00** 细分方向深挖 — LLM infra / Agent 框架 / 推理优化 / 向量检索
- **20:00** 沉淀之作 — 有半年积累、工程成熟度高的项目

时区 Asia/Singapore。

## 部署

这是一个 Jekyll 站点，可直接由 GitHub Pages 构建，无需本地环境。

1. 仓库 **Settings → Pages → Build and deployment → Source** 选 **Deploy from a branch**
2. Branch 选 `main`，目录选 `/ (root)`，保存
3. 等 1–2 分钟，站点发布在 `https://<username>.github.io/<repo>/`

如果部署在子路径（即仓库名不是 `<username>.github.io`），把 `_config.yml` 里的 `baseurl` 改成 `"/<repo>"`。

## 文章格式

文件放在 `_posts/`，命名为 `YYYY-MM-DD-<slot>.md`，front matter 如下：

```yaml
---
layout: post
title: "技术简报 · 沉淀之作"
date: 2026-07-26 20:00:00 +0800
slot: 晚间
summary: "一句话摘要，显示在首页列表。"
---
```

`slot` 取值：`早报` / `午间` / `晚间`，会渲染成标题旁的小标签。

## RSS

站点自带 RSS，地址 `/feed.xml`。用 RSS 阅读器订阅后，新简报会直接推送到手机 —— 比依赖通知更可靠。

## 本地预览（可选）

```bash
gem install bundler jekyll
bundle exec jekyll serve
```
