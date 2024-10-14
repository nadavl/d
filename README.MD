# Web Crawler and HTML Saver

This project is a web crawler that extracts URLs from a sitemap, crawls each URL, and saves the HTML content along with associated assets (CSS, images, fonts) to a local directory.

## Features
- Extracts URLs from a sitemap XML.
- Crawls each URL and saves the HTML content.
- Replaces internal URLs with absolute URLs.
- Removes all `<script>` tags from the HTML.
- Saves associated CSS files.
- Saves assets like images and fonts.

## Files
- `index.ts`: The main TypeScript file containing the web crawler logic.

## Functions

### `extractUrlsFromSitemap(sitemapXml: string): string[]`
Extracts URLs from the provided sitemap XML string.

### `async function crawlUrl(url: string)`
Crawls the given URL, saves the HTML content, replaces internal URLs, removes `<script>` tags, and saves associated assets.

### `async function main()`
Main function that extracts URLs from the sitemap and crawls each URL.

## How to Run

1. **Install Deno**: Follow the instructions on the [Deno website](https://deno.land/#installation) to install Deno.

2. **Install Playwright**: Run the following command to install Playwright:
    ```sh
    deno run -A https://deno.land/x/playwright/install.ts
    ```

3. **Run the Script**: Execute the script using Deno:
    ```sh
    deno run --allow-net --allow-write --allow-read --allow-env --allow-run index.ts
    ```

## Dependencies
- [Deno](https://deno.land/): A secure runtime for JavaScript and TypeScript.
- [Playwright](https://playwright.dev/): A Node.js library to automate Chromium, Firefox, and WebKit with a single API.
- [Deno Standard Library](https://deno.land/std): Standard library for Deno, used for file system operations and path manipulation.

## Notes
- The script will create a `pages` directory in the current working directory to save the crawled HTML and assets.
- Ensure that the sitemap XML string in the `index.ts` file is updated with the correct URLs to crawl.
