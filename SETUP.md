# SKA ACADEMY — Learn with Passion

A responsive static website for GitHub Pages, with a free-launch message and enrollment form.

## Publish for free with your GitHub account

1. Sign in at https://github.com/.
2. Create a **new public repository** named `ska-academy` (or another name).
3. Upload all files and folders from this project. Keep `index.html` in the repository root and keep the `assets` folder.
4. In the repository, open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Choose branch `main` and folder `/ (root)`, then click **Save**.
7. Wait a few minutes. GitHub will show your public website URL, usually:
   `https://YOUR-USERNAME.github.io/ska-academy/`

GitHub Pages hosting is free for public repositories. A custom domain is optional and normally costs money.

## Important: connect enrollment requests before launch

GitHub Pages only hosts static files. It does not save student registrations or provide a secure admin dashboard by itself.

This project includes `google-apps-script/Code.gs` for a free Google Sheets enrollment receiver:

1. Create a Google Sheet in your Google account.
2. In that sheet, select **Extensions → Apps Script**.
3. Replace the editor contents with the code in `google-apps-script/Code.gs`.
4. Save the project.
5. Select **Deploy → New deployment → Web app**.
6. Set **Execute as** to `Me`.
7. Set **Who has access** to `Anyone`, then deploy and authorize it.
8. Copy the Web app URL ending in `/exec`.
9. Open `index.html` in the GitHub repository editor. Find:
   `YOUR_GOOGLE_APPS_SCRIPT_WEB_APP_URL`
10. Replace that exact text with your Web app URL, commit the change, and wait for GitHub Pages to redeploy.
11. Submit a test enrollment and confirm that a new row appears in your Google Sheet.

The Google Sheet becomes your simple enrollment inbox. Open it to view student details and update the Status column (for example, New, Contacted, Confirmed). Keep the sheet private and do not publish it.

## Before accepting real student details

- Test the form yourself.
- Add an academy contact email/phone and actual offline-class location.
- Review how you will protect and retain student contact information.
- Do not describe the demo as a secure admin dashboard. A separate authenticated admin portal requires additional implementation.
- The free launch message is intentionally clear: fees are currently zero; students should be informed in advance if fees change later.

## Files

- `index.html` — website
- `assets/ska-academy-logo.png` — selected SKA Academy logo
- `google-apps-script/Code.gs` — optional Google Sheets receiver
\n\nWebsite updates: students must select Online or Offline before proceeding to enrollment. Academic Syllabus is an intentionally empty placeholder for future updates. Lecturing Faculty currently shows faculty categories only; add confirmed professional names and qualifications when available. Subtle animations are included, with reduced-motion accessibility support.\n