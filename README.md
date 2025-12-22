# n8n-workflows-News-bot
AI-Powered News Aggregator & Curator
An automated n8n workflow that fetches content from various news sources (using Hacker News tool), uses AI to generate concise summaries, and logs curated results to Google Sheets for easy tracking and analysis.

What it does
This workflow automatically:

Retrieves stories and discussions from Hacker News based on customizable keyword searches
Processes each item through an AI agent (GPT-4.1-mini) to create concise, newsworthy headlines (5 words or less)
Extracts and structures data (title, URL, date) using an AI-powered output parser
Validates entries to ensure data quality
Saves curated results to a Google Sheets spreadsheet
Key Features
AI-Powered Content Curation: Leverages OpenAI's GPT-4.1-mini to transform verbose headlines into concise, impactful summaries
Structured Data Extraction: Ensures consistent output format with validated title, date, and URL fields
Smart Filtering: Automatically skips incomplete or invalid entries
Rate-Limited Processing: Includes configurable delays between items to respect API limits
Batch Processing: Handles multiple items sequentially with automatic loop control
Customizable Keywords: Easily modify search terms to track any topic of interest
Use Cases
Monitor specific topics or industries on Hacker News
Build curated content databases for research or analysis
Track trending discussions in your field
Automate content discovery for newsletters or reports
Create topic-specific news archives
Workflow Architecture
Manual Trigger → Fetch from Hacker News → Loop Through Items → AI Summarization → Data Validation → Save to Google Sheets

Technologies
n8n: Workflow automation platform
OpenAI API: GPT-4.1-mini for natural language processing and summarization
Google Sheets API: Structured data storage and tracking
Hacker News API: Content source
Customization
Simply change the keyword parameter in the Hacker News node to track any topic (e.g., "AI", "Startups", "Cybersecurity", "Remote Work", etc.)
