# Option A Setup Guide: Secure External Portal + Public Website

This project has been converted to the **Option A model**:

- `index.html` is now the safer public website.
- Clinical appointment/screening buttons open a secure external portal/form provider.
- The public website does **not** store psychiatric screening answers, suicide-risk answers, or appointment submissions in browser localStorage.
- `prototype-local-demo.html` is a backup of the earlier local demo with browser-only dashboard.

## Important reality check

A public website can be hosted free on GitHub Pages or Cloudflare Pages, but a truly secure healthcare portal is usually **not free forever**. For psychiatric data, suicide-risk triage, child forms, and rating scales, use a platform that provides strong privacy/security controls and is appropriate for your country/regulatory context.

## What to choose in a portal provider

Choose a secure healthcare form/patient portal provider that supports:

1. HTTPS on all pages.
2. Staff login with strong passwords and ideally 2-factor authentication.
3. Role-based permissions for clinician/reception/admin.
4. Encrypted records and encrypted backups.
5. Audit logs showing who viewed/exported records.
6. Secure file upload, if referral documents are needed.
7. Form logic/conditional questions.
8. Email/SMS alert workflow that does **not** expose private answers.
9. Data export for office records.
10. Clear data retention/deletion tools.
11. A privacy/security agreement suitable for your legal context.

Examples of platform categories: healthcare intake portal, clinic EMR/EHR portal, secure form platform with healthcare compliance features, or a local hospital/clinic management platform.

## Forms to create inside the portal

Create these separate secure forms:

### 1. New adult appointment/intake

Sections:

- Consent and emergency disclaimer
- Full name
- Phone / WhatsApp
- Email
- Preferred appointment date/time
- Brief reason for visit
- Adult screening section
- Safety/suicide-risk triage section
- Permission to contact
- Submit

### 2. Child/adolescent parent/guardian intake, age 6–17

Sections:

- Parent/guardian consent
- Child name/age
- Parent/guardian name
- Relationship to child
- Contact information
- Main concerns
- Parent/guardian-rated screening section
- School/family concerns
- Safety section
- Submit

### 3. Follow-up patient form

Sections:

- Patient identifying information
- Current concern since last visit
- Medication/adherence side effects if applicable
- Follow-up rating scales requested by clinician
- Safety questions
- Submit

### 4. Secure general message form

Use this for non-urgent secure messages. Include a warning that emergencies should not be sent through the website.

### 5. Staff portal/dashboard link

This is the login page where office staff review submissions.

## Suicide-risk alert workflow

Inside the portal, configure conditional logic:

If a visitor answers risk questions positively, then:

1. Show emergency guidance immediately on the form confirmation page.
2. Mark the submission as urgent/high priority.
3. Notify staff by email/SMS/portal notification.
4. The notification should say only something like:

```text
URGENT: A high-priority appointment request was submitted. Log in to the secure portal to review.
```

Do **not** send detailed suicide-risk answers by ordinary email or SMS.

## How to connect the public website to your portal

After creating forms, copy their secure share links and open `index.html`.

Find this section near the bottom:

```javascript
const portalLinks = {
  adultNew: '#',
  childGuardian: '#',
  followUp: '#',
  generalContact: '#',
  staff: '#'
};
```

Replace `#` with your real secure portal links, for example:

```javascript
const portalLinks = {
  adultNew: 'https://secure-portal.example.com/forms/adult-intake',
  childGuardian: 'https://secure-portal.example.com/forms/child-guardian-intake',
  followUp: 'https://secure-portal.example.com/forms/follow-up',
  generalContact: 'https://secure-portal.example.com/forms/secure-message',
  staff: 'https://secure-portal.example.com/staff/login'
};
```

Save the file and redeploy to GitHub Pages/Cloudflare Pages.

## Before using with real patients

Do a full test:

1. Submit test adult form.
2. Submit test child/guardian form.
3. Submit test follow-up form.
4. Submit a test high-risk answer.
5. Confirm staff receive only a privacy-safe urgent alert.
6. Confirm staff can log in and see full details.
7. Confirm unauthorized people cannot access records.
8. Confirm exports are controlled.
9. Confirm the emergency instructions are clear in all three languages.
10. Have a clinician/legal reviewer approve the final form text.

## Files

- `index.html` — Option A public website.
- `prototype-local-demo.html` — old browser-only prototype backup; do not use it for real patient data.
- `OPTION_A_SETUP.md` — this guide.
- `FORM_BLUEPRINT.md` — detailed form structure checklist.
