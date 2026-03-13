# uMSA Competitive Research: Office of the CIO Vendor Agreement Analysis
*Last updated: 2026-03-13 | Status: Research complete — all 6 vendors. Workday content sourced from Universal Main Subscription Agreement (uMSA) US and Canada v26.2 and Universal Amendment to the MSA.*

---

## Purpose
This document provides deep analysis of enterprise agreement structures across the top Office of the CIO (oCIO) vendors — GCP, AWS, Snowflake, Anthropic, OpenAI, and Databricks — to inform the Workday uMSA competitive one-pager. **Workday positioning is based on the actual MSA and Universal Amendment that Workday provides to customers at tier/NDA.** Each section covers agreement structure, liability, data ownership, security, breach notification, IP/indemnification, termination/portability, SLA/uptime, enterprise vs. standard tiers, and key gotchas.

### Workday uMSA — Quick Reference
*Source: Universal Main Subscription Agreement (uMSA) US and Canada v26.2 and Universal Amendment to the MSA. This is the agreement Workday provides to customers at tier/NDA.*

| Dimension | Workday uMSA (contract language) |
|---|---|
| **Agreement type** | Single **Universal Main Subscription Agreement (MSA)** covering all Workday products. Includes Order Form, MSA, Security Exhibit, Data Processing Exhibit (DPE), Business Associate Exhibit (if applicable), and Product Terms. Order Form takes precedence over MSA and exhibits (Cl. 10.14). |
| **Customer Content / Data** | "Customer Content" means electronic data or information submitted to the Service by Customer, its Affiliates or Authorized Parties. **"As between Workday and Customer, Customer owns all right, title and interest to its Customer Content. Workday will have the right to use Customer Content only to provide the Service, subject to this Agreement."** (Cl. 3(a)) |
| **AI / Outputs** | Per Amendment: Workday develops AI Systems in accordance with applicable Law (including EU AI Act). **Customer owns all right, title, and interest in and to any Outputs.** Workday uses Customer Content only to provide the Service — no training of external AI/ML models on Customer Content. Customer may request AI fact sheets. |
| **Liability cap** | **General Cap:** Fees paid or payable in the immediately preceding 12-month period for the Service from which the claim arose. **Enhanced Cap:** For breach of confidentiality, security, or privacy obligations — 24-month fees for that Service (Cl. 8.1). **Caps do NOT apply to:** (A) gross negligence, willful misconduct, or fraud; (B) either party’s indemnification obligations; (C) Customer’s payment obligations; (D) **Workday’s remediation obligations in Clause 8.3** (Cl. 8.1). |
| **Breach remediation (carveout)** | **Clause 8.3 — Workday Remediation Obligations:** If unauthorized disclosure of or access to Personal Data is caused by Workday’s breach of its security, privacy, or data protection obligations, Workday will pay **reasonable and documented costs** for: (a) forensic investigation; (b) notification to government/industry/media (if required by Law) and Affected Individuals; (c) credit monitoring for Affected Individuals who elect it, for **one year**; (d) operating a **call center** for Affected Individuals for **one year**. No responsibility to the extent due to gross negligence, willful misconduct, or fraud by Customer, its Affiliates or their personnel (Cl. 8.3). |
| **Breach notification** | **48 hours (contractual):** "If either party becomes aware of a Security Breach, that party must promptly notify the other party, unless legally prohibited, **within 48 hours or any shorter period required by Law**." Workday will conduct a root cause analysis and, upon request, share results and remediation plan with Customer (Cl. 5.3). |
| **Security & Audit Reports** | Security program conforms to **Security Exhibit** and **Audit Reports**. Through self-service or upon written request, Workday makes available then-current **Audit Reports** for the applicable Service. Audit Reports are Workday Confidential Information. No update may materially decrease protections during the Term (Cl. 5.1; Amendment §5). |
| **Privacy** | Personal Data processed only in accordance with the **Data Processing Exhibit (DPE)**. DPE may be updated to comply with Data Protection Laws; no update may materially decrease Workday’s data processor obligations (Cl. 5.2; Amendment §5). |
| **SLA & Service Credits** | **SLA:** Production support and service level availability per **Product Terms**; no update may materially decrease Workday’s responsibilities during the Order Term. **Service Credits (Cl. 10.13):** If Workday fails to meet Service Availability or Service Response in any rolling six-month period — first Failure: meeting to discuss corrective actions; second: 10% credit; third: 20%; fourth: 30%. Customer must request remedy within **60 days** of the Failure. Credits applied to next invoice or refunded. |
| **Retrieval & portability** | Upon Customer’s written request on or before expiration/termination (including any Transition Period), Workday gives **up to 60 days** at no additional cost solely to retrieve Customer Content. **Customer Content made available for extraction in a machine-readable format** as described in the Documentation. After Retrieval Period, Workday deletes Customer Content (e.g., by deleting Customer’s Instance) subject to legal obligations and backup schedules (Cl. 9.2; Amendment §6). |
| **Transition Period** | If Customer requests before termination, Workday will continue to provide the Service for **up to three months** after termination. Monthly fees: 1/12 of the immediately preceding 12-month fee **plus 5%**. Transition assistance via SOW at then-current rates (Cl. 9.3). |
| **IP indemnification** | Workday defends Customer against third-party Claims that use of the Service as contemplated infringes third-party Intellectual Property Rights and indemnifies for Losses. Carveouts: modification by others, use inconsistent with Documentation or in violation of Agreement, combination with non-Workday products. Remedy options: obtain right to use, replace/modify, or terminate affected Service with refund of prepaid fees (Cl. 7.1). |
| **Product Terms / changes** | Product Terms may be updated; **no update may materially decrease applicable security and privacy commitments**; such changes **not effective until 30 days after publication** of updated Product Terms (MSA def.; Amendment §11). |
| **BAA** | Yes — Business Associate Exhibit if applicable (HIPAA). |

---

## Anthropic

*Research compiled March 2026. Sources: Anthropic Commercial Terms of Service, DPA, Privacy Center, Trust Center, Help Center, third-party legal analysis.*

---

### 1. Agreement Structure

Anthropic's commercial agreement is a multi-document stack. Accepting the Commercial Terms of Service (CToS) automatically incorporates all of the following by reference:

| Document | How Incorporated | Notes |
|---|---|---|
| **Commercial Terms of Service** | Master document | anthropic.com/legal/commercial-terms |
| **Usage Policy** | Incorporated by reference | Sets permissible use boundaries |
| **Data Processing Addendum (DPA)** | Automatically at CToS acceptance | Includes EU SCCs Modules 2 & 3, UK/Swiss addenda |
| **Supported Regions Policy** | Incorporated by reference | |
| **Service Specific Terms** | Incorporated by reference | Model-specific or product-specific terms |
| **Subprocessor List** | Referenced in DPA | Live list at anthropic.com/subprocessors |

**Optional/Add-On Instruments (require sales):**
- **Zero Data Retention (ZDR) Addendum** — applies only to eligible API endpoints, not Claude.ai chat products
- **Business Associate Agreement (BAA)** — HIPAA-eligible Enterprise customers only (not self-serve)
- **Custom Enterprise Agreement** — sales-assisted customers can negotiate custom contracts, pricing, and SLAs

**Contracting entity:** EEA/Switzerland/UK customers contract with Anthropic Ireland, Limited; all others with Anthropic, PBC.

**Product Tier Distinctions:**

| Tier | Training Default | BAA Available | ZDR Available |
|---|---|---|---|
| API (Commercial Terms) | No training | Yes (with ZDR, via sales) | Yes (approval required) |
| Claude Enterprise | No training | Yes (sales-assisted only) | Yes (via API key) |
| Claude for Work (Team) | No training | No | No |
| Claude Pro/Max | Training ON by default | No | No |
| Amazon Bedrock / Vertex AI | No training | Via cloud provider | Via cloud provider |

**Critical gotcha:** Claude Pro and Team are classified as *consumer* accounts. Employees using personal accounts are subject to training by default (as of Sept. 28, 2025).

---

### 2. Liability

**Cap:** Fees paid to Anthropic in the previous 12 months. No minimum floor.

**Excluded damages (mutual):** Consequential, incidental, special, indirect, or exemplary damages including lost profits, business, revenue, goodwill, production, anticipated savings, or data.

**Carveouts — cap does NOT apply to:** Indemnification obligations (IP and third-party claims).

**AI-specific liability shift:** Anthropic contractually requires customers to notify users that outputs "may be false, incomplete, misleading or not reflective of recent events." Hallucination-related downstream harm is fully on the customer.

**Jury trial/class action waiver:** Mutual waivers; disputes go to mandatory arbitration (Dublin for EEA/UK; San Francisco for others).

---

### 3. Data Ownership & Privacy

**Ownership:** "As between the Parties...Anthropic agrees that Customer owns all Outputs, and Anthropic disclaims any rights it receives to Customer Content." Customer owns both inputs and outputs.

**Model Training by Tier:**

| Tier | Default | How to Change |
|---|---|---|
| API / Enterprise | No training | Opt-in via Development Partner Program only |
| Claude.ai Free/Pro/Max | Training ON by default | Opt-out via Privacy Settings |
| Team plan | No training | Opt-in only |

**Feedback exception:** Thumbs-up/down ratings retain the full conversation for up to 5 years for training (de-linked from user ID). Org admins on Team/Enterprise can disable this.

**Safety classifier exception:** Even ZDR customers have safety classifier results retained — non-negotiable.

**Data retention (commercial):** Conversations not retained beyond processing for API/Enterprise. DPA requires deletion within 30 days of termination.

**Subprocessors:** 15 days' advance notice of new subprocessors; customers may object.

---

### 4. Security Commitments

| Certification | Scope |
|---|---|
| SOC 2 Type II | Commercial products (API, Claude Enterprise) |
| ISO 27001:2022 | Commercial products |
| ISO/IEC 42001:2023 | AI Management Systems (industry-first) |
| CSA STAR Level 2 | Commercial products |
| HIPAA-Ready | Requires BAA + specific configuration |

*Consumer products (Free/Pro/Max) are NOT covered by these certifications.*

**Contractual controls (DPA):** AES-256 encryption at rest, TLS 1.2+ in transit, MFA, RBAC, annual third-party pen tests, annual audits. Customers may audit annually (customer bears cost unless triggered by breach).

---

### 5. Breach Notification

**DPA commitment:** 48 hours after discovering a breach affecting Customer Personal Data.

**Real-world gap (GTG-1002 incident, Sept.–Nov. 2025):** Nation-state breach detected mid-September 2025, customers likely notified within ~10 days, but public disclosure not until November 13 — ~2 months after detection. No breach remediation cost coverage in standard terms.

---

### 6. IP / Indemnification

**Anthropic's IP indemnification (effective Jan. 1, 2024):** Defends customers against third-party claims that authorized use of the Services or their Outputs infringes IP rights.

**Exclusions:** Customer modifications, combinations with non-Anthropic tech where the combination is the source, customer-provided infringing inputs, trademark violations, unauthorized use, free/non-paying users.

**Bartz v. Anthropic copyright settlement (2025):** $1.5B settlement for ~500K pirated books used in training. Settlement does NOT release claims for *infringing outputs* — Claude reproducing copyrighted text verbatim remains independently actionable.

**No hallucination indemnity:** Zero indemnification for downstream harm from inaccurate AI outputs.

---

### 7. Termination & Portability

**Termination:** Either party may terminate for convenience (30 days' notice from Anthropic); either party for material breach (30-day cure).

**Immediate suspension rights:** Anthropic may suspend with no minimum notice for policy violations, legal prohibition, or third-party vendor termination — business continuity risk.

**Data after termination:** DPA requires return or deletion of Customer Personal Data within 30 days. **No structured data export mechanism in standard terms** — no specified format, no transition period.

---

### 8. SLA / Uptime

**Standard API:** No SLA. Services provided "AS IS" and "AS AVAILABLE." No service credit mechanism.

**Priority Tier:** Targets 99.5% uptime — "target" language only, not a binding SLA with automatic credits.

**Enterprise:** Negotiable SLAs for sales-assisted custom contracts. Self-serve Enterprise has no SLA.

**No standard service credit regime.** Unlike AWS/Azure/GCP, there is no published credit schedule.

---

### 9. Enterprise vs. API Terms

| Dimension | API (Commercial) | Claude Enterprise (Sales) |
|---|---|---|
| Contract | Standard CToS (click-through) | Custom contract + CToS baseline |
| Pricing | Token-based (usage only) | Per-seat + usage |
| Training prohibition | Automatic | Automatic |
| ZDR | Available (approval required) | Available |
| BAA/HIPAA | Available (sales only) | Available (sales only; legacy BAAs pre-Dec 2025 must be renegotiated) |
| SSO/SCIM | Not included | Included |
| Audit logs | Not included | Included |
| SLA | None (Priority: target 99.5%) | Negotiable |
| Context window | Model-standard | 500K tokens (Sonnet 4.6 chat), 1M (Claude Code) |

---

### 10. Key Gotchas

1. **No default SLA** — dramatic gap vs. traditional enterprise SaaS
2. **Liability cap tied to trailing fees** — low for early deployments; no minimum floor
3. **Immediate suspension without notice** — business continuity risk for production deployments
4. **No data portability mechanism** — no structured export format on termination
5. **Training data indemnification gap** — Bartz settlement didn't release output-infringement claims
6. **Safety classifier retention survives ZDR** — not truly zero data
7. **Hallucination risk fully shifted to customer** — no accuracy warranty
8. **Competing use prohibition** — can't use Services to train competing AI models; broader than typical SaaS
9. **Consumer-grade plans misused by enterprises** — Pro/Team = consumer accounts, training ON by default since Sept. 2025
10. **Legacy BAA invalidation** — pre-Dec 2, 2025 BAAs don't extend to Claude.ai Enterprise
11. **Model deprecation without contractual protection** — no notice commitment in standard terms

---

## Databricks

*Research compiled March 2026. Sources: MCSA (v3.2, GSA-approved Apr. 2023), Platform Services Schedule, Security Addendum, DPA (July 2023), Service Specific Terms.*

---

### 1. Agreement Structure

| Document | Role |
|---|---|
| **Master Cloud Services Agreement (MCSA)** | Governing framework; all general terms, liability, confidentiality |
| **Platform Services Schedule (Multi-Cloud)** | SLA, workspace terms, availability commitments for AWS/GCP |
| **Service Specific Terms** | Per-product terms (GenAI, Mosaic AI, Delta Sharing, etc.) |
| **Order Form** | Commercial terms, quantities, pricing |
| **Security Addendum** | Contractually committed security controls, certifications, breach notification |
| **Data Processing Addendum (DPA)** | GDPR/CCPA processor obligations, SCCs, subprocessor rights |
| **External Use Schedule** | Terms for customer-built apps that expose Databricks to end users |
| **US Public Sector Services Schedule** | FedRAMP-specific terms |
| **Private Cloud Schedule** | Single-tenant/VPC deployment terms |
| **BAA** | Required separately for HIPAA/PHI workloads |

**Precedence:** (1) Order Form, (2) Service Specific Terms, (3) MCSA. Changes to MCSA for pay-as-you-go customers are unilateral; continued use = consent.

---

### 2. Liability

**General Cap (1x):** Total fees paid in the 12 months preceding the first incident.

**Data Breach Super Cap (2x) — Notable:** For claims from unauthorized disclosure of Customer Content resulting from Databricks' breach of confidentiality, security, or data protection obligations: **2x fees paid in prior 12 months**. This elevated multiplier is a meaningful departure from standard SaaS (which typically cap breach liability at the same 1x or less).

**Cap interaction:** General Cap and Super Cap are non-cumulative. Maximum for all claims = the Super Cap.

**Consequential damages exclusion:** Explicitly includes "loss or corruption of data" — Databricks accepts no liability for data loss beyond the General Cap even from its own negligence.

**Uncapped claims:** IP indemnification; GenAI Claims liability (explicitly stated as NOT subject to any damages cap — unusual); death/personal injury (jurisdiction-dependent).

**Insurance:** Databricks contractually commits to maintaining cyber liability insurance rated A-IX or better.

---

### 3. Data Ownership & Privacy

**Customer owns data:** "Customer retains all right, title and interest in and to the Customer Content and Customer Materials." Includes Inputs and Outputs.

**Model training prohibition (hard):** "Databricks shall not use Customer Content, Inputs, or Outputs to train, re-train, or fine-tune GenAI Models that Databricks makes available for use by third parties." Hard prohibition.

**Usage Data rights:** Databricks may collect aggregated/anonymized metadata about platform use to improve products. Cannot share with third parties unless fully anonymized.

**DPA:** Customer = data controller; Databricks = data processor. Incorporates 2021 EU SCCs. Subprocessor list at databricks.com/subprocessors — email subscription required to receive change notifications.

---

### 4. Security Commitments

**Security program:** NIST 800-53 + ISO 27001 frameworks; annual third-party pen tests; public bug bounty program.

| Certification | Status |
|---|---|
| SOC 2 Type II | Ongoing |
| ISO 27001 / 27017 / 27018 / 27701 | Certified |
| FedRAMP Moderate | Authorized (AWS, 2022) |
| FedRAMP High | Agency ATO on AWS GovCloud (~Mar. 2025) |
| HITRUST CSF | Certified for Azure Databricks |
| HIPAA | Via BAA + Compliance Security Profile |
| PCI-DSS | Supported in PCI Permitted Workspaces (limitations apply) |

**Vulnerability remediation SLAs (contractual):**
- Critical: 14 days
- High: 30 days
- Medium: 60 days

**Compliance Security Profile:** Required for PHI, PCI, and FedRAMP workloads — an enhanced security configuration mode. Preview features excluded.

---

### 5. Breach Notification

**Timeline:** 3 business days after becoming aware of a confirmed Security Breach.

**GDPR gap:** 3 business days ≠ 72 calendar hours. A Thursday breach may not be reported until the following Wednesday — potentially beyond the GDPR 72-hour supervisory authority clock. Enterprise customers should negotiate calendar-day notification.

**Remediation:** The 2x Super Cap is the primary financial remedy. No specific remediation fund or breach expense coverage beyond that.

---

### 6. IP / Indemnification

**Databricks indemnifies** against third-party claims that the Platform Services infringe IP rights. Coverage is uncapped (excluded from general liability cap).

**Carve-outs:** Open-source Apache Spark layer; combinations with non-Databricks equipment/software; use outside documentation.

**GenAI IP Indemnity:** Separate indemnity for claims that AI Outputs infringe third-party IP. Uncapped. Stated as the "sole and exclusive remedy" for AI output IP claims.

---

### 7. Termination & Portability

**Termination:** 30 days' written notice (no active orders); either party for material breach (30-day cure).

**Data deletion:** All Customer Content in a Workspace deleted within **30 days** of workspace cancellation. No guaranteed post-termination read-only period. Customers must export before cancellation.

**Portability strength:** Databricks is built on **Delta Lake** (Apache-licensed open format) — data is inherently portable and readable without Databricks software. Strongest portability story of all vendors reviewed.

---

### 8. SLA / Uptime

**AWS & GCP:** 99.9% monthly uptime SLA.
**Azure Databricks:** 99.95% (governed by Microsoft Azure SLA).

| Monthly Uptime | Credit |
|---|---|
| 99.0% – 99.9% | 10% of monthly fees |
| Below 99.0% | 25% of monthly fees |

Credits applied within 45 days of verification. Sole and exclusive remedy for uptime failures.

**SLA does not apply to:** Azure Databricks (covered by Azure SLA), "Databricks Powered Services."

**SLA is measured in aggregate** across all workspaces in the customer account — individual workspace outages may not trigger credits.

---

### 9. Enterprise vs. Standard Terms

**Pay-as-you-go:** Databricks may unilaterally modify MCSA and pricing; continued use = consent. No negotiated liability or SLA terms.

**Enterprise (Order Form):** Pricing locked for term; 2x Super Cap; uncapped IP indemnification; Security Addendum contractually binding with vuln remediation SLAs; BAA available; FedRAMP via US Public Sector Schedule.

---

### 10. Key Gotchas

1. **PHI/PCI hard stop without configuration** — processing PHI outside designated workspaces: Databricks disclaims all liability. Metadata fields (workspace names, tags, job names) are outside the compliance boundary.
2. **Data loss explicitly excluded from consequential damages** — for a data platform, this is notable
3. **30-day data deletion with no post-termination read access** — no grace period
4. **Unilateral MCSA modifications for PayGo** — no protection against changes
5. **Apache Spark open-source carveout** — IP claims against Spark itself leave customers exposed
6. **Aggregate SLA measurement** — single critical workspace can be down without triggering credits
7. **3 business days breach notification vs. GDPR 72-hour calendar clock**
8. **No published renewal price protection** — discounts decrease year over year at renewal
9. **Subprocessor notification is subscription-based** — customers who miss signup aren't proactively notified

---

## GCP (Google Cloud Platform)

*Research compiled March 2026. Sources: Google Cloud Terms of Service, Cloud Data Processing Addendum (CDPA), Service Specific Terms, legal change log, third-party procurement analysis.*

---

### 1. Agreement Structure

| Layer | Document |
|---|---|
| Master | Google Cloud Terms of Service (cloud.google.com/terms) |
| Data | Cloud Data Processing Addendum (CDPA) — auto-incorporated |
| Service | Service Specific Terms (SST) — per-product |
| Use | Acceptable Use Policy (AUP) |
| Compliance | HIPAA BAA (separately executed) |
| Compliance | Standard Contractual Clauses (SCCs) — via CDPA Appendix 3 |
| Security | Appendix 2 (Security Measures) — referenced in CDPA |

**Precedence:** SST > ToS; CDPA Appendix 3 > CDPA general terms. Enterprise agreements replace or amend the standard ToS via a separately executed Master Agreement.

**Self-amending:** Google can change the ToS unilaterally with **30 days' notice**; continued use = consent. 90 days' notice required for adverse SLA changes.

**Pre-GA gap:** Any service labeled Preview/Alpha/Beta has: no SLA, no indemnification, no DPA, $25K liability cap, may be discontinued at any time. Google has a history of keeping products in Preview for 1–2 years.

---

### 2. Liability

**Cap:** 12-month trailing fees. No floor for standard services. Free services capped at $5,000.

**Special cases:** Pre-GA services: lesser of 12-month cap or $25K. Google-Managed Multi-Cloud: greater of 12-month fees or $25K.

**Consequential damages exclusion:** No indirect, consequential, special, incidental, or punitive damages; no lost revenues, profits, savings, or goodwill.

**Uncapped carve-outs:** Fraud/fraudulent misrepresentation; indemnification obligations; IP rights infringement; payment obligations; matters where liability cannot be excluded by law (death/personal injury).

**Critical gap:** No carve-out for gross negligence or willful misconduct — the damage cap applies even to catastrophic Google-caused failures.

---

### 3. Data Ownership & Privacy

**Ownership:** "Customer retains all Intellectual Property Rights in Customer Data and Customer Applications."

**Use restriction:** "Google will only access or use Customer Data to provide the Services...and will not use it for any other Google products, services, or advertising."

**AI/ML training ambiguity:** Cloud ToS/CDPA do not explicitly prohibit Google from using Customer Data to train AI/ML models. The instruction-following framework limits processing to stated purposes, but the Privacy Notice notes Google may use "algorithms to recognize patterns in Service Data" for service improvement. Explicit prohibition requires separate negotiation.

**Prompt logging exception:** Section 4.3 — Google may log customer prompts when automated safety tools detect potential AUP violations. No opt-out.

**Region controls:** Data at rest stored only in selected Region/Multi-Region (for listed services). Does not cover resource identifiers, labels, or metadata.

**Reseller exception:** If accessing via a Google Cloud reseller, Section 5.2 data protection obligations may not apply directly — a significant and easily overlooked gap.

---

### 4. Security Commitments

**Contractually committed (CDPA Section 7.1.1):** Encryption of Customer Data; ongoing CIA + resilience; regular testing; restricting access to what is "strictly necessary."

**Contractually committed certifications (CDPA Section 7.4 — binding obligation):**
- ISO 27001 and additional certifications per Appendix 4
- SOC 2 and SOC 3 reports, updated annually

If Google loses ISO 27001 or fails to produce annual SOC reports, it is in breach of the CDPA.

**Also maintained (not contractually guaranteed in ToS):** SOC 1 Type II, ISO 27017/27018, PCI DSS Level 1, FedRAMP Moderate/High (via Assured Workloads), HIPAA (via BAA), HITRUST CSF, CSA STAR Level 2.

**Unilateral security updates:** Google may update security measures provided the update does "not result in a material reduction of the security of the Services" — Google's determination.

**Customer pre-accepts Google's security level (CDPA 7.3.2):** By accepting the agreement, customers contractually concede Google's security is adequate — potentially limiting negligence claims.

---

### 5. Breach Notification

**Timeline:** "Promptly and without undue delay" — **no specific hours or days specified.** Notification runs to the customer only (not regulators). The GDPR 72-hour supervisory authority clock runs separately from the customer.

**Content required:** Nature of incident, customer resources impacted, measures taken/planned, recommended customer mitigation steps, contact point.

**Remediation:** None contractually specified beyond "reasonable steps to minimize harm." No forensic investigation obligation, no defined remediation timeline, no credit monitoring commitment.

---

### 6. IP / Indemnification

**Google indemnifies customer** for Third-Party Legal Proceedings alleging that use of Google's technology or Brand Features infringes third-party IP rights.

**Generative AI indemnification (2023 expansion — market differentiating):**
1. **Generated output indemnity** — covers IP claims for content generated via Google's AI products (provided customer didn't intentionally create infringing output and used responsible AI tools)
2. **Training data indemnity** — covers allegations that Google's use of training data to build its models infringes third-party IP

**Customer indemnifies Google** for Customer Applications, Customer Data, Customer Brand Features, and AUP/usage violations.

**Google's IP remedy options (at its discretion):** Procure a license, modify the service, replace it, or **terminate the service and refund prepaid fees** — meaning IP risk can result in service loss with only a refund.

---

### 7. Termination & Portability

**Termination:** Customer may terminate for convenience at any time; Google with 30 days' notice; either party for material breach (30-day cure); Google for inactivity (30 days' notice after 60 days of no activity/fees).

**Non-cancellable fees:** "Customer's obligation to pay all Fees is non-cancellable." Credits only (no cash) for billing errors.

**Data on termination:** 30-day recovery window from Term end; Google deletes all Customer Data within a maximum of **180 days** after the recovery window.

**Free egress program (Cloud Exit):** Customers migrating all workloads off GCP get free data transfer for 30+ supported services. Requires Exit Notice form submission and 30-day initiation window.

---

### 8. SLA / Uptime

GCP has **per-service SLAs** — no single platform-wide guarantee.

| Service | Monthly Uptime |
|---|---|
| Compute Engine (single zone) | 99.95% |
| Compute Engine (multi-zone + LB Premium) | 99.99% |
| BigQuery | 99.99% |
| Cloud Storage (Standard) | 99.9% |
| Cloud Spanner (multi-region) | 99.999% |
| Cloud Run | 99.95% |

**Compute Engine credit tiers (single instance):**
- 95.0–99.95%: 10% credit
- 90.0–95.0%: 25% credit
- <90.0%: 100% credit

**SLA mechanics:** Credits are sole remedy. Customer must file a claim within **60 days** with log files. Credits capped at monthly charge for affected service in affected region. Pre-GA services: zero SLA coverage.

---

### 9. Enterprise vs. Standard Terms

| Dimension | Standard | Enterprise (Negotiated) |
|---|---|---|
| Pricing | List price | 20–40% discounts; spend commitments |
| Liability cap | 12 months fees | Negotiable fixed dollar amount |
| SLA | Standard per-service | Higher uptime; stronger remedies negotiable |
| Data residency | Standard region controls | Assured Workloads + VPC Service Controls |
| Termination assistance | Not included | Negotiable |
| Price escalation at renewal | Revert to list price immediately | Negotiate cap or transition period |

**Post-discount cliff:** When committed term expires, all enterprise discounts revert to list prices immediately — potential 25–35% cost increase overnight. Should be negotiated out.

---

### 10. Key Gotchas

1. **No floor on liability cap for standard services** — catastrophic breach in month one = near-zero cap
2. **No carve-out for gross negligence or willful misconduct** — damage cap applies to everything
3. **Data breach remediation entirely uncovered** — no forensic obligation, no notification cost coverage, no regulatory penalty coverage
4. **Vague breach notification** — "promptly and without undue delay" with no hours standard
5. **Pre-GA services have no contractual protections** — no SLA, no indemnification, no DPA
6. **Unilateral service modification with 30 days' notice**
7. **Post-discount cliff at contract expiration** — no grace period, no price-match obligation
8. **Non-cancellable fees** — payment obligation persists even if Google changes service materially
9. **Credits-only SLA remedy with 60-day claim window**
10. **Reseller customers lose direct data protection rights**
11. **Customer pre-accepts Google's security as "appropriate"** — CDPA 7.3.2 limits negligence claims
12. **AI/ML training prohibition not explicit** — must be separately negotiated

---

## OpenAI

*Research compiled March 2026. Sources: Services Agreement (effective Jan. 1, 2026, superseding May 31, 2025 version), Business Terms, DPA, Service-Specific Terms.*

---

### 1. Agreement Structure

**Document hierarchy (higher = controls in conflict):**
1. **Order Form** — customer-negotiated commercial terms
2. **Service-Specific Terms** — product-level terms (ChatGPT Enterprise, API, ChatGPT Team)
3. **Services Agreement** — master commercial framework (does not apply to individual/consumer use)
4. **OpenAI Policies** — AUP, Usage Policies; incorporated by reference as contract terms
5. **Data Processing Addendum (DPA)** — auto-activated when processing personal data
6. **Business Associate Agreement (BAA)** — optional, separately executed; HIPAA use cases

**Contracting entity:** US customers → OpenAI OpCo, LLC; EEA/Switzerland (DPA purposes) → OpenAI Ireland Ltd.

**Key change in May 2025 Services Agreement:** Training restriction moved from policy language to contractual default. Security Measures now defined as contractual exhibit. Geographic restriction clause added. Suspension grounds codified including "Security Emergencies." Price-change notice reduced to 14 days.

---

### 2. Liability

**Cap:** Mutual 12-month trailing fee cap. For early/low-spend deployments, this can be very low.

**Excluded from cap (carve-outs):** Gross negligence or willful misconduct; indemnification obligations; customer payment obligations; **IP/Copyright Shield indemnity is explicitly uncapped** and cannot be materially reduced without customer's written agreement.

**Consequential damages waiver:** Services provided "as is." Exclusions apply except for gross negligence, willful misconduct, security breaches, confidentiality breaches, and indemnification obligations.

**AI-specific disclaimer:** "Customer must not rely on output as a sole source of truth or factual information, or as a substitute for professional advice." Customer bears full evaluation burden for output quality.

---

### 3. Data Ownership & Privacy

**Ownership:** "Customer retains all ownership rights in Input" and "owns all Output." OpenAI assigns to Customer all of OpenAI's right, title, and interest in Output.

**Output uniqueness caveat:** "Output may not be unique, and other users may receive similar content from OpenAI's services." Ownership doesn't guarantee exclusivity.

**Training (contractual default as of May 2025):** No training for ChatGPT Enterprise, Business/Team, Edu, Healthcare, and API Platform. Customers can opt in voluntarily.

**Zero Data Retention (ZDR):** Available on API for qualifying orgs. Data deleted after inference; not reviewed by humans. Not all endpoints are ZDR-eligible (e.g., Web Search is not).

**Data residency:** Available in US, EU, UK, Canada, Japan, South Korea, Singapore, India, Australia, UAE. EU residency: data at rest in Europe, but inference still runs on US infrastructure by default (in-region GPU inference available only to select Enterprise/Edu/Healthcare customers). Cannot be set on existing projects.

**Enterprise Key Management (EKM/BYOK):** Available for Enterprise/Edu with named account rep. Supports AWS KMS, GCP KMS, Azure Key Vault. OpenAI never sees customer KEKs.

**Retention on termination:** Customer Content deleted within **30 days** of termination.

---

### 4. Security Commitments

| Certification | Coverage |
|---|---|
| SOC 2 Type II | API, ChatGPT Enterprise, Edu, Team (Jan–Jun 2025 period) |
| ISO/IEC 27001:2022 | API, ChatGPT Enterprise, Edu |
| ISO/IEC 27701:2019 | Privacy Information Management |
| ISO/IEC 27017:2015 | Cloud security controls |
| ISO/IEC 27018:2019 | PII in public clouds |

**Audit rights:** DPA permits customer audits no more than once per year; minimally disruptive to OpenAI. In practice, OpenAI satisfies via SOC 2/ISO reports.

---

### 5. Breach Notification

**DPA:** "Without undue delay after becoming aware of any Personal Data Breach." No specific hours specified.

**Real-world gap (Mixpanel incident, Nov. 2025):** Mixpanel identified unauthorized access Nov. 9; shared dataset with OpenAI Nov. 25; OpenAI disclosed Nov. 26 — 16-day lag from incident to notification.

**Remediation:** No contractual commitment to cover remediation costs, credit monitoring, or breach-related customer expenses.

---

### 6. IP / Indemnification

**IP indemnification:** OpenAI defends against claims that the Services or customer's use/distribution of Output infringes third-party IP rights (this is the "Copyright Shield" extension covering outputs).

**Copyright Shield carve-outs:** Claims from combination with third-party products not provided by OpenAI; modification of Services by others; **Customer Content** (customer-provided inputs); **Customer Applications** (apps built on top). Practically: if customer's prompt was the proximate cause of infringing output, the carve-out may apply.

**Copyright Shield is UNCAPPED:** "The Service-Specific Terms Indemnity is not subject to any liability cap, and OpenAI may not materially reduce Customer's protections under the Service-Specific Terms Indemnity without Customer's written agreement." Major customer-favorable differentiator.

**Competitive use restriction:** Customers cannot use outputs to develop AI models that compete with OpenAI's services — an AI-specific restriction with no analog in traditional SaaS.

---

### 7. Termination & Portability

**Termination:** Either party for material breach (30-day cure); insolvency (immediate).

**Suspension (without termination):** OpenAI may suspend for Security Emergencies, Policy violations, geographic/trade control violations. No minimum notice period.

**Data deletion post-termination:** All Customer Content deleted within **30 days**. Subprocessors directed to delete within **30 days**.

**Data export:** No contractual right to export in a specific format in standard terms. Enterprise customers should negotiate export rights (structured format, timeframe) in the Order Form.

**Dispute resolution:** 60-day informal negotiation → binding arbitration (NAM, San Francisco). Governing law: California.

---

### 8. SLA / Uptime

**Standard terms:** No SLA. Zero uptime guarantee. No service credits.

**Priority Processing (Enterprise API add-on):** 99.9% monthly uptime SLA + predictably low latency. Premium pricing.

**Scale Tier (API):** 99.9% uptime SLA with reserved capacity.

**ChatGPT Enterprise:** No publicly documented SLA in standard terms. Negotiable in sales-managed agreements (typically 10–50% of monthly fees as credits).

**Model changes not covered:** No SLA covers model behavior changes, deprecations, or capability regressions. No version pinning by default. Token prices can change with only **14 days' notice** on the Pricing Page.

---

### 9. Enterprise vs. API vs. ChatGPT Team

| Dimension | ChatGPT Enterprise | API Platform | ChatGPT Team |
|---|---|---|---|
| Min. seats | ~150 | N/A | 2 |
| Training default | No (contractual) | No (contractual) | No (contractual) |
| BAA | Yes (sales only) | Yes (email baa@openai.com; ZDR endpoints) | No |
| ZDR | Configurable | Yes (eligible endpoints) | No |
| Data residency | EU/US/others (new workspaces) | EU/US/others (new projects) | US only |
| EKM/BYOK | Yes (named account rep) | No | No |
| SLA | Negotiable | 99.9% (Priority/Scale Tier only) | None |
| SSO/SAML | Yes | N/A | No |
| Copyright Shield | Yes (uncapped) | Yes (uncapped) | Not clearly documented |
| Pricing | ~$60–100/user/mo | Usage-based | $25–30/user/mo |

---

### 10. Key Gotchas

1. **"As Is" AI output disclaimer** — no warranty that outputs are accurate, complete, or fit for purpose
2. **No default SLA** — zero uptime guarantee; SLA only on paid add-on tiers
3. **Training prohibition is now contractual (post-May 2025)** — was previously policy-only; verify Order Form reflects this
4. **Liability cap tied to trailing fees** — very low for early/low-spend deployments
5. **14-day pricing change notice** — no rate lock by default
6. **Model changes without notice** — no advance notice obligation; no version pinning by default
7. **Competitive use restriction on outputs** — cannot use to train competing AI models
8. **Copyright Shield carve-outs are narrow** — customer content/applications exclusions leave gaps
9. **Breach notification: "without undue delay" with no hours standard**
10. **End-user privity gap** — end-customers have zero enforceable rights against OpenAI; enterprises absorb all downstream liability
11. **California mandatory arbitration** — no jurisdiction flexibility

---

## Snowflake

*Research compiled March 2026. Sources: Snowflake Terms of Service (archived 2024-08-01), Customer Data Processing Addendum, Security Addendum (2020-11-09), Support Policy & SLA, Provider/Consumer Terms (2024-05-31).*

---

### 1. Agreement Structure

| Document | Governs |
|---|---|
| **Terms of Service (ToS)** | Master agreement |
| **Data Processing Addendum (DPA)** | GDPR/CCPA obligations |
| **Security Addendum** | Security controls, audit rights, certifications |
| **Acceptable Use Policy (AUP)** | Prohibited uses, suspension triggers |
| **Support Policy & SLA** | Uptime targets, support tiers, credits |
| **Offering-Specific Terms** | Supplemental terms for specific products |
| **Order Form** | Commercial terms, subscription period, edition |
| **BAA** | HIPAA (Business Critical+ only) |
| **Vendor Data Protection Addendum** | Governs Snowflake's subprocessors (last updated Mar. 10, 2025) |

**Critical — unilateral mid-contract URL updates:** The DPA, Security Addendum, Support Policy, AUP, and Offering-Specific Terms are incorporated by URL reference. The ToS explicitly states these include "any updates made thereto, as posted to snowflake.com/legal." Snowflake can change security standards, data processing obligations, and SLA structure during the term without customer consent.

---

### 2. Liability

**General Cap (1x):** Total fees paid or payable in prior 12 months under the applicable Order Form(s).

**Data Protection Claims Cap (2x):** For claims involving breaches of data privacy, security, confidentiality, BAA obligations, or Use Obligations resulting in unauthorized disclosure: **2x amounts paid in prior 12 months**.

**Non-cumulative:** Caps don't stack. Maximum for all claims = the higher cap (2x) regardless of claim type.

**Cross-affiliate aggregation:** Caps aggregated across the base agreement AND any separate agreements governing Customer Affiliates' use of Snowflake — prevents enterprises from treating each affiliate relationship as a separate liability bucket.

**Excluded claims (uncapped):** Breaches of the Confidentiality section (excluding Customer Data obligations); express indemnification obligations; liability that cannot be limited by law.

**Consequential damages waiver:** No loss of use, lost/inaccurate data, interruption of business, costs of delay, lost profits, or indirect/special/incidental/punitive/exemplary/consequential damages.

**HIPAA liability carve-out:** Without a BAA, Snowflake disclaims all liability for HIPAA Data regardless of any other agreement term.

---

### 3. Data Ownership & Privacy

**Customer owns data:** "Customer or its licensors retain all right, title and interest in and to the Customer Data."

**Snowflake's permitted use:** Limited license to process Customer Data solely to provide the Offerings, prevent technical problems, or as required by law.

**Usage Data (notable carve-out):** Snowflake collects and uses Usage Data (operations data, query logs, metadata) for product development and improvement. Customers receive no compensation and there is no opt-out in standard terms.

**Customer's responsibility:** Solely responsible for accuracy, content, and legality of all Customer Data. Warrants sufficient rights to grant processing.

**Region controls:** Customers choose region at account creation. Data remains in the selected region unless customer configures cross-region replication. DPA incorporates 2021 EU SCCs for transfers.

---

### 4. Security Commitments

| Certification | Edition |
|---|---|
| SOC 1 & SOC 2 Type II | All commercial editions |
| ISO 27001:2022 / 27017 / 27018 | All commercial editions |
| HIPAA / HITRUST CSF | Business Critical and VPS only |
| PCI DSS / FedRAMP / ITAR / IRAP | Business Critical and VPS only (specific regions) |

**Security Addendum:** Contractually binding (incorporated by reference). Commitments include penetration testing, access controls, encryption. However, it is a URL-referenced living document — Snowflake can update it unilaterally.

**Edition-specific controls:**
- Standard: SOC 2, OAuth, network policies, AES-256 at rest, TLS in transit, MFA, RBAC
- Enterprise: Adds periodic encryption rekeying, column/row-level security, 90-day Time Travel
- Business Critical: Adds customer-managed encryption keys (Tri-Secret Secure), private connectivity, PHI/HIPAA support, enhanced security monitoring
- VPS: Fully dedicated hardware (no shared compute or metadata store with any other Snowflake tenant)

**Support by edition:**
- Standard/Enterprise: Standard support (business hours)
- Business Critical/VPS: **Premier Support — 24/7, 1-hour response for Severity 1**

---

### 5. Breach Notification

**DPA commitment:** "Without undue delay, and in any case, where feasible, within seventy-two (72) hours after becoming aware."

**Subprocessor-to-Snowflake obligation:** 48 hours (Vendor DPA, updated Mar. 10, 2025).

**Real-world failure (May–June 2024 breach):** Snowflake identified unusual activity in mid-April 2024 but did not notify customers until approximately May 30 — roughly **45 days after first detection**, grossly exceeding contractual 72-hour targets and GDPR notification requirements. Class-action lawsuit filed (District of Montana). Post-breach: mandatory MFA announced June 10, 2024.

**Remediation:** No contractual obligation to cover customer remediation costs. The 2x Data Protection Cap is the financial ceiling; all indirect/consequential damages (regulatory fines, third-party notification costs, business interruption) are excluded.

---

### 6. IP / Indemnification

**Snowflake indemnifies** against third-party claims that the Service (used as authorized) infringes a U.S. patent, copyright, or trademark.

**U.S.-only scope — notable weakness:** Non-U.S. IP claims are not covered.

**Remedy options:** Replace/modify; procure license; terminate and refund unused fees.

**Sole remedy clause:** This is the "Customer's sole remedy with respect to any claim of intellectual property infringement."

**Customer indemnifies Snowflake** for all claims arising from Customer Data, Customer Materials, or any Customer-offered product or service.

**Feedback:** Snowflake may "freely use and incorporate any suggestions, comments or other feedback" into its products. No compensation or attribution required.

---

### 7. Termination & Portability

**Data retrieval window:** Up to **30 calendar days** from termination/expiration to access the Service solely to retrieve Customer Data. After that, Snowflake "shall promptly delete the Customer Data." No guaranteed post-termination read-only access in standard terms.

**Export format:** COPY INTO command and GET command export data in flat/delimited text or to external cloud storage (S3, Azure Blob, GCP Storage). No contractual obligation for migration assistance.

**Termination for cause:** Either party if material breach not cured within **30 days** of written notice.

**Customer refund on for-cause termination:** If *customer* terminates for Snowflake's breach → refund of prepaid unused Fees. If *Snowflake* terminates for customer's breach → no refund.

**Suspension rights (broad):** Snowflake may suspend for fees 30+ days overdue, AUP breach, or to "avoid material harm to Snowflake or its other customers" — a vague and discretionary standard.

---

### 8. SLA / Uptime

| Edition | Monthly Uptime SLA |
|---|---|
| Enterprise | 99.9% |
| Business Critical | 99.99% (added Sept. 2024) |
| VPS | Negotiated (typically 99.99%+) |

**Availability measurement:** Snowflake defines "Unavailable" as Error Rate > threshold over a one-minute interval. Measures only backend query execution errors — not authentication failures, client library issues, or connectivity problems external to the query engine. Snowflake itself acknowledges "industry-standard SLA thresholds are not particularly good measures of user experience."

**Credits:** Sole and exclusive remedy for SLA failures. Subject to overall liability cap.

---

### 9. Enterprise vs. Standard Terms

| Dimension | Self-Serve | Enterprise |
|---|---|---|
| Pricing | ~$2–4/credit (list) | Negotiated (10–30% discounts for multi-year >$1M ARR) |
| Uptime SLA | 99.9% (Enterprise edition) | 99.99% (Business Critical) |
| Support | Standard | Premier (24/7, 1-hr Sev1) |
| HIPAA/PHI | Not eligible | Eligible (Business Critical + BAA) |
| Customer-managed keys | No | Yes (Tri-Secret Secure) |
| FedRAMP | No | Yes (Business Critical, specific regions) |
| Custom DPA | No | Available for large enterprises |
| Expanded liability | No | Negotiable |
| Unused credit rollover | No | Negotiable |

---

### 10. Key Gotchas

1. **Unilateral mid-contract updates via URL incorporation** — security standards, DPA, SLA can change without customer consent
2. **Liability cap aggregated across affiliates** — can't treat each affiliate agreement separately
3. **No consequential damages — ever** — including for Snowflake's gross negligence
4. **IP indemnity is U.S.-only and sole-remedy** — non-U.S. enterprises have no contractual backstop
5. **30-day retrieval window with no transition assistance** — self-service export only
6. **Broad, vague suspension trigger** — "material harm to Snowflake or its other customers" undefined
7. **Customer reference/marketing without consent** — removal is only "to the extent commercially feasible"
8. **Feedback becomes Snowflake IP** — voluntary feedback usable without compensation
9. **Taxes fully customer-borne with gross-up** — above-standard in enterprise SaaS
10. **Real-world 45-day breach notification failure (2024)** — contract provides no penalties for missing the timeline
11. **HIPAA complete liability exclusion without BAA** — no exception
12. **Purchase orders explicitly nullified** — PO-incorporated terms have no contractual effect

---

## AWS

*Research compiled March 2026. AWS Customer Agreement last updated February 16, 2026. Sources: AWS Customer Agreement, Service Terms, DPA, SLA pages, AWS Artifact, third-party procurement analysis.*

---

### 1. Agreement Structure

| Document | Role |
|---|---|
| **AWS Customer Agreement (ACA)** | Master agreement; governs payment, liability, indemnification, termination, IP |
| **AWS Service Terms** | Per-service terms incorporated by reference; govern individual services (EC2, S3, Bedrock, etc.) |
| **Service Level Agreements (SLAs)** | Per-service uptime commitments and credit schedules; separate documents per service |
| **AWS Data Processing Addendum (DPA)** | Governs processing of personal data; auto-incorporated globally for any customer processing personal data |
| **Business Associate Addendum (BAA)** | Governs PHI under HIPAA; self-service acceptance via AWS Artifact; applies only to designated "HIPAA Accounts" |
| **Acceptable Use Policy (AUP)** | Defines prohibited activities; incorporated by reference |
| **Supplementary Addenda** | UK GDPR, Swiss FDPA, CCPA Terms — auto-incorporated when applicable law triggers them |

**How they layer:** ACA at top. Service Terms and SLAs incorporated by reference; Service Terms control for service-specific matters. DPA incorporated into Service Terms. In conflict: Service Terms prevail over ACA for service-specific matters.

**Enterprise Agreement (EDP/PPA):** A negotiated overlay — not a replacement — to the standard ACA. The EDP/Private Pricing Agreement primarily changes: committed spend discounts, payment terms, AWS Enterprise Support enrollment (mandatory), and service-specific pricing. The underlying ACA liability, indemnification, and IP provisions remain largely intact unless the customer is large enough to demand direct legal negotiation.

**Version control:** All changes posted at aws.amazon.com/agreement/recent-changes/. Continued use = acceptance.

---

### 2. Liability

**Cap (ACA Section 9.2):** "The aggregate liability...will not exceed the amounts paid by you to AWS under this agreement for the services that gave rise to the liability during the 12 months before the liability arose."

Key nuance: **the cap is per-service**, not total AWS spend. Only fees for the specific service that caused harm count — not aggregate AWS spend.

**Excluded damages (Section 9.1):** Neither party has liability for indirect, incidental, special, consequential, or exemplary damages; the value of customer content; loss of profits, revenues, customers, opportunities, or goodwill; or **unavailability of the services**. The explicit exclusion of "unavailability" as a consequential damage means even a total outage won't trigger meaningful liability beyond SLA credits.

**Carve-outs:**
- IP indemnification obligations are excluded from the cap
- **EU customers (Sept. 9, 2025 update):** For Amazon Web Services EMEA SARL customers in EU countries, Section 7.1 indemnification will not apply to the extent losses are caused by AWS's gross negligence or willful misconduct — a meaningful EU-specific improvement
- Added language: limitations apply only "to the extent permitted by applicable law"

---

### 3. Data Ownership & Privacy

**Ownership:** "You or your licensors own all right, title, and interest in and to Your Content." No AWS claim to customer content.

**Use restrictions:** AWS will not access or use customer content except to maintain or provide services, or as required by law. Will not disclose to any government or third party without consent (with commitment to notify customer where legally permitted).

**Training:** AWS does not use customer content to train AI/ML models for external use. This is a posted policy commitment backed by the ACA's access restriction language — not an explicit contractual clause with defined remedies.

**Data residency:** Customer chooses AWS Region(s). AWS will not move customer content outside selected region without customer instruction, except as required by law.

**GDPR/International transfers:** DPA applies automatically and globally — no separate opt-in. SCCs incorporated for EEA transfers. UK GDPR and Swiss FDPA addenda apply automatically when triggered. AWS has implemented the EU-US Data Privacy Framework adequacy decision (July 2023).

---

### 4. Security Commitments

**Shared Responsibility Model (contractually binding):**

| AWS Responsible ("Security of the Cloud") | Customer Responsible ("Security in the Cloud") |
|---|---|
| Physical data center security | Guest OS patching (IaaS/EC2) |
| Hardware and virtualization layer | Application security |
| Host OS and hypervisor | IAM configuration and access management |
| Network infrastructure | Data encryption selection and key management |
| AWS-managed service patching | Firewall/security group configuration |

For managed/abstracted services (S3, DynamoDB, Lambda), AWS takes on more responsibility — customers primarily manage data classification, access permissions, and encryption choices.

**Certifications:** SOC 1/2/3, ISO 27001/27017/27018, PCI DSS Level 1, FedRAMP, and many others. Available via AWS Artifact as compliance evidence.

**What is NOT contractually committed:** Specific penetration testing frequency; specific patch SLAs; mean time to detect/respond for security incidents; specific audit report delivery timelines.

---

### 5. Breach Notification

**DPA language:** AWS will notify customers "without undue delay" after becoming aware of a personal data breach. **No specific hour count committed.**

**Notification channel:** Email to one or more administrator accounts. No commitment to phone notification, dedicated incident management, or named contact notification.

**Division of responsibility:** AWS notifies the customer; the customer is then responsible for determining whether applicable law requires notification to regulators or data subjects and taking necessary action. AWS does not notify regulators on the customer's behalf.

**What AWS does NOT commit to:** Root cause analysis timeline; remediation steps or timeline; forensic evidence preservation; specific containment measures; covering customer-side notification costs.

---

### 6. IP / Indemnification

**AWS indemnifies customers against** third-party claims that any AWS service infringes a third party's intellectual property rights. Will defend and pay resulting damages and costs.

**IP indemnification exclusions — AWS does NOT indemnify where:**
- Claim arises from customer modifications to the service
- Claim arises from combination of the service with non-AWS products
- Customer continued using the service after AWS notified them to stop to avoid infringement
- Claim arises from customer content

**Customer indemnifies AWS** against third-party claims arising from customer content, customer use of services, or customer's breach of the agreement — a broad obligation covering privacy violations, IP infringement in customer content, and regulatory actions triggered by customer data.

**No Shared Responsibility carve-out:** For incidents jointly caused by AWS misconfiguration and customer misconfiguration, both parties' indemnification obligations could apply — creating disputes about causation.

---

### 7. Termination & Portability

| Scenario | Notice |
|---|---|
| Either party (convenience) | 30 days |
| Either party (material breach) | 30-day cure period |
| AWS (security risk, fraud, legal risk) | Immediately, no cure period |
| AWS (discontinues a service — material functionality) | 12 months |
| AWS (emergency discontinuation) | Immediately |

**Post-termination data:**
- During 30 days post-termination: content not erased; customer may retrieve
- Up to 90 days post-termination: AWS will return or delete Customer Data upon request using Service Controls
- After 90 days: permanently deleted (except backup/log retention per technical documentation)

**Data egress fees:** AWS announced in March 2024 it will waive egress fees for customers migrating away (>100 GB/month requires contacting Support for credits). Driven by the EU Data Act (effective September 2025). **Caveat:** This is a pricing policy, not a contractual ACA guarantee — it could theoretically be changed without ACA amendment.

---

### 8. SLA / Uptime

**Per-service SLA commitments (representative sample):**

| Service | Deployment | Uptime SLA |
|---|---|---|
| EC2 | Multi-AZ | 99.99% |
| EC2 | Single-AZ | 99.5% |
| Lambda | — | 99.95% |
| Elastic Load Balancing | — | 99.99% |
| Amazon S3 | — | 99.9% |
| Amazon EBS | — | 99.99% |
| RDS | Multi-AZ | 99.95% |
| RDS | Single-AZ | No SLA |
| DynamoDB | Standard | 99.99% |
| DynamoDB | Global Tables | 99.999% |

**S3 credit schedule:**
- <99.9% but ≥99%: 10% of monthly S3 fees
- <99%: 25% of monthly S3 fees

**Credit mechanics:** Applied only to future bills (not cash). Require a formal support case with logs and resource IDs. Capped at 25–30% of monthly fees for the affected service — representing perhaps 1–3 days of downtime cost relative to a full month.

**SLA exclusions:** Scheduled maintenance; customer misconfiguration; third-party software failures; DDoS/force majeure; beta services/regions (explicitly excluded from all SLAs).

**Key weakness:** SLAs cover availability only — not performance (latency, throughput). A service can be "available" but severely degraded without triggering credit obligations.

---

### 9. Enterprise vs. Standard Terms

**Standard ACA:** Click-through, take-it-or-leave-it. Governed by Washington State law (or applicable AWS Contracting Party jurisdiction for non-US).

**Enterprise Discount Program (EDP) / Private Pricing Agreement (PPA):**
- Triggered by committed spend typically starting at $1M–$5M/year
- Duration: typically 1–5 years
- Primary negotiables: platform-wide discount rate, specific service pricing, commitment structure, payment terms, migration credits
- AWS Enterprise Support enrollment is **mandatory** for EDP customers
- AWS Marketplace spend counts partially toward EDP commitment but cannot be discounted at EDP rate

**What typically does NOT change in an EDP:**
- ACA liability cap (trailing 12 months fees, per-service)
- Consequential damages exclusion
- AWS's suspension and termination rights
- Indemnification structure
- Governing law and dispute resolution

**What CAN be negotiated for very large customers:** Custom legal addenda replacing portions of ACA; extended data retention post-termination; dedicated TAM commitments; custom SLA terms; audit rights beyond standard SOC/ISO reports.

**AWS Enterprise Support tier:** Mandatory for EDP. Provides: <15 min response for business-critical issues, Technical Account Manager (TAM), Trusted Advisor, Infrastructure Event Management. Priced at 10% of monthly AWS usage (volume discounts apply). Does not change liability or legal terms.

---

### 10. Key Gotchas

1. **Trailing 12-month cap is per-service, not total spend** — a $10M AWS customer causing a major outage tied to one service gets a cap based only on fees for that service, not the full $10M
2. **"Unavailability" explicitly excluded from consequential damages** — even a total outage won't trigger meaningful liability; SLA credits (max 25–30% of monthly service fees) are the effective ceiling
3. **Unilateral amendment rights** — AWS posts a revised version; continued use = acceptance. No minimum notice period for non-SLA changes
4. **Suspension on "reasonable belief" with no cure period** — AWS can immediately cut off all production data and workloads if it "reasonably determines" a security risk, with no opportunity to cure before suspension
5. **30-day termination for convenience by AWS** — 30 days is insufficient for most enterprises to migrate deeply integrated workloads
6. **Content removal — 2-business-day rule** — AWS can demand AUP-violating content be removed within 2 business days or suspend services
7. **SLA credits are not cash and require manual claiming** — applied only to future bills; require formal support case with technical evidence; no automatic issuance
8. **Free egress is a pricing policy, not an ACA term** — could theoretically be reversed without contract amendment (though regulatory pressure makes this unlikely)
9. **Broad customer indemnification of AWS** — covers privacy violations, IP infringement in customer content, and regulatory actions against AWS triggered by customer data; no carve-out for AWS's own negligence contributing to the trigger
10. **No specific breach notification SLA** — "without undue delay" provides no actionable hours commitment
11. **Beta services have no SLA, no liability** — AWS launches many significant services in preview/beta; production workloads on these have essentially no contractual protection

---

## Cross-Vendor Comparison Summary

*Workday column reflects Universal MSA v26.2 and Universal Amendment to the MSA.*

| Dimension | Workday uMSA | Anthropic | Databricks | GCP | OpenAI | Snowflake | AWS |
|---|---|---|---|---|---|---|---|
| **Agreement type** | Single Universal MSA (all products); Order Form + MSA + Security Exhibit + DPE + Product Terms; Order Form precedence (Cl. 10.14) | Multi-doc stack | Layered (MCSA + Schedules) | Layered (ToS + CDPA + SST) | Layered (Services Agreement + DPA) | ToS + URL-incorporated supplements | Multi-doc (Customer Agreement + Service Terms) |
| **Data ownership / use** | Customer owns all Customer Content; Workday uses it **only to provide the Service** (Cl. 3(a)). Customer owns all Outputs (Amendment §1). No training of external models on Customer Content. | Customer owns Content + Outputs; no training on commercial/API by default | Customer owns Content; hard prohibition on training GenAI on it | Customer retains IP in Customer Data; use for AI/ML not explicitly prohibited in ToS | Customer owns Input + Output; no training (contractual May 2025) | Customer owns Customer Data; limited license to Snowflake | Customer owns Your Content; no use to train AI for external use (policy) |
| **Liability cap** | 12-mo. fees (General Cap); **24-mo. fees** for breach of confidentiality/security/privacy (Enhanced Cap). **Remediation (Cl. 8.3) excluded from cap.** Gross negligence, willful misconduct, fraud, indemnification, payment also excluded (Cl. 8.1). | 12 mo. fees (no floor) | 1x (general); 2x (breach) | 12 mo. fees (no floor) | 12 mo. fees | 1x (general); 2x (data protection) | 12 mo. fees |
| **Breach remediation coverage** | ✅ **Cl. 8.3:** Forensics, notifications, credit monitoring (1 yr), call center (1 yr) — reasonable & documented costs; excluded from liability cap | ❌ No | ❌ No | ❌ No | ❌ No | ❌ No | ❌ No |
| **Breach notification** | **48 hours** or shorter if required by Law (Cl. 5.3); root cause analysis and remediation plan shared upon request | 48 hours (DPA) | 3 business days | "Promptly, without undue delay" | "Without undue delay" | 72 hours (DPA) | Varies |
| **Default SLA** | SLA per Product Terms; no material decrease during Order Term. Service Credits: 10% / 20% / 30% for 2nd/3rd/4th Failure in rolling 6-mo. (Cl. 10.13) | ❌ None (standard) | 99.9% (AWS/GCP) | Per-service (99.9%–99.999%) | ❌ None (standard) | 99.9% (Ent.); 99.99% (Biz Crit.) | Per-service |
| **IP indemnification** | Workday defends and indemnifies for third-party IP claims re use of Service; carveouts for modification, misuse, combination (Cl. 7.1) | Yes (excl. consumer) | Yes + GenAI (uncapped) | Yes + GenAI output + training | Yes (Copyright Shield, uncapped) | Yes (U.S. only) | Yes |
| **Data portability** | **60-day Retrieval Period** at no cost; extraction in **machine-readable format** per Documentation (Cl. 9.2). Up to **3-month Transition** available (Cl. 9.3). | ❌ No structured mechanism | ✅ Strong (Delta Lake) | ✅ Free Cloud Exit | ❌ No structured mechanism | Limited (30-day self-service) | Standard |
| **Mid-contract changes** | Product Terms: no material decrease in security/privacy; changes **not effective until 30 days after publication** (MSA def.; Amendment §11) | Via policy updates | Via URL docs (PayGo) | 30 days' notice | 14 days' pricing notice | ✅ Yes (URL incorporation) | Continued use = acceptance |
| **HIPAA BAA** | ✅ Yes (Business Associate Exhibit if applicable) | ✅ Yes (sales-assisted) | ✅ Yes (Enterprise) | ✅ Yes (separately executed) | ✅ Yes (sales-assisted) | ✅ Yes (Business Critical+) | ✅ Yes |

---

## Key Workday uMSA Differentiators vs. oCIO Vendors
*Based on the Universal MSA and Universal Amendment to the MSA.*

1. **Breach remediation carveout (Clause 8.3)** — Only Workday contractually commits to pay *reasonable and documented costs* for forensic investigation, breach notifications, credit monitoring (one year), and call center operations (one year) when unauthorized disclosure of or access to Personal Data is caused by Workday’s breach of its security, privacy, or data protection obligations. These remediation obligations are **excluded from the liability cap** (Cl. 8.1(D)). No other vendor in this set does this.

2. **48-hour breach notification (Clause 5.3)** — Workday commits to notify the other party **within 48 hours or any shorter period required by Law** upon awareness of a Security Breach, and to conduct a root cause analysis and share results and remediation plan upon request. Snowflake has a 72-hour DPA commitment but failed to meet it in 2024; GCP and OpenAI use undefined "without undue delay" language.

3. **Single Universal MSA for all products** — One agreement (Order Form + MSA + Security Exhibit + DPE + Product Terms) covers all Workday products; Order Form takes precedence. Competitors use layered, multi-document stacks with URL-incorporated documents that can change mid-contract or require product-specific overlays.

4. **Customer Content used only to provide the Service; Customer owns Outputs** — MSA Cl. 3(a): Workday has the right to use Customer Content **only to provide the Service**. Amendment: Customer owns all Outputs from AI Systems; Workday develops AI Systems in accordance with applicable Law (e.g., EU AI Act). Workday does not use Customer Content to train external AI/ML models — a clear, contract-level commitment that contrasts with vendors where “no training” is tier-dependent or policy-based.

5. **Security Exhibit and Audit Reports** — Security program conforms to the Security Exhibit and Audit Reports; Workday makes Audit Reports available via self-service or upon written request. No update may materially decrease protections during the Term. Replaces need for per-customer audit negotiation.

6. **Predictable Product Terms** — Product Terms may be updated only such that no update materially decreases security and privacy commitments, and such changes do not become effective until **30 days after publication** (MSA definition; Amendment §11). Contrast with vendors that incorporate terms by URL with no minimum notice before material changes.

7. **Retrieval and Transition** — Up to **60 days** at no cost to retrieve Customer Content in a **machine-readable format** (Cl. 9.2). Optional **up to three months** Transition Period after termination if requested before termination (Cl. 9.3).

---

*Sources for this document are cited within each vendor section.*
