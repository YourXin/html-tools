# 🛠️ HTML 工具集

> 个人常用在线工具集合 · 纯前端、零构建、即开即用

[![GitHub Pages](https://img.shields.io/badge/demo-GitHub%20Pages-blue?logo=github)](https://yourxin.github.io/html-tools/)
[![License](https://img.shields.io/badge/license-MIT-green)]()

一个由 19 个单文件 HTML 工具组成的集合，覆盖加解密、JSON 处理、SQL 工具、日志分析、代码处理、图片压缩等场景。所有工具均**纯前端运行**，无需后端、无需安装、双击 HTML 即可使用。

## 🌐 在线访问

👉 **<https://yourxin.github.io/html-tools/>**

> 部署在 GitHub Pages，打开首页即可看到所有工具的卡片导航。

## 📂 工具列表

### 🔐 加解密
| 工具 | 说明 |
|---|---|
| **AES-CBC 解密 (Base64)** | 自动清洗 Base64（兼容 URL-safe），Latin1 编码匹配 Java `getBytes("ASCII")` |
| **AES-128-CBC (Hex)** | 原生 Web Crypto API，十六进制输入，零外部依赖 |

### 📦 JSON 工具
| 工具 | 说明 |
|---|---|
| **JSON 压缩/转义** | 格式化、压缩、Unicode 互转、中文标点转英文 |
| **JSON Formatter** | JSON 美化与精简 |
| **JSON 问答表格解析器** | 从 JSON 提取问答对（"提取龙珠"业务） |
| **龙湖 JSON 转问答** | 龙湖数据 JSON → 问答表格 |

### 🗄️ SQL / 数据库
| 工具 | 说明 |
|---|---|
| **MyBatis SQL 解析** | 从 MyBatis 日志中提取真实 SQL |
| **数据导出 (SQL→Excel)** | 支持多行字段的导出 |
| **SQL 处理** | SQL 文本批量替换 |
| **积分商城补发 SQL** | 自动生成补发 SQL 语句 |

### 📜 日志 / 调试
| 工具 | 说明 |
|---|---|
| **日志按时间合并** | 多源日志按时间戳对齐合并 |
| **堆栈过滤** | 仅保留 `com.qianfan123.` 开头的栈行 |

### 💻 代码 / 文本
| 工具 | 说明 |
|---|---|
| **Java 代码排序** | `tradeParam.setXxx` 按自然顺序排序 |
| **自增数据生成器** | 批量生成自增编号 |
| **Fiddler Raw → cURL** | Fiddler 抓包报文转 cURL 命令 |
| **随机数字生成器** | 支持日期前缀 + 可控长度 |

### 🖼️ 图片处理
| 工具 | 说明 |
|---|---|
| **图片压缩** | 通用 canvas 压缩，可指定目标大小 |
| **JPEG 压缩 (保 EXIF)** | 保留 EXIF 元数据，去除 JFIF 段（piexifjs） |

### 📝 表格 / 文本
| 工具 | 说明 |
|---|---|
| **表格转 Markdown** | 实时转换表格为 Markdown |

## 🚀 本地预览

```bash
# 直接用浏览器打开 index.html
open index.html           # macOS
start index.html          # Windows
xdg-open index.html       # Linux

# 或起一个本地服务器（推荐）
python3 -m http.server 8000
# 访问 http://localhost:8000
```

## 📦 部署到 GitHub Pages

```bash
# 1. 初始化并推送
git init
git add .
git commit -m "feat: 工具集首页 + 19个工具"
git branch -M main
git remote add origin https://github.com/YourXin/html-tools.git
git push -u origin main

# 2. GitHub 仓库 → Settings → Pages
#    Source: Deploy from a branch
#    Branch: main / root → Save

# 3. 等待 1-2 分钟，访问 https://yourxin.github.io/html-tools/
```

## 🗂️ 目录结构

```
html-tools/
├── index.html                       # 工具导航首页
├── README.md                        # 本文件
│
├── 128-decrpyt.html                 # AES-CBC 解密 (Base64)
├── aes-decrpyt (2).html             # AES-128-CBC (Hex)
│
├── json-format.html                 # JSON 压缩/转义
├── json_trim.html                   # JSON Formatter
├── 提取龙珠.html                    # JSON 问答解析
├── 龙湖-转问答.html                 # 龙湖 JSON 转问答
│
├── mybatis-sql.html                 # MyBatis SQL 解析
├── sql2excel.html                   # SQL → Excel
├── sql_replace.html                 # SQL 替换
├── 生成积分商城补发sql.html         # 积分补发 SQL
│
├── merge_logs_by_time.html          # 日志按时间合并
├── 堆栈处理.html                    # 堆栈过滤
│
├── sort_code.html                   # Java 代码排序
├── increase_num1.html               # 自增数据生成
├── fiddler-raw-to-curl.html         # Fiddler → cURL
├── random.html                      # 随机数字生成器
│
├── 压缩图片.html                    # 图片压缩
├── 压缩图片 (1).html                # JPEG 压缩 (保 EXIF)
│
└── 表格转 Markdown.html             # 表格转 Markdown
```

## ✨ 特性

- 🎨 **统一首页** — 卡片化分类导航，搜索过滤 (`/` 快捷键聚焦)
- 📱 **响应式** — 桌面 / 移动端自适应
- 🌗 **暗色模式** — 跟随系统
- 🚀 **零依赖** — 除个别工具用 CDN（crypto-js、piexifjs），其余纯原生 JS
- 🔒 **隐私安全** — 所有计算在浏览器本地完成，数据不上传任何服务器

## 🤝 贡献

欢迎提交 PR 添加新工具：

1. 新建 `xxx.html` 单文件工具
2. 在 `index.html` 的对应分类下添加卡片
3. 提交 PR

## 📄 License

MIT
