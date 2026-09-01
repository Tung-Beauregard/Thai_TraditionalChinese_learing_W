# Learning Thai in Chinese ・ Learning Traditional Chinese in Thai

單一 HTML 檔案的語言學習網頁，不需要建置流程，瀏覽器打開就能用。`.jsx` 原始碼無法直接發布。

## 檔案
```
.
├── index.html
├── Learning_Thai_in_Chinese.html
└── Learning_Traditional_Chinese_in_Thai.html
```

## 內容
課程闖關（泰語 42 個子音／中文 24 個漢字，各自一課含例句）、手寫練習（自動評分）、
打字練習、旅遊短語／聊天用語（各 42 句）、口說練習、測驗練習。

## 部署到 GitHub Pages
1. 三個檔案 push 到 repo 的 `main` branch 根目錄。
2. Settings → Pages：Deploy from a branch，main、/ (root)，Save。
3. 網址：`https://<帳號>.github.io/<repo>/` 及各檔名。

## 技術
React 18 + Babel Standalone + Tailwind CSS，CDN 載入。進度存在 localStorage。
手寫評分用純前端 canvas 像素比對；口說練習用瀏覽器 SpeechRecognition，
需要麥克風＋網路，電腦版 Chrome/Edge 支援最好。
