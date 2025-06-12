# NodeScrape

A Firebase Cloud Functions project for scraping metadata and images from web pages, including Instagram, using Node.js.

## Features

- **Metadata Scraper:**
  - Extracts title, favicon, description, image, and author from any provided URL.
  - Uses Cheerio and node-fetch for fast server-side scraping.
- **Instagram Image Scraper:**
  - Automates Instagram login and image extraction using Puppeteer.
  - (Note: Instagram credentials are hardcoded for demonstration; use environment variables for security in production.)
- **CORS Enabled:**
  - Handles cross-origin requests for flexible API usage.


## Setup & Installation

1. **Clone the repository:**

2. **Install Firebase CLI:**
   ```sh
   npm install firebase-tools
   ```
3. **Install dependencies:**
   ```sh
   cd functions
   npm install
   ```
4. **Configure Firebase:**
   - Set up your Firebase project and initialize Cloud Functions:
     ```sh
     firebase init functions
     ```
5. **Emulate locally:**
   ```sh
   npm run serve
   ```
6. **Deploy to Firebase:**
   ```sh
   npm run deploy
   ```

## Usage

- **Metadata Scraper:**
  - Send an HTTP POST request to the deployed `scraper` endpoint with a JSON body containing URLs.
- **Instagram Scraper:**
  - Call the `scrapeImages` function (see `index.js`).


## Dependencies
- [firebase-functions](https://www.npmjs.com/package/firebase-functions)
- [firebase-admin](https://www.npmjs.com/package/firebase-admin)
- [cheerio](https://www.npmjs.com/package/cheerio)
- [get-urls](https://www.npmjs.com/package/get-urls)
- [node-fetch](https://www.npmjs.com/package/node-fetch)
- [puppeteer](https://www.npmjs.com/package/puppeteer)
- [cors](https://www.npmjs.com/package/cors)


> **Note:** This project is for educational/demo purposes. For production use, ensure all credentials are secured and scraping complies with target site terms of service.
