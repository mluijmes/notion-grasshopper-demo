# Notion Parametric Explorer Setup Guide

Follow the steps below to connect your workflow to Notion and start sending parametric study results to your own Notion-based explorer.

---

## STEP 1 — Create a Notion Integration

1. Create a free Notion account (if you don’t have one).
2. Go to: https://www.notion.so/my-integrations
3. Click **“New integration”**.
4. Create a token with default permissions.
5. Copy the generated **Internal Integration Token**.

---

## STEP 2 — Create a Workspace Page (API Scope)

1. Create a new empty page inside your designated workspace.  
   This page will act as the **API scope**.
2. Go back to your integration settings (from Step 1).
3. Under **Content Access**, grant access to the page you just created.

> Only pages shared with the integration can be accessed via the API.

---

## STEP 3 — Insert the Token

Insert your integration token into your script:

NOTION_TOKEN = "your_token_here"
