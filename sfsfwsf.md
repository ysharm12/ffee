Below is a **3-slide package** (each slide has **on-slide content + detailed voiceover script**) tuned for an **executive presenter**: first the **data strategy/architecture**, then the **AI Concierge** as the “cherry on top / USP”.

---

# Slide 1 — Executive Summary (On-slide)

**Title:** UHG Consumer & Customer Engagement (CCE) Data Platform — 2026 Data Strategy

**Bullets (keep tight):**

* **One unified lakehouse foundation** for all CCE domains (Marketing, Digital, Sales, Service)
* **Batch + Real-time + CDC** ingestion into a governed Delta Lake (Bronze → Silver → Gold)
* **Databricks as the processing + AI engine** for scalable ELT, analytics, and ML workflows
* **Governance-by-default** with Unity Catalog, enterprise audit, security, and compliance controls
* **Faster time-to-value**: reusable ingestion + medallion patterns → rapid onboarding of new sources
* **Activation & sharing**: curated data products served to BI, teams, and partners—securely

## Voiceover Script (Slide 1)

“Today I’ll walk through our 2026 target-state data strategy for Consumer and Customer Engagement at UHG.
The objective is simple: **turn fragmented engagement data into a single governed platform** that can power analytics, AI, and activation across Marketing, Digital, Sales, and Service.

This platform is built around a **lakehouse foundation**: we ingest data in **three modes—real-time streams, batch loads, and CDC incremental updates**—and land everything into a **Delta Lake with a Medallion architecture: Bronze, Silver, and Gold**. That layered design is what gives us both **auditability and trusted business-ready datasets**.

On top of that, **Databricks is our core processing and AI engine**—so we can do scalable transformations, SQL analytics, and ML workflows in the same governed environment.

Finally, governance and security aren’t an afterthought—they span the entire system: access control, auditing, monitoring, cost management, and compliance.
After we cover the architecture, I’ll show the differentiator: a **Proactive AI Data Concierge** that sits on top of this foundation to accelerate self-service, quality triage, and impact analysis.”

---

# Slide 2 — Architecture (On-slide)

**Title:** CCE Data Platform — Birds-eye Architecture (Source → Ingest → Lakehouse → Data Marts → Serve)

**Callouts (match the picture, left to right):**

1. **Source Layer**: SQL/SharePoint/Postgres/Oracle/APIs/files/ops tools
2. **Ingestion**

   * **Azure Event Hubs** (real-time events)
   * **Batch + CDC** via **Azure Data Factory**
3. **Storage (CCE Delta Lake)** — **Bronze → Silver → Gold**
4. **Processing & AI**

   * Data Quality & Validation
   * Databricks (Workflows/Jobs, SQL Analytics)
   * Unity Catalog governance
5. **Product/Data Marts**: Marketing / Digital / Sales / Service
6. **Serve + Share**: Power BI, Catalog Share, External Workspace Share, Self-Service
7. **Governance & Security Layer**: logs, IAM, security center, monitoring, cost mgmt, AI/ML alerts

## Voiceover Script (Slide 2)

“Now let’s walk through the architecture from left to right—exactly how data flows.

**First is the Source Layer.** This is a diverse neighborhood: SQL databases, SharePoint, Postgres, Oracle, API-driven applications, operational tools, and file-based inputs. Each source is valuable, but they’re fragmented and speak different ‘data languages’. Our mission is to bring them into **one unified ecosystem**.

**Next is Ingestion**, and we support two main patterns:

* **Azure Event Hubs** for real-time and streaming signals—think clickstreams, events, telemetry, API feeds. This is our always-on pipeline for near-real-time ingestion.
* **Azure Data Factory for Batch + CDC.** Batch covers scheduled loads and bulk movement. **CDC—Change Data Capture—means we pull only what changed**, which reduces cost, improves freshness, and keeps the platform responsive.

From ingestion, data lands into our **CCE Delta Lake**, which is organized into the Medallion layers:

* **Bronze** is raw and immutable—what came in, time-stamped, auditable.
* **Silver** is cleaned, validated, deduplicated, and conformed—this is where quality and consistency become reliable.
* **Gold** is curated and business-ready—these are the data products optimized for analytics, reporting, and activation.

Above storage sits the **Processing & AI layer**, which is our engine room:

* We enforce **data quality and validation**—so bad data doesn’t silently become business metrics.
* **Databricks** runs our transformations, streaming jobs, and SQL analytics using governed compute.
* **Workflows and Jobs** operationalize the pipelines from Bronze to Silver to Gold.
* And **Unity Catalog** is the governance backbone—centralized access control, auditability, and managed metadata.

Once Gold data products are ready, they feed our **Product/Data Mart layer** aligned to real business outcomes:
Marketing, Digital, Sales, and Service each get domain-aligned, analytics-ready datasets.

Finally on the right is **Serve and Share**:

* **Power BI** dashboards and reporting,
* **Catalog Share** and **External Workspace Share** where appropriate,
* and **Self-Service** so business users can discover and consume governed datasets without waiting on manual handoffs.

And across everything, the **Governance & Security layer** runs end-to-end: identity and access, logs, monitoring, security controls, cost management, and operational alerts.
So the key takeaway is: this architecture gives us both **scale and speed**, without sacrificing **trust, security, or compliance**.”

---

# Slide 3 — Proactive AI Data Concierge (On-slide blocks)

**Title:** Proactive AI Data Concierge (2026) — Self-Service + Trust + Faster Recovery

## Block Group A — Business Self-Service (Front Door)

**1) Ask Data Interface**

* Natural language entrypoint for business users
* Routes to the right **certified Gold data product** (not random tables)

**2) Data Product Concierge**

* Finds the right dataset by intent (“member 360”, “campaign performance”)
* Explains definitions, grain, joins, certified use cases
* Guides access request if needed

## Block Group B — Reliability & Change Safety (Operations)

**3) Quality Triage Agent**

* Detects anomalies (freshness, completeness, metric spikes)
* Traces upstream root cause via lineage
* Proposes rollback/backfill/re-run plan

**4) Schema Drift Agent (Contract Guardian)**

* Detects breaking schema/type changes early
* Recommends contract updates + pipeline patch steps
* Prevents silent corruption of Gold outputs

**5) Impact Analysis Agent**

* Answers: “If we change table X, what breaks?”
* Lists impacted dashboards, marts, ML features, and owners

## Block Group C — Trust at Scale (Governance Automation)

**6) Auto-Documentation Agent**

* Generates/refreshes dataset documentation continuously
* Publishes: purpose, grain, SLAs, sensitivity notes, usage guidance

**7) Enterprise Lineage Bridge**

* Unifies lineage view across ingestion → lakehouse → marts → BI
* Enables audits, impact analysis, and faster troubleshooting

**Guardrail Banner (bottom of slide):**
**Policy-Aware + Approval-Gated**: AI cannot bypass permissions; it proposes, humans approve, workflows execute.

---

## Voiceover Script (Slide 3)

“Now that you’ve seen the foundation, here’s the differentiator—the **Proactive AI Data Concierge**.
This is not a gimmick, and it’s not replacing governance. It only works because the platform underneath is already governed, layered, and observable.

Think of the concierge as **three capabilities stacked together**:

**First: Business Self-Service — the front door.**
Business teams don’t want to hunt through folders or ask around. They want to ask, in plain English:
‘What is the trusted dataset for campaign conversions?’ or ‘Where is the member engagement view?’
The **Ask Data interface** becomes that entrypoint—and the **Data Product Concierge** routes users to the right **certified Gold dataset**, explains what it means, what the grain is, what joins are safe, and what definition we’re using.
If the user doesn’t have access, it doesn’t leak information—it guides them through the proper access request path.

**Second: Reliability and change safety — the operations layer.**
This is where we get real leverage.

* The **Quality Triage Agent** watches platform signals like freshness gaps, missing data, or sudden metric spikes.
  Instead of just raising an alert, it answers the executive question: **‘What broke, why, and what do we do now?’**
  It traces upstream dependencies using lineage and proposes a recovery plan—re-run, backfill from Bronze, or roll back to the last known good state.

* The **Schema Drift Agent** prevents a classic failure mode: a source system changes a column type or field name, and suddenly downstream tables break—or worse, silently produce incorrect metrics.
  This agent detects drift early, identifies blast radius, and proposes the minimum safe patch: contract update plus pipeline adjustments, before it contaminates Gold datasets.

* The **Impact Analysis Agent** makes change management safe.
  When someone asks, ‘Can we change table X?’ it can answer immediately: which dashboards, marts, features, and teams will be impacted—so we stop discovering consequences after the fact.

**Third: Trust at scale — governance automation.**
Two key pieces here:

* The **Auto-Documentation Agent** solves a universal problem: documentation rots.
  Instead of manual docs that get outdated, it continuously refreshes dataset descriptions, SLAs, sensitivity notes, and usage guidance—so the catalog stays accurate.

* And the **Enterprise Lineage Bridge** ensures we can trace data end-to-end: from source → ingestion → medallion layers → marts → BI and sharing.
  That makes audits, troubleshooting, and impact analysis dramatically faster and safer.

Finally, the most important point for stakeholders: **guardrails**.
This concierge is **policy-aware and approval-gated**. It can recommend actions, but it cannot bypass access controls, and it doesn’t directly push changes without governance workflows.

So the headline is:
The data platform gives us the foundation—scale, quality, governance.
The AI Concierge is the multiplier—**faster self-service, faster recovery, safer change, and higher trust**.”

---

If you want, I can also convert these voiceovers into **shorter “executive speaking notes” (30–45 sec each)** *or* **longer “architect talk track” (3–5 min each)** depending on the audience mix in the room.
