# 🏮 劉家莊燜雞 官方網站 (Liujiazhuang Menji Official Website)

> 傳承二十年的客家溫暖，新竹九芎湖必吃美食。
> 本專案為「劉家莊燜雞」打造全新的數位品牌門面，結合東方美學設計與現代化網頁技術，提供流暢的跨裝置瀏覽體驗，並實作輕量級的無伺服器內容管理系統 (Serverless CMS)。

🔗 **Live Demo (網站上線網址):** [https://M11202131.github.io/liujiazhuang-web/](https://M11202131.github.io/liujiazhuang-web/)

---

## ✨ 核心特色與功能 (Features)

* 📱 **響應式網頁設計 (RWD):** 完美適配桌機、平板與手機螢幕。使用 CSS Media Queries 自動切換排版，確保行動裝置優先的瀏覽體驗。
* ⚡ **極致的載入效能:** 採用純前端技術 (Vanilla JS, HTML5, CSS3) 手工打造，無多餘的沉重框架，網頁秒速載入。
* 📝 **無痛協作內容管理 (Serverless CMS):** 針對「最新消息」區塊，串接 Google Sheets API。餐廳員工只需像平常一樣編輯 Google 試算表，網頁即會透過 `Fetch API` 即時抓取 CSV 資料並自動渲染更新，達成零學習成本的後台管理。
* 🔍 **SEO 與社群分享優化:** 導入 Open Graph (OG) Tags 與完整 Meta 標籤。當網址分享至 LINE、Facebook 等社群軟體時，會自動呈現帶有品牌視覺的精美縮圖與介紹。
* 🎨 **質感東方美學:** 運用 `writing-mode` 實作直式中文排版，搭配印章紅 (`#A62B2B`)、墨黑 (`#2A2A2A`) 與宣紙米白 (`#F7F5F0`) 的色彩計畫，完美傳遞老店底蘊。並使用 `mix-blend-mode` 處理影像去背融合。

---

## 🛠️ 技術棧 (Tech Stack)

### 前端技術 (Frontend)
* **HTML5:** 語意化標籤架構，包含完整的跨頁面導覽結構 (共 6 頁)。
* **CSS3:** * 使用 CSS Flexbox 與 CSS Grid 建構複雜的雙欄與網格佈局。
    * 全域 CSS Variables (變數) 集中管理品牌色彩。
    * Media Queries 處理 RWD 斷點 (Breakpoints: 768px)。
* **JavaScript (ES6+):** * Vanilla JS 實作動態資料載入。
    * 使用 `fetch()` 進行非同步 API 請求 (Asynchronous requests)。

### 工具與部署 (Tools & Deployment)
* **Version Control:** Git / GitHub
* **Hosting:** GitHub Pages (CI/CD 自動化靜態部署)
* **Database / CMS:** Google Sheets (發布為 CSV 格式作為唯讀 API)

---

## ⚙️ 核心架構解析：Google Sheets 輕量化後台
為了解決無程式背景使用者的更新痛點，本專案放棄傳統的關聯式資料庫與沉重後台，改採 Serverless 架構：

1. Data Source: 將 Google 試算表發布為網頁 (CSV 格式)。

2. Fetch & Parse: 在前端使用 JavaScript fetch() 抓取該 CSV 網址。

3. Data Binding: 透過 JS 的字串處理 (split, substring) 解析逗號分隔值，並使用 DOM API (document.createElement) 動態生成 HTML 結構 (<li>) 插入網頁中。

4. Error Handling: 實作 .catch() 捕捉連線異常，並提供友善的 fallback UI。

--- 

## 👨‍💻 作者 (Author)
謝霆鋒

* Role: Full-Stack Developer / Web Engineer

* GitHub: @M11202131

(歡迎透過 GitHub 或 Email 與我聯繫，交流網頁開發與系統架構相關技術！)