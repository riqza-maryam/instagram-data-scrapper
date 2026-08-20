# Instagram Data Scrapper
A ready-to-use tool to scrape Instagram data and collect leads, save it to a database, and download as a CSV file.
It helps marketing agencies and businesses gather verified public emails, bios, and follower stats without hitting standard API limits.

It automates scraping workflows across 50+ hashtag streams, removes duplicate contacts in PostgreSQL, and exports clean lead lists ready for outreach campaigns.

<p align="center">
  <a href="https://scrapecrew.com/" target="_blank">
    <img width="1018" height="334" alt="insta scraper" src="https://github.com/user-attachments/assets/54fd1c05-3399-4b40-8589-b634608bdf35" />
  </a>
</p>

<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%2C%20I'm%20interested%20in%20an%20Instagram%20Data%20Scraper." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:bitbash9@gmail.com" target="_blank">
    <img src="https://img.shields.io/badge/Email-bitbash9@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://scrapecrew.com/" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>

## Introduction
Finding leads manually on Instagram takes a lot of time. You have to open accounts one by one, copy bio texts and emails, and organize spreadsheets. 

This project automates the process with an Instagram data scraper that finds profiles using target hashtags, extracts public contact info, and stores everything in a structured database.

## What It Can Do
* Collects public Instagram profile data, bios, and business emails.
* Runs concurrent hashtag discovery jobs across 50+ streams.
* Uses proxy rotation to avoid rate limits and blocks.
* Stores clean, deduplicated contact records in PostgreSQL.
* Allows one-click CSV export ready for email outreach.

## Features
* **Hashtag Discovery Engine:** Scrapes public posts across 50+ concurrent hashtag streams.
* **Structured Lead Extraction:** Pulls public emails, names, follower counts, bios, and profile URLs without login walls.
* **Automated Deduplication:** Validates records and merges existing contacts in PostgreSQL without creating duplicate rows.
* **Proxy Rotation & Jitter:** Uses residential and mobile proxies with randomized delays to avoid rate limits and blocks.
* **Queue Management:** Easily add, remove, pause, or resume individual hashtag scraping tasks.
* **Relational Storage:** Saves and structures all scraped data cleanly into a PostgreSQL database.
* **One-Click CSV Export:** Filter leads by niche or follower count and download clean spreadsheet lists.

## Workflow
1. **Input / Queue:** Add target niche hashtags (e.g., `#ecommerce`, `#b2bmarketing`) to the queue.
2. **Post Discovery:** The scraper finds recent public posts across all target hashtag streams.
3. **Profile Extraction:** Fetches public user profiles to extract verified emails, bios, follower counts, and links.
4. **Deduplication & Storage:** Validates records, discards duplicates, and saves structured leads into PostgreSQL.
5. **Export & Outreach:** Filter by niche or follower threshold and download clean CSV lists ready for campaigns.

## Tech Stack
* **Language:** Python 3.10+
* **APIs & Extraction:** Instagram Private Mobile API & Python Graph API Wrappers
* **Database:** PostgreSQL
* **Libraries:** Requests, Psycopg2, Pydantic, PyYAML
* **Demo Video:** [Watch System Demo on YouTube](https://youtu.be/u2YJMTuWC84)

## Directory Structure
```text
Instagram-Data-Scraper/
├── src/
│   ├── main.py
│   ├── scraper/
│   │   ├── instagram_scraper.py
│   │   ├── hashtag_crawler.py
│   │   └── profile_parser.py
│   ├── database/
│   │   ├── db_manager.py
│   │   └── models.py
│   └── utils/
│       ├── proxy_rotator.py
│       └── rate_limiter.py
├── config/
│   ├── settings.yaml
│   └── .env.example
├── data/
│   └── raw/
├── requirements.txt
└── README.md
```
## Who it's for
* **Agencies & B2B Teams:** Scrape targeted niche profiles to build high-converting cold email outreach lists.
* **E-commerce Brands:** Discover active micro-influencers by filtering follower metrics and bio keywords.
* **Growth Marketers:** Extract public business contacts and audience signals directly from competitor hashtags.
* **Data Engineers:** Integrate structured profile data into analytics dashboards, CRMs, or downstream pipelines.

## FAQs
**How to scrape Instagram data?**<br>
Instagram data can be scraped by querying public endpoints and parsing rendered profile metadata in a controlled environment. This project uses endpoint handlers, rate limiting, and proxy rotation to extract structured profile information and emails consistently.

**Does this support scrape Instagram without login?**<br>
Yes. The scraper operates on public endpoints and session simulation, allowing public profile and hashtag discovery without requiring personal account login credentials.

**Is this similar to an Apify Instagram scrape workflow?**<br>
The architecture follows similar principles—such as queue-based crawling, proxy management, and structured data export—while being optimized for local execution, self-hosting, and full pipeline control.

**Can it export directly to CSV and databases?**<br>
Yes. In addition to direct PostgreSQL database storage and deduplication, the system supports one-click filtered exports directly into CSV format.

**How does it handle layout and endpoint changes?**<br>
The scraper uses dynamic field validation with fallback parsing logic to adapt to platform UI shifts and internal schema updates without breaking the scraping pipeline.

**Does this use Instagram Graph API or Private APIs?**<br>
This project uses public mobile API endpoint logic and Graph API protocol wrappers[cite: 1] to capture public contact signals, bios, and follower stats without typical Graph API access restrictions.
