<p align="center">
  <img src="https://img.shields.io/badge/STDN-Studio-6366f1?style=for-the-badge&logo=qrcode&logoColor=white" alt="STDN Studio" />
  <br/>
  <strong>专业品牌化二维码生成与解析平台</strong>
  <br/>
  <sub>支持多类型数据嵌入、批量文件智能解析、艺术融合码与全功能扫码识别。</sub>
</p>


<p align="center">
  <a href="https://github.com/marychobbs/qr-studio">
    <img src="https://img.shields.io/badge/🔗_GitHub_仓库-4f46e5?style=for-the-badge&logo=github" alt="GitHub Repo" />
  </a>
  &nbsp;
  <img src="https://img.shields.io/badge/license-MIT-22c55e?style=for-the-badge" alt="License" />
  &nbsp;
  <img src="https://img.shields.io/badge/dependencies-TailwindCSS_%7C_SheetJS_%7C_PDF.js-8b5cf6?style=for-the-badge" alt="Tech Stack" />
</p>


---

## 🚀 项目简介

**STDN Studio** 是一个功能强大、开箱即用的现代化专业二维码生成与解析平台。本项目采用纯前端架构设计，所有数据计算、文件解析及二维码渲染均在用户的本地浏览器中安全完成，无需依赖任何后端服务器。

无论您是需要制作带有品牌 Logo 与精美海报边框的营销码、通过上传 Excel / Word / PDF / TXT 批量生成产品批次二维码，还是进行实时扫码与文档解析，STDN Studio 都能为您提供极致的体验。

---

## ✨ 核心功能特性

### 1. 丰富的数据类型支持 (Data Types)

* **网络与基础**：网址 (URL)、纯文本 (Text)、电子邮箱 (Email)、电话 (Phone)、短信 (SMS)。
* **商务与便民**：
  * **电子名片 (vCard)**：一键将姓名、电话、公司、职位及邮箱存入手机通讯录。
  * **WiFi 快捷连接**：内嵌网络名称与密码，扫码免密直连。
  * **地理位置 (Geo)**：内嵌经纬度与位置描述，一键拉起地图导航。
  * **社交/社群 (Social)**：支持微信、钉钉、WhatsApp、领英等快捷跳转。
  * **日历事件 (iCal)**：一键将日程活动加入手机日历。
  * **应用下载 (App Store / Google Play)**：智能识别设备系统跳转。

### 2. 多格式文件批量解析与二维码生成 (Batch & File Import)

* 支持**批量文本**多行输入，毫秒级实时生成多个独立二维码预览及下载。
* **多格式文件智能导入与提取**：
  * **Excel (.xlsx / .xls)**：自动解析表格单元格提取文本源（基于 `SheetJS`）。
  * **Word (.docx)**：精准提取文档原生文本（基于 `Mammoth.js`）。
  * **PDF 文档**：多页文字安全提取与转换（基于 `PDF.js`）。
  * **TXT 纯文本**：按行自动拆分批量生成。

### 3. 品牌美化与海报模板 (Styling & Posters)

* **码点形状定制**：支持经典方形、圆角矩形、圆点阵列、晶体菱形、动态胶囊、潮流十字及纵横条纹等多种风格。
* **中心 Logo 嵌入**：支持自定义上传品牌 Logo 图标，并自带防遮挡白色保护遮罩。
* **海报边框与自定义文字**：提供丰富的边框预设模板（商务简约、节日预设等），支持独立可调节的顶部标语与底部说明，支持自定义字号、字重,、颜色及多达几十种中英文字体。

### 4. ChromaCode 艺术融合码 (Art Fusion)

* 支持上传自定义背景画布图片，自由调节背景清晰度与矩阵逻辑无缝融合，生成高视觉冲击力的艺术二维码。

### 5. 实时扫码与文件识别 (Scanner & Decoder)

* 支持开启设备摄像头进行实时视频流扫码识别（基于 `jsQR`）。
* 支持本地上传二维码图片进行精准解析与内容提取。

---

## 快速开始

### 选项 1：直接使用

访问 **[marychobbs.github.io/qr-studio](https://github.com/marychobbs/qr-studio)** — 即刻体验。

### 选项 2：私有化部署 (Self-host)

```bash
git clone [https://github.com/marychobbs/qr-studio.git](https://github.com/marychobbs/qr-studio.git)
cd qr-studio
# 在任意浏览器中打开 index.html 即可。
```

无需安装任何依赖。无需构建步骤。无需繁琐配置。

qr-studio/
├── index.html   ← 整个应用（单文件）
├── worker.js   ← 用于 ChromaCode 网站图标代理的 Cloudflare Worker（可选）[cite: 1, 2]
├── README.md  [cite: 1, 2]
└── LICENSE    [cite: 1, 2]



### **选项 3：部署到 GitHub Pages**

1. Fork 本仓库

2. 前往 **Settings → Pages**

   

3. 在 **Source** 下方，选择 main 分支和 / (root) 根目录

4. 点击 **Save**

   

5. 您的项目将发布在 https://<你的用户名>.github.io/qr-studio

   

## **技术栈**

| **层级**       | **技术**                                                     |
| -------------- | ------------------------------------------------------------ |
| **标记与逻辑** | 原生 HTML、Tailwind CSS、JavaScript                          |
| **二维码引擎** | [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) (1.4.4) |
| **二维码扫描** | [jsQR](https://github.com/cozmo/jsQR) (1.4.0，懒加载)        |
| **文件解析库** | SheetJS (xlsx) + Mammoth.js + PDF.js                         |
| **构建系统**   | 无。只有一个文件。                                           |
| **后端**       | 无。纯客户端运行。                                           |
| **CORS 代理**  | [Cloudflare Worker](https://workers.cloudflare.com)（可选，用于 ChromaCode 网站图标代理） |
| **追踪统计**   | 无。我们严格尊重您的隐私。                                   |

## **支持的二维码类型**

| **类型**             | **编码格式**                      | **示例**                 |
| -------------------- | --------------------------------- | ------------------------ |
| **网址 (URL)**       | https://example.com               | 网站链接                 |
| **文本 (Text)**      | 原始文本                          | 消息、便签               |
| **WiFi**             | WIFI:T:WPA;S:MyNet;P:pass123;;    | 自动连接网络             |
| **电子名片 (vCard)** | vCard 3.0 格式                    | 完整的个人名片卡片       |
| **地理位置 (Geo)**   | geo:48.8584,2.2945                | 地图与坐标               |
| **社交/社群**        | 平台链接 / 账号 ID                | 微信、钉钉、WhatsApp 等  |
| **日历事件**         | iCalendar (.ics) 格式             | 包含时间、地点的日程活动 |
| **应用下载**         | App Store / Google Play 链接      | 智能设备系统跳转         |
| **邮箱 (Email)**     | mailto:hi@example.com?subject=... | 预填邮件                 |
| **电话 (Phone)**     | tel:+15551234567                  | 点击拨打电话             |
| **短信 (SMS)**       | sms:+15551234567?body=...         | 预填短信内容             |

## **ChromaCode 网站图标代理配置（可选）**

ChromaCode 的 **Favicon**（网站图标）标签页会自动获取网站图标并将其融合进二维码中。由于浏览器会阻止跨域图片请求（CORS），因此这需要一个代理。如果没有配置代理，**Upload**（上传）和 **Image URL**（图片链接）标签页依然可以完美工作。

您可以使用免费的 [Cloudflare Worker](https://workers.cloudflare.com) 搭建属于您自己的个人 CORS 代理（免费层每天可提供 100,000 次请求）。

### **部署步骤参考（基于 worker.js）**

：

1. 注册并登录 [workers.cloudflare.com](https://workers.cloudflare.com)（免费）

2. 点击 **Create Worker**（创建 Worker）→ **Start with Hello World!**（从 Hello World 开始）

3. 将其命名为 qr-proxy

   

4. 点击 **Edit Code**（编辑代码），清空所有默认内容，并将 [worker.js](https://www.google.com/search?q=worker.js) 中的完整代码粘贴进去[cite: 1, 2]

5. 点击 **Deploy**（部署）

6. 进行测试 —— 通过浏览器访问您的 worker 地址并附带一个测试图标链接：
   [https://qr-proxy.你的子域名.workers.dev/?url=https://www.google.com/favicon.ico](https://qr-proxy.你的子域名.workers.dev/?url=https://www.google.com/favicon.ico)

   如果配置成功，您应当能看到 Google 的网站图标。

7. 打开 index.html，找到以下这一行代码，并将您的 worker 地址填入其中：
   JavaScript
   const MY_PROXY = ''; // ← 在此处粘贴您的 worker URL

   修改为：
   JavaScript
   const MY_PROXY = '[https://qr-proxy.你的子域名.workers.dev](https://qr-proxy.你的子域名.workers.dev)';

   

8. 推送代码到 GitHub —— 大功告成。现在 ChromaCode 的网站图标自动获取功能已对所有网站生效。

### **无代理模式**

公共 CORS 代理（如 allorigins.win、codetabs.com）在代码中被用作备用方案。它们适用于大多数网站，但有时可能会较慢或阻止某些特定域名。而“上传”标签页则不受影响，任何时候都可以正常使用[cite: 1]。

## **参与贡献**

欢迎提交贡献！如果您对新功能有好的想法、发现了漏洞，或是想要改进代码[cite: 1]：

1. Fork 本仓库[cite: 1]
2. 创建您的特性分支 (git checkout -b feature/amazing-thing)[cite: 1]
3. 提交您的修改 (git commit -m 'Add amazing thing')[cite: 1]
4. 推送到该分支 (git push origin feature/amazing-thing)[cite: 1]
5. 开启 Pull Request[cite: 1]

由于整个应用仅仅是一个单 HTML 文件，贡献代码就像编辑单个文件一样简单 —— 无需面对复杂的项目目录结构[cite: 1]。

## **开源许可证**

本项目基于开源的 [MIT License](https://www.google.com/search?q=LICENSE) 协议进行分发与使用[cite: 1]。
