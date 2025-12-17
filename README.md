# Academic Portfolio Template (Jekyll)

这是一个基于 [Jekyll](https://jekyllrb.com/) 构建的现代学术个人主页模板，专为科研人员、博士生和工程师设计。它托管于 GitHub Pages，无需服务器维护，支持 Markdown 写作，并拥有干净、专业的学术风格。
- 生成于2025.12.17 By Gemini

## 🚀 特性

* **纯静态 & 快速**：无后端数据库，加载速度极快。
* **学术风设计**：专注于展示 Publications（论文）、Research Interests（研究方向）和 Projects（项目）。
* **响应式布局**：完美适配手机、平板和桌面端。
* **易于维护**：大部分内容通过 Markdown 或简单的 HTML 修改。
* **GitHub Pages 原生支持**：推送到 GitHub 即可自动部署。

---

## 🛠️ 本地运行 (Local Development)

### 选项 A：使用 GitHub Codespaces (推荐)

1. 在 GitHub 仓库页面点击绿色 `<> Code` 按钮。
2. 选择 **Codespaces** -> **Create codespace on main**。
3. 等待环境加载完毕后，在终端运行：
```bash
bundle install
bundle exec jekyll serve
```
4. 点击弹出的端口通知（Port 4000）预览网站。

### 选项 B：本地电脑 (需安装 Ruby)

1. 克隆仓库：
```bash
git clone https://github.com/yourusername/my-portfolio.git
cd my-portfolio
```
2. 安装依赖：
```bash
bundle install
```
3. 启动服务：
```bash
bundle exec jekyll serve
```
4. 访问 `http://127.0.0.1:4000`。

---

## 📝 自定义指南 (Customization Guide)

### 1. 修改全局信息 (姓名、邮箱、社交链接)

**文件位置：** `_config.yml`

这是站点的配置文件。请找到以下字段进行修改：

```yaml
title: "Your Name | AI Researcher"  # 浏览器标签页标题
email: your-email@domain.com      # Contract页面 你的邮箱
description: "..."                # 网站描述（用于SEO）
url: "https://yourusername.github.io" # 你的最终网址

# baseurl: "/my-portfolio" # 如果是自定义域名，留空；如果是 username.github.io/repo-name，填 "/repo-name"
# url: "https://shiwei-dev.github.io" # 您的最终域名

author:
  name: "Your Name"               # 你的名字（显示在导航栏和页脚）
  role: "AI Researcher"           # 你的职位
  
social:
  github: "yourusername"          # GitHub 用户名
  linkedin: "yourusername"        # LinkedIn 用户名

```

### 2. 修改主页简介 (Hero Section)

**文件位置：** `index.html`

打开 `index.html`，找到顶部的 `<section>` 区域：

* **自我介绍**：修改 `<h1>` 和 `<p>` 标签中的文字。
* **头像**：找到 `<img src="...">`，将链接替换为你自己的照片链接（推荐使用稳定的图床或放入 `assets/images/` 目录）。
* **简历**：将你的 PDF 简历重命名为 `resume_en.pdf`，放入 `assets/pdf/` 文件夹中覆盖原文件。

### 3. 修改研究兴趣 (Research Interests)

**文件位置：** `index.html`

找到 `<h2>Research Interests</h2>` 下方的 `.research-grid`。每个方向是一个 `.card`：

```html
<div class="card">
    <div style="...">
        <img src="图片链接" alt="方向名称">
    </div>
    <h3>方向名称 (如: Reinforcement Learning)</h3>
    <p>简短描述...</p>
</div>

```
示例：
```html
<div class="card">
    <div style="height: 140px; overflow: hidden; border-radius: 4px; margin-bottom: 1rem;">
        <img src="https://images.unsplash.com/photo-1485827404703-89b55fcc595e?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" 
                alt="Embodied AI" style="width: 100%; height: 100%; object-fit: cover;">
    </div>
    <h3>Embodied AI</h3>
    <p style="font-size: 0.9rem; color: var(--text-muted);">
        Sim-to-Real transfer for quadrupedal locomotion tasks.
    </p>
</div>
```

### 4. 添加/修改项目 (Projects)

本项目有两个展示项目的区域，修改方式略有不同：

#### A. 主页精选项目 (Selected Projects)

* **文件位置**：`index.html`
* **修改指南**：
找到 `<h2>Selected Projects</h2>` 下方的 `<div class="research-grid">`。这里每一个 `<a href="..." class="card">` 标签代表一个项目卡片。
* **代码模板**（复制这段代码插入到 `.research-grid` 中即可添加新卡片）：

```html
<a href="项目链接 (如 https://github.com/xxx 或 /about.html)" class="card" style="display: block;">
    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 0.5rem;">
        <h3 style="margin:0; font-size: 1.2rem;">Project Name</h3>
        <span style="font-size: 0.8rem; color: var(--accent); border: 1px solid var(--accent); padding: 2px 6px; border-radius: 4px;">Tag</span>
    </div>
    <p style="font-size: 0.9rem; color: var(--text-muted);">
        A short description of your project (1-2 sentences).
    </p>
    <div style="margin-top: 1rem; font-size: 0.85rem; font-weight: 500;">View Code &rarr;</div>
</a>

```

#### B. 详细项目经历 (Project Experience)

* **文件位置**：`about.md`
* **修改指南**：
虽然这是 Markdown 文件，但为了实现“左边标题、右边时间”的对齐效果，我们使用了 HTML 代码块。请找到 `## Research & Project Experience` 标题下方。
* **代码模板**（复制这段代码，粘贴到上一个 `</div>` 后面）：

```html
<div style="margin-bottom: 3rem;">
    <div style="display: flex; justify-content: space-between; align-items: baseline; margin-bottom: 0.5rem;">
        <h3 style="margin: 0; font-size: 1.4rem;">My Awesome Research</h3>
        <span style="color: var(--text-muted); font-family: monospace;">2024 - Present</span>
    </div>
    <div style="color: var(--accent); font-weight: 500; margin-bottom: 1rem;">Core Developer / First Author</div>
    <ul style="margin-left: 1.5rem; color: var(--text-main); line-height: 1.7;">
        <li>Designed a novel algorithm using <strong>PyTorch</strong>.</li>
        <li>Achieved state-of-the-art performance on benchmarks.</li>
        <li><strong>Tech Stack:</strong> Python, Docker, AWS.</li>
    </ul>
</div>

```

### 5. 添加/修改论文 (Publications)

**文件位置：** `index.html`

找到 `id="publications"` 的 `<section>`。每篇论文是一个 `.pub-item`：

```html
<div class="pub-item">
    <div class="pub-year">2024</div> <div>
        <a href="#" class="pub-title">论文标题</a>
        <div class="pub-authors"><strong>Your Name</strong>, Co-author A...</div>
        <div class="pub-venue">会议/期刊名称 (如 ICRA 2024)</div>
        <div style="...">
            <a href="PDF链接">[PDF]</a>
            <a href="代码链接">[Code]</a>
        </div>
    </div>
</div>

```

*复制一个完整的 `.pub-item` 块并修改内容即可添加新论文。*

### 6. 写博客 (Blog)

**文件位置：** `_posts/` 文件夹

1. 在 `_posts/` 目录下创建一个新文件。
2. **文件名格式必须为**：`YYYY-MM-DD-your-title.md` (例如 `2025-05-20-my-new-paper.md`)。
3. 文件开头必须包含 Front Matter（头部信息）：
```markdown
---
layout: post
title:  "文章标题"
date:   2025-05-20 10:00:00 +0800
categories: [学术, 随笔]
---

这里开始写正文内容，支持 **Markdown** 语法。

```



---

## 📦 部署 (Deployment)

只需将代码推送到 GitHub 的 `main` 分支：

```bash
git add .
git commit -m "Update content"
git push origin main

```

然后去 GitHub 仓库的 **Settings -> Pages**，确保 Source 设置为 `GitHub Actions` 或 `Deploy from a branch (main / root)`。等待几分钟，你的网站就会更新。

---

## 📂 目录结构说明

```text
├── _config.yml        # 全局配置文件 (姓名、SEO、网址)
├── index.html         # 主页 (简介、研究方向、精选论文)
├── about.md           # 关于页 (详细简历、技能)
├── contact.html       # 联系页
├── blog.html          # 博客列表页
├── _posts/            # 存放博客文章 (.md)
├── _includes/         # 公共组件 (Header, Footer)
├── _layouts/          # 页面模板 (Default, Post)
└── assets/            # 静态资源
    ├── css/           # 样式表
    ├── images/        # 图片
    └── pdf/           # 简历文件

```

