# Amazon-Sale-Summary-Extractor -- Created by Gemini
Extract sales and expenses from amazon summary pdf files
# Amazon Financial Report Extractor 📊

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Pure Frontend](https://img.shields.io/badge/Architecture-Pure%20Frontend-success)](#)
[![Data Privacy](https://img.shields.io/badge/Data-100%25%20Local-brightgreen)](#)

[🇨🇳 简体中文文档请向下滚动 / Scroll down for Chinese documentation](#亚马逊财务报表智能提取工具-)

A highly robust, pure frontend web application designed for Amazon Sellers to batch extract **Income** and **Expense** data from Seller Central PDF summary reports. 

It intelligently handles various global formatting quirks (like European decimal commas and special minus signs), auto-detects currencies, fetches real-time exchange rates, and calculates your net profit in your local currency.

## ✨ Features

- **🛡️ 100% Data Privacy (Zero Server Upload):** All PDF parsing and data extraction are done entirely within your browser using `PDF.js`. Your sensitive financial data never leaves your computer.
- **🌍 Global Marketplace Support:** Intelligently recognizes keywords and currencies across multiple regions (US, CA, UK, DE, FR, IT, ES, SE, TR, PL, JP, AU).
- **🧠 Smart Number Parsing:** Flawlessly handles tricky European number formats (e.g., `1.234,56`), Swedish spaced formats (`2 150,90`), and Unicode minus signs (`−`).
- **💱 Real-Time Exchange Rates:** Fetch live exchange rates against CNY (or your base currency) via API with one click. Rates are cached locally in `localStorage` for 24 hours to save API calls.
- **⚙️ Manual Overrides:** Auto-detection isn't perfect? Easily change the recognized currency for any file via a dropdown menu, and the net totals will recalculate instantly.
- **📥 CSV Export:** Export all extracted data, including calculated exchange rates and a Grand Total summary row, directly to a CSV file for Excel accounting.

## 🚀 Quick Start

Since this is a pure frontend application, no Node.js, Python, or database backend is required.

1. **Clone or Download** this repository.
2. Ensure you have the required files in the same directory:
   - `index.html`
   - `pdf.min.js` (PDF.js core)
   - `pdf.worker.min.js` (PDF.js worker)
   - `tailwindcss.js` (Optional, for styling)
3. **Open `index.html`** in any modern web browser (Chrome, Edge, Safari, Firefox).
4. **Drag and drop** your Amazon PDF reports into the designated area.
5. Click **"Extract Data"** and export your CSV!

## 🛠️ Tech Stack

- **HTML5 / Vanilla JavaScript** (No heavy frameworks like React/Vue needed)
- **[PDF.js](https://mozilla.github.io/pdf.js/)** (For rendering and extracting text coordinates from PDFs)
- **[Tailwind CSS](https://tailwindcss.com/)** (For modern, responsive UI)
- **[ExchangeRate-API](https://www.exchangerate-api.com/)** (For fetching real-time currency rates)

---

<br>

# 亚马逊财务报表智能提取工具 📊

一个强大且完全运行在浏览器端的纯前端网页工具，专为亚马逊卖家设计。用于批量从 Seller Central 下载的 PDF 汇总报表中精准提取**收入 (Income)** 和 **支出 (Expense)** 数据。

本工具能智能处理全球各个站点的格式差异（如欧洲的逗号小数点、特殊的减号等），自动识别货币类型，支持一键获取实时汇率，并自动计算折合人民币的净利润。

## ✨ 核心亮点

- **🛡️ 绝对的数据安全（零上传）：** 所有的 PDF 解析和数据计算都在您的本地浏览器中完成。您的敏感财务数据**绝对不会**被上传到任何服务器。
- **🌍 全球站点兼容：** 完美识别欧美及冷门站点的报表语言与货币（支持 US, CA, UK, DE, FR, IT, ES, SE, TR, PL, JP, AU 等）。
- **🧠 智能数值解析引擎：** 专治各种“奇葩”数字格式。完美兼容欧洲格式（如 `1.234,56`）、带空格的瑞典格式（如 `2 150,90`）以及特殊的 Unicode 减号（`−`）。
- **💱 实时汇率联网与缓存：** 一键调用免费 API 获取全球最新汇率，并自动换算人民币。获取后自动缓存在浏览器 `localStorage` 中 24 小时，避免频繁请求。
- **⚙️ 灵活的人工干预：** 支持手动微调特定货币的汇率，也支持在表格中直接通过下拉菜单修正程序识别错误的货币类型，总计金额会实时重算。
- **📥 报表导出：** 一键导出为包含 BOM 头的 CSV 文件（防止 Excel 乱码），并在文件末尾自动附加“总收入”与“总支出”的人民币汇总行。

## 🚀 快速使用

本工具为纯前端项目，无需安装 Node.js、Python 环境或任何数据库。

1. **下载或克隆** 本仓库到您的电脑。
2. 确保以下文件在同一个文件夹内：
   - `index.html` (主程序)
   - `pdf.min.js` (PDF 解析核心库)
   - `pdf.worker.min.js` (PDF 解析引擎)
   - `tailwindcss.js` (UI 样式库)
3. **双击打开 `index.html`** （使用 Chrome、Edge 等现代浏览器）。
4. 将您的亚马逊 PDF 报表**拖拽**到网页指定区域。
5. 点击 **"开始提取数据"**，核对无误后点击导出即可！

## 💡 部署指南 (可选)

如果您希望在任何设备上都能随时访问此工具，您可以将其免费托管在任何静态网页服务商上：
- [Cloudflare Pages](https://pages.cloudflare.com/) (极力推荐，直接拖拽文件夹即可上线)
- [Netlify Drop](https://app.netlify.com/drop)
- [GitHub Pages](https://pages.github.com/)

Screenshot
- <img width="1830" height="873" alt="image" src="https://github.com/user-attachments/assets/394689c0-9f1f-4a62-9777-8015dc86e8f0" />


## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
