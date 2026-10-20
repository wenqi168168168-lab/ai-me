# AI 聊天版个人档案 — 部署教程

整站只有 2 个文件：`index.html`（页面+聊天逻辑）、`config.js`（你的资料）。AI 接口用的是免费公开服务，无需注册、无需 key。

## 上线步骤（5 分钟）

1. **建仓库**：GitHub 点 New repository，名字随意（比如 `ai-me`），选 **Public**，Create。
2. **传文件**：进仓库点 `uploading an existing file`，把 `index.html` 和 `config.js` 拖进去，Commit。
3. **开 Pages**：仓库的 **Settings → Pages** → Build and deployment 下面 Source 选 **Deploy from a branch** → Branch 选 `main`、文件夹选 `/(root)` → Save。
4. **等 1~2 分钟**，访问 `https://你的用户名.github.io/仓库名/`，就能跟"AI 版的你"聊天了。

## 改成你自己的资料

只改 `config.js` 里 `PROFILE` 对象：
- `name` / `tagline` / `greeting`：名字、一句话介绍、开场白
- `quickQuestions`：快捷问题按钮
- `systemPrompt`：**最关键**——AI 靠这段指令扮演你。想让它多说什么、少说什么、什么语气，改这里。

改完重新上传 `config.js`，刷新页面即生效。

## 两点提醒

- 这是**公开页面**：`config.js` 里不要写电话、微信号、住址、收入明细。systemPrompt 里我已经写了红线，AI 会拒绝回答这类问题并引导去 X 私信。
- 免费接口适合个人展示页；如果以后访问量大了想换更强的模型或防滥用，再加一层后端藏 key（到时找我，我帮你搭）。
