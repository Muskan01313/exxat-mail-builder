# Exxat Mail Builder

A one-page website that builds the files needed to set up evaluation-form notifications, without editing JSON by hand.

## What it does

1. **Select notifications:** Action notification (Alert.Admin), Low Score, and/or Response based.
2. **Add forms:** enter each form's feature ID and form name, or paste a list (`Form name | Feature ID`, one per line).
3. **Choose files:**
   - **Fusion file:** the Mongo email template for each form and notification, with a new GUID in `id` and `_id`.
   - **Notification file:** the action notification setup for each form.
   - **Stakeholder file:** one file per person, listing the feature IDs of every form entered.
4. **Review details:** your organization (Tenant ID, owning organization unit and partition key), stakeholder first name, last name and email, and an optional shared email template ID.

The files can be copied or downloaded one by one, or downloaded together as a zip.

There is also a GUID generator in the header (same format as PowerShell `[guid]::NewGuid()`).

## How to use it

Open `index.html` in a browser. Everything runs in the browser; nothing is sent anywhere. The zip download loads JSZip from cdnjs.

To host it, turn on **GitHub Pages** (Settings → Pages → Deploy from branch → `main`, folder `/`), or upload `index.html` to any static web host.
