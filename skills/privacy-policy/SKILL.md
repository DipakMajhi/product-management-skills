---
name: privacy-policy
description: "Draft comprehensive privacy policies for digital products covering GDPR, CCPA/CPRA, COPPA, LGPD, PIPEDA, and Privacy by Design. Generate plain-language policies with lawful basis frameworks, data classification tables, third-party disclosures, and DPA guidance. Use when a PM or founder needs a production-ready privacy policy template. Always recommend legal review."
argument-hint: "Product type (web app/mobile app/SaaS), regions served (US/EU/Global), data collected (email/payment/location/behavior), third-party services, age of users"
---

# Comprehensive Privacy Policy Drafter

You draft expert-level, plain-language privacy policies for digital products across jurisdictions. Always include a disclaimer that the draft requires review by a qualified attorney before publication.

## Regulatory Frameworks Reference

Apply this skill to: $ARGUMENTS

### GDPR (EU/UK/EEA - Applies to all EU residents data)

**Lawful Basis Options (choose applicable ones):**

| Basis | When to Use | Requirements | Examples |
|-------|-----------|--------------|----------|
| Consent | Not mandatory for other bases | Explicit, informed, freely given, withdrawable | Marketing, non-essential cookies, optional analytics |
| Legitimate Interest | Balancing rights with business needs | Balancing test, transparency, non-overriding | Fraud prevention, security, internal operations |
| Contract | Performance of service agreement | User is party to contract | Account creation, service delivery |
| Legal Obligation | Compliance requirement | Statutory requirement exists | Tax records, court orders, regulatory mandates |
| Vital Interest | Protect life or health | Emergency situations only | Medical emergencies, rescue operations |
| Public Task | Government functions | Statutory authority required | Public administration, regulatory compliance |

**Required Data Subject Rights (cannot be waived):**
- Right of access (SAR - copy of personal data within 30 days)
- Right to rectification (correct inaccurate data)
- Right to erasure (right to be forgotten, with exceptions)
- Right to restrict processing (suspend but retain)
- Right to data portability (export in machine-readable format)
- Right to object (opt-out of processing, including marketing)
- Right to explanation (human review of automated decisions)

**Essential GDPR Requirements:**
- Data Processing Agreement (DPA) with all vendors (mandatory for data processors)
- Data Protection Impact Assessment (DPIA) for high-risk processing
- Data Retention Schedule (justify why data held beyond current need)
- Data Protection Officer (DPO) contact if public authority or large-scale systematic monitoring
- 72-hour breach notification requirement to supervisory authority

### CCPA (California) and CPRA (California Privacy Rights Act - effective Jan 1, 2023)

**Categories of Personal Information (define each collected):**
- Identifiers (name, email, phone, device IDs)
- Commercial information (purchase history, product preferences)
- Biometric information (fingerprint, facial recognition)
- Internet activity (browsing history, search history, click behavior)
- Geolocation data (precise or approximate location)
- Sensory information (audio, video recordings)
- Professional information (job title, employer, work history)
- Education information (schooling, degrees)

**Consumer Rights Under CPRA:**
- Right to know (what data collected, used, shared)
- Right to delete (with limited exceptions)
- Right to correct (inaccurate personal information)
- Right to opt-out of sale or sharing (all third-party uses)
- Right to limit use of sensitive data (health, SSN, precise geolocation, etc.)
- Right to non-discrimination (cannot punish users for exercising rights)
- Right to withdraw consent (for marketing)

**Sensitive Data Sub-Categories (stricter rules):**
- Social Security numbers, financial account info
- Precise geolocation (real-time location)
- Racial/ethnic origin, religious beliefs, sexual orientation
- Health, genetic information
- Biometric data for identification

**CPRA Timeline (staggered enforcement):**
- Jan 1, 2023: Consumer rights (know, delete, correct, opt-out)
- Jan 1, 2024: Service provider obligations, automated decision-making rules

### COPPA (Children's Online Privacy Protection Act - applies to children under 13 in US)

**COPPA Requirements (non-negotiable):**
- Verifiable parental consent BEFORE collecting any personal information from children
- Clear, understandable privacy policy written in child-friendly language AND parent-friendly language
- Mechanism for parents to review, delete child's data, and withdraw consent
- Cannot condition service on unnecessary data collection
- Cannot use data for behavioral advertising or profiling
- Must implement reasonable security measures
- Data deletion procedures (purge within reasonable timeframe upon request)

**COPPA "Personal Information" Definition:**
- Name, address, phone, email
- Persistent identifiers (cookie ID, IP address, device ID)
- Information combining identifiers with location, health, or biometric data
- Photos/videos of child

**Exceptions requiring parental consent:**
- Collecting child's name or direct contact info
- Tracking child's location
- Recording child's voice/video
- Any combination of data that identifies the child

### LGPD (Brazil Lei Geral de Protecao de Dados - applies to Brazilian residents)

**Key Differences from GDPR:**
- Broader definition of personal data (includes anonymous data that can identify person)
- 10 legitimate purposes for processing (must pick specific ones; consent is just one)
- Data controller must appoint Data Protection Officer
- Explicit right to automated decision review (human intervention)
- Maximum fine: 2% of annual revenue (up to R$50 million per violation)

### PIPEDA (Personal Information Protection and Electronic Documents Act - applies to Canadian residents)

**10 Fair Information Principles:**
1. Accountability - appoint privacy officer, document procedures
2. Identifying purpose - state purpose before collecting
3. Consent - obtain freely given, informed consent
4. Limiting collection - only necessary information
5. Limiting use - only for identified purposes
6. Accuracy - keep accurate, complete, up-to-date
7. Safeguarding - security measures appropriate to sensitivity
8. Openness - transparent policies and procedures
9. Individual access - right to access personal information
10. Challenging compliance - independent review mechanism

### Australia Privacy Act (applies to Australian residents)

**Australian Privacy Principles (APPs) - 13 principles:**
- Personal data handling standards
- Privacy policies must be clear and accessible
- Consent for collection unless unreasonable to obtain
- Use and disclosure limited to identified purpose
- Data quality and security
- Individual access and correction rights

---

## Data Classification Framework

Create a matrix in your privacy policy showing what data you collect and its classification:

| Data Category | Type | Source | Purpose | Recipient | Retention |
|---------------|------|--------|---------|-----------|-----------|
| Email | PII | User input | Account, marketing | Internal, email vendor | Until deletion |
| Location | Sensitive PII | Device (optional) | Service personalization | Internal only | Session only |
| Payment info | Sensitive PII | Payment form | Transaction processing | Payment processor only | As required by law |
| Usage analytics | Pseudonymous | Automatic tracking | Product improvement | Analytics vendor | 12 months |
| Device ID | Pseudonymous | Browser/app | Session management | Internal, ad partners | 24 months |
| IP address | Pseudonymous | Automatic | Security, fraud prevention | Internal only | 30 days |
| Aggregated behavior | Anonymous | Derived data | Product insights | Public reporting | Indefinite |

**Data Types Explained:**
- PII (Personally Identifiable Information): Name, email, phone, address
- Sensitive PII: Payment info, SSN, health data, biometric data, children's data
- Pseudonymous: Linked to identifier but identifier not disclosed (user ID, device ID)
- Anonymous: Cannot identify individual even with additional data (aggregate statistics)

---

## Third-Party Service Disclosure Template

For each third-party that accesses user data, document:

**Common service categories:**

1. Analytics (Google Analytics, Mixpanel, Amplitude)
   - Data shared: User ID, behavior, events, properties
   - Purpose: Usage tracking, product improvement
   - Jurisdiction: May be US-based (implications for data residency)

2. Payment processing (Stripe, Square, PayPal)
   - Data shared: Payment info, billing address, transaction history
   - Purpose: Payment authorization and fraud prevention
   - Note: Usually PCI DSS certified; you may not retain raw card data

3. Email/Marketing (SendGrid, Mailchimp, Klaviyo)
   - Data shared: Email address, user properties, engagement tracking
   - Purpose: Transactional and marketing communications
   - Compliance: CAN-SPAM (US), GDPR consent, CASL (Canada)

4. Customer support (Zendesk, Intercom, Freshdesk)
   - Data shared: User communication, account info, interaction history
   - Purpose: Support ticket management, customer service
   - Note: Must disclose in data processing agreement

5. Advertising/tracking (Facebook Pixel, Google Ads, TikTok)
   - Data shared: User ID, behavior, conversion events
   - Purpose: Remarketing, audience targeting, conversion tracking
   - Compliance: Requires explicit user consent for tracking (GDPR, CCPA)

6. Hosting/infrastructure (AWS, Google Cloud, Vercel)
   - Data shared: All user data processed
   - Purpose: Technical infrastructure, availability
   - Note: Standard data processing agreement required

---

## Cookie Consent Implementation Guidance

Implement a cookie banner with these categories:

| Category | Required? | Examples | User Control |
|----------|-----------|----------|---------------|
| Strictly Necessary | Yes, no consent needed | Session cookies, CSRF tokens, security cookies | Cannot be disabled |
| Functional | Consent required | Remembering preferences, language settings | Granular consent |
| Analytics | Consent required (GDPR/CCPA) | Google Analytics, Mixpanel, Hotjar | Opt-in or opt-out |
| Advertising/Marketing | Consent required | Pixel tracking, retargeting, email lists | Opt-in required |
| Social Media | Consent required | Social login, sharing widgets | Opt-in required |

**Implementation best practices:**
- Consent management platform (CMP) integration: OneTrust, Termly, CookieBot
- Granular consent per category (not single checkbox)
- Easy opt-out and cookie preference center
- Document consent timestamp and preferences
- Honor DNT (Do Not Track) header where applicable
- Maintain cookie inventory (name, purpose, vendor, duration)

---

## Data Breach Notification Requirements by Jurisdiction

| Jurisdiction | Timeline | Notification to | Threshold | Exceptions |
|--------------|----------|-----------------|-----------|-----------|
| GDPR (EU) | Without undue delay, max 72 hours | Supervisory authority, users if high risk | Any breach of protected data | Anonymous data only |
| CCPA (CA) | "As expeditiously as possible" | Affected residents, state attorney general | Personal information breach | Cannot be practicably determined |
| CPRA (CA) | Same as CCPA plus more obligations | Enhanced notification requirements | Sensitive data gets priority | Encrypted/unusable data |
| US state laws | Varies (30-60 days typical) | Residents, media if large scale | Varies by state | Encrypted, unusable data sometimes |
| Canada PIPEDA | Reasonable timeliness | Privacy Commissioner if reasonable likelihood of harm | PII breach | Minimal harm exception |
| Australia | 30 days if serious/eligible | Individuals, Information Commissioner | Serious invasions of privacy | Low-risk breaches |
| Brazil LGPD | Without undue delay | Authorities, affected individuals | Any data breach | Law enforcement exemptions |

**Breach notification SOP:**
- Implement incident response plan before breach occurs
- Document timeline, scope, and response measures
- Draft notification template with required elements
- Identify who has authority to declare data breach
- Consult legal counsel before public disclosure

---

## Privacy by Design - 7 Foundational Principles

By Ann Cavoukian (revised):

1. **Proactive not Reactive**: Prevent privacy issues before they occur, not respond afterward. Conduct DPIA, security audits, and privacy impact assessments during design phase.

2. **Privacy as Default**: Maximum data protection is default setting. Users should not need to configure anything to get strong privacy. Implement data minimization by design.

3. **Privacy Embedded in Design**: Build privacy into core functionality, not as add-on or afterthought. Technical and organizational measures must be integrated.

4. **Full Functionality**: Achieve all objectives; don't sacrifice privacy to achieve business goals. Find solutions meeting both needs (not false dichotomy).

5. **End-to-End Security**: Protect data from collection through retention to secure deletion. Implement encryption, access controls, audit logs throughout lifecycle.

6. **Visibility and Transparency**: Keep operations visible and transparent to users and stakeholders. Plain language policies, user-facing data dashboards, published security measures.

7. **Respect for User Privacy**: Recognize rights, interests, and expectations of data subjects. Implement easy opt-out, data deletion, consent withdrawal, and user control.

**Implementation checklist:**
- [ ] Conduct Privacy Impact Assessment (PIA) at design phase
- [ ] Data minimization: collect only essential data
- [ ] Pseudonymization and encryption: default techniques
- [ ] Purpose limitation: clearly state data uses
- [ ] Retention: set automatic deletion policies
- [ ] User controls: easy access, correction, deletion, export
- [ ] Access controls: least privilege, audit logging
- [ ] Vendor management: DPAs with all data processors
- [ ] Incident response: documented breach procedures
- [ ] Documentation: privacy assessments, vendor lists, data maps

---

## Complete Privacy Policy Template

```
PRIVACY POLICY

[COMPANY NAME] Privacy Policy
Last Updated: [DATE]
Effective Date: [DATE]

1. INTRODUCTION

[Company Name] ("we," "us," "our," or "Company") operates [product/service description].
This Privacy Policy explains how we collect, use, disclose, and otherwise process your personal
information through our website, mobile application, and related services (collectively, the "Services").

This Privacy Policy applies to all users, including residents of the European Union, California,
Canada, Brazil, and Australia. Depending on your jurisdiction, you may have specific rights
outlined in Section [X].

IMPORTANT: This policy is for informational purposes and does not constitute legal advice.
Consult a qualified attorney in your jurisdiction before publishing.

2. INFORMATION WE COLLECT

We collect information in the following ways:

A. Information You Provide Directly
- Account registration (name, email, password)
- Profile information (bio, photo, preferences)
- Payment information (via secure payment processor; we do not store raw card data)
- Communication information (emails, support tickets, survey responses)
- Content you create (documents, messages, uploaded files)

B. Information Collected Automatically
- Device information (device type, operating system, browser)
- Usage data (features accessed, time spent, clickstream data)
- Location data (IP address; precise location only with explicit permission)
- Cookies and tracking technologies (see Section [X])

C. Information from Third Parties
- Third-party data providers (for fraud prevention, enrichment)
- Payment processors (transaction verification)
- Social platforms (if you sign in via OAuth)
- Marketing partners (audience data, if applicable)

3. LAWFUL BASIS FOR PROCESSING (GDPR/LGPD)

We process your personal information on the following legal bases:

A. Consent
- Marketing communications: [We rely on your express consent]
- Optional cookies (analytics, advertising): [Consent required]
- Biometric data collection: [Consent required]

B. Contract Performance
- Account creation and management
- Service delivery and support
- Payment processing and billing

C. Legitimate Interests
- Fraud prevention and security
- Service improvement and analytics
- Compliance with legal obligations
- Protection of rights, property, safety

D. Legal Obligation
- Tax and accounting records [X years]
- Court orders and legal processes
- Regulatory compliance

E. Public Interest
- [Insert if applicable: e.g., aggregate safety data]

4. HOW WE USE YOUR INFORMATION

We use your information for:
- Account management and authentication
- Service delivery and improvement
- Communications (transactional, support, marketing)
- Analytics and usage tracking
- Fraud prevention and security
- Legal compliance and dispute resolution
- Personalization and recommendations
- Marketing and promotional campaigns (with consent)

5. DATA SHARING AND THIRD PARTIES

We share your information with:

[INSERT FROM TABLE ABOVE - Third-party service categories, vendors, jurisdiction, data type shared]

A. Service Providers
We share data with vendors that process information on our behalf under data processing
agreements (DPAs). These vendors are bound by confidentiality and may not use data for
their own purposes.

B. Legal Compliance
We may disclose information when required by law, court order, or government request.

C. Business Transfer
If we merge, are acquired, or sell assets, your information may be transferred as part
of that transaction.

D. Aggregated/Anonymous Data
We may share aggregated or de-identified data without restriction.

6. COOKIES AND TRACKING TECHNOLOGIES

[INSERT FROM COOKIE TABLE ABOVE]

We use cookies for:
- Session management (strictly necessary)
- Functionality preferences (functional)
- Usage analytics (analytics; consent required)
- Advertising and remarketing (advertising; consent required)

You can control cookies through:
- Browser cookie settings
- Cookie preference center: [LINK]
- Browser privacy settings and extensions
- Opt-out tools: [INSERT LINKS]

7. YOUR PRIVACY RIGHTS AND CHOICES

A. EU/UK/EEA Residents (GDPR)
You have the right to:
- Access: Request a copy of your personal data
- Rectification: Correct inaccurate information
- Erasure: Request deletion (right to be forgotten)
- Restrict: Limit how we use your data
- Data Portability: Export your data in portable format
- Object: Opt-out of processing, including marketing
- Automated Decisions: Human review of automated decisions
- Withdraw Consent: Withdraw consent at any time for processing based on consent

Contact: privacy@[company].com | Data Protection Officer: [NAME/CONTACT]

B. California Residents (CCPA/CPRA)
You have the right to:
- Know: What personal information we collect, use, and share
- Delete: Request deletion of your information (with exceptions)
- Correct: Request correction of inaccurate information
- Opt-Out: Opt-out of sale or sharing of personal information
- Limit: Limit use of sensitive personal information
- Non-Discrimination: We will not discriminate for exercising these rights

To submit a request: [FORM/EMAIL/PHONE]
Verification: We will verify identity before responding

C. Canadian Residents (PIPEDA)
You have the right to:
- Access personal information held about you
- Request correction of inaccurate information
- Understand our privacy practices
- File complaints with Privacy Commissioner of Canada

Contact: privacy@[company].com

D. Brazilian Residents (LGPD)
You have the right to:
- Access your personal data
- Correct incomplete or inaccurate data
- Request deletion (where applicable)
- Data portability
- Opt-out of processing for legitimate interests
- Request human review of automated decisions

Contact Data Protection Officer: [NAME/CONTACT]

E. Australian Residents (Privacy Act)
You have the right to:
- Access personal information about you
- Request correction of information
- Complain to the Office of the Australian Information Commissioner

Contact: privacy@[company].com

8. CHILDREN'S PRIVACY (COPPA - US)

This service is not directed to children under 13. We do not knowingly collect information
from children under 13 without verifiable parental consent.

If we become aware that a child under 13 has provided information without parental consent,
we will delete it promptly and notify the parent.

For children 13-18: [Different consent process if applicable]

Parent Contact: If you believe your child has provided information, contact privacy@[company].com

9. DATA RETENTION

We retain personal information for:
- Account data: Duration of account + [X] years after deletion
- Transaction data: [X] years (legal requirement)
- Marketing data: Until consent withdrawn or email bounces [X] times
- Cookies: See Section [X]
- Usage analytics: [X] months rolling window
- Support/communication: [X] years for business records
- Legal holds: Longer if required by law or litigation hold

10. SECURITY

We implement reasonable technical and organizational measures to protect your information:
- Encryption (TLS for transmission, AES-256 for storage)
- Access controls (principle of least privilege)
- Regular security assessments and penetration testing
- Vendor security requirements (SOC 2, ISO 27001)
- Incident response procedures
- Employee training on data protection

However, no security is absolute. We cannot guarantee complete security.

11. DATA PROCESSING AGREEMENTS (B2B/SaaS)

For customers processing personal data on our platform:
- We execute Data Processing Addendums (DPAs) with all customers
- DPA available at: [LINK]
- Standard terms: [Briefly describe Standard Terms]
- We implement Standard Contractual Clauses (SCCs) for international transfers
- We comply with [Adequacy Decision/Binding Corporate Rules, if applicable]

12. INTERNATIONAL DATA TRANSFERS

We may transfer data internationally. Where required (GDPR, LGPD, PIPEDA):
- We implement Standard Contractual Clauses (SCCs)
- We conduct Transfer Impact Assessments
- We maintain [Adequacy Decisions where applicable]
- We notify you of transfer mechanisms in place

13. DATA PROTECTION OFFICER / PRIVACY CONTACT

Data Protection Officer (if applicable):
[NAME, TITLE, EMAIL]

Privacy Inquiries:
[COMPANY NAME]
[ADDRESS]
privacy@[company].com
[PHONE]

Supervisory Authority (EU): [RELEVANT DPA]

14. CHANGES TO THIS POLICY

We may update this policy. Material changes will be announced:
- Via email to registered users
- Posted on our website with new effective date
- Continued use implies acceptance of updated policy

15. JURISDICTION-SPECIFIC ADDENDUM

[Include jurisdiction-specific requirements for all regions served]
```

---

## Data Processing Agreement (DPA) Guidance for B2B SaaS

If your product processes data on behalf of customers, provide a DPA template including:

**Standard sections:**
- Definitions (Controller, Processor, Sub-processor, Personal Data)
- Scope of processing (data types, duration, categories of data subjects)
- Responsibilities (controller obligations vs. processor obligations)
- Sub-processor management (right to audit, list of approved sub-processors)
- Data subject rights (processor must facilitate user access/deletion requests)
- Security obligations (technical measures, audit rights, certifications)
- Data transfers (SCCs, adequacy decisions, restrictions)
- Return/deletion of data (post-termination data handling)
- Confidentiality (processor staff confidentiality obligations)
- Audit rights (customer right to audit processor compliance)
- Insurance requirements (Cyber liability minimum coverage)
- Liability and indemnification (limits and carve-outs)
- Term and termination (notice periods, data return/deletion timeline)
- Governing law (usually customer's jurisdiction to reduce negotiation)

---

## Customization Checklist

- [ ] Replace all [COMPANY NAME] and [PRODUCT] placeholders
- [ ] Confirm all data categories collected (remove unused sections)
- [ ] Confirm all third-party services and add to disclosure table
- [ ] Set specific retention periods for each data category
- [ ] Confirm applicable jurisdictions (remove non-applicable sections)
- [ ] Set Cookie categories and consent mechanism
- [ ] Add Data Protection Officer contact if required (GDPR threshold: typically 250+ employees or large-scale monitoring)
- [ ] Add Privacy Officer or Privacy contact
- [ ] Set procedures for rights requests (access, deletion, correction, etc.)
- [ ] Include data breach notification procedures
- [ ] If B2B SaaS: Include DPA language and reference DPA template
- [ ] If serving children under 13: Add COPPA-compliant verification mechanism
- [ ] Review all lawful bases and ensure supported by actual practice
- [ ] Verify third-party vendor DPAs are signed and maintained
- [ ] Have qualified attorney review before publishing

---

**DISCLAIMER**

This skill provides informational templates and frameworks for developing a privacy policy. It does not constitute legal advice. Privacy regulations are complex, jurisdiction-specific, and subject to frequent updates. The templates provided are starting points only. You must:

1. Consult a qualified attorney licensed in your jurisdiction(s)
2. Conduct a Privacy Impact Assessment (PIA) specific to your product
3. Review all applicable regulations for your industry and jurisdiction
4. Ensure alignment with actual data practices and security measures
5. Maintain ongoing compliance monitoring as regulations evolve
6. Document all data processing activities and retain records

The user (you) are responsible for compliance with all applicable privacy laws. Using this template without legal review exposes you to regulatory fines, litigation, and reputational harm.
