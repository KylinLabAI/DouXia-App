# DouXia — User Manual

[中文介绍](user_manual.zh.md)

![DouXia Logo](https://raw.githubusercontent.com/KylinLabAI/DouXia-App/master/user_manual/resources/logo_256.png)

## Introduction

Welcome to DouXia. This manual guides you through every feature, organized by what you want to accomplish. DouXia is a single-user desktop app — all data stays on your computer.

## Getting Started Guide

### Task: Install DouXia

**Prerequisites:**
- Windows 10+ or macOS 11+ (Apple Silicon or Intel)
- Internet connection for download

**Steps:**

1. Download the installer from the [GitHub Releases page](https://github.com/KylinLabAI/DouXia-App/releases/latest)
   - Windows: `DouXia-Setup-x.x.x.exe`
   - macOS (Apple Silicon): `DouXia-x.x.x-arm64.dmg`
   - macOS (Intel): `DouXia-x.x.x-x64.dmg`
2. Run the installer and follow the prompts
3. Launch DouXia from your applications folder
   - You will see: The main window with Chat, Knowledge, and Settings tabs

**Expected result:** DouXia launches and shows the main interface.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Windows blocks the installer | Right-click the file → Properties → check "Unblock", then run again |
| macOS says "cannot be opened" | Right-click → Open, or allow in System Settings → Privacy & Security |

### Task: First Launch & Platform Login

**Prerequisites:**
- DouXia installed

**Steps:**

1. Open the Chat tab
2. Choose your preferred AI platform (Doubao, Yuanbao, DeepSeek, or ChatGPT)
3. Log in to your AI account within the embedded browser
   - You will see: The familiar AI platform interface inside DouXia
4. Start chatting — conversations are automatically captured by default
   - You will see: A capture indicator confirming the conversation is being saved

**Expected result:** You can chat with your AI platform and conversations are auto-captured to the local database.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Platform page won't load | Check internet connection; the embedded browser needs network access |
| Conversations not captured | Verify auto-capture is enabled in Settings → AI Platform |

## Daily Operations

### Task: Import Existing Conversations

**Prerequisites:**
- An account on the source AI platform
- Logged in to the platform inside DouXia's Chat tab

**Steps:**

1. Go to the Knowledge tab
2. Click the Import button
   - You will see: The Import dialog
3. Select which platform to import from
4. Choose the import scope (all conversations or recent ones only)
5. Confirm and wait for the import to complete
   - You will see: Imported conversations appear in the Knowledge list

**Expected result:** Historical conversations are added to your local knowledge base.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Import is slow | Large histories take time; keep the window open until complete |
| Some conversations missing | Re-run import; very old chats may need manual scroll-loading first |

### Task: Search & Filter Conversations

**Prerequisites:**
- Conversations imported or captured

**Steps:**

1. Go to the Knowledge tab
2. Enter keywords in the search bar to run a full-text search (FTS5)
   - You will see: Matching conversations across all platforms
3. Click the Filter button to narrow results
   - Filter by platform, date range, tags, or status
4. Click a conversation to view its full content

**Expected result:** You can quickly locate any conversation across all platforms.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Search returns no results | Check spelling or broaden the date range filter |
| Filters don't apply | Refresh the Knowledge tab and retry |

### Task: Organize with Tags, Clusters & Graph

**Prerequisites:**
- Conversations in the Knowledge base
- AI service configured (Settings → AI Configuration)

**Steps:**

1. Select one or more conversations and trigger AI Auto-Tagging
   - You will see: Suggested topic tags added to the conversations
2. Open Topic Clusters to view automatically grouped conversations
   - Click a cluster to view all conversations within it
   - Rename clusters for better organization
3. Open the Knowledge Graph to visualize topic connections
   - Click nodes to view related conversations
   - Use zoom controls to explore

**Expected result:** Conversations are organized into a navigable, visual knowledge structure.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| AI tagging produces no tags | Verify AI API key is set in Settings → AI Configuration |
| Graph appears empty | Generate tags and clusters first; the graph depends on tagged topics |

### Task: AI Summary & Knowledge Cards

**Prerequisites:**
- A conversation selected in the Knowledge tab
- AI service configured

**Steps:**

1. Select a conversation and trigger AI Summary
   - You will see: A concise overview saved alongside the conversation
2. To extract structured notes, trigger AI Notes (Knowledge Cards)
   - You will see: Key points and actionable items extracted
3. Review and edit the generated content
4. Save the knowledge card to your knowledge base

**Expected result:** Long conversations are distilled into reusable summaries and structured notes.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Summary is inaccurate | Edit the result manually before saving |
| AI request fails | Check API key, model parameters, and network connectivity |

### Task: AI Recommended Cleanup

**Prerequisites:**
- Multiple conversations in the Knowledge base
- AI service configured

**Steps:**

1. Open AI Recommended Delete
   - You will see: A list of conversations the AI considers outdated or low-value
2. Review the recommendations
3. Select conversations to remove and delete in bulk
   - You will see: Selected conversations permanently removed

**Expected result:** Your knowledge base is decluttered, keeping only valuable conversations.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Useful conversation flagged | Uncheck it before deleting; recommendations are advisory only |
| Bulk delete is slow | Large selections take time; wait for confirmation before closing |

### Task: Delete Conversations

**Prerequisites:**
- Conversations in the Knowledge tab

**Steps:**

1. Select one or multiple conversations
2. Click Delete
   - You will see: Confirmation prompt
3. Confirm deletion
   - You will see: Conversations removed from the list

**Expected result:** Unwanted conversations are permanently removed.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Deleted by mistake | Restore from a recent database backup (Settings → Data Folder) |

### Task: Export Conversations

**Prerequisites:**
- Conversations to export
- (Optional) Default export folder set in Settings → File Export Folder

**Steps:**

1. Select a conversation or a collection
2. Click Export and choose a format: Markdown, HTML, or PDF
3. Choose the destination folder (or use the default)
   - You will see: Exported files saved to the chosen location

**Expected result:** Conversations are exported in your chosen format.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Export fails | Ensure the destination folder is writable and has enough disk space |
| PDF export missing content | Try HTML or Markdown format as an alternative |

### Task: Share Knowledge Base over LAN

**Prerequisites:**
- Other devices on the same local network
- A web browser on the viewing device

**Steps:**

1. Go to Settings → LAN Sharing
2. Enable LAN sharing and set a port number
   - You will see: A shareable URL displayed
3. Open the URL on another device's web browser
   - You will see: Your knowledge base browsable from the other device

**Expected result:** Other devices on your LAN can browse your knowledge base via browser.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Other device can't connect | Check both devices are on the same network and the port isn't blocked by firewall |
| URL not displayed | Re-enable LAN sharing to regenerate the URL |

## Settings Guide

### Task: Configure AI Service

**Prerequisites:**
- An API key from a supported AI provider

**Steps:**

1. Go to Settings → AI Configuration
2. Enter your API key
3. Choose an AI provider
4. Configure model parameters (temperature, max tokens)
5. Save settings and verify the connection
   - You will see: Green status indicator confirming the AI service is reachable

**Expected result:** Smart features (tagging, summaries, clustering) are enabled.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| AI service unreachable | Verify API key and network access |
| Results are low quality | Adjust temperature or switch to a different model |

### Task: Manage AI Platforms

**Steps:**

1. Go to Settings → AI Platform
2. Enable or disable specific AI platforms
3. Configure platform-specific settings
4. Set the default platform for new sessions
   - You will see: Updated platform list reflecting your choices

**Expected result:** Only your preferred platforms appear, with a default selected.

### Task: Set Data & Export Folders

**Steps:**

1. Go to Settings → Data Folder
   - Choose the directory for your SQLite database
   - View database size and storage usage
   - Move the database to a different location if needed
2. Go to Settings → File Export Folder
   - Set a default folder for exports
   - Choose default export format and options

**Expected result:** Data and exports are stored in your chosen locations.

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Database move fails | Ensure DouXia is idle and the target folder is writable |

### Task: Configure Auto Import

**Steps:**

1. Go to Settings → Auto Import
2. Enable automatic import
3. Set the import frequency
4. Choose which platforms to auto-import from
   - You will see: Import schedule active

**Expected result:** New conversations are imported automatically on the configured schedule.

### Task: Switch Language

**Steps:**

1. Go to Settings → Language
2. Choose English or Chinese
   - You will see: The interface updates immediately

**Expected result:** All UI text and menus are translated.

## Troubleshooting

### Task: Database Backup & Restore

**Steps:**

1. Go to Settings → Data Folder
2. Use the backup option to create a database snapshot
3. To restore, select a previous backup file
   - You will see: Database restored to the snapshot state

**Troubleshooting:**

| Problem | Solution |
|---------|----------|
| Restore fails | Ensure the backup file is from a compatible DouXia version |

## Appendix

### Quick Reference

| Action | Location |
|--------|----------|
| Start a new chat | Chat tab → Select platform |
| Capture conversation | Chat tab → Capture button |
| Import conversations | Knowledge tab → Import button |
| Search conversations | Knowledge tab → Search bar |
| Filter conversations | Knowledge tab → Filter button |
| Generate summary | Knowledge tab → AI Summary |
| Generate knowledge card | Knowledge tab → AI Notes |
| Export conversations | Knowledge tab → Export button |
| Configure AI | Settings → AI Configuration |
| Switch language | Settings → Language |

### Glossary

| Term | Definition |
|------|------------|
| Auto-Capture | Automatic saving of AI conversations to the local database in real time |
| FTS5 | SQLite full-text search module used for instant conversation search |
| Knowledge Graph | Visual representation of how conversation topics connect |
| Topic Cluster | A group of conversations automatically grouped by semantic similarity |
| Knowledge Card | Structured notes extracted from one or more conversations |
| LAN Sharing | Browsing your knowledge base from other devices on the local network |
