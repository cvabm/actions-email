# actions-email

用 GitHub Actions + Gmail 定时发邮件。当前：**每 5 分钟** 发一封，主题/正文为 **定时任务A**（附北京时间戳）。

## Secrets

**Settings → Secrets and variables → Actions** 配置：

| Name | 说明 |
|------|------|
| `GMAIL_USERNAME` | Gmail 地址 |
| `GMAIL_APP_PASSWORD` | [应用专用密码](https://myaccount.google.com/apppasswords)（需先开两步验证） |
| `EMAIL_TO` | 收件人邮箱 |

## 配置

编辑 `.github/workflows/actions-email.yml`：

- `cron` — 定时（UTC）
- `subject` / `body` — 主题与正文

> `schedule` 可能延迟；仓库长期无活动时可能暂停，推一次代码或手动 Run 可恢复。
