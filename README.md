---
name: "laravel-multilingual"
title: "Laravel Multilingual Implementation & Localization"
description: "Comprehensive agent workflow and Cursor rule for configuring multi-language support in Laravel, including locale-aware URLs, translation catalogs, JSON Eloquent models, and Filament admin panels"
version: "1.0.0"
author: "Saddam Al-Slfi"
repository: "https://github.com/saddamalsalfi/laravel-skills-multilingual"
license: "MIT"
created_at: "2026-09-12"
---

# Laravel Multilingual Implementation & Localization 🌐🐘

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Open Plugins Compliant](https://img.shields.io/badge/Open%20Plugins-Compliant-success.svg)](https://open-plugins.com)
[![Cursor Rule](https://img.shields.io/badge/Cursor%20Rule-.mdc-purple.svg)](rules/laravel-multilingual.mdc)
[![Laravel](https://img.shields.io/badge/Laravel-10%20%7C%2011%20%7C%2012%20%7C%2013-red.svg)](https://laravel.com)

A production-grade AI agent skill and **Cursor Rule** engineered to implement and maintain bulletproof internationalization (i18n) and localization (L10n) in modern Laravel applications.

Optimized for **[cursor.directory](https://cursor.directory)**, **[LangChain Hub](https://smith.langchain.com/hub)**, and **[Open Plugins](https://open-plugins.com)**.

---

## 🎯 What This Skill Solves

Localization in Laravel involves complex edge cases: SEO canonical URLs, locale-prefixed routes, translatable Eloquent attributes, Filament admin panels, and queue worker locale leaks.

This skill guides the AI coding assistant through:
- **Zero Security Risk in Web Root:** Forbids exposing translation catalogs in `public/lang/` and enforces `<project-root>/lang/` as the sole authoritative path.
- **SEO & Canonical Routing:** Handles locale prefix routing via `mcamara/laravel-localization`, enforces redirect invariants (`hideDefaultLocaleInURL => true`), and eliminates redirect loops.
- **Admin Panel Isolation:** Completely decouples Filament administration panels from public localized routing while keeping admin language switching seamless via Livewire.
- **Data Integrity:** Manages JSON-backed translatable Eloquent attributes using `spatie/laravel-translatable` without data loss or partial overwrite bugs.
- **Queue & Worker Safety:** Explicitly isolates and resets locale state inside queue workers and asynchronous jobs to avoid cross-tenant locale leakage.
- **RTL & LTR Support:** Enforces correct CSS and typography direction switching for Arabic, Hebrew, and Persian.

---

## 📂 Repository Structure (Open Plugins Standard)

```text
├── skills/
│   └── laravel-multilingual/
│       └── SKILL.md                 # Agent skill for Antigravity, Claude Code, etc.
├── rules/
│   └── laravel-multilingual.mdc     # Optimized rule for Cursor IDE
├── mcp.json                         # Model Context Protocol configuration
├── plugin.json                      # Open Plugins manifest
├── LICENSE                          # MIT License with explicit AI Agent Grant
└── README.md                        # Documentation and usage guides
```

---

## 🚀 Quick Start & Installation

### 1. Cursor IDE
Copy the rule directly into `.cursor/rules/`:
```bash
mkdir -p .cursor/rules
curl -o .cursor/rules/laravel-multilingual.mdc https://raw.githubusercontent.com/saddamalsalfi/laravel-skills-multilingual/main/rules/laravel-multilingual.mdc
```

### 2. Google Antigravity / Gemini IDE
Place into your workspace under `.agents/skills/`:
```bash
mkdir -p .agents/skills/laravel-multilingual
curl -o .agents/skills/laravel-multilingual/SKILL.md https://raw.githubusercontent.com/saddamalsalfi/laravel-skills-multilingual/main/skills/laravel-multilingual/SKILL.md
```

### 3. Open Plugins CLI
```bash
open-plugins install https://github.com/saddamalsalfi/laravel-skills-multilingual
```

---

## 📄 License & Attribution

Authored by **Saddam Al-Slfi** ([@saddamalsalfi](https://github.com/saddamalsalfi)).

Licensed under the **[MIT License](LICENSE)** with a **Special Grant for Artificial Intelligence (AI) Agents & Automated Systems**.
