<div align="center">

# Data Access Decision Simulator

Deliverable: Data Access Decision Forms (EduConnect Ghana)

Prepared by: Irimaso Maurice

</div>

---

<table>
<tr><th colspan="2" align="left">Request 1: Marketing Campaign</th></tr>
<tr><td colspan="2">Data Access Decision Form</td></tr>
<tr><td width="20%"><strong>Requested by</strong></td><td>Sarah Owusu, Marketing Manager (current access: INTERNAL)</td></tr>
<tr><td width="20%"><strong>Request</strong></td><td>Full student database (names, emails, phone numbers, course enrolments) for a referral campaign starting Friday</td></tr>
<tr><td width="20%"><strong>Decision</strong></td><td><strong>DENY</strong> the raw export. <strong>CONDITIONAL APPROVAL</strong> of a platform-based alternative.</td></tr>
<tr><td width="20%"><strong>Lifecycle stage</strong></td><td><strong>Use</strong>, plus internal <strong>Share</strong> (data moving from production to the marketing team)</td></tr>
<tr><td width="20%"><strong>Justification</strong></td><td>• <strong>Classification:</strong> Sarah holds INTERNAL access; emails are CONFIDENTIAL and phone numbers are direct contact PII (treat as CONFIDENTIAL). Urgency does not change her access level.<br>• <strong>Least privilege:</strong> the campaign needs messages delivered, not 50,000 records held by one person.<br>• <strong>s.40 Direct marketing:</strong> prior written consent required (s.40(1)); students may opt out at any time (s.40(2)).<br>• <strong>ss.19, 22, 25 Minimality and purpose:</strong> data collected for course delivery; marketing is further processing needing compatibility or consent; a full export is excessive.<br>• <strong>s.37(1)(a) Minors:</strong> under-18 data is special personal data; exclude unless parental consent exists.</td></tr>
<tr><td width="20%"><strong>Safeguards (conditional)</strong></td><td>1. Target only students with a recorded marketing opt-in.<br>2. Send via the email platform/CRM; Sarah builds the campaign but never sees a raw list.<br>3. Planning data limited to aggregated counts (INTERNAL, within her access).<br>4. Exclude under-18s; unsubscribe link in every message; honour opt-outs immediately.</td></tr>
<tr><td width="20%"><strong>Consult</strong></td><td>Data Protection Supervisor / DPO (s.58), data owner of the student database, Legal if opt-in records are incomplete</td></tr>
<tr><td width="20%"><strong>Action steps</strong></td><td>1. Reply to Sarah declining the export, explaining why, and offering the platform route so Friday's launch can proceed.<br>2. Ask the DPO to confirm opt-in status of the student base.<br>3. Configure an opted-in adult segment with only the needed enrolment fields.<br>4. Log the decision in the ticket for audit.<br>5. Flag a policy gap: names combined with enrolments identify individuals, so the INTERNAL rating for names should be reviewed.</td></tr>
</table>

---

<table>
<tr><th colspan="2" align="left">Request 2: Analytics Partnership</th></tr>
<tr><td colspan="2">Data Access Decision Form</td></tr>
<tr><td width="20%"><strong>Requested by</strong></td><td>David Mensah, Head of Product</td></tr>
<tr><td width="20%"><strong>Request</strong></td><td>Give DataInsights Inc. (US-based) access to the AWS database to analyse learning patterns; login credentials attached</td></tr>
<tr><td width="20%"><strong>Decision</strong></td><td><strong>DENY.</strong> Treat the shared credentials as a security incident.</td></tr>
<tr><td width="20%"><strong>Lifecycle stage</strong></td><td><strong>Share</strong>: external, cross-border disclosure to a third party</td></tr>
<tr><td width="20%"><strong>Legal / compliance red flags</strong></td><td>• <strong>s.28 Security:</strong> credentials given to an outside party and pasted in a ticket; treat as compromised.<br>• <strong>s.30(2)-(3) Processor contract:</strong> a written contract with confidentiality and security terms is required; none reviewed by Legal/DPO.<br>• <strong>s.30(4) Foreign processor:</strong> controller must ensure a non-Ghana processor complies with Ghanaian law; EduConnect stays accountable (s.17(a)).<br>• <strong>ss.47(1)(f)-(g), 55 Registration:</strong> new recipient and transfer country must be notified to the Commission within 14 days.<br>• <strong>s.27(2)(g) Transparency:</strong> students must be told who receives their data.<br>• <strong>ss.19, 25:</strong> full access is excessive; purpose compatibility must be assessed, not assumed.<br>• <strong>ss.37, 62(b):</strong> minors' data is special personal data; Legal to confirm whether pupil-data rules apply.<br>• <strong>s.88:</strong> reckless disclosure of personal data is an offence (fine or up to two years' imprisonment).</td></tr>
<tr><td width="20%"><strong>Controls if later approved</strong></td><td>1. Signed data processing agreement: purpose limits, security, no onward sharing, breach notice, audit rights, deletion at contract end.<br>2. Share de-identified or pseudonymised activity logs, not profiles (ss.24(2), 65).<br>3. No production access: scoped extract or read-only replica with approved fields only.<br>4. Named accounts, MFA, IP allow-listing, time-boxed access, full query logging.<br>5. Encryption in transit and at rest; transfer records kept.</td></tr>
<tr><td width="20%"><strong>Documentation</strong></td><td>DPA contract; privacy impact assessment; updated Commission registration; updated privacy notice; data-sharing record (fields, volume, dates); DPO sign-off</td></tr>
<tr><td width="20%"><strong>Action steps</strong></td><td>1. <strong>Immediately</strong> rotate credentials, revoke any access, and remove credentials from the ticket.<br>2. Review logs for DataInsights logins; if access occurred, escalate and notify the Commission and affected students (s.31).<br>3. Tell David the request is on hold pending Legal and DPO review, and why.<br>4. Escalate to DPO, Legal and CISO / security lead.<br>5. Implement all controls before any data moves, if the partnership proceeds.</td></tr>
</table>

---

<table>
<tr><th colspan="2" align="left">Request 3: Archive & Deletion</th></tr>
<tr><td colspan="2">Data Access Decision Form</td></tr>
<tr><td width="20%"><strong>Requested by</strong></td><td>Comfort Asante, Customer Support Lead, for student James Boateng</td></tr>
<tr><td width="20%"><strong>Request</strong></td><td>Full deletion of account and data; last course completed 6 months ago; no pending payments</td></tr>
<tr><td width="20%"><strong>Decision</strong></td><td><strong>APPROVE</strong>, with limited lawful retention</td></tr>
<tr><td width="20%"><strong>Lifecycle stage</strong></td><td><strong>Destroy</strong>; minimal retained records move to <strong>Archive</strong></td></tr>
<tr><td width="20%"><strong>Can it be fulfilled?</strong></td><td>Yes, largely. The Act has no "right to be forgotten" by name, but s.33(1)(b) allows destruction of records the controller may no longer keep, s.24(1) bars retention beyond the purpose (now spent), and s.20(2)-(3) lets him object so processing must stop.</td></tr>
<tr><td width="20%"><strong>Legal obligations</strong></td><td>• <strong>ss.32(1), 35(3):</strong> verify James's identity first.<br>• <strong>s.33(2):</strong> comply or give credible reasons; <strong>s.39(2):</strong> reply in writing within 21 days to a notice to stop processing.<br>• <strong>s.24(6):</strong> delete so data cannot be reconstructed.<br>• <strong>s.33(4):</strong> notify recipients (processors, email and payment tools).<br>• <strong>s.33(5):</strong> confirm to James what was done.</td></tr>
<tr><td width="20%"><strong>Support process</strong></td><td>1. Log the request with receipt date; verify identity.<br>2. Confirm with Finance: no open obligations, and which records the law requires.<br>3. Ask James whether to keep his completion record.<br>4. Raise an Engineering deletion ticket: databases, analytics, CRM/email, file storage, marketing lists.<br>5. Backups expire on normal rotation; suppression flag prevents restore.<br>6. Notify processors to delete copies (s.33(4)).<br>7. Archive retained financial records with restricted access and a destruction date.<br>8. Send James written confirmation: deleted, kept, why, how long (s.33(5)).<br>9. Close the ticket with a full audit trail.</td></tr>
</table>
