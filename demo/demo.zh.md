# 豆匣 DouXia — 演示文档

[English](demo.md)

![豆匣 Logo](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/logo_256.png)

---

## 一、产品概览

豆匣 DouXia 是一款 AI 知识管理桌面应用，将散落在豆包、元宝、DeepSeek、ChatGPT 之间的 AI 对话，整理为有序、可搜索、可导出的知识。它将 AI 平台直接内嵌于原生桌面应用中，自动将每条对话捕获到本地 SQLite 数据库，并帮助用户搜索、整理、抽取与复用知识——所有数据均保存在用户自己的电脑上。

### 1.1 核心价值

| 价值维度 | 说明 | 界面预览 |
|----------|------|----------|
| **永不丢失对话** | 自动捕获实时将每条对话保存到本地 SQLite 数据库 | ![导入](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Import.png) |
| **瞬时找到任意内容** | 跨所有平台、所有 AI 对话的全文搜索（FTS5） | ![筛选](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Filter.png) |
| **规模化整理** | AI 打标签、话题聚类与知识图谱可视化 | ![图谱](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Graph.png) |
| **抽取真实知识** | 从散落对话中生成 AI 摘要与结构化知识卡片 | ![AI 摘要](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_AI_Summary.png) |

### 1.2 适用用户

豆匣为单用户桌面应用，面向重度依赖 AI 助手的个人用户：

| 用户类型 | 核心用途 | 界面示例 |
|----------|----------|----------|
| **AI 重度用户** | 捕获并搜索跨多个平台的日常 AI 对话 | ![知识图谱](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Graph.png) |
| **研究人员** | 将研究问答整理为可搜索、结构化的知识库 | ![AI 笔记](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_AI_Notes.png) |
| **开发者** | 检索过往编程方案并导出复用 | ![导出设置](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_File_Export_Folder.png) |
| **写作者** | 收集写作草稿与 AI 建议以备后用 | ![话题聚类](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Topic_Clusters.png) |

---

## 二、业务流程总览

```
连接 AI 平台 → 对话与自动捕获 → 导入历史
    ↓
搜索与筛选 → 整理（标签 / 聚类 / 图谱）
    ↓
AI 抽取知识（摘要 / 知识卡片） → AI 推荐清理
    ↓
导出（Markdown / HTML / PDF） → 局域网分享 / 备份
```

| 阶段 | 操作角色 | 核心动作 |
|------|----------|----------|
| **连接与捕获** | 用户 | 在豆匣中登录 AI 平台，对话自动捕获 |
| **导入历史** | 用户 | 从受支持平台导入已有对话 |
| **搜索与整理** | 用户 | 全文搜索、筛选、打标签、聚类、图谱可视化 |
| **AI 知识抽取** | AI | 生成摘要与结构化知识卡片 |
| **AI 清理** | AI | 推荐过时或低价值对话，批量删除 |
| **导出与分享** | 用户 | 导出 Markdown/HTML/PDF、局域网分享、备份数据库 |

---

## 三、功能详解

### 3.1 知识管理

#### 3.1.1 导入对话

从任一受支持的 AI 平台将已有对话导入豆匣。可选择来源平台与导入范围（全部对话或仅近期对话）：

![导入对话](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Import.png)

导入对话为知识库奠定基础，支持跨所有平台的搜索、整理与分析。

#### 3.1.2 知识图谱

知识图谱可视化对话话题之间的联系。节点代表话题，边表示关系，点击节点可跳转到相关对话：

![知识图谱](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Graph.png)

#### 3.1.3 话题聚类

豆匣按语义相似度自动将相关对话分组为聚类。每个聚类显示话题摘要，可重命名以便整理：

![话题聚类](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Topic_Clusters.png)

#### 3.1.4 筛选对话

筛选面板可按平台、日期范围、标签与状态缩小对话列表：

![筛选](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Filter.png)

#### 3.1.5 删除对话

支持单条与批量删除，便于高效管理对话归档：

![删除](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Delete.png)

---

### 3.2 AI 智能功能

#### 3.2.1 AI 摘要

AI 摘要为长对话生成精炼概述，保存在对话旁便于快速查阅：

![AI 摘要](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_AI_Summary.png)

#### 3.2.2 AI 笔记（知识卡片）

AI 笔记从一条或多条对话中抽取结构化知识卡片——关键点、可执行项与洞察。生成内容可在保存前审阅与编辑：

![AI 笔记](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_AI_Notes.png)

#### 3.2.3 AI 推荐删除

AI 分析所有对话，推荐哪些过时或低价值。用户审阅推荐结果并批量删除：

![AI 推荐删除](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_AI_Recommend_Delete.png)

---

### 3.3 设置

#### 3.3.1 AI 配置

配置用于智能功能的 AI 服务——API Key、AI 服务商及模型参数（温度、最大 token 数）：

![AI 配置](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_AI_Config.png)

#### 3.3.2 AI 平台

管理已连接的 AI 平台——启用/禁用平台、配置平台专属设置、设置新会话的默认平台：

![AI 平台](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_AI_Platform.png)

#### 3.3.3 数据文件夹

选择 SQLite 数据库目录，查看数据库大小与存储占用，并可将数据库移动到其他位置：

![数据文件夹](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_Data_Folder.png)

#### 3.3.4 文件导出文件夹

设置默认导出文件夹，选择导出格式（Markdown、HTML、PDF），配置导出选项：

![文件导出文件夹](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_File_Export_Folder.png)

#### 3.3.5 自动导入设置

启用自动导入，设置导入频率，配置自动导入的平台：

![自动导入](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_Import_Auto.png)

#### 3.3.6 局域网分享

在局域网内分享知识库——启用分享、设置端口，让其他设备通过浏览器浏览：

![局域网分享](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_Lan_Share.png)

#### 3.3.7 语言设置

在中英文界面间切换，更改立即生效：

![语言](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_Language.png)

---

### 3.4 关于

查看应用信息——当前版本、项目网站与仓库、许可证及致谢：

![关于](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_About.png)

---

## 四、技术架构

### 4.1 整体架构

豆匣采用本地优先的桌面架构：

- **桌面应用**：原生桌面应用（Electron），内嵌 AI 平台 webview
- **存储层**：本地 SQLite 数据库 + FTS5 全文搜索索引
- **捕获层**：按平台差异化策略——DOM 抓取（豆包/元宝）、API 注入 + Bearer token（DeepSeek）、CDP 网络层拦截（ChatGPT）
- **AI 流水线**：用户自配 AI 服务商，用于打标签、摘要、聚类与知识卡片抽取
- **分享层**：本地 HTTP 服务器，支持局域网浏览器知识库浏览

### 4.2 技术亮点

| 技术亮点 | 说明 |
|----------|------|
| **本地优先存储** | 所有对话存于本地 SQLite——绝不上传服务器 |
| **FTS5 全文搜索** | 跨所有平台与对话的即时搜索 |
| **平台专属捕获** | 针对各 AI 平台定制捕获策略，提取更可靠 |
| **用户自有 AI Key** | 智能功能使用用户自己的 API Key——完全掌控服务商与成本 |
| **离线可用** | 核心功能（搜索、浏览、导出、整理）无需联网 |

---

## 五、业务规模与约束

| 项目 | 说明 |
|------|------|
| 适用规模 | 跨平台拥有数百至数千条 AI 对话的个人用户 |
| 支持平台 | 豆包、元宝、DeepSeek、ChatGPT（捕获 + 永久删除） |
| 系统要求 | Windows 10+ 或 macOS 11+（Apple Silicon / Intel） |
| AI 功能依赖 | 智能功能（打标签、摘要、聚类）需配置 AI API Key |
| 数据存储 | 仅本地磁盘；存储大小取决于对话量 |
| 网络依赖 | 核心功能可离线使用；对话与捕获需联网访问 AI 平台 |

---

## 六、总结

豆匣为个人用户数字化了 AI 对话知识的完整生命周期——从捕获与导入，到搜索与整理，再到 AI 抽取与清理，最终导出与分享。

核心价值：**你的对话，你的电脑，你做主。** 豆匣把数月碎片化的 AI 问答，变成一个结构化、可搜索、可复用且永不离开本机的个人知识库。

> **系统名称**：豆匣 DouXia AI 知识库收纳工具
> **核心愿景**：将散落的 AI 对话整理为有序、可搜索、可导出的本地知识。
