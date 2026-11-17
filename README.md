# 蜘蛛小英雄 (my-spider)

給小朋友玩的蜘蛛人遊戲：射蜘蛛絲黏房子盪過城市，黏住怪獸再一拳打倒。
遊戲本體是 `app/src/main/assets/index.html`，Android 版用 WebView 包起來。

## 發佈新版（build release）

1. **先放 key**：Settings → Secrets and variables → Actions，需要這 4 個：
   `KEYSTORE_BASE64`、`KEYSTORE_PASSWORD`、`KEY_ALIAS`、`KEY_PASSWORD`
   （沒放的話，workflow 第一步就會停下來並提醒你）
2. 打標籤：`git tag v1.0.1 && git push origin v1.0.1`
3. Actions 會建置簽章 APK、發佈 release，並**自動刪除所有舊 release 與舊 tag，只留最新一個**。
