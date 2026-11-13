<div align="center">

# Data Access Decision Simulator

Deliverable: Data Access Decision Forms (EduConnect Ghana)

Prepared by: Irimaso Maurice

</div>

---

## Request 1: Marketing Campaign

*Data Access Decision Form*

| | |
|---|---|
| **Requested by** | Sarah Owusu, Marketing Manager (current access: INTERNAL) |
| **Request** | Full student database (names, emails, phone numbers, course enrolments) for a referral campaign starting Friday |
| **Decision** | **DENY** the raw export. **CONDITIONAL APPROVAL** of a platform-based alternative. |
| **Lifecycle stage** | **Use**, plus internal **Share** (data moving from production to the marketing team) |
| **Justification** | • **Classification:** Sarah holds INTERNAL access; emails are CONFIDENTIAL and phone numbers are direct contact PII (treat as CONFIDENTIAL). Urgency does not change her access level.<br>• **Least privilege:** the campaign needs messages delivered, not 50,000 records held by one person.<br>• **s.40 Direct marketing:** prior written consent required (s.40(1)); students may opt out at any time (s.40(2)).<br>• **ss.19, 22, 25 Minimality and purpose:** data collected for course delivery; marketing is further processing needing compatibility or consent; a full export is excessive.<br>• **s.37(1)(a) Minors:** under-18 data is special personal data; exclude unless parental consent exists. |
| **Safeguards (conditional)** | 1. Target only students with a recorded marketing opt-in.<br>2. Send via the email platform/CRM; Sarah builds the campaign but never sees a raw list.<br>3. Planning data limited to aggregated counts (INTERNAL, within her access).<br>4. Exclude under-18s; unsubscribe link in every message; honour opt-outs immediately. |
| **Consult** | Data Protection Supervisor / DPO (s.58), data owner of the student database, Legal if opt-in records are incomplete |
| **Action steps** | 1. Reply to Sarah declining the export, explaining why, and offering the platform route so Friday's launch can proceed.<br>2. Ask the DPO to confirm opt-in status of the student base.<br>3. Configure an opted-in adult segment with only the needed enrolment fields.<br>4. Log the decision in the ticket for audit.<br>5. Flag a policy gap: names combined with enrolments identify individuals, so the INTERNAL rating for names should be reviewed. |

---

## Request 2: Analytics Partnership

*Data Access Decision Form*

| | |
|---|---|
| **Requested by** | David Mensah, Head of Product |
| **Request** | Give DataInsights Inc. (US-based) access to the AWS database to analyse learning patterns; login credentials attached |
| **Decision** | **DENY.** Treat the shared credentials as a security incident. |
| **Lifecycle stage** | **Share**: external, cross-border disclosure to a third party |
| **Legal / compliance red flags** | • **s.28 Security:** credentials given to an outside party and pasted in a ticket; treat as compromised.<br>• **s.30(2)-(3) Processor contract:** a written contract with confidentiality and security terms is required; none reviewed by Legal/DPO.<br>• **s.30(4) Foreign processor:** controller must ensure a non-Ghana processor complies with Ghanaian law; EduConnect stays accountable (s.17(a)).<br>• **ss.47(1)(f)-(g), 55 Registration:** new recipient and transfer country must be notified to the Commission within 14 days.<br>• **s.27(2)(g) Transparency:** students must be told who receives their data.<br>• **ss.19, 25:** full access is excessive; purpose compatibility must be assessed, not assumed.<br>• **ss.37, 62(b):** minors' data is special personal data; Legal to confirm whether pupil-data rules apply.<br>• **s.88:** reckless disclosure of personal data is an offence (fine or up to two years' imprisonment). |
| **Controls if later approved** | 1. Signed data processing agreement: purpose limits, security, no onward sharing, breach notice, audit rights, deletion at contract end.<br>2. Share de-identified or pseudonymised activity logs, not profiles (ss.24(2), 65).<br>3. No production access: scoped extract or read-only replica with approved fields only.<br>4. Named accounts, MFA, IP allow-listing, time-boxed access, full query logging.<br>5. Encryption in transit and at rest; transfer records kept. |
| **Documentation** | DPA contract; privacy impact assessment; updated Commission registration; updated privacy notice; data-sharing record (fields, volume, dates); DPO sign-off |
| **Action steps** | 1. **Immediately** rotate credentials, revoke any access, and remove credentials from the ticket.<br>2. Review logs for DataInsights logins; if access occurred, escalate and notify the Commission and affected students (s.31).<br>3. Tell David the request is on hold pending Legal and DPO review, and why.<br>4. Escalate to DPO, Legal and CISO / security lead.<br>5. Implement all controls before any data moves, if the partnership proceeds. |

---

## Request 3: Archive & Deletion

*Data Access Decision Form*

| | |
|---|---|
| **Requested by** | Comfort Asante, Customer Support Lead, for student James Boateng |
| **Request** | Full deletion of account and data; last course completed 6 months ago; no pending payments |
| **Decision** | **APPROVE**, with limited lawful retention |
| **Lifecycle stage** | **Destroy**; minimal retained records move to **Archive** |
| **Can it be fulfilled?** | Yes, largely. The Act has no "right to be forgotten" by name, but s.33(1)(b) allows destruction of records the controller may no longer keep, s.24(1) bars retention beyond the purpose (now spent), and s.20(2)-(3) lets him object so processing must stop. |
| **Legal obligations** | • **ss.32(1), 35(3):** verify James's identity first.<br>• **s.33(2):** comply or give credible reasons; **s.39(2):** reply in writing within 21 days to a notice to stop processing.<br>• **s.24(6):** delete so data cannot be reconstructed.<br>• **s.33(4):** notify recipients (processors, email and payment tools).<br>• **s.33(5):** confirm to James what was done. |
| **Retention** | See retention table below. |
| **Support process** | 1. Log the request with receipt date; verify identity.<br>2. Confirm with Finance: no open obligations, and which records the law requires.<br>3. Ask James whether to keep his completion record.<br>4. Raise an Engineering deletion ticket: databases, analytics, CRM/email, file storage, marketing lists.<br>5. Backups expire on normal rotation; suppression flag prevents restore.<br>6. Notify processors to delete copies (s.33(4)).<br>7. Archive retained financial records with restricted access and a destruction date.<br>8. Send James written confirmation: deleted, kept, why, how long (s.33(5)).<br>9. Close the ticket with a full audit trail. |

**Retention**

| Data | Retain? | Basis |
|---|---|---|
| Payment / invoice records | Yes, statutory period | Required by law (s.24(1)(a)); Finance/Legal confirm tax period |
| Minimal deletion record (hashed ID) | Yes | Proves compliance, prevents re-contact (s.24(1)(b)) |
| De-identified / aggregated analytics | Yes | No longer personal data (ss.24(5), 65) |
| Completion / certificate record | Only with consent | s.24(1)(d); ask James (employer verification) |
| Profile, contacts, logs, grades, tickets | No: delete | No remaining purpose |
