# Secure Portal Form Blueprint

Use this blueprint to build forms inside your chosen secure healthcare portal. The public website should only link to these secure forms.

## General requirements for every form

Every secure form should include:

1. Language choice: Afaan Oromo, Amharic, English.
2. Emergency warning at the top.
3. Consent checkbox.
4. Privacy note.
5. Contact permission.
6. Required phone number.
7. Clear submit confirmation.
8. High-risk workflow if safety answers indicate urgent risk.

Recommended emergency text:

```text
This form is not monitored 24/7. If you are in immediate danger or cannot stay safe, call local emergency services or go to the nearest emergency department now.
```

## Form 1: Adult new appointment/intake

### A. Consent and privacy

- I understand this form is not for emergencies.
- I consent to the office reviewing my answers.
- I understand the office may contact me by phone/SMS/email according to clinic policy.

### B. Demographics/contact

- Full name
- Age/date of birth
- Phone / WhatsApp
- Email
- Address/city, if clinically necessary
- Preferred language
- Preferred appointment date/time
- New appointment or urgent appointment request

### C. Visit reason

- Main concern in visitor's own words
- When did the problem start?
- What has helped or worsened it?
- Prior mental health care? yes/no
- Current medications? yes/no/details if needed

### D. Broad symptom screening area

Use official/licensed instruments where required. If using DSM-5 Level 1 Cross-Cutting Symptom Measure, confirm permission, exact wording, scoring, and clinical review.

Domains to include if clinically approved:

- Depression/low mood
- Anxiety/fear
- Sleep problems
- Irritability/high energy
- Trauma-related symptoms
- Psychosis-like experiences
- Substance use
- Attention/functioning problems
- Somatic concerns if desired

### E. Safety/suicide-risk triage

Use an approved suicide-risk protocol such as C-SSRS if licensed/authorized and clinically reviewed.

Workflow logic:

- Passive death wish → priority review
- Suicidal thoughts → priority review
- Plan/method/access to means → urgent review
- Intent/recent attempt/unable to stay safe → urgent instructions and immediate staff alert

Notification to staff should not include detailed private answers.

## Form 2: Child/adolescent parent/guardian intake, age 6–17

### A. Parent/guardian consent

- Parent/guardian name
- Relationship to child
- Guardian phone/email
- Consent to submit information

### B. Child information

- Child name
- Age/date of birth
- School grade
- Preferred language

### C. Main concerns

- Parent/guardian concern
- Child's reported concern, if known
- School concerns
- Family/social concerns

### D. Parent/guardian-rated screening

Use the official Parent/Guardian-Rated DSM-5 Level 1 Cross-Cutting Symptom Measure for child age 6–17 only after confirming permission, exact wording, scoring, and clinical review.

Possible domains:

- Depression/withdrawal
- Anxiety/fear
- Sleep/appetite
- Anger/behavior change
- Attention/school problems
- Trauma-related symptoms
- Unusual perceptions/thoughts
- Substance concern, if age-appropriate

### E. Child safety section

Ask parent/guardian about:

- Self-harm statements
- Suicidal thoughts/behaviors
- Recent attempts
- Aggression/risk to others
- Immediate safety concerns

High-risk answers should trigger urgent portal workflow.

## Form 3: Follow-up patient form

### A. Identity and visit info

- Full name
- Phone
- Follow-up appointment date
- Clinician name if applicable
- Main update since last visit

### B. Medication/treatment update

- Current medications
- Missed doses
- Side effects
- Therapy attendance
- Hospital/emergency visits since last appointment

### C. Rating scale section

Only include tools requested by the clinician and approved for use.

Possible areas:

- GAD-7 anxiety
- Depression follow-up scale
- Hamilton Depression Rating Scale note: clinician-rated; patient pre-visit symptom collection should not replace clinician scoring
- PDQ/personality questionnaire area
- Community Assessment of Psychic Experiences/CAPE area

### D. Safety update

- Since last visit, any thoughts of self-harm?
- Any plan or intent?
- Any recent attempt?
- Any risk to others?
- Can the patient stay safe now?

High-risk answers should trigger urgent workflow.

## Form 4: Secure general message

This is for non-urgent messages only.

Fields:

- Name
- Phone
- Email
- Message category
- Message
- Consent to be contacted

Warning:

```text
Do not use this form for emergencies. Do not include unnecessary private clinical details unless the secure portal has been approved by the clinic.
```

## Confirmation messages

### Normal submission confirmation

```text
Thank you. Your request was submitted. The office will review it during working hours. This website is not for emergencies.
```

### High-risk confirmation

```text
Your answers show a possible urgent safety concern. If you are in immediate danger or cannot stay safe, call local emergency services or go to the nearest emergency department now. The office will prioritize review of your request, but online messages may not be monitored 24/7.
```

## Translation review

All clinical text should be reviewed by fluent medical/mental-health translators for:

- Afaan Oromo
- Amharic
- English

Do not rely only on automated translation for clinical consent, suicide-risk, or legal/privacy text.
