Notion Parametric Explorer Setup Guide

Follow the steps below to connect your workflow to Notion and start sending parametric study results to your own Notion-based explorer.

STEP 1 — Create a Notion Integration

Create a free Notion account (if you don’t have one).

Go to:
👉 https://www.notion.so/my-integrations

Click “New integration”.

Create a token with default permissions.

Copy the generated Internal Integration Token.

STEP 2 — Create a Workspace Page (API Scope)

Create a new empty page inside your designated workspace.
This page will act as the API scope.

Go back to your integration settings (from Step 1).

Under Content Access, grant access to the page you just created.

Only pages shared with the integration can be accessed via the API.

STEP 3 — Insert the Token

Insert your integration token into your script:

NOTION_TOKEN = "your_token_here"

⚠️ Important:
For production use, sensitive keys should be stored as environment variables.
For demo purposes, inserting directly is acceptable.

STEP 4 — Set Temporary Image Directory (Optional)

If your workflow exports images (e.g., viewport captures),
define a local directory path for temporary storage.

These files can be deleted after upload.

Example:

TEMP_IMAGE_DIR = "C:/temp/notion_exports"

STEP 5 — Structure Your Parameters

Organize your input or output parameters as structured key–value pairs.

Example:

data = {
"Width": 12000,
"Height": 3200,
"GWP": 145.2,
"Variant ID": "Option_12"
}

Clean, structured data ensures proper database mapping.

STEP 6 — Set parent_id

Retrieve the parent_id of the page created in Step 2.

This ID defines where your database will be created.

Example:

parent_id = "your_page_id_here"

STEP 7 — Instantiate the Database

Use the Notion API to create a new database inside the parent page.

Define the database schema based on your parameter structure.

Once created, this database becomes your Parametric Explorer interface.

STEP 8 — Start Sending Data 🚀

Your setup is now ready.

You can begin sending parametric variants directly from Grasshopper (or other workflows) into your Notion database.

You now have:

Structured design variants

Organized performance metrics

Shareable live links

A lightweight decision-review environment

Welcome to your own Notion-powered Parametric Explorer 🙂
