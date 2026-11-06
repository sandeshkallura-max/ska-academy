# SKA ACADEMY — Learn with Passion

A responsive static website for GitHub Pages, featuring a professional navy, white and gold design, Online/Offline-first enrollment, a secure **Member Login Portal**, a gated **Academic Syllabus** (with a "Coming Soon / Under Update" state for logged-in members), faculty categories, and subtle scroll animations.

## Publish on GitHub Pages

1. Sign in at https://github.com/ and open your existing `ska-academy` repository.
2. Upload/replace the project files in the repository root. Keep `index.html` in the root and the `assets` folder beside it.
3. Open **Settings → Pages** and confirm deployment from branch `main`, folder `/ (root)`.
4. Wait for GitHub Pages to publish the changes.

## Connect student enrollment to email

Enrollment uses EmailJS and sends notifications to `s79178917@gmail.com`. Google Sheets is not used. Before accepting real registrations, complete the steps in **EMAILJS_SETUP.md**:

- Connect a Gmail service in EmailJS.
- Create the enrollment email template with the documented variables.
- Add your EmailJS Public Key, Service ID and Template ID to `index.html`.
- Publish and submit a test registration.

The form requires students to select Online or Offline before enrollment. A success message is shown only after EmailJS confirms the email request was sent.

## Direct Student Access (No Manual Approval Needed)
- **Automatic Instant Login:** When a student submits the free registration form, they are automatically signed in and redirected straight to the Academic Syllabus section.
- **Member Login Portal:** Existing registered students can log in anytime by clicking **Member Login 🔑** in the header using their email or phone number.
- **Academic Syllabus State:** Displays the gated **"Syllabus Content Coming Soon ⏳"** dashboard view once logged in.

## Project files

- `index.html` — website, EmailJS enrollment integration, and member login portal
- `EMAILJS_SETUP.md` — step-by-step EmailJS configuration
- `SETUP.md` — GitHub Pages publishing instructions
