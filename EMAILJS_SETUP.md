# SKA Academy — EmailJS enrollment setup

This package sends enrollment form submissions to `s79178917@gmail.com` using EmailJS. Google Sheets is not used.

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

Save the template and copy its **Template ID**.

## 3. Copy your EmailJS Public Key

In the EmailJS dashboard, open **Account** → **General** (or **Public Key** in the account settings) and copy the **Public Key**.

## 4. Add the three IDs to the website

Open `index.html` and update these lines near the bottom:

```js
const EMAILJS_PUBLIC_KEY = 'Qh-XlHZ5neSWK8lIo';
const EMAILJS_SERVICE_ID = 'service_x531zbm';
const EMAILJS_TEMPLATE_ID = 'template_6atoww5';
```
