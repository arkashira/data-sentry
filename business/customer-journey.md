# Customer Journey – **data‑sentry**

| Phase | Trigger Event | Friction Points | User Emotions | Opportunities to Delight | Success Metric |
|------|---------------|----------------|---------------|--------------------------|----------------|
| **Aware** | • A SaaS founder reads a blog post about “90 % of data‑loss incidents are preventable with automated backups.” <br>• A competitor suffers a public outage and loses 12 % of its paying users. | • Information overload – many backup tools claim “automated.” <br>• Lack of clear ROI numbers for backup investments. | Curious → Anxious (about data loss) | • Publish a one‑page “Backup ROI Calculator” that instantly shows potential churn savings (e.g., $120 k/yr for a $5 M ARR SaaS). <br>• Release a short 2‑minute explainer video with real‑world loss stats. | **% of target SaaS founders who click the ROI calculator** (goal ≥ 8 %). |
| **Consider** | • Founder receives the ROI report and sees a projected 0.5 % churn reduction → schedules a 15‑min discovery call. | • Complex pricing tables; unclear integration scope (SQL, NoSQL, object storage). <br>• Need to convince CTO/security team of compliance. | Hopeful → Overwhelmed (by technical details) | • Provide a **dynamic pricing sandbox** that tailors cost to data volume (e.g., $0.10/GB/mo). <br>• Offer a downloadable **Compliance Checklist** (SOC 2, GDPR, ISO 27001) that maps data‑sentry features to each control. | **Conversion rate** from ROI download → discovery call (target ≥ 25 %). |
| **Try** | • Free 30‑day trial is provisioned after the call; trial includes 1 TB of backup storage and automated restore testing. | • Setup time (API keys, bucket permissions) can take >2 h. <br>• Trial UI shows “backup in progress” without clear status. | Excited → Frustrated (if onboarding stalls) | • Deploy an **onboarding wizard** that auto‑detects data sources and creates the first backup in <5 min. <br>• Real‑time progress bar with “next‑step” suggestions (e.g., “Schedule daily incremental”). <br>• Dedicated Slack channel with a **Customer Success Bot** that answers “Where is my backup?” within 30 s. | **Trial activation rate** (percentage of sign‑ups that complete first backup) – goal ≥ 70 %. |
| **Adopt** | • Trial ends; user sees a dashboard showing 99.99 % backup success and a projected $75 k churn avoidance for the next year. | • Contract negotiation (annual vs. monthly) and perceived lock‑in risk. <br>• Need for migration of existing backups from legacy tools. | Confident → Cautious (about long‑term commitment) | • Offer a **“no‑lock‑in” 30‑day money‑back guarantee** and a **pay‑as‑you‑grow** pricing tier. <br>• Provide a **one‑click migration tool** that imports historic backups from AWS S3, GCP Cloud Storage, or on‑prem solutions. <br>• Assign a **Customer Success Manager** for the first 90 days with quarterly business reviews. | **Closed‑won rate** after trial (target ≥ 55 %). |
| **Expand** | • After 6 months, the SaaS scales to 3 TB of data; usage spikes trigger a “You’re approaching your limit” alert. | • Upsell friction: perceived price jump, need for internal approval. <br>• Limited visibility into backup analytics beyond storage usage. | Satisfied → Ambitious (looking to deepen protection) | • Introduce **tiered add‑ons** (e.g., “Instant Restore”, “Geo‑Redundant Archive”) with transparent per‑GB pricing. <br>• Provide an **Analytics Dashboard** showing backup trends, RTO/RPO compliance, and cost‑savings over time. <br>• Run a **Quarterly Health Check** webinar that showcases new features and gathers feedback. | **Net Revenue Expansion Rate (NRE)** – target ≥ 30 % YoY increase from existing customers. |

---  

### Narrative Flow (High‑Level)

1. **Awareness** – The prospect discovers the hidden cost of data loss and is nudged toward a concrete ROI estimate.  
2. **Consideration** – They evaluate data‑sentry against competitors, aided by transparent pricing and compliance artifacts.  
3. **Trial** – A friction‑free, rapid‑setup experience proves the product’s value in real time.  
4. **Adoption** – Clear financial upside, risk‑free guarantees, and migration assistance convert trial users into paying customers.  
5. **Expansion** – Ongoing analytics, proactive alerts, and modular add‑ons drive deeper usage and higher lifetime value.  

---  

### Key Success Levers

- **Speed of First Backup** ≤ 5 min (reduces trial friction).  
- **ROI Calculator Click‑through** ≥ 8 % of target audience.  
- **Trial Activation** ≥ 70 % (first backup completed).  
- **Close Rate** ≥ 55 % after trial.  
- **NRE** ≥ 30 % YoY from existing accounts.  

---  

### Action Items for Product & Growth Teams

| Owner | Action | Deadline |
|-------|--------|----------|
| Growth | Build and embed the ROI calculator on the landing page. | +2 weeks |
| Product | Release onboarding wizard & progress UI for trial. | +4 weeks |
| CS | Create Compliance Checklist & Slack Success Bot. | +3 weeks |
| Sales | Draft “no‑lock‑in” contract language & migration tool spec. | +5 weeks |
| Analytics | Design backup analytics dashboard & NRE tracking. | +6 weeks |

---  

*End of `customer-journey.md`*