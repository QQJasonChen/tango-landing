# 単語ノート landing page

- `index.html` — **目前線上這一版**（2026-07-31）
- `index-v2.html` — 新版（2026-09-01），還沒切上線
- `index-v1-backup.html` — 切換前的備份

線上：https://qqjasonchen.github.io/tango-landing/
新版預覽：https://qqjasonchen.github.io/tango-landing/index-v2.html

## 要切上線就這一步

```bash
cp index-v2.html index.html && git commit -am "landing v2 上線" && git push
```

## v2 跟 v1 差在哪

| | v1 | v2 |
|---|---|---|
| 截圖 | 舊的深藍介面 | App 已改版成朱色和風，**v1 的截圖跟下載後看到的不是同一個 App** |
| 最強的證明 | 用文字描述「有 AI 文法解析」 | **頁面上直接翻一張真的卡**，再展開 App 裡真正的解析內容 |
| 主打的例子 | 泛泛的賣點 | 「新聞」在日文是**報紙**——中日同形異義詞，一句話證明它真的懂 |
| 頁面長度（手機） | — | 5,647px（截圖改成橫向膠捲，原本疊起來要 10,414px） |
| 資料 | — | 卡片、文法、統計全部從 `multilang/data/` 真實資料抽出，不是示意圖 |

## 重新產生

`/tmp/tango-ui/mkland.py`（會讀 `multilang/data/ja.json`、`grammar_ja.json`、
`tpl/icons_ja.json` 與 App 截圖）。資產有嵌成 base64，所以單檔可直接部署。
