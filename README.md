# Mermaid 圖表工具 / Mermaid Chart Tool

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![HTML](https://img.shields.io/badge/Built%20with-HTML%2FJS-orange.svg)]()
[![No Build Required](https://img.shields.io/badge/No%20Build-Required-green.svg)]()

> 純前端的 Mermaid 圖表即時預覽與匯出工具，無需後端，直接部署即用。  
> A pure frontend Mermaid diagram editor with live preview and high-res export — no backend required.

---

## 目錄 / Table of Contents

- [功能特色 / Features](#功能特色--features)
- [快速開始 / Quick Start](#快速開始--quick-start)
- [使用說明 / Usage Guide](#使用說明--usage-guide)
- [部署 / Deployment](#部署--deployment)
- [Mermaid 語法參考 / Syntax Reference](#mermaid-語法參考--syntax-reference)
- [瀏覽器支援 / Browser Support](#瀏覽器支援--browser-support)
- [授權 / License](#授權--license)

---

## 功能特色 / Features

**中文**
- 即時渲染：輸入後 350ms 自動更新圖表
- 高解析度匯出：PNG 支援 2×、3×、4× 倍率輸出
- SVG 向量匯出：適合印刷與縮放不失真
- 全螢幕預覽：點擊圖表區或按鈕放大，ESC 關閉
- 亮色／暗色主題切換，設定自動記憶
- 中英文介面切換
- 狀態指示燈（渲染中 / 成功 / 語法錯誤）
- 一鍵複製語法

**English**
- Live rendering: diagram updates 350ms after you stop typing
- High-res PNG export: 2×, 3×, or 4× scale multipliers
- SVG vector export: lossless at any size, ideal for print
- Fullscreen preview: click the diagram or press the button; ESC to close
- Light / dark theme with persistent preference
- Chinese / English UI toggle
- Status indicator: loading / success / syntax error
- One-click code copy

---

## 快速開始 / Quick Start

**中文**

無需安裝任何套件。下載後直接用瀏覽器打開，或放到任意靜態伺服器：

```bash
# 用 Python 快速啟動本機伺服器
python3 -m http.server 8080
# 然後打開 http://localhost:8080
```

**English**

No build tools or dependencies to install. Just open the file in a browser, or serve it from any static host:

```bash
# Quick local server with Python
python3 -m http.server 8080
# Then open http://localhost:8080
```

---

## 使用說明 / Usage Guide

### 編輯器 / Editor

**中文**

左側面板為 Mermaid 語法編輯器。輸入或貼上語法後，右側預覽會自動更新。編輯器底部的狀態列會顯示目前狀態：

| 指示燈顏色 | 狀態 |
|-----------|------|
| 🟢 綠色 | 渲染成功 |
| 🟡 黃色（閃爍） | 渲染中 |
| 🔴 紅色 | 語法錯誤 |

**English**

The left panel is the Mermaid syntax editor. The preview updates automatically after you stop typing. The status bar at the bottom shows the current state:

| Indicator color | State |
|----------------|-------|
| 🟢 Green | Rendered successfully |
| 🟡 Yellow (blinking) | Rendering |
| 🔴 Red | Syntax error |

---

### 全螢幕預覽 / Fullscreen Preview

**中文**

- 點擊右側預覽區任意位置放大
- 或點擊右上角「⛶ 全螢幕」按鈕
- 按 `ESC` 或點擊遮罩背景關閉

**English**

- Click anywhere in the right preview pane to zoom in
- Or click the "⛶ Fullscreen" button in the top bar
- Press `ESC` or click the dark overlay to close

---

### 匯出圖片 / Exporting

**中文**

圖表下方工具列提供兩種匯出格式：

**PNG 高解析度匯出**
1. 在檔名欄位輸入想要的檔名（可選，預設為 `mermaid_diagram`）
2. 選擇解析度倍率：
   - `2×`：一般網頁、簡報使用
   - `3×`：Retina 螢幕、高品質截圖
   - `4×`：印刷、大尺寸輸出
3. 點擊「下載 PNG」

**SVG 向量匯出**
- 點擊「SVG」按鈕
- 適合需要縮放不失真的場合（印刷、簡報設計）
- 可直接在 Illustrator、Figma、Inkscape 等工具開啟編輯

**English**

The toolbar below the preview offers two export formats:

**PNG high-res export**
1. Enter a filename (optional; defaults to `mermaid_diagram`)
2. Choose a resolution multiplier:
   - `2×`: General web use and presentations
   - `3×`: Retina displays, high-quality screenshots
   - `4×`: Print and large-format output
3. Click "Download PNG"

**SVG vector export**
- Click the "SVG" button
- Ideal when you need to scale without quality loss
- Opens directly in Illustrator, Figma, Inkscape, and similar tools

---

### 主題與語言 / Theme & Language

**中文**

右上角工具列提供：
- **語言切換**：中文 ↔ English（設定自動儲存於瀏覽器）
- **主題切換**：亮色 ↔ 暗色（設定自動儲存於瀏覽器）

**English**

The top bar provides:
- **Language toggle**: 中文 ↔ English (saved in browser)
- **Theme toggle**: Light ↔ Dark (saved in browser)

---

## 部署 / Deployment

**中文**

本工具為單一 HTML 檔，可部署至任何靜態伺服器：

**Apache2**
```bash
# 將 index.html 複製到網站根目錄
cp mermaid-tool.html /var/www/html/index.html
```

**Nginx**
```bash
cp mermaid-tool.html /usr/share/nginx/html/index.html
```

**GitHub Pages**
1. 將檔案重命名為 `index.html` 並推送到 `main` 分支
2. 在 Repository Settings → Pages 啟用 GitHub Pages
3. 選擇 Source: `Deploy from a branch` → `main` → `/ (root)`

**Netlify / Vercel**
直接拖曳 `index.html` 到部署介面即可。

**English**

This is a single HTML file. Deploy to any static host:

**Apache2**
```bash
cp mermaid-tool.html /var/www/html/index.html
```

**Nginx**
```bash
cp mermaid-tool.html /usr/share/nginx/html/index.html
```

**GitHub Pages**
1. Rename the file to `index.html` and push to `main`
2. Go to Repository Settings → Pages
3. Set Source: `Deploy from a branch` → `main` → `/ (root)`

**Netlify / Vercel**
Drag and drop `index.html` onto the deploy interface.

---

## Mermaid 語法參考 / Syntax Reference

以下為常用圖表類型範例 / Common diagram types:

**流程圖 / Flowchart**
```
graph TD
    A[開始] --> B{條件判斷}
    B -- 是 --> C[執行 A]
    B -- 否 --> D[執行 B]
    C --> E[結束]
    D --> E
```

**時序圖 / Sequence Diagram**
```
sequenceDiagram
    participant 使用者
    participant 伺服器
    使用者->>伺服器: 發送請求
    伺服器-->>使用者: 回傳結果
```

**甘特圖 / Gantt Chart**
```
gantt
    title 專案時程
    dateFormat YYYY-MM-DD
    section 開發
    需求分析: 2024-01-01, 7d
    設計:     2024-01-08, 7d
    開發:     2024-01-15, 14d
```

**類別圖 / Class Diagram**
```
classDiagram
    class Animal {
        +String name
        +makeSound()
    }
    class Dog {
        +fetch()
    }
    Animal <|-- Dog
```

完整語法文件請參考 [Mermaid 官方文件](https://mermaid.js.org/intro/)。  
For full syntax documentation, see the [Mermaid official docs](https://mermaid.js.org/intro/).

---

## 瀏覽器支援 / Browser Support

| 瀏覽器 / Browser | 支援版本 / Supported Version |
|----------------|---------------------------|
| Chrome / Edge  | 90+                       |
| Firefox        | 88+                       |
| Safari         | 14+                       |

本工具使用 CDN 載入 Mermaid.js，需要網路連線。  
This tool loads Mermaid.js from CDN and requires an internet connection.

---

## 授權 / License

本專案採用 **MIT License** 授權。詳見 [LICENSE](LICENSE) 檔案。  
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 [你的名字 / Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

*Built with [Mermaid.js](https://mermaid.js.org/) · [Tailwind CSS](https://tailwindcss.com/)*
