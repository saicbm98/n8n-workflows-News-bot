# AI-Powered News Aggregator and Curator (n8n)

An automated **n8n workflow** that fetches stories from **Hacker News**, uses **AI-powered summarisation** to generate concise headlines, and logs curated results into **Google Sheets** for easy tracking, analysis, and reuse.

This project is designed for builders, researchers, and operators who want a lightweight, customisable system for monitoring trends and discussions around specific topics.

---

## Overview

This workflow continuously collects relevant Hacker News posts based on keyword searches, processes them through an AI agent to create short, newsworthy summaries, validates the extracted data, and stores the final output in Google Sheets.

The result is a structured, searchable, and reusable dataset of curated news items without any manual effort.

---

## What This Workflow Does

The workflow automatically:

- Fetches stories and discussions from Hacker News using configurable keyword searches  
- Sends each item to an AI agent (GPT-4.1-mini) to generate concise headlines of five words or fewer  
- Extracts and structures key fields such as title, URL, and date  
- Validates outputs to ensure completeness and consistency  
- Skips incomplete or low quality entries  
- Saves curated results to a Google Sheets spreadsheet  
- Processes items sequentially with built-in rate limiting  

---

## Key Features

### AI-Powered Content Curation  
Uses OpenAI’s GPT-4.1-mini to convert verbose or technical titles into short, high signal headlines suitable for dashboards, reports, or newsletters.

### Structured Data Extraction  
An AI-powered output parser ensures consistent formatting for titles, URLs, and dates, making the data easy to analyse downstream.

### Smart Filtering and Validation  
Entries missing required fields are automatically skipped to maintain data quality.

### Rate-Limited and Safe Processing  
Configurable delays between items help avoid API throttling and ensure stable execution.

### Batch and Loop Control  
Processes multiple Hacker News items sequentially using n8n’s loop controls.

### Fully Customisable Keywords  
Easily adjust the search keywords to track any topic of interest.

---

## Common Use Cases

- Monitoring specific industries or technologies on Hacker News  
- Building curated research datasets  
- Tracking emerging trends and discussions  
- Powering internal newsletters or weekly reports  
- Creating topic-specific news archives  
- Supporting competitive or market intelligence workflows  

---

## Workflow Architecture
