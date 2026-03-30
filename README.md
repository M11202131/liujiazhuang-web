# 🏮 劉家莊燜雞 (Liu Jia Zhuang Men Ji) 官方網站 V2

本專案為「劉家莊燜雞」打造全新的數位品牌門面，這是一個為新竹九芎湖二十年老店「劉家莊燜雞」翻新開發的現代化響應式官方網站。專注於體現客家傳統風味、柴火燜燒等職人意象，並透過流暢的動態效果與現代感 UI/UX 設計來提升整體瀏覽體驗。

🔗 Live Demo (網站上線網址): https://M11202131.github.io/liujiazhuang-web/

## 🌟 專案特色 (Features)

*   **現代化響應式設計 (RWD)**：全站支援手機、平板、電腦等多種裝置完美顯示。導覽列支援手機版漢堡選單。
*   **深色質感 UI 結合客家意象**：利用大地色系 (Primary `#8B4513`, Secondary `#D97706`)、漸層背景與獨特徽章標籤 (`.stamp`)，傳遞厚重的職人氣息與溫暖純樸的客家文化。
*   **動態載入特效**：全站結合 `IntersectionObserver` 打造滑動視差 (Scroll) 與淡入 (Fade-in) 動畫，增加視覺層次感。
*   **最新消息自動同步 (Google Sheets API)**：
    *   網站首頁的「最新消息」區塊串接了 Google 試算表 (Google Sheets CSV 發布)。
    *   店家只需編輯 Google 試算表內容，網站就會自動抓取更新，無需懂程式碼即可即時維護行銷內容。
    *   內建 CORS 快取與跨域請求代理機制，方便本地直接開啟 (`file://`) 也能順利讀取資料。
*   **無縫聯絡設計**：整合社群按鈕（Line、Facebook、Instagram），並配備固定在右下角的懸浮導航、電話直撥按鈕，優化來客轉換率 (CTA)。

## 📁 網站架構 (Structure)

*   `index.html`: 首頁 (最新消息、招牌美饌預覽、英雄區)
*   `關於我們.html`: 介紹品牌故事、古法傳承工藝與秘境景觀展示 (包含動態輪播)
*   `美味菜單.html`: 完整菜單羅列，以及各項隱藏特色料理的圖片佈局
*   `常見問題.html`: 透過優雅的漸變下拉式摺疊選單提供內用、外帶與宅配相關資訊
*   `交通.html`: 詳細行車指南與在地 Google Maps 內嵌地圖
*   `聯絡我們.html`: 統整營業時間、注意事項與 Line 線上客服預約區
*   `style.css`: 客製化共用樣式 (如 stamp、垂直文字效果、自訂字型調整)
*   `images/`: 存放優化後的影像素材

## 🛠️ 技術棧 (Tech Stack)

*   **HTML5** 語意化結構
*   **CSS3** + [TailwindCSS (CDN)](https://tailwindcss.com/) 快速構建佈局與元件
*   **Vanilla JavaScript (ES6)** 處理輪播、延遲加載、選單開關與 API Fetch
*   **Google Apps API** (CSV Output Format) 作為無伺服器 CMS 資料來源

## 🚀 如何在本地運行

本專案無需特殊構建工具 (No build step required)。

1.  將專案下載或 Clone 至本地。
2.  可以直接雙擊 `index.html` 在瀏覽器中開啟（本地端因為有內建 CORS 中繼代理，可以正常顯示最新消息）。
3.  或使用 VSCode 的 `Live Server` 擴充套件啟動小型的 HTTP Server 瀏覽。

## 📝 部署建議 (Deployment)

適合部屬在任何靜態網頁代管平台上，例如：
*   GitHub Pages
*   Vercel
*   Netlify
*   任何傳統 Web Server (Apache/Nginx)

*註：當網站於正式環境 (`http/https`) 執行時，Google Sheets 資料請求將自動切換為無代理直連，享受最高載入速度。*
