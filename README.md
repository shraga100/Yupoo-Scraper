# 🚀 Yupoo Scraper Pro: The Ultimate E-commerce Data Extractor

Welcome to **Yupoo Scraper Pro** – the most advanced, fast, and smart tool for scraping full album data from Yupoo catalogs — the ultimate tool for dropshippers.

* Scrape entire Yupoo stores, clean the data with GPT-4o, and migrate images for easy import to Shopify/WooCommerce.*

---

## 💡 Who is this for?

- **Dropshipping / E-commerce store owners / Automation systems** who want to export and import entire catalogs quickly.
- **Product suppliers** who need to reorganize their catalog.
- **Inventory managers** who need to migrate hundreds of Yupoo images to stable servers.

## **🚀 Why is it better than other downloaders?**

Unlike basic tools that download images from only one album, **this Actor is a full business solution.**

| **Feature** | **❌ Basic Downloaders** | **✅ This Smart Scraper** |
| --- | --- | --- |
| **Scope** | Single album only | **Full store**, including categories and sub-categories logging |
| **Data Quality** | Images only | Titles, full description, IDs, and prices **(including optional AI cleaning)** |
| **Images** | ZIP file (requires downloading and uploading for each album separately) | **Cloud hosting** (valid links for 7 days, or permanent with your own R2) |
| **Automation** | Manual input for each album | One-click **bulk automation** |

---

> ### 💡 First Time? Start Small — Save Time & Money
>
> Before scraping an entire store, **we strongly recommend testing on a single album or a small category first.**
>
> A test run lets you verify that the output is useful for your needs before committing to a full store with thousands of products and tens of thousands of images.
>
> - **AI Processing (OpenAI):** The AI module uses your own OpenAI API key to call GPT-4o. **OpenAI charges are billed directly to your OpenAI account** — there is no additional charge from us for AI processing. Every store has a unique catalog structure, so test on a single album first to make sure the extracted fields (`productId`, `price`, `storeLink`) match your catalog's format before scaling up.
> - **Image Migration:** Billed per image through Apify. A quick test confirms everything works before migrating thousands of images.
> - **General tip:** Running on a single album first ensures the output format, AI results, and image links all look correct and are usable for your workflow — before you're billed for thousands of products and tens of thousands of images.
> - **Troubleshooting:** All credentials (R2 and OpenAI) are validated at the start of each run. If something is wrong, you'll see a clear error in the **Log** tab — always check there first.
>
> ✅ **Recommended flow:** Single album → Small category → Full store.

---

## ✨ Key Features:

### 🕷️ Comprehensive and Deep Scraping

This Actor scans the Yupoo store and extracts all available information accurately and quickly. It extracts the following raw fields from each album:

- Full **Title and Description**.
- **Categories:** Includes main category and sub-categories (available in full store scraping only).
- **Images:** Links for the Main Image and links for **all other images** in the album in the highest original quality.
- **Videos:** Extraction of video links if available.
- **Original Album URL** and Store Name.

### 📂 Full Store & Category Scraping

- **Full Catalog/Store (Domain) Support:** Enter the link to the store's main page and the Actor will scrape all albums in the catalog for you.

Example URL:
✅`https://xxxxx.x.yupoo.com`
- **Specific Category:** Want all products from the "Shoes" category? Paste the category link, and the Actor will collect all albums inside it (including sub-categories).

Example URL:
✅`https://xxxxx.x.yupoo.com/categories/123456`
- **Single Album:** Need just one specific product? The Actor supports this too.

Example URL:
✅`https://xxxxx.x.yupoo.com/albums/205921667`

### 🔓 Password-Protected Album Support

Is the album locked with a password? No problem. Just enter the password in the Input settings and the Actor will handle the login.

### 🤖 2. [Optional] Smart AI-Based Data Processing

Yupoo is full of unstructured and unclear texts. After the basic scraping phase, you can enable the AI module (powered by GPT-4o). The LLM will read the text and perform **precise extraction**:

- **Product ID Finding:** Extracts the exact product identifier/SKU from the title into a separate key.
- **Price Locating:** Finds the price even if it's hidden deep within the description or title (including ranges and different currencies) and moves it to a separate key.
- **Size-to-Link Mapping:** Identifies purchase links and moves them to a separate key.

⚠️ **Cost Warning:** Using the AI feature requires your own OpenAI API key. Since we use the advanced **GPT-4o** model with advanced reasoning for high accuracy, please pay attention to your OpenAI usage costs, especially when scraping thousands of products. Note that AI-generated output may occasionally be imprecise; raw data is always preserved regardless.

> 💡 **Important:** AI extraction quality depends on how the seller structured their catalog. Before running on a full store, test on a single album to confirm the output (`productId`, `price`, `storeLink`) is being extracted correctly for your specific catalog format.

### ☁️ 3. [Optional - Separate Pay-Per-Image] Bypassing Image Blocks (Temporary Upload to R2)

Often, Yupoo images do not load on external sites due to "Referrer" protection. To solve this, the Actor includes a **built-in Migration system**. The system takes the original scanned images and videos and uploads them to high-performance cloud storage (Cloudflare R2). The result? You get new, stable links that you can display and import to any site or system without any issues or blocks!

**Two migration modes are supported:**
- **Built-in R2 (default):** Use the Actor's shared R2 storage — no configuration needed. Links are valid for **7 days**.
- **Custom R2 (your own bucket):** Bring your own Cloudflare R2 credentials (Account ID, Access Key, Secret Key, Bucket Name, and Public Domain). Images are uploaded directly to your private bucket, giving you full control over storage and link expiration.

⚠️ **Note:** When using the built-in R2, links are temporary (valid for **7 days only**). You must import them into your store within this timeframe. With a custom R2 bucket, link expiration is fully under your control.

However, if you know how to generate a valid referrer yourself, you can skip this step and use the original links.

---

## **📤** Example Final Output

The Actor saves the final output as JSON files in the **Key-Value Store**. These files contain the complete product data — ready for import into Shopify, WooCommerce, or any automation system. Below is an example of what a product object looks like:

* *After basic scraping (without AI processing and image migration, which are optional processing layers)**:
```json
[
  {
    "type": "PRODUCT",
    "scrapedAt": "2025-01-15T12:30:00.000Z",
    "title": "SW9 35$ Swarovski",
    "storeName": "xxxxxxx",
    "parentCategory": [
      "Accessories",
      "RALPH LAURE*"
    ],
    "category": [
      "watch"
    ],
    "description": "they are made of steel \n  the diameter of dial is about 30mm.\n it is quartz.\n type: watch 2\n buy link: https://aliexpress.com/item/111111111",
    "mainImage": "https://photo.yupoo.com/xxxxxx/71388c3a/c3075b6d.jpg",
    "images": [
      "https://photo.yupoo.com/xxxxxx/71388c3a/c3075b6d.jpg",
      "https://photo.yupoo.com/xxxxxx/9744fcdf/81b4c360.jpg",
      "https://photo.yupoo.com/xxxxxx/66958810/e9c47967.jpg",
      "https://photo.yupoo.com/xxxxxx/9b34dd83/b64c7e4b.jpg",
      "https://photo.yupoo.com/xxxxxx/28f68dce/9503710b.jpg",
      "https://photo.yupoo.com/xxxxxx/194b891b/9d9df8bf.jpg",
      "https://photo.yupoo.com/xxxxxx/c41c98cf/55eee397.jpg",
      "https://photo.yupoo.com/xxxxxx/92b34e02/a8e696b5.jpg"
    ],
    "videos": [],
    "url": "https://xxxxxx.x.yupoo.com/albums/205921667"
  }
]
```

* *After full processing (added keys `productId`, `price`, `storeLink`, and Yupoo image links converted to open links):**
```json
[
  {
    "type": "PRODUCT",
    "scrapedAt": "2025-01-15T12:30:00.000Z",
    "title": "SW9 Swarovski",
    "storeName": "xxxxxxx",
    "parentCategory": [
      "Accessories",
      "RALPH LAURE*"
    ],
    "category": [
      "watch"
    ],
    "description": "they are made of steel \n  the diameter of dial is about 30mm.\n it is quartz.\n type: watch 2\n buy link: https://aliexpress.com/item/111111111",
    "mainImage": "https://pub-08e8dc8e344540c7b852736701dfad98.r2.dev/xxxxxx/71388c3a/c3075b6d.jpg",
    "images": [
      "https://pub-08e8dc8e344540c7b852736701dfad98.r2.dev/xxxxxx/71388c3a/c3075b6d.jpg",
      "https://pub-08e8dc8e344540c7b852736701dfad98.r2.dev/xxxxxx/9744fcdf/81b4c360.jpg",
      "https://pub-08e8dc8e344540c7b852736701dfad98.r2.dev/xxxxxx/66958810/e9c47967.jpg",
      "https://pub-08e8dc8e344540c7b852736701dfad98.r2.dev/xxxxxx/9b34dd83/b64c7e4b.jpg",
      "https://pub-08e8dc8e344540c7b852736701dfad98.r2.dev/xxxxxx/28f68dce/9503710b.jpg",
      "https://pub-08e8dc8e344540c7b852736701dfad98.r2.dev/xxxxxx/194b891b/9d9df8bf.jpg",
      "https://pub-08e8dc8e344540c7b852736701dfad98.r2.dev/xxxxxx/c41c98cf/55eee397.jpg",
      "https://pub-08e8dc8e344540c7b852736701dfad98.r2.dev/xxxxxx/92b34e02/a8e696b5.jpg"
    ],
    "videos": [],
    "url": "https://xxxxxx.x.yupoo.com/albums/205921667",
    "productId": "SW9",
    "price": "35",
    "storeLink": [
      {
        "size": "",
        "link": "https://aliexpress.com/item/111111111"
      }
    ]
  }
]
```

---

## 📦 Where to Find Your Output Files

> **Your final data is saved in the Key-Value Store — this is where you should get your output files.**

After each run, the Actor saves JSON files at every stage of processing. You can access them from the **Output** tab (the default view is "Final Output (R2) 🚀") or from the **Key-Value Store** tab in your run's page.

| **File** | **What It Contains** | **When It's Created** |
| --- | --- | --- |
| `RAW__storename_date_N_items` | Raw scraped data exactly as it appears on Yupoo — titles, descriptions, images, videos, and URLs. | Always |
| `AI__storename_date_N_items` | AI-enhanced data with extracted `productId`, `price`, and `storeLink` fields added to each product. | Only when AI is enabled |
| **`FINAL__storename_date_N_items`** | **The complete final output** — includes all AI enhancements plus image URLs replaced with stable R2 links. **This is the file you should use for import.** | Only when Image Migration is enabled |
| `ERROR__storename_date` | Detailed error report broken down by stage (scraping, AI, migration). | Always |

**Which file should I use?**
- If you enabled **both AI and Image Migration** → use the **`FINAL__`** file (it has everything).
- If you enabled **only AI** → use the **`AI__`** file.
- If you used **basic scraping only** → use the **`RAW__`** file.

**How to access:**
1. Open your run in the Apify Console
2. Go to the **Output** tab → click **"Final Output (R2) 🚀"** (this is the default view)
3. Or go to the **Key-Value Store** tab → click on the file you need → download as JSON

---

## 🛠️ How it works?

## **📥** (Input)

Running the Actor is simple and requires configuring a few basic parameters:

| **Parameter** | **Type** | **Description** |
| --- | --- | --- |
| `startUrl` | Required — String | The URL address to scrape. Can be a main store page, a single category, or a specific album. |
| `password` | Optional — String | Password for the album (if it's locked). |
| `useAi` | Optional — Boolean | Enable smart data sorting and cleaning. |
| `openaiApiKey` | Optional — String | Your OpenAI API key (required only if `useAi` is on). |
| `useMigration` | Optional — Boolean | Enable image upload to R2 storage for stable, block-free links (7 days validity by default). |
| `r2AccountId` | Optional — String | Cloudflare Account ID (for custom R2 bucket). |
| `r2AccessKeyId` | Optional — String | R2 Access Key ID (for custom R2 bucket). |
| `r2SecretAccessKey` | Optional — String | R2 Secret Access Key (for custom R2 bucket). |
| `r2BucketName` | Optional — String | Your R2 Bucket Name (for custom R2 bucket). |
| `r2PublicDomain` | Optional — String | Public URL of your R2 bucket, e.g. `https://pub-xxxx.r2.dev` (for custom R2 bucket). |

---

## ☁️ Setting Up Your Own Cloudflare R2 Bucket (Step-by-Step)

Want permanent image links instead of the 7-day temporary ones? Follow these steps to set up your own Cloudflare R2 bucket. It only takes a few minutes.

### Step 1: Create a Bucket

1. Go to [**dash.cloudflare.com**](https://dash.cloudflare.com/)
2. In the left sidebar, click **Storage & Databases**
3. Select **R2 Object Storage** → **Overview**
4. Click the **"Create bucket"** button
5. Enter a **Bucket name** (e.g., `yupoo-images`) and click **"Create a bucket"** to confirm

> ✅ **Save this name** — you'll enter it in the Actor's **Bucket Name** field.

### Step 2: Enable Public Access

1. Inside your newly created bucket, go to the **Settings** tab
2. Find the **"Public Development URL"** section
3. Click **Enable**
4. Copy the URL that appears — it looks like `https://pub-xxxxxxxxxxxx.r2.dev`

> ✅ **Save this URL** — you'll enter it in the Actor's **Bucket Public Domain (URL)** field.

### Step 3: Get Your Account ID

1. Go back to **R2 Object Storage** → **Overview**
2. On the **right side of the page**, you'll see your **Account ID**
3. Copy it

> ✅ **Save this ID** — you'll enter it in the Actor's **R2 Account ID** field.

### Step 4: Create an API Token

1. On the same R2 Overview page, find **"API Tokens"** on the right side
2. Click the **"Manage"** button
3. Under **"User API Tokens"**, click **"Create User API Token"**
4. Choose any **Token name** (e.g., `yupoo-scraper`)
5. Under **Permissions**, select: **"Object Read & Write: Allows the ability to read, write, and list objects in specific buckets."**
6. Under **"Specify bucket(s)"**, choose **"Apply to specific buckets only"** and select the bucket you created in Step 1
7. Click **"Create User API Token"** to save
8. On the confirmation screen, copy both the **Access Key ID** and the **Secret Access Key**

> ⚠️ **Important:** The Secret Access Key is shown **only once**. Make sure to copy it immediately — you cannot retrieve it later.

> ✅ **Save both values** — enter them in the Actor's **R2 Access Key ID** and **R2 Secret Access Key** fields.

### Summary — Field Mapping

| **Where to Find It** | **Actor Input Field** |
| --- | --- |
| Bucket name you chose in Step 1 | `Bucket Name` |
| Public URL from Step 2 (`https://pub-xxx.r2.dev`) | `Bucket Public Domain (URL)` |
| Account ID from Step 3 | `R2 Account ID` |
| Access Key ID from Step 4 | `R2 Access Key ID` |
| Secret Access Key from Step 4 | `R2 Secret Access Key` |

---

## **💡 Tips for Importers**

1. **For WooCommerce/Shopify users:** It's always recommended to enable the **"Image Download (Recommended)"** (Migration) option. If you don't, image links might break when trying to import them to your store because Yupoo blocks external requests.
2. **Bulk Scraping:** If scraping is done via a main store URL with many albums, the run might take a while. You can track the progress in the "Log" tab.
3. **Migrated Link Validity:** Remember, the built-in migrated image links are **temporary (7 days)**. After importing the product to your store, your store will usually download the image and host it on your storage permanently, so the expiration won't affect you after the import. If you need permanent links, use your own Custom R2 bucket.

### ⚠️ Process Abort and Data Safety

Aborting the Actor mid-run can result in partial data and unexpected billing. Here is what happens at each stage:

| **Stage** | **What Happens If You Abort** |
| --- | --- |
| **During Scraping** | All collected data may be lost — nothing has been saved to the Key-Value Store yet. You are still charged for each product already scraped (`product-scraped` billing event fires immediately per product). |
| **After Raw Data Save** | Raw scraped data is preserved in the Key-Value Store (`RAW__*` key). However, it will NOT appear in the Dataset (the standard output). You can retrieve it manually from the KV Store. |
| **During AI Processing** | Raw data is safe in the Key-Value Store. AI-enhanced data may be partial or lost. OpenAI API charges for already-processed items are non-refundable. |
| **During Image Migration** | **Highest risk.** Images already uploaded to R2 are billed immediately upon success. If you abort mid-migration, you will be charged for images already migrated, but the final data (with updated image URLs) may not be saved to the Dataset. You could end up paying for migrated images without receiving usable output. |

**Recommendations:**
- **Estimate costs before running** by testing on a single album first (see the advice at the top of this page).
- **Avoid aborting during image migration** if possible — this is the most expensive stage to interrupt.
- If you must abort, check the **Key-Value Store** for partial data (keys starting with `RAW__`, `AI__`, or `FINAL__`).
- Data in the Key-Value Store may be partial and should be validated before use.

### ⚠️ Maximum Cost Per Run (`maxTotalChargeUsd`)

This Actor supports Apify's **"Maximum cost per run"** limit. When the budget is exhausted, the Actor will **stop gracefully** and push all data collected so far to the Dataset.

**What to expect when the cost limit is reached:**
- **Scraping stops** — no more products will be scraped after the limit is hit.
- **AI processing and image migration are skipped** if the limit was reached during the scraping phase.
- **If the limit is reached during image migration** — uploads in progress will finish, but no new uploads will start. Some product image URLs may remain as original Yupoo links (not migrated), while others will have the new R2 links.
- **All data collected up to that point is saved** to both the Dataset and the Key-Value Store.
- The run summary will clearly indicate that the run was **partial** due to the cost limit.

**Important:** When using a cost limit with image migration enabled, some products in your output may have **mixed image URLs** — a combination of migrated R2 links and original Yupoo links. Make sure your import workflow can handle both URL formats. Check the `ERROR__` file in the Key-Value Store for the `chargeLimitReached` flag to know if the run was stopped early.

> **Disclaimer:** The behavior described above is the *expected* behavior, but we **do not recommend** setting a cost limit or aborting mid-run, and we **do not take responsibility** for the quality or completeness of the data in such cases. Partial runs may produce incomplete, inconsistent, or mixed-format output. **Always test on a single album or a small category first** to estimate costs before running on a full store — this way you can avoid the need for a cost limit altogether.

### ⚠️ Important Billing Notes

- The Actor exports data directly to the Apify Dataset, and also saves the JSON files in the Key-Value Store.
- When using the image migration service, migrated images are logged as separate entries in the Dataset to provide you with full transparency on the amount of successfully migrated images.
- Payment is per product (album) and per image saved in R2.

---

## 🔌 API Integration Guide

You can run this Actor programmatically using the Apify API. This guide covers the full flow — from starting a run to downloading the final output.

### How to Get Your API Token

1. Go to [console.apify.com](https://console.apify.com)
2. In the left sidebar, click **Settings** (last item in the menu)
3. On the page that opens, click the **API & Integrations** tab
4. Copy the existing token or create a new one

### The 3 IDs

| ID | Where it comes from |
|----|---------------------|
| `UAYk0FDgVBjF8WoAz` | Fixed — hardcode it in every request |
| `runId` | Returned in the Step 1 response |
| `kvStoreId` | Returned in the Step 1 response (`defaultKeyValueStoreId`) |

### Step 1 — Start the Run

```bash
curl -X POST \
  "https://api.apify.com/v2/acts/UAYk0FDgVBjF8WoAz/runs?token=YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
    "startUrl":          "https://STORE.x.yupoo.com",

    "password":          "ALBUM_PASSWORD",

    "useAi":             true,
    "openaiApiKey":      "YOUR_OPENAI_KEY",

    "useMigration":      true,
    "r2AccountId":       "CF_ACCOUNT_ID",
    "r2AccessKeyId":     "R2_ACCESS_KEY",
    "r2SecretAccessKey": "R2_SECRET_KEY",
    "r2BucketName":      "YOUR_BUCKET",
    "r2PublicDomain":    "https://pub-xxx.r2.dev"
  }'
```

| Parameter | Required | Description |
|-----------|----------|-------------|
| `startUrl` | **Required** | Yupoo URL — store, category, or single album |
| `password` | Optional | Album password (only if the store is locked) |
| `useAi` | Optional | Enable AI processing (GPT-4o) |
| `openaiApiKey` | Optional | Your OpenAI API key (required if `useAi` is `true`) |
| `useMigration` | Optional | Enable image upload to R2 storage |
| `r2AccountId` | Optional | Cloudflare Account ID (required if `useMigration` is `true` and you want your own bucket) |
| `r2AccessKeyId` | Optional | R2 Access Key ID (required if `useMigration` is `true` and you want your own bucket) |
| `r2SecretAccessKey` | Optional | R2 Secret Access Key (required if `useMigration` is `true` and you want your own bucket) |
| `r2BucketName` | Optional | Your R2 bucket name (required if `useMigration` is `true` and you want your own bucket) |
| `r2PublicDomain` | Optional | Public URL of your R2 bucket (required if `useMigration` is `true` and you want your own bucket) |

> **Minimal example** — scraping only (no AI, no migration):
> ```json
> { "startUrl": "https://STORE.x.yupoo.com" }
> ```

From the response, save:
- `data.id` → your **runId**
- `data.defaultKeyValueStoreId` → your **kvStoreId**

### Step 2 — Poll Until SUCCEEDED

Large stores take hours. Repeat every 60s until `status` is `SUCCEEDED`.

```bash
curl "https://api.apify.com/v2/acts/UAYk0FDgVBjF8WoAz/runs/RUN_ID?token=YOUR_TOKEN"
```

Check `data.status`:
- `"RUNNING"` → wait and retry
- `"SUCCEEDED"` → proceed to Step 3
- `"FAILED"` / `"ABORTED"` → check the Log tab in Apify Console

### Step 3 — Find the FINAL__ File Key

The filename includes store name + date + item count, so you need to look it up.

```bash
curl "https://api.apify.com/v2/key-value-stores/KV_STORE_ID/keys?token=YOUR_TOKEN"
```

Look for a key starting with `FINAL__`, e.g. `FINAL__mystore_2025-01-15_340items`.
No `FINAL__`? Fall back to `AI__` or `RAW__`.

### Step 4 — Download the JSON

```bash
curl \
  "https://api.apify.com/v2/key-value-stores/KV_STORE_ID/records/FINAL__mystore_2025-01-15_340items?token=YOUR_TOKEN" \
  -o output.json
```

`output.json` is an array of all products. Each item contains: title, images (R2 links), description, price, SKU, storeLink.

### Full Script (Node.js)

Save as `scraper.mjs`, run with `node scraper.mjs`.

```js
// ─────────────────────────────────────────────
//  scraper.mjs — Yupoo Scraper full flow
//  Runs all 4 steps and saves output.json
// ─────────────────────────────────────────────

// ── CONFIGURATION ─────────────────────────────

const ACTOR_ID = 'UAYk0FDgVBjF8WoAz'; // Fixed Actor ID — never changes

const TOKEN = 'YOUR_APIFY_TOKEN';      // Your Apify API token

const INPUT = {
  // ── Required ────────────────────────────────
  startUrl: 'https://STORE.x.yupoo.com', // Store, category, or single album URL

  // ── Optional — album password ───────────────
  password: 'ALBUM_PASSWORD',             // Only if the store is locked

  // ── Optional — AI processing ────────────────
  // Extracts price, SKU, and purchase links from raw text
  useAi:        true,
  openaiApiKey: 'YOUR_OPENAI_KEY',        // Required if useAi is true (billed to your OpenAI account)

  // ── Optional — image migration ──────────────
  // Uploads images to Cloudflare R2 for stable, unblocked links
  useMigration:      true,
  // The 5 fields below are optional — leave them out to use the built-in R2 (7-day links).
  // Provide ALL 5 to use your own R2 bucket (permanent links).
  r2AccountId:       'CF_ACCOUNT_ID',     // Cloudflare Account ID
  r2AccessKeyId:     'R2_ACCESS_KEY',     // R2 Access Key ID
  r2SecretAccessKey: 'R2_SECRET_KEY',     // R2 Secret Access Key
  r2BucketName:      'YOUR_BUCKET',       // R2 bucket name
  r2PublicDomain:    'https://pub-xxx.r2.dev', // Public URL of your R2 bucket
};

// ── HELPERS ───────────────────────────────────

const BASE = 'https://api.apify.com/v2';

// Wait helper — pauses execution for the given milliseconds
const wait = ms => new Promise(resolve => setTimeout(resolve, ms));

// Fetch JSON helper
const getJson = async url => (await fetch(url)).json();

// ── MAIN ──────────────────────────────────────

async function main() {

  // ── STEP 1: Start the run ──────────────────
  console.log('Starting run...');

  const startResponse = await (await fetch(
    `${BASE}/acts/${ACTOR_ID}/runs?token=${TOKEN}`,
    {
      method:  'POST',
      headers: { 'Content-Type': 'application/json' },
      body:    JSON.stringify(INPUT),
    }
  )).json();

  const runId = startResponse.data.id;                        // Save runId
  const kvId  = startResponse.data.defaultKeyValueStoreId;   // Save kvStoreId

  console.log('Run ID:      ', runId);
  console.log('KV Store ID: ', kvId);

  // ── STEP 2: Wait for the run to finish ─────
  console.log('\nWaiting for run to finish (checking every 60s)...');

  let status = 'RUNNING';

  while (['RUNNING', 'READY'].includes(status)) {
    await wait(60_000); // Wait 60 seconds between each check

    const checkResponse = await getJson(
      `${BASE}/acts/${ACTOR_ID}/runs/${runId}?token=${TOKEN}`
    );

    status = checkResponse.data.status;
    console.log('Status:', status);
  }

  if (status !== 'SUCCEEDED') {
    throw new Error(`Run ended with status: ${status}`);
  }

  console.log('Run completed successfully.');

  // ── STEP 3: Find the output file key ───────
  console.log('\nLooking for output file...');

  const keysResponse = await getJson(
    `${BASE}/key-value-stores/${kvId}/keys?token=${TOKEN}`
  );

  const allKeys = keysResponse.data.items.map(item => item.key);

  // Prefer FINAL__ (migration + AI), fall back to AI__ then RAW__
  const fileKey = allKeys.find(k => k.startsWith('FINAL__'))
               || allKeys.find(k => k.startsWith('AI__'))
               || allKeys.find(k => k.startsWith('RAW__'));

  if (!fileKey) throw new Error('No output file found in KV Store.');

  console.log('Output file: ', fileKey);

  // ── STEP 4: Download the JSON ──────────────
  console.log('\nDownloading output...');

  const data = await getJson(
    `${BASE}/key-value-stores/${kvId}/records/${encodeURIComponent(fileKey)}?token=${TOKEN}`
  );

  const { writeFileSync } = await import('fs');
  writeFileSync('output.json', JSON.stringify(data, null, 2));

  console.log(`\nDone — ${data.length} products saved to output.json`);
}

main().catch(console.error);
```

### Output File Keys

| Key prefix | When it exists | Contains |
|------------|----------------|----------|
| `FINAL__` | Migration enabled | All data + stable R2 image links — **use this** |
| `AI__` | AI enabled, no migration | Data with extracted price / SKU / storeLink |
| `RAW__` | Always | Raw scraped data, original Yupoo image URLs |
| `ERROR__` | Always | Error report per stage (scraping / AI / migration) |
