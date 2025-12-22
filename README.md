# AI-Powered News Aggregator and Curator (n8n)

An automated **n8n workflow** that fetches stories from **Hacker News**, uses **AI-powered summarisation** to generate concise headlines, and logs curated results into **Google Sheets** for easy tracking, analysis, and reuse.

This project demonstrates how no-code automation and AI can be combined to build a reliable, scalable content discovery pipeline.

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
- Processes items sequentially with built-in delays  

---

## Key Features

### AI-Powered Content Curation
Uses OpenAI’s GPT-4.1-mini to convert verbose or technical titles into short, high signal headlines suitable for dashboards, reports, or newsletters.

### Structured Data Extraction
An AI-powered output parser ensures consistent formatting for titles, URLs, and dates, making the data easy to analyse downstream.

### Smart Filtering and Validation
Entries missing required fields are automatically skipped to maintain data quality.

### Safe Processing with Delays
Configurable delays between items help prevent API overload and ensure stable execution.

### Batch and Loop Control
Processes multiple Hacker News items sequentially using n8n’s loop controls.

### Fully Customisable Keywords
Easily adjust the search keywords to track any topic of interest.

---

## Workflow Architecture

The entire automation flow is represented below.

```mermaid
flowchart TD
    A[Manual Trigger]
    B[Fetch from Hacker News]
    C[Loop Through Items]
    D[AI Summarisation<br/>GPT-4.1-mini]
    E[Data Validation]
    F[Save to Google Sheets]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F
