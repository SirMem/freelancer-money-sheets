# AUDIENCE-RENT R0 公开探针 · 2026-10-29 ~10:49 Asia/Shanghai

| URL | HTTP | 含义 |
|-----|------|------|
| https://keithjenn.gumroad.com/affiliates | **404** | 卖家公开联盟报名页未开 / 不存在 |
| https://gumroad.com/affiliates | **302 → login** | 平台通用入口需登录；不能当作 keithjenn 已开联盟 |

结论：R0 **FAIL**（与 AUDIENCE-RENT-GATE 一致）。本探针可复跑；PASS 条件仍是 Kevin 在 Dashboard 对 Invoice/Expense/Client/Bundle 开启联盟并生成可分享 `/a/` 或公开报名页返回非 404。

```bash
curl -sI -o /dev/null -w '%{http_code}\n' https://keithjenn.gumroad.com/affiliates
# expect 200 (or soft landing) when R0 PASS; currently 404
```
