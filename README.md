# Custom Logic 🌐

Welcome to **Custom Logic**, a sleek, single-file web platform designed to deliver a full SaaS experience without the usual bloat. This project is proof that you can create a modern, responsive, and highly interactive website **all in one source file**, while leveraging the power of the cloud.

---

## 🚀 Project Overview

**Custom Logic** is the web presence for the company [custom-logic.co.za](https://custom-logic.co.za). It handles:

- User feedback collection  
- Service orders and requests  
- Clean, single-page interface  
- SEO-ready architecture, fully crawlable  

All of this is delivered in a **single HTML/JS/CSS source file**, powered by the serverless cloud.

---

## 💻 Tech Stack

This project isn’t your average SPA. Here’s what makes it tick:

| Layer | Technology | Notes |
|-------|------------|-------|
| Hosting | **Cloudflare Pages** | Single-page static hosting with lightning-fast global distribution. |
| Serverless | **Cloudflare Workers** | Handles dynamic actions like feedback forms, service order submissions, and virtual endpoints (`/sitemap.xml`, `/robots.txt`). |
| Database | **GitHub as a database** | All persistent storage is managed via GitHub commits + API. This means no traditional DB required — just raw CSV stored in repos. |
| Frontend | **Vanilla JS + HTML + CSS** | Everything lives in a single source file. Modular enough to maintain sanity, yet compact for lightning performance. |
| SEO | Pre-rendered meta tags + JSON-LD | Single-page doesn’t mean invisible to search engines. SEO-ready structured data, Open Graph tags, and dynamic sitemap are served via Workers. |

---

## 🔧 Architecture

Here’s the brain behind the simplicity:

1. **Single-File SPA**
   - All HTML, CSS, and JS live in one file.
   - Interactive sections are powered by vanilla JS.
   - SEO sections pre-rendered to ensure crawlability.

2. **Serverless Dynamic Layer**
   - Cloudflare Workers intercept requests for dynamic endpoints:
     - `/sitemap.xml` → serves automatically generated sitemap.
     - `/robots.txt` → search engine instructions.
     - `/feedback` and `/orders` → handles multi-form submissions.
   - Each submission is validated, processed, and **stored in CSV files on GitHub**.

3. **GitHub as a Backend**
   - Workers push data to a dedicated repository branch.
   - Each submission creates a commit, providing **version history and audit trail**.
   - No database server required.

4. **SEO & Metadata**
   - Structured data (JSON-LD) embedded directly in the SPA.
   - Open Graph meta tags included in `<head>` for social previews.
   - Cloudflare Workers allow dynamic injection of per-section `<title>` and `<meta>` if needed.

---

## ⚡ Features

- **Single-source SPA** – lightning fast, minimal dependencies.  
- **Serverless feedback & order system** – no backend servers.  
- **Multi-form handling** – different solutions are routed to separate CSV files (`unicenta-pos`, `funeral-manager`, `jobfinders`, `custom-development`).  
- **CORS-secured** – allows requests only from approved domains.  
- **SEO ready** – sitemap, robots.txt, structured data, and pre-rendered content.  
- **Cloud-native** – leverages Cloudflare Pages + Workers for full-stack functionality.  
- **GitHub as a “database”** – versioned, persistent, and auditable.  

---

## 🛠 Cloudflare Worker – Multi-Form Submission

The Worker handles:

1. **CORS setup** for requests from `custom-logic.co.za`.  
2. **POST-only submissions**, with preflight OPTIONS support.  
3. **Payload validation** for required fields (`fullName`, `email`, `solution`).  
4. **Dynamic CSV routing** per solution:
   - `unicenta-pos` → `unicenta_pos_leads.csv`  
   - `funeral-manager` → `funeral_manager_leads.csv`  
   - `jobfinders` → `jobfinders_leads.csv`  
   - `custom-development` → `custom_development_leads.csv`  
5. **GitHub storage**:
   - Fetch existing CSV or create a new one with headers.
   - Append new submission row.
   - Commit changes using GitHub REST API.
6. **Unique submission IDs** and timestamps for tracking.  
7. **Error handling** for invalid payloads, GitHub errors, or misconfigured environment variables.  

> This setup allows **scalable form handling** without adding backend servers, fully integrating with GitHub for persistent storage and auditing.

---

## 🌐 Deployment

1. **Cloudflare Pages**
   - Deploy the single source HTML.
   - Automatic global CDN distribution.

2. **Cloudflare Workers**
   - Script intercepts dynamic routes (`/sitemap.xml`, `/robots.txt`, `/feedback`, `/orders`).
   - Integrates with GitHub API to persist user submissions.

3. **GitHub Integration**
   - Workers push data to a dedicated repository branch.
   - Data is versioned and auditable.

---

## 🔍 SEO Strategy

Even with a single-file SPA:

- Pre-rendered `<title>` and `<meta>` tags for main sections.  
- JSON-LD structured data for organization info.  
- `/sitemap.xml` and `/robots.txt` dynamically served via Workers.  
- Anchor links for in-page sections help Google crawl content.

---

## 💡 Philosophy

Custom Logic is a **love letter to minimalism** in web development:

- One file, one source of truth.  
- Serverless logic for everything dynamic.  
- GitHub as a versioned database.  
- Optimized for speed, SEO, and maintainability.  

If you’re a coder who likes **clever, compact, cloud-first architectures**, this project is a playground of ideas.

---

## 📜 License

MIT License — go ahead, explore, fork, or remix this single-file marvel.  

---

**Written by a coder who genuinely enjoys building clever, minimalist, cloud-native apps.**
