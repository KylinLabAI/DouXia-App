# DouXia — Demo Documentation

[中文介绍](demo.zh.md)

![DouXia Logo](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/logo_256.png)

---

## I. Product Overview

DouXia (Chinese: 豆匣) is an AI knowledge management desktop app that turns scattered AI conversations across Doubao, Yuanbao, DeepSeek, and ChatGPT into organized, searchable, exportable knowledge. It embeds AI platforms directly inside a native desktop app, automatically capturing every conversation to a local SQLite database, then helping users search, organize, extract, and reuse knowledge — all stored on the user's own computer.

### 1.1 Core Value

| Value Dimension | Description | Interface Preview |
|-----------------|-------------|-------------------|
| **Never lose a conversation** | Auto-capture saves every chat in real time to the local SQLite database | ![Import](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Import.png) |
| **Find anything instantly** | Full-text search (FTS5) across all AI conversations, all platforms | ![Filter](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Filter.png) |
| **Organize at scale** | AI-powered tagging, topic clustering, and knowledge graph visualization | ![Graph](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Graph.png) |
| **Extract real knowledge** | AI summaries and structured knowledge cards from scattered chats | ![AI Summary](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_AI_Summary.png) |

### 1.2 Applicable Users

DouXia is a single-user desktop app for individuals who rely heavily on AI assistants:

| User Type | Core Use Case | Interface Example |
|-----------|---------------|-------------------|
| **AI Power Users** | Capture and search daily AI conversations across multiple platforms | ![Knowledge Graph](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Graph.png) |
| **Researchers** | Organize research Q&A into a searchable, structured knowledge base | ![AI Notes](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_AI_Notes.png) |
| **Developers** | Retrieve past coding solutions and export them for reuse | ![Export Settings](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_File_Export_Folder.png) |
| **Writers** | Collect writing drafts and AI suggestions for later reference | ![Topic Clusters](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Topic_Clusters.png) |

---

## II. Business Process Overview

```
Connect AI Platform → Chat & Auto-Capture → Import History
    ↓
Search & Filter → Organize (Tags / Clusters / Graph)
    ↓
AI Extract Knowledge (Summary / Knowledge Cards) → AI Recommended Cleanup
    ↓
Export (Markdown / HTML / PDF) → LAN Share / Backup
```

| Phase | Operating Role | Core Action |
|-------|----------------|-------------|
| **Connect & Capture** | User | Log in to AI platform inside DouXia, chat auto-captured |
| **Import History** | User | Import existing conversations from supported platforms |
| **Search & Organize** | User | Full-text search, filter, tag, cluster, visualize graph |
| **AI Knowledge Extraction** | AI | Generate summaries and structured knowledge cards |
| **AI Cleanup** | AI | Recommend outdated or low-value conversations for bulk delete |
| **Export & Share** | User | Export to Markdown/HTML/PDF, share via LAN, backup database |

---

## III. Feature Details

### 3.1 Knowledge Management

#### 3.1.1 Import Conversations

Bring your existing conversations into DouXia from any supported AI platform. Select the source platform and import scope (all conversations or recent ones):

![Import Conversations](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Import.png)

Importing conversations creates the foundation for your knowledge base, enabling search, organization, and analysis across all platforms.

#### 3.1.2 Knowledge Graph

The knowledge graph visualizes connections between your conversation topics. Nodes represent topics, edges show relationships, and clicking nodes navigates to related conversations:

![Knowledge Graph](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Graph.png)

#### 3.1.3 Topic Clusters

DouXia automatically groups related conversations into clusters by semantic similarity. Each cluster shows a topic summary and can be renamed for better organization:

![Topic Clusters](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Topic_Clusters.png)

#### 3.1.4 Filter Conversations

The filter panel narrows down the conversation list by platform, date range, tags, and status:

![Filter](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Filter.png)

#### 3.1.5 Delete Conversations

Both single and batch deletion are supported for efficient archive management:

![Delete](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_Delete.png)

---

### 3.2 AI-Powered Features

#### 3.2.1 AI Summary

AI Summary generates a concise overview of long conversations, saved alongside the conversation for quick reference:

![AI Summary](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_AI_Summary.png)

#### 3.2.2 AI Notes (Knowledge Cards)

AI Notes extracts structured knowledge cards — key points, actionable items, and insights — from one or multiple conversations. Generated content can be reviewed and edited before saving:

![AI Notes](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_AI_Notes.png)

#### 3.2.3 AI Recommended Delete

AI analyzes all conversations and recommends which ones are outdated or low-value. Users review recommendations and delete in bulk:

![AI Recommended Delete](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Knowledge_AI_Recommend_Delete.png)

---

### 3.3 Settings

#### 3.3.1 AI Configuration

Configure the AI service used for smart features — API key, AI provider, and model parameters (temperature, max tokens):

![AI Config](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_AI_Config.png)

#### 3.3.2 AI Platform

Manage connected AI platforms — enable/disable platforms, configure platform-specific settings, and set the default platform for new sessions:

![AI Platform](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_AI_Platform.png)

#### 3.3.3 Data Folder

Choose the SQLite database directory, view database size and storage usage, and move the database to a different location:

![Data Folder](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_Data_Folder.png)

#### 3.3.4 File Export Folder

Set a default export folder, choose export format (Markdown, HTML, PDF), and configure export options:

![File Export Folder](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_File_Export_Folder.png)

#### 3.3.5 Auto Import Settings

Enable automatic import, set import frequency, and configure which platforms to auto-import from:

![Auto Import](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_Import_Auto.png)

#### 3.3.6 LAN Sharing

Share your knowledge base on the local network — enable sharing, set the port, and let other devices browse via web browser:

![LAN Share](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_Lan_Share.png)

#### 3.3.7 Language Settings

Switch between English and Chinese interface; changes take effect immediately:

![Language](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_Settings_Language.png)

---

### 3.4 About

View application information — current version, project website and repository, license, and credits:

![About](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/demo/resources/DouXia_About.png)

---

## IV. Technical Architecture

### 4.1 Overall Architecture

DouXia adopts a local-first desktop architecture:

- **Desktop Application**: Native desktop app (Electron) embedding AI platform webviews
- **Storage Layer**: Local SQLite database with FTS5 full-text search index
- **Capture Layer**: Platform-specific strategies — DOM scraping (Doubao/Yuanbao), API injection with Bearer token (DeepSeek), CDP network-layer interception (ChatGPT)
- **AI Pipeline**: User-configured AI provider for tagging, summarization, clustering, and knowledge card extraction
- **Sharing Layer**: Local HTTP server for LAN browser-based knowledge base browsing

### 4.2 Technical Highlights

| Technical Highlight | Description |
|---------------------|-------------|
| **Local-first storage** | All conversations stored in local SQLite — no server uploads, ever |
| **FTS5 full-text search** | Instant search across all platforms and conversations |
| **Platform-specific capture** | Tailored capture strategy per AI platform for reliable extraction |
| **User-owned AI key** | Smart features use the user's own API key — full control over provider and cost |
| **Offline-capable** | Core features (search, browse, export, organize) work without internet |

---

## V. Business Scale and Constraints

| Item | Description |
|------|-------------|
| Applicable scale | Individual users with hundreds to thousands of AI conversations across platforms |
| Supported platforms | Doubao, Yuanbao, DeepSeek, ChatGPT (capture + permanent delete) |
| System requirements | Windows 10+ or macOS 11+ (Apple Silicon / Intel) |
| AI feature dependency | Smart features (tagging, summaries, clustering) require a configured AI API key |
| Data storage | Local disk only; storage size depends on conversation volume |
| Network dependency | Core features work offline; chat and capture require internet to reach AI platforms |

---

## VI. Summary

DouXia digitizes the full lifecycle of AI conversation knowledge for individuals — from capture and import, through search and organization, to AI-powered extraction and cleanup, and finally to export and sharing.

Core value: **Your conversations. Your computer. Your rules.** — DouXia turns months of fragmented AI Q&A into a structured, searchable, reusable personal knowledge base that never leaves your device.

> **System Name**: 豆匣 DouXia AI 知识库收纳工具
> **Core Vision**: Turn scattered AI conversations into organized, searchable, exportable knowledge stored locally.
