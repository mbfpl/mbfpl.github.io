# MASH Bio Fuels — Material & Inventory Tracker

A static web application (ready for **GitHub Pages**, **Netlify**, or **Vercel**) that connects to your 7 Google Sheets to track every unique **Material Code** and **Item Description** across **Indents**, **GRNs (FY 24-25, 25-26, 26-27)**, **Daily Issues**, and **Daily Stock**.

## Step 1: Deploy the Google Apps Script API (`Code.gs`)
1. Open [script.google.com](https://script.google.com) under the Google account that has access to all 7 Google Sheets.
2. Click **New project**, delete the default `myFunction`, and paste the entire contents of `Code.gs`.
3. Click **Deploy &rarr; New deployment**.
4. Select type: **Web app**.
   - **Execute as:** `Me`
   - **Who has access:** `Anyone` (or `Anyone within your organization` if internal-only, though `Anyone` is required for public GitHub Pages without login).
5. Click **Deploy**, authorize permissions, and copy the **Web app URL** (`https://script.google.com/macros/s/.../exec`).

## Step 2: Host `index.html` on GitHub Pages (Free)
1. Create a new repository on [GitHub](https://github.com/new) (e.g., `material-tracker`).
2. Upload `index.html` to the root of the repository.
3. Go to **Settings &rarr; Pages**, set **Source** to `Deploy from a branch`, select `main` / `/ (root)`, and click **Save**.
4. Open your live GitHub Pages URL (`https://<your-username>.github.io/material-tracker/`).
5. Click **Connect Google Sheets** in the top right, paste your Apps Script Web App URL, and click **Save & Load Live Data**.
