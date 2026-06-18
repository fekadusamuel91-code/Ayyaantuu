# Nagaa Mind Care — Option A Website

This is the **Option A** version of the psychiatry and psychotherapy consultation website.

## What Option A means

The public website is simple, multilingual, and low-data. Sensitive appointment and screening forms are handled by a separate secure healthcare portal/form provider.

The public website does **not** store clinical submissions in browser localStorage.

## Files

- `index.html` — current Option A public website.
- `prototype-local-demo.html` — backup of the earlier local demo; do not use for real patient data.
- `OPTION_A_SETUP.md` — step-by-step setup guide for connecting a secure external portal.
- `FORM_BLUEPRINT.md` — form structure checklist for building intake/follow-up forms inside the secure portal.

## Current contact details

- Phone / WhatsApp: `0900068887`
- Email: `fekadusamuel92@outlook.com`
- Address: placeholder until the full clinic location is provided.

## How to connect secure forms

Open `index.html` and find:

```javascript
const portalLinks = {
  adultNew: '#',
  childGuardian: '#',
  followUp: '#',
  generalContact: '#',
  staff: '#'
};
```

Replace each `#` with the secure link from your chosen portal provider.

## Important safety note

Do not collect real psychiatric screening, suicide-risk answers, child/guardian clinical information, or rating scale answers through ordinary email, Google Sheets, or a simple public website form. Use a secure healthcare portal with staff login, encryption, permissions, audit logs, backups, and safe urgent-alert workflow.
