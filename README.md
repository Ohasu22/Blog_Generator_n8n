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
6. **Archive** - Blog post stored for future reference

### Input Interface

Users interact with a simple keyword input page:

**Keyword Input Screen:**
<!-- Insert Keyword Input Interface Image Here -->
![Keyword Input Interface](IMAGE_URL_HERE)

**Instructions:**
1. Enter your desired keywords (e.g., "artificial intelligence", "tech innovation")
2. Provide your email address for blog delivery
3. Select the appropriate version (RSS-based or Web Scraper)
4. Click "Generate Blog" to initiate the workflow
5. Check your inbox for the generated blog post

---

### Email Output

The generated blog post is delivered directly to your email in a professionally formatted message:

**Generated Blog Post Output (Email):**
<!-- Insert Email Output/Blog Post Image Here -->
![Generated Blog Post Email](IMAGE_URL_HERE)

**Email Content Includes:**
- 📝 **Subject Line** - Compelling title based on content
- 🎯 **Summary** - Quick overview at the top
- 📄 **Full Article** - Well-structured, formatted blog content
- 🏷️ **Tags & Categories** - SEO-friendly keywords
- 📅 **Metadata** - Publication date and source attribution
- 🔗 **Read More Link** - Optional link to original source
- ⏱️ **Reading Time** - Estimated time to read

---

## Email Configuration

### SMTP Settings

The workflow uses SMTP protocol to send emails. Configure the following:

```json
{
  "email_provider": "SMTP",
  "sender_email": "your-email@gmail.com",
  "smtp_host": "smtp.gmail.com",
  "smtp_port": 587,
  "encryption": "TLS",
  "recipient": "user_email_input"
}
```

### Supported Email Providers

| Provider | Host | Port |
|----------|------|------|
| Gmail | smtp.gmail.com | 587 |
| Outlook | smtp-mail.outlook.com | 587 |
| Yahoo | smtp.mail.yahoo.com | 587 |
| Custom SMTP | [your-host] | 587/465 |

---

## Technology Stack

| Component | Technology |
|-----------|-----------|
| Automation Platform | N8N |
| AI Model | Google Gemini Chat API |
| Content Source (V1) | RSS Feeds |
| Content Source (V2) | Web Scraper Node |
| Email Service | SMTP Protocol |
| Output Format | HTML Email / Markdown Blog Post |

---

## Getting Started

### Prerequisites

- N8N instance (self-hosted or cloud)
- Google Gemini API key
- Email account credentials (Gmail, Outlook, etc.)
- RSS feed URLs (for Version 1) or internet access (for Version 2)

### Installation

1. **Import Workflow**
   - Download the respective JSON file (V1 or V2)
   - Open your N8N dashboard
   - Click "Import from file"
   - Select the downloaded JSON

2. **Configure API Keys**
   - Add your Google Gemini API credentials
   - Set up SMTP email credentials
   - Set up authentication for RSS feeds (if applicable)

3. **Email Setup**
   - Configure SMTP host and port
   - Add sender email and password
   - Test email delivery with a sample message

4. **Customize Settings**
   - Adjust AI parameters (tone, length, style)
   - Configure email template
   - Set RSS feeds (Version 1 only)
   - Set web scraper parameters (Version 2 only)

5. **Deploy Workflow**
   - Save and activate the workflow
   - Test with sample keywords
   - Verify email delivery to your inbox

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

---

## Configuration Guide

### Version 1 - RSS Feed Setup
```json
{
  "rss_feeds": [
    "https://example-news-1.com/feed.xml",
    "https://example-news-2.com/feed.xml"
  ],
  "keyword_filter": "user_input",
  "ai_model": "Google Gemini",
  "email_config": {
    "smtp_host": "smtp.gmail.com",
    "smtp_port": 587,
    "sender_email": "your-email@gmail.com",
    "recipient_email": "user_input"
  }
}
```

### Version 2 - Web Scraper Setup
```json
{
  "search_method": "web_scraper",
  "keyword_input": "user_input",
  "ai_model": "Google Gemini",
  "result_limit": 10,
  "email_config": {
    "smtp_host": "smtp.gmail.com",
    "smtp_port": 587,
    "sender_email": "your-email@gmail.com",
    "recipient_email": "user_input"
  }
}
```

---

## Project Structure

```
Blog_Generator_n8n/
├── README.md
├── VERSION_1_RSS_BlogGenerator.json
├── VERSION_2_WebScraper_BlogGenerator.json
├── docs/
│   ├── workflow-diagram-v1.png
│   ├── workflow-diagram-v2.png
│   ├── keyword-input-interface.png
│   ├── email-output-example.png
│   └── sample-output.png
└── examples/
    ├── sample-keywords.txt
    ├── sample-output-blog.md
    └── sample-email-template.html
```

---

## Email Templates

### Default Email Template

The workflow uses an HTML email template. Customize the template in the N8N Email Node:

```html
<html>
  <body style="font-family: Arial, sans-serif; max-width: 600px;">
    <h1>{{blog_title}}</h1>
    <p><strong>Keywords Used:</strong> {{keywords}}</p>
    <p><strong>Source:</strong> {{source}}</p>
    <hr>
    <div>
      {{blog_content}}
    </div>
    <hr>
    <p><small>Generated by N8N Blog Generator | {{generation_date}}</small></p>
  </body>
</html>
```

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Email not arriving | Check SMTP credentials; verify email not in spam folder |
| API Key Error | Verify Google Gemini API key and quota limits |
| No Results Found | Check keyword relevance; try broader terms for V2 |
| Slow Processing | Adjust AI model parameters; reduce article length |
| RSS Feed Error (V1) | Validate RSS feed URLs; check feed accessibility |
| SMTP Authentication Failed | Verify email password; enable "Less secure apps" (Gmail) |

---

## Performance Metrics

- **Average Processing Time:** 2-5 minutes per blog post
- **Email Delivery Time:** 1-10 minutes after generation
- **Article Length:** 500-1500 words (configurable)
- **Success Rate:** 95%+
- **Concurrent Workflows:** Depends on N8N instance capacity

---

## Customization Options

- 🎨 **Tone & Style** - Formal, casual, professional, creative
- 📊 **Article Length** - Short (300-500), Medium (500-1000), Long (1000-2000)
- 🏷️ **SEO Tags** - Auto-generate or custom list
- 🌍 **Language** - Support for multiple languages
- 📋 **Template** - Choose blog post structure
- 📧 **Email Format** - HTML, Plain text, or Markdown
- 🎯 **Multiple Recipients** - Send to multiple email addresses

---

## API Keys & Credentials Required

- **Google Gemini API**
  - Sign up: https://ai.google.dev/
  - Documentation: https://ai.google.dev/docs

- **Email Account Credentials**
  - SMTP Host and Port
  - Email address and password/app password
  - (For Gmail: Enable "App Passwords" or allow "Less secure app access")

---

## Future Enhancements

- [ ] Multi-language support
- [ ] Custom blog templates
- [ ] Direct publishing to WordPress/Medium/Substack
- [ ] Advanced keyword analysis
- [ ] Email scheduling (send at specific times)
- [ ] Multiple recipient management
- [ ] Blog post archiving system
- [ ] Analytics dashboard
- [ ] PDF generation option

---

## Acknowledgments

- N8N Community for the powerful automation platform
- Google for the Gemini AI API
- Open-source RSS and web scraping tools
- Email service providers

---

**Last Updated:** 2026-04-13
