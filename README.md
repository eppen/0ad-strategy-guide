# 0 A.D. 游戏攻略

> 面向 **Release 28 "Boiorix"** 及后续版本的非官方中文攻略。

## 在线阅读

**站点：** https://0ad.eppencn.com/

备用地址：https://eppen.github.io/0ad-strategy-guide/

## 本地预览

```bash
pip install -r requirements.txt
mkdocs serve
```

浏览器打开 <http://127.0.0.1:8000/>

## 内容目录

| 章节 | 文件 |
|------|------|
| 首页 | [docs/index.md](docs/index.md) |
| 入门指南 | [docs/01-getting-started.md](docs/01-getting-started.md) |
| 核心机制 | [docs/02-game-basics.md](docs/02-game-basics.md) |
| 经济发展 | [docs/03-economy.md](docs/03-economy.md) |
| 军事战术 | [docs/04-military.md](docs/04-military.md) |
| 三阶段进阶 | [docs/05-phases.md](docs/05-phases.md) |
| 文明详解 | [docs/06-civilizations.md](docs/06-civilizations.md) |
| 多人对战 | [docs/07-multiplayer.md](docs/07-multiplayer.md) |
| 进阶技巧 | [docs/08-advanced-tips.md](docs/08-advanced-tips.md) |

## 自定义域名 `0ad.eppencn.com`

域名在 [Cloudflare](https://dash.cloudflare.com/) 管理（`eppencn.com` 注册商为 Cloudflare Registrar）。

### 1. Cloudflare DNS

在 **DNS → Records** 添加：

| 类型 | 名称 | 内容 | 代理 |
|------|------|------|------|
| CNAME | `0ad` | `eppen.github.io` | 仅 DNS（灰云）推荐 |

GitHub Pages 要求验证域名所有权；若 Enforce HTTPS 异常，可先关闭橙云代理再试。

### 2. GitHub Pages

仓库 **Settings → Pages → Custom domain** 填入：

```
0ad.eppencn.com
```

保存后勾选 **Enforce HTTPS**。`docs/CNAME` 已随构建产物一并部署。

### 3. 自动部署

push 到 `main` 分支时，`.github/workflows/deploy-pages.yml` 自动构建并发布。

## 技术栈

- 文档源文件：Markdown（`docs/`）
- 静态站点：[MkDocs Material](https://squidfunk.github.io/mkdocs-material/)
- 部署：GitHub Actions + GitHub Pages
- 主站博客：[eppencn.com](https://eppencn.com/)（Hexo）

## 许可

攻略文本 [CC BY-SA 4.0](LICENSE)。0 A.D. 游戏版权归 Wildfire Games；本仓库与官方无关联。
