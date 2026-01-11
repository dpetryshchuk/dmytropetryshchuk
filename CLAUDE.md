# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Architecture

This is a personal website for Dmytro Petryshchuk with two main components:

### 1. Static Website
- **Root**: Simple HTML/CSS personal site with hand-written code
- **Structure**: 
  - `index.html` - Main homepage
  - `pages/` - Static pages (watercolors, agentic development, etc.)
  - `sources/writings/` - Writing content and templates
  - `styles.css` - Global stylesheet with Georgia serif font and aquamarine links
- **Philosophy**: Minimal, hand-coded approach as "the bike to a car" - emphasizing autonomy and creativity over industrialization

### 2. Ima Chatbot (Subdirectory: `ima/`)
- **Framework**: FastAPI backend with static file serving
- **AI Integration**: Uses OpenRouter API with Llama 3.3 70B model
- **Character**: "Ima" - patient, curious AI that asks one question at a time to understand users
- **Deployment**: Hosted at ima.dmytropetryshchuk.com

## Common Commands

### Ima Chatbot Development
```bash
cd ima
pip install -r requirements.txt
uvicorn main:app --reload
```

### Static Site Development
The main site is served directly from HTML files - no build process required. Simply open `index.html` in a browser or serve with any static file server.

## Key Implementation Details

- **Ima API Endpoint**: `/chat` accepts history array and returns AI response
- **Environment**: Ima requires `OPENROUTER_API_KEY` in `.env` file
- **Static Assets**: Ima serves frontend from `ima/static/` directory
- **Styling**: Consistent CSS approach across both main site and Ima interface
- **Content Management**: Writing templates use query parameters for dynamic content loading