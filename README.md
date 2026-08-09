# cyk1231.github.io

极简卡片风格个人主页，自动展示 GitHub 公开仓库。

## 工作原理

- `index.html` — 纯静态页面，读取 `repos.json` 渲染卡片
- `.github/workflows/sync-repos.yml` — 每 6 小时自动拉取仓库数据 + pinned 列表，更新 `repos.json`
- 无后端、无框架、无构建步骤

## 本地预览

```bash
# 任一静态服务器即可
python -m http.server 8000
# 访问 http://localhost:8000
```

## 技术栈

- 纯 HTML / CSS / Vanilla JS
- GitHub Pages 托管
- GitHub Actions 定时同步
- 暗色模式跟随系统 + 手动切换
