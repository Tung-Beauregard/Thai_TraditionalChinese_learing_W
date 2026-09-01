# Learning Thai in Chinese ・ Learning Traditional Chinese in Thai

兩個各自獨立、單一 HTML 檔案就能跑的語言學習網頁，不需要建置流程，瀏覽器打開就能用。

**注意：`.jsx` 原始碼無法直接發布**，能部署的是這裡的 `.html` 檔案。

## 檔案

```
.
├── index.html
├── Learning_Thai_in_Chinese.html
└── Learning_Traditional_Chinese_in_Thai.html
```

## 內容

- **課程闖關**：泰語版 42 個子音、中文版 24 個漢字，各自一課，含例句強化練習
- **手寫練習**：Canvas 描摹，含自動評分
- **打字練習**：泰語 Kedmanee 鍵盤／中文拼音＋注音雙模式
- **旅遊短語 / 聊天用語**：各 42 句
- **口說練習**：麥克風錄音比對相似度（見下方說明）
- **測驗練習**：字卡複習 + 選擇題

## 無障礙 / 環境限制設計

- **聽力題可跳過**：任何「只播音、不顯示文字」的聽力題旁都有「跳過這題」，跳過不扣血、
  不算答錯，避免裝置沒聲音時卡關
- **口說練習會主動偵測支援度**：頁面載入時就檢查瀏覽器是否支援 `SpeechRecognition`，
  不支援時直接顯示停用狀態＋提示文字（需要電腦版 Chrome / Edge），不用等使用者點了才報錯

## 技術

React 18 + Babel Standalone + Tailwind CSS + Google Fonts，全部透過 CDN 載入。
沒有後端，進度存在瀏覽器 `localStorage`。

**手寫評分**：純前端 canvas 像素比對，離線也能算分。

**口說練習**：Web Speech API 的 `SpeechRecognition`，需要麥克風權限與網路連線
（辨識雲端處理），電腦版 Chrome / Edge 支援最好，Safari / Firefox 支援有限或不支援。
分數是比對「辨識出的文字」跟目標句子的文字相似度，不是精準的發音評分，僅供參考。

## 部署到 GitHub Pages

1. 把這三個檔案 push 到 repo 的 `main` branch 根目錄（不需要子資料夾）。
2. Settings → Pages：Source 選 Deploy from a branch，Branch 選 main、資料夾選 / (root)，Save。
3. 網址：
   - `https://<帳號>.github.io/<repo>/`
   - `https://<帳號>.github.io/<repo>/Learning_Thai_in_Chinese.html`
   - `https://<帳號>.github.io/<repo>/Learning_Traditional_Chinese_in_Thai.html`
