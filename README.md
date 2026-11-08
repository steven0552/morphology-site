# 型態掃描器 — 網站

純靜態網站（HTML／CSS／JS＋預先產生的 JSON 資料），無需建置。
資料是某一時間點的快照，不會自動更新；要持續更新需另有掃描程式產生新資料。

## 結構
```
├── index.html
├── css/  js/  img/
├── data/            # scan.json、bars/、triangles.json、tw/（台股）…
├── _headers         # Cloudflare 標頭與快取
└── wrangler.toml
```

## 本機預覽
```bash
python -m http.server 8000   # 然後開 http://localhost:8000
```

## 選用：Discord 登入／雲端觀察名單
`js/app.js` 約第 1701 行的 `YOUR_SUBDOMAIN` 是 Discord 觀察名單 Worker 的網址佔位。
沒有自己的 Worker 就保持原樣，網站照常運作（星號只存瀏覽器，登入會顯示無法使用）。
