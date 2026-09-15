# cloudflare-trip

行程规划网页项目，部署在 Cloudflare Workers。

## 部署纪律

- **push 到 GitHub 只是存代码，绝对不能自动部署**
- 部署必须用户明确说"发布/部署/上线"才执行
- Windows 本机部署命令：`wrangler deploy`（在 D:\cloudflare-trip 下运行）
- iOS/远程部署命令：`gh workflow run deploy`
- 网址：https://trip.daxiang0007.workers.dev

## 项目结构

- `public/` — 静态网页文件
- `public/singapore/` — 新加坡行程
- `wrangler.jsonc` — Cloudflare 配置（name: trip）
- `.github/workflows/deploy.yml` — 手动触发的部署流水线

## 工作流程

1. 网页文件放 `public/` 下对应子目录
2. commit + push 存档
3. 用户确认后才执行部署
