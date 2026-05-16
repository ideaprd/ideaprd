# 凌霄阁 / ideaprd

静态多语言示例站点（无构建步骤），发布目录为仓库根目录。线上域名：**https://prd.ideaprd.com**。

## 目录说明

| 路径 | 说明 |
|------|------|
| `index.html` | 根首页：按浏览器语言跳转 `zh/` 或 `en/` |
| `robots.txt` / `sitemap.xml` | 被动收录：爬虫发现全站 URL |
| `.nojekyll` | GitHub Pages 使用，避免 Jekyll 处理 |
| `zh/` | 中文站（凌霄阁）：`index.html`、`nav.json`、`pages/*.html` |
| `en/` | 英文站（ideaprd）：结构对称 |
| `assets/brand/` | 品牌 SVG：`icon.svg`（站点图标）、`logo-zn.svg`（中文首页主视觉）、`logo-en.svg`（英文首页主视觉） |

新增页面：在对应语言 `pages/` 下添加 HTML，并编辑该语言的 `nav.json`。

## 本地预览

`fetch('nav.json')` 在 `file://` 下常失败，请用本地 HTTP 服务打开，例如：

```bash
cd ideaprd-github
python -m http.server 8080
```

浏览器访问 `http://127.0.0.1:8080/zh/index.html` 或 `http://127.0.0.1:8080/en/index.html`。

## 设计与字体

视觉令牌（暖色画布、油墨字、hairline 卡片、主色橙 CTA 等）见仓库同级的 **`ideaprd-github-DESIGN.md`**（若仅在本地工作区，路径以你克隆的目录为准）。

正文使用 **Inter**（设计文档中作为 CursorGothic 的开源替代），代码字体为 **JetBrains Mono**，通过 **Google Fonts** 加载。若需完全离线，可改为自托管 `woff2` 并删除各页中的 `fonts.googleapis.com` 链接。

## Open Graph 图片

各页 `og:image` 指向 `https://prd.ideaprd.com/og-cover.png`。仓库未包含该文件时，请在上线后于站点根目录添加 `og-cover.png`，或批量修改各页 meta 为实际图片地址。

## 联系

邮件：**[mail@ideaprd.com](mailto:mail@ideaprd.com)**

## GitHub Pages

将站点根目录设为仓库根目录；已包含 `.nojekyll`。
