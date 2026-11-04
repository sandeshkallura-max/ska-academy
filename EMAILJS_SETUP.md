# SKA Academy — EmailJS enrollment setup

This V3 package sends enrollment form submissions to `s79178917@gmail.com` using EmailJS. Google Sheets is not used.

## 1. Create/connect your EmailJS email service

1. Sign in at https://dashboard.emailjs.com/.
2. Open **Email Services** → **Add New Service** → choose **Gmail**.
3. Connect the Gmail account that will send the notifications. The receiving address can remain `s79178917@gmail.com`.
4. Save the service and copy its **Service ID**.

## 2. Create the enrollment email template

Create a new Email Template and configure these fields:

- **To Email:** `s79178917@gmail.com`
- **From Name:** `SKA Academy Enrollment`
- **From Email:** Use Default Email Address (the connected service)
- **Reply To:** `{{email}}`
- **Subject:** `New Student Enrollment – SKA Academy`

Use this as the template body:

```text
New student enrollment received — SKA Academy

Student name: {{name}}
Phone number: {{phone}}
Student email: {{email}}
Selected course: {{course}}
Learning mode: {{mode}}
Preferred batch: {{batch}}
Message: {{message}}

Please contact the student to follow up.
```

Save the template and copy its **Template ID**. The `Reply To` field should contain only `{{email}}` (do not add other text there).

## 3. Copy your EmailJS Public Key

In the EmailJS dashboard, open **Account** → **General** (or **Public Key** in the account settings) and copy the **Public Key**. Do not share your Gmail password, Google verification codes, or private keys.

## 4. Add the three IDs to the website

Open `index.html` and find these lines near the bottom, before the main website script:

```js
const EMAILJS_PUBLIC_KEY = 'Qh-XlHZ5neSWK8lIo';
const EMAILJS_SERVICE_ID = 'service_x531zbm';
const EMAILJS_TEMPLATE_ID = 'template_6atoww5';
```

The Public Key, Service ID, and Template ID are now filled in for your account. Verify the template fields match the form variables before publishing. The value `__ejs-test-mail-service__` is not a real enrollment template ID. These are browser-side EmailJS identifiers; never put your Gmail password or a private server secret in this file.

## 5. Publish and test

1. Upload the contents of this project to the root of your existing GitHub Pages repository, replacing the previous V3 files. Keep `assets/` alongside `index.html`.
2. Commit the changes and wait for GitHub Pages to publish.
3. Open the live website, select Online or Offline first, and submit a test registration using an email address you can access.
4. Confirm that the notification arrives at `s79178917@gmail.com`. Check Spam if it does not appear.

## Notes

- The website now uses EmailJS only; the Google Apps Script/Sheets integration has been removed from this package.
- The form does not show success until EmailJS confirms the send request.
- Configure EmailJS account security/rate limits and consider adding CAPTCHA or other anti-spam protection before broad public promotion. The EmailJS public key is expected to be visible in a static website; do not add private credentials.
- Do not collect unnecessary student information. Keep the receiving mailbox secured.
