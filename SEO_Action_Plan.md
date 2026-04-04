# JP AutoHub - SEO Implementation Plan

Follow these steps exactly to clean up duplicate content and optimize the WordPress/WooCommerce site properly.

- [ ] **SAFETY CHECK:** Make sure there is a backup of the site (via hosting panel or a plugin like UpdraftPlus) before proceeding.

- [ ] **Step 1:** Install RankMath
  - *Go to:* Plugins → Add New → Search for "RankMath SEO"
  - *Action:* Install and Activate.
  - *Setup:* Choose Advanced Mode. Connect to GSC.
  - *Enable Modules:* Sitemap, Redirections, 404 Monitor.

- [ ] **Step 2:** Delete Junk Pages
  - *Go to:* Pages → All Pages
  - *Action:* Find `home-2`, `home-3`, `home-4`, `home-5`, `home-6`. If they are indexed, consider a 301 redirect. Otherwise, Trash all 5.

- [ ] **Step 3:** Update `robots.txt`
  - *Go to:* RankMath → General Settings → Edit robots.txt
  - *Action:* Paste the contents from the `robots.txt` file located in this repository.

- [ ] **Step 4:** Configure the Sitemap
  - *Go to:* RankMath → Sitemap Settings
  - *Action:* 
    - Posts: OFF (unless you run a blog)
    - Pages: ON
    - Products: ON
    - Tags/Authors: OFF
  - *Test:* Visit `jpautohub.com/sitemap_index.xml` to verify.

- [ ] **Step 5:** Create the New Category Structure
  - *Go to:* Products → Categories
  - *Action:* Create "Used & Salvage Parts" as the parent. Create the 7 make sub-categories using the structure laid out in `Categories_and_URLs.md`. Paste in your SEO descriptions.

- [ ] **Step 6:** Reassign the 8 Salvage Listings
  - *Go to:* Products → All Products
  - *Action:* Move the salvage products from "Alloy Wheels" to their proper make sub-category. Fill out the RankMath SEO panel for each product (Focus Keyword + Meta Description).

- [ ] **Step 7:** Submit to Google Search Console
  - *Go to:* [Google Search Console](https://search.google.com/search-console)
  - *Action:* Submit the new sitemap. Use URL Inspection to "Request Indexing" on the Homepage and Main Category pages.

- [ ] **FINAL STEP:** Refresh Permalinks
  - *Go to:* Settings → Permalinks
  - *Action:* Click "Save" at the bottom. This prevents 404 errors after changing category structures.
