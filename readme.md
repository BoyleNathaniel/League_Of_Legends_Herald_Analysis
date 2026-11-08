# gol.gg Scraper

## Project Overview

A Python web scraping project designed to collect and
organize League of Legends esports data from gol.gg.

Serper API will be used to discover relevant gol.gg pages
and retrieve search results. Additional extraction and
parsing methods will be developed to collect structured
data from the relevant pages.

## Project Objectives

- Identify relevant gol.gg pages.
- Collect relevant URLs using Serper API.
- Extract information from selected pages.
- Clean and validate collected data.
- Store datasets in CSV format.
- Create reproducible data collection workflows.

## API Configuration

This project uses SteadyAPI's ScrapeFlow service
to retrieve webpage content.

Create a `.env` file in the project root.

Add your personal access token:

```text
STEADY_API_TOKEN=your_personal_access_token_here
```

API Base URL:
https://api.steadyapi.com

ScrapeFlow Endpoint:
POST /v1/scrapeflow/scraper

Authentication:
Authorization: Bearer YOUR_API_TOKEN

Never upload `.env` to GitHub.
