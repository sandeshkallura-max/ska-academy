# SKA ACADEMY — Learn with Passion

A responsive static website for GitHub Pages, with a professional navy, white and gold design, Online/Offline-first enrollment, academic syllabus placeholder, faculty categories and subtle animations.

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

## Project files

- `index.html` — website and EmailJS enrollment integration
- `assets/ska-academy-logo.png` — SKA Academy logo
- `EMAILJS_SETUP.md` — step-by-step EmailJS configuration
- `SETUP.md` — GitHub Pages publishing instructions
