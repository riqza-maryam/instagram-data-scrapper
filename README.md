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

### Key Capabilities
* Collects public Instagram profile data, bios, and business emails.
* Runs concurrent hashtag discovery jobs across 50+ streams.
* Uses proxy rotation to avoid rate limits and blocks.
* Stores clean, deduplicated contact records in PostgreSQL.
* Allows one-click CSV export ready for email outreach.

## Core Features
| Feature | Description |
|---|---|
| Hashtag Discovery | Finds public posts across 50+ hashtag streams at the same time |
| Profile Lead Extraction | Pulls public emails, names, follower counts, bios, and profile URLs |
| Duplicate Removal | Automatically updates existing profiles without creating duplicate rows |
| Proxy Rotation | Uses residential and mobile proxies with delays to keep scrapers safe |
| Queue Controls | Add, remove, pause, or resume individual hashtag tasks |
| PostgreSQL Storage | Saves all scraped data cleanly into a relational database |
| One-Click CSV Export | Download your filtered lead lists straight to CSV format |

## How It Works
| Step | Description |
|---|---|
| **1. Input Hashtags** | Add your target niche hashtags (e.g., `#ecommerce`, `#b2bmarketing`) |
| **2. Post Discovery** | The scraper finds public posts under those hashtags |
| **3. Profile Extraction** | Visits public profiles to extract contact information and stats |
| **4. Clean & Save** | Removes duplicates and saves structured data to PostgreSQL |
| **5. Export Leads** | Filter your leads and export them as a CSV spreadsheet |

## Tech Stack
| Component | Description |
|---|---|
| **Language** | Python |
| **Engine / APIs** | Private Mobile API & Python Graph API Wrappers |
| **Database** | PostgreSQL |
| **Libraries** | Requests, Psycopg2, Pydantic, PyYAML |
| **Demo Walkthrough** | [Watch System Demo on YouTube](https://youtu.be/u2YJMTuWC84) |

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
