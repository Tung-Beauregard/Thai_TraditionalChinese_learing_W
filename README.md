# Learning Thai in Chinese ・ Learning Traditional Chinese in Thai

兩個各自獨立、單一 HTML 檔案就能跑的語言學習網頁，不需要建置流程，瀏覽器打開就能用。

**注意：`.jsx` 原始碼無法直接發布**，能部署的是這裡的 `.html` 檔案。

## 檔案

```
.
├── index.html
├── Learning_Thai_in_Chinese.html               # 中文介面／學泰語
└── Learning_Traditional_Chinese_in_Thai.html   # 泰文介面／學中文
```

### Learning_Thai_in_Chinese.html
中文介面，學泰語：課程闖關（愛心／XP／連續天數）、44 個泰文子音手寫練習（含自動評分）、
Kedmanee 標準鍵盤打字、42 句旅遊聊天短語、測驗練習。

### Learning_Traditional_Chinese_in_Thai.html
泰文介面，學中文（繁體）：ด่านบทเรียน、24 個基礎漢字手寫練習（含自動評分）、
拼音／注音（大千式鍵盤）雙模式打字、42 句旅遊聊天短語、แบบทดสอบ。

## 技術

單一 HTML 檔案，透過 CDN 載入 React 18 + Babel Standalone + Tailwind CSS + Google Fonts。
沒有後端，進度存在瀏覽器 `localStorage`。發音用 Web Speech API。手寫評分是純前端 canvas
像素比對，不需要外部 API。

## 部署到 GitHub Pages

1. 把這三個檔案 push 到 repo 的 `main` branch 根目錄（不需要子資料夾）。
2. Settings → Pages：Source 選 **Deploy from a branch**，Branch 選 **main**、
   資料夾選 **/ (root)**，Save。
3. 等 1-2 分鐘，網址：
   - `https://<帳號>.github.io/<repo>/`
   - `https://<帳號>.github.io/<repo>/Learning_Thai_in_Chinese.html`
   - `https://<帳號>.github.io/<repo>/Learning_Traditional_Chinese_in_Thai.html`
