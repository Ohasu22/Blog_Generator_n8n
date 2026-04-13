# N8N Blog Generator

> Automated blog generation from news sources using AI-powered content creation with Google Gemini, delivered directly to your inbox

## Overview

N8N Blog Generator is an automation workflow that transforms news articles into engaging blog posts using AI and automatically delivers them via email. This project offers two powerful versions to suit different content sourcing needs.

---

## Features

✨ **Automated Blog Generation** - Convert news articles into well-structured blog posts  
🔍 **Keyword-Based Search** - Input custom keywords to find relevant content  
🤖 **AI-Powered** - Leverages Google Gemini Chat Model for intelligent content creation  
📧 **Email Delivery** - Generated blogs automatically sent to your inbox  
📰 **Multiple Source Options** - Choose between hardcoded RSS feeds or dynamic web scraping  
⚡ **Real-time Processing** - Instant blog generation with workflow automation

---

## Project Versions

### Version 1: RSS Feed-Based Blog Generator
**Ideal for:** Monitoring specific, predetermined news sources

- Extracts articles from hardcoded RSS feed links
- Users input keywords to filter relevant articles
- Processes selected content through Gemini AI model
- Generates formatted blog posts automatically
- **Sends completed blog to user email**

**Screenshot of Workflow:**
<!-- Insert V1 Workflow Image Here -->

<img width="1667" height="862" alt="image" src="https://github.com/user-attachments/assets/aeb1d6a9-8a4f-4409-b470-7374596d8c12" />
![N8N Workflow - Version 1](IMAGE_URL_HERE)

**Keyword Input Screen:**
<img width="873" height="727" alt="image" src="https://github.com/user-attachments/assets/95148682-9f6a-4158-af43-b785e9d5f5fd" />

### Email Output

The generated blog post is delivered directly to your email in a professionally formatted message:

**Generated Blog Post Output (Email):**

<img width="1908" height="869" alt="image" src="https://github.com/user-attachments/assets/2312fd5d-df49-4174-b7d2-f8c062d75bfd" />

---

### Version 2: Web Scraper-Based Blog Generator
**Ideal for:** Dynamic, unrestricted content discovery

- Uses web scraper node for real-time internet searches
- Searches for articles based on user-provided keywords
- Dynamically retrieves fresh content from the web
- Converts findings into polished blog posts via Gemini AI
- **Automatically emails the generated blog to user**


**Screenshot of Workflow:**
<!-- Insert V2 Workflow Image Here -->
![N8N Workflow - Version 2](IMAGE_URL_HERE)

---

## How It Works

### Step-by-Step Process

1. **User Input** - Enter keywords via the input interface
2. **Content Discovery** - RSS feeds (V1) or web scraper (V2) retrieves relevant articles
3. **AI Processing** - Google Gemini transforms articles into blog posts
4. **Email Generation** - Blog formatted as email-ready content
5. **Delivery** - Automated email sent to user's registered inbox


### Input Interface

**Instructions:**
1. Enter your desired keywords (e.g., "artificial intelligence", "tech innovation")
2. Provide your email address for blog delivery
3. Select the appropriate version (RSS-based or Web Scraper)
4. Click "Generate Blog" to initiate the workflow
5. Check your inbox for the generated blog post

---

### Email Output

The generated blog post is delivered directly to your email in a professionally formatted message:

**Email Content Includes:**
- 📝 **Subject Line** - Compelling title based on content
- 🎯 **Summary** - Quick overview at the top
- 🏷️ **Tags & Categories** - SEO-friendly keywords
- 📅 **Metadata** - Publication date and source attribution
- 🔗 **Read More Link** - Optional link to original source
- 
---
## Usage Examples

### Example 1: Tech News Blog (Version 1 - RSS)
```
Input Keywords: "Machine Learning", "AI Breakthroughs"
Email Recipient: user@example.com
Output: 3-4 blog posts from predetermined tech news RSS feeds
Processing Time: ~2-3 minutes
Delivery: Email arrives within 5 minutes of generation
```

### Example 2: General Web Search (Version 2 - Web Scraper)
```
Input Keywords: "Renewable Energy Innovation"
Email Recipient: user@example.com
Output: Latest articles on renewable energy converted to blog posts
Processing Time: ~3-5 minutes
Sources: Multiple web sources (dynamically sourced)
Delivery: Email arrives within 10 minutes of generation
```

## API Keys & Credentials Required

- **Google Gemini API**
  - Sign up: https://ai.google.dev/
  - Documentation: https://ai.google.dev/docs

- **Email Account Credentials**
  - SMTP Host and Port
  - Email address and password/app password
  - (For Gmail: Enable "App Passwords" or allow "Less secure app access")

---


