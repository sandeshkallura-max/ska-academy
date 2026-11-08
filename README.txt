SKA Academy website package

PUBLISHING
1. Extract this ZIP file.
2. Upload index.html to the root of your GitHub Pages repository, replacing the existing index.html.
3. Commit the change and wait for the GitHub Pages deployment to finish.

EMAILJS TEMPLATE
The website sends these template parameters for a new registration:
- to_email
- from_name
- phone
- email
- course
- mode
- batch
- message
- password
- message_type

Use these exact EmailJS placeholders in the template body:
Student name: {{from_name}}
Phone: {{phone}}
Student email: {{email}}
Selected course: {{course}}
Learning mode: {{mode}}
Preferred batch: {{batch}}
Message: {{message}}
Student password: {{password}}
Notification type: {{message_type}}

PASSWORD SECURITY WARNING
This package includes the requested password email field. That sends the student's password in readable plain text through email and is not recommended. Prefer a proper authentication provider (such as Firebase Authentication or Supabase Auth), and never email passwords. Do not use this demo/localStorage login for sensitive or production student accounts.

REGISTRATION VALIDATION
The form checks that Create Password and Confirm Password match before it sends the registration notification or saves the local demo account. The old Update Login ID / Password panel has been removed from the student portal.
