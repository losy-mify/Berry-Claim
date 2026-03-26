# 🍇 TheBerryHost 每日自动签到

自动每天领取 TheBerryHost Discord 服务器的每日 BerryCoins 奖励。

## 使用方法

### 1. 设置 GitHub Secrets

**Settings** → **Secrets and variables** → **Actions** → **New repository secret**

| Secret 名称 | 是否必填 | 说明 | 格式 |
|-------------|----------|------|------|
| `DISCORD_TOKEN` | ✅ 必填 | Discord 账号 Token | 打开 Discord 网页版 → F12 → Network → 任意请求 → Headers → `authorization` |
| `SESSION_ID` | ✅ 必填 | Discord Session ID | F12 → Network → 找一个 `interactions` 请求 → Payload → `session_id` |
| `PRIVATE_REPO_TOKEN` | ✅ 必填 | GitHub PAT（有私库读取权限） | `github_pat_xxxxxx` |
| `GOST_PROXY` | ⭕ 可选 | 代理地址，不填则直连 | `socks5://user:pass@host:port` |
| `TG_BOT` | ⭕ 可选 | Telegram 通知，不填则跳过 | `CHAT_ID,BOT_TOKEN` |

### 2. 运行

- **自动运行**：每天北京时间 09:00 自动执行
- **手动运行**：Actions → TheBerryHost 每日领取 → Run workflow

## ⚠️ 注意事项

- 本脚本仅供学习研究，使用前请了解 [Discord 服务条款](https://discord.com/terms)
- **请勿**将你的 `DISCORD_TOKEN` 泄露给任何人
- Secrets 在 GitHub 中是加密存储的，Fork 后他人无法看到你的配置
