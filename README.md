# iOS Web Clipper → Obsidian Shortcut

Save webpage content from Chrome or Safari on iOS as Markdown into an Obsidian vault.

This shortcut extracts webpage content, converts it to Markdown, attaches YAML metadata, and saves it automatically into the vault.

---

# Workflow

URL  
↓  
Get contents of web page  
↓  
Make Markdown from contents  
↓  
Add YAML metadata  
↓  
Rename file  
↓  
Save to Obsidian vault  

---

# Shortcut Actions

## 1 Receive URLs from Share Sheet

Input type

URLs

This allows the shortcut to appear in the iOS share menu.

Usage

Chrome / Safari  
↓  
Share  
↓  
Run shortcut  

---

## 2 Get Contents of Web Page

Action

Get contents of web page at Shortcut Input

Purpose

download the webpage HTML  
provide content for Markdown conversion  

---

## 3 Convert Web Page to Markdown

Action

Make Markdown from Contents of Web Page

Output

Markdown from Rich Text

This produces the main article content.

---

## 4 Get Page Title

Action

Get Details of Web Page

Detail type

Name

Output variable

Name

Used as filename and title metadata.

---

## 5 Get Current Date

Actions

Current Date  
↓  
Format Date  

Format

yyyy-MM-dd

Output

Formatted Date

---

## 6 Generate YAML Metadata

Action

Text

Template

---
title: Name  
source: Shortcut Input  
date: Formatted Date  
tags: webclip  
---

Markdown from Rich Text

Variables inserted

Name  
Shortcut Input  
Formatted Date  
Markdown from Rich Text  

---

## 7 Rename File

Action

Set Name

Set name to

Name.md

---

## 8 Save File

Action

Save File

Recommended settings

Ask Where to Save: OFF  

Destination

iCloud Drive / Obsidian / GaoVault / inbox

---

# Output Example

Saved Markdown file

---
title: Example Article  
source: https://example.com  
date: 2026-03-11  
tags: webclip  
---

# Example Article

Article content...

---

# Recommended Vault Structure

vault

inbox  
research  
pipeline  
chatgpt  
ideas  

Captured webpages are saved into

inbox

Then processed later.

---

# Usage

Chrome / Safari  
↓  
Share  
↓  
Webclipper Shortcut  
↓  
Saved to Obsidian inbox  

---

# Notes

Dynamic websites such as Taobao may not expose article content in the raw HTML.

In those cases only metadata may be captured.

---

# Possible Improvements

Future upgrades

extract first image as cover  
estimate reading time  
auto tag by domain  
auto archive read articles  
