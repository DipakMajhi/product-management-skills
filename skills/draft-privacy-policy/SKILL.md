---
name: draft-privacy-policy
description: "Draft a privacy policy for a digital product. Routes to the privacy-policy skill."
argument-hint: "[describe your product, what personal data it collects, your user base geography, and whether children under 13 may use it]"
---

# Draft Privacy Policy

This skill routes to **privacy-policy**, which provides a complete privacy policy drafting framework covering GDPR, CCPA/CPRA, COPPA, LGPD, PIPEDA, and Privacy by Design principles.

**When to use this:**
- Writing a privacy policy for a new product before launch
- Updating an existing policy to comply with new regulations (GDPR, CCPA, etc.)
- Ensuring your policy covers all the data types your product actually collects
- Preparing a privacy policy for an app store submission (Google Play, Apple App Store)

**Quick jurisdiction guide:**
- Users in EU/EEA → GDPR is mandatory: lawful basis, data subject rights (access, deletion, portability), DPA contact
- Users in California → CCPA/CPRA applies: right to know, right to delete, right to opt-out of sale, Do Not Sell link
- Users under 13 anywhere → COPPA (US) applies: verifiable parental consent required before data collection
- Users in Brazil → LGPD applies (similar to GDPR): lawful basis, data subject rights, DPO appointment
- Users in Canada → PIPEDA applies: meaningful consent, purpose limitation, data accuracy obligations

**What privacy-policy covers:**
- Data inventory framework: what to collect, why, legal basis, retention period, sharing
- GDPR compliance: lawful basis for processing (consent, legitimate interest, contract), data subject rights, DPA contact, international transfers (SCCs)
- CCPA/CPRA compliance: "Do Not Sell or Share My Personal Information" link, categories of data, third-party disclosures
- COPPA compliance: age gate design, verifiable parental consent, limited data collection for minors
- Cookie policy: categories of cookies (necessary, functional, analytics, marketing), consent banner requirements
- Data retention policy: how long each data type is kept and why
- Breach notification: what triggers notification, who is notified (users, regulators), timeline requirements
- Third-party data sharing: categories of recipients, purpose, and legal basis for sharing
- Privacy by Design principles (Ann Cavoukian): proactive vs. reactive, privacy as default, full functionality
- Policy template: plain-language policy sections with jurisdiction-specific clauses

**The skill will:**
1. Ask about data collected, user geography, business model (ads? data sales?), and user age range
2. Identify which regulations apply and what they specifically require
3. Flag any data collection practices that require special handling (sensitive data, children's data)
4. Draft the full privacy policy with jurisdiction-appropriate clauses
5. Add cookie policy section if the product uses cookies
6. Provide a plain-language summary for users

Load the full skill: **privacy-policy**

Apply your product and data context to: $ARGUMENTS
