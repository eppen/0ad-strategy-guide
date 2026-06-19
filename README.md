# 0 A.D. 游戏攻略

> 面向 **Release 28 "Boiorix"** 及后续版本的非官方中文攻略。

## 在线阅读

**GitHub Pages：** `https://<你的用户名>.github.io/0ad-strategy-guide/`

（仓库推送至 GitHub 并启用 Pages 后自动部署，详见下方说明。）

## 本地预览

```bash
pip install -r requirements.txt
mkdocs serve
```

浏览器打开 <http://127.0.0.1:8000/0ad-strategy-guide/>

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

## 发布到 GitHub Pages

1. 创建 GitHub 仓库 `0ad-strategy-guide` 并推送本目录：

   ```bash
   gh auth login
   gh repo create 0ad-strategy-guide --public --source=. --remote=origin --push
   ```

   或手动 `git remote add origin ...` 后 `git push -u origin main`。

2. 在仓库 **Settings → Pages** 中，Source 选择 **GitHub Actions**（工作流 `.github/workflows/deploy-pages.yml` 会在 push 到 `main` 时自动构建部署）。

3. 首次部署完成后，站点地址为：

   `https://<GitHub用户名>.github.io/0ad-strategy-guide/`

## 技术栈

- 文档源文件：Markdown（`docs/`）
- 静态站点：[MkDocs Material](https://squidfunk.github.io/mkdocs-material/)
- 部署：GitHub Actions + GitHub Pages

## 许可

攻略文本 [CC BY-SA 4.0](LICENSE)。0 A.D. 游戏版权归 Wildfire Games；本仓库与官方无关联。
