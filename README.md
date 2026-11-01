# Awesome-Predictive-Lead-Scoring-Qualification

## Top Predictive Lead Scoring & Qualification Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Behavioral Signal Detection, AI-Powered Qualification & Self-Hosted Scoring Engines*  

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Predictive Lead Scoring & Qualification**. These tools enable revenue teams to identify which leads are most likely to convert, prioritize outreach based on behavioral and firmographic signals, and route sales attention to the highest-value opportunities—turning raw lead lists into ranked, actionable pipelines.



**Examples** include HubSpot Lead Scoring, MadKudu, 6sense, Demandbase, Leadspace, Breadcrumbs.io, Infer, ZoomInfo Score, Forter, and Salespanel (the category leaders).



**Open-source emphasis**: Predictive Lead Scoring is a domain where open-source tooling is **genuinely emerging but fragmented across distinct approaches**. The strongest active projects are **Beton** (an open-source, self-hostable MadKudu alternative with LLM-powered autopilot signal detection) , **ai-lead-scoring-engine** (a comprehensive B2B scoring engine with 136 features, tri-dimensional scoring, and local LLM reasoning) , and **looot-score** (a MIT-licensed repo that rebuilds the data half of MadKudu with firmographic and tech-stack rules) . For a complete pipeline with CRM integration, **ai-lead-agent** combines Google Gemini analysis with n8n automation and Airtable storage . The critical caveat: **no open-source project matches MadKudu's model trained on your own closed-won deals**—the commercial platform's predictive power comes from learning your specific conversion patterns, while open-source tools typically use fixed rules or generic LLM analysis . As one open-source rebuild explicitly admits: "Models trained on your own outcomes" is the part it left out .



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[HubSpot Lead Scoring](https://www.hubspot.com/)**  

  Native lead scoring within HubSpot's Marketing Hub; assigns points based on contact properties and behavioral events (email opens, page views, form submissions) to rank leads for sales follow-up.



- **[MadKudu](https://www.madkudu.com/)**  

  Predictive lead scoring platform that uses machine learning models trained on your closed-won deals to score leads based on fit, behavior, and product usage. **Starting price around $999/month** . Integrates with CRM and marketing automation to prioritize MQLs and PQLs . **Best for organizations with enough historical data** to train predictive models—but closed-source with opaque scoring and complex setup .



- **[6sense](https://6sense.com/)**  

  Account-based predictive intelligence with intent data from bidstream and technographic sources; identifies accounts in active buying cycles before they fill out forms.



- **[Demandbase](https://www.demandbase.com/)**  

  Account-based marketing and predictive scoring platform with intent data, firmographic enrichment, and AI-driven account prioritization.



- **[Leadspace](https://www.leadspace.com/)**  

  Predictive lead scoring and data enrichment platform; combines third-party data with AI models to score and prioritize leads.



- **[Breadcrumbs.io](https://breadcrumbs.io/)**  

  Lead scoring platform focused on product-led growth signals; tracks user behavior and scores leads based on fit and engagement.



- **[Infer](https://www.infer.com/)**  

  Predictive lead scoring platform (now part of Ignite Technologies); uses external signals and firmographic data to score leads.



- **[ZoomInfo Score](https://www.zoominfo.com/)**  

  Lead and account scoring within ZoomInfo's data platform; combines firmographic, technographic, and intent data to rank opportunities.



- **[Forter](https://www.forter.com/)**  

  Fraud prevention platform (not lead scoring); included in the search query for context but not relevant to lead qualification.



- **[Salespanel](https://salespanel.io/)**  

  Lead tracking and scoring platform with website visitor identification, behavioral scoring, and CRM integration.



## Open-Source GitHub Projects



### AI-Powered Scoring Engines



- **[Beton](https://www.getbeton.ai/)**  

  Open-source, self-hostable **MadKudu alternative** (AGPLv3) focused on product-led B2B SaaS . Connects your PostHog product analytics to your CRM (Attio, HubSpot, Zoho, Pipedrive) and automatically discovers **behavioral signals**—buying intent, expansion readiness, churn risk—using **LLM-powered autopilot detection** (no manual rules required) . **Key differentiator**: data stays on your infrastructure, no third-party cloud, no per-seat pricing . **Honest limitation**: while it uses LLM-powered detection, it does not train a model on your closed-won deals like MadKudu does—it identifies signals from behavior and firmographics . **Best for product-led SaaS teams** wanting transparent, self-hosted scoring without MadKudu's $999/month price tag .



- **[ai-lead-scoring-engine](https://github.com/Nikkk2312/ai-lead-scoring-engine)**  

  The most feature-complete open-source **B2B lead scoring engine** available (self-hosted, privacy-first, zero API costs) . Features: **136 features** across **tri-dimensional scoring** (Fit/Engagement/Intent), **buying stage pipeline** (6sense-inspired), **Fit-Engagement matrix** (A1–C3 grid), **local LLM reasoning** for natural-language score explanations, sales feedback loop, **scoring model versioning**, **champion/challenger A/B testing**, **account-based scoring (ABM)**, **Kanban pipeline board**, **workflow automation builder**, **HubSpot/Salesforce/Apollo import templates**, **GDPR data export/deletion**, SLA monitoring, and duplicate detection . Tech: Python, SQLite/PostgreSQL, Docker Compose. **Best for teams wanting a comprehensive, self-hosted scoring platform** with transparency and no per-lead API costs—but it is a newer project and the local LLM reasoning may be less sophisticated than a model trained on your own conversion data .



- **[looot-score](https://github.com/loootai)**  

  MIT-licensed open-source repo that rebuilds the **data half of MadKudu**—grades leads from firmographics and tech stack with **fixed points per rule** . **Honest disclosure from the author**: "Models trained on your own outcomes" is listed as a feature it left out; rules are "easier to read and worse at surprises" . Quoted cost at list price: **$0.83 to $1.67 per 100 leads** (data API usage). **Best for teams wanting a transparent, inspectable scoring baseline**—but it is rules-based, not predictive machine learning .



- **[ai-lead-agent](https://github.com/WaltGreenwich/ai-lead-agent)**  

  Open-source **AI lead qualification system** using **Google Gemini** for analysis, FastAPI for the API, **n8n for automation**, and **Airtable for storage** . Extracts from lead messages: **lead score (0–100)** based on buying signals, **priority level** (Hot/Warm/Cold), industry/company size, urgency/buying intent, budget signals, pain points, and recommended actions . Features: React dashboard, RESTful API, Docker Compose deployment . **Best for teams wanting a practical AI-powered qualification pipeline** with CRM automation—but it requires Google Gemini and Airtable API keys, and scoring is LLM-based rather than trained on your conversion data .



### ML-Based Scoring Models (Research & Prototypes)



- **[Cuana-E2E](https://github.com/avrtt/Cuana-E2E)**  

  Open-source **end-to-end customer analytics suite** with **XGBoost-based lead scoring**, churn/CLV prediction, and customer segmentation . Features: Python data pipeline (pandas/NumPy), supervised model for lead prioritization, interactive Dash/Plotly dashboard . **Best for data science teams** wanting a reference implementation of ML-based lead scoring alongside broader customer analytics—but it uses **synthetic data** and is a portfolio/freelance project rather than a production platform .



- **[Kaggle Lead Scoring System (denis911)](https://github.com/denis911/kaggle-lead-scoring-v3-data-analysis-modeling-and-cloud-deployment)**  

  Production-ready **ML pipeline** with XGBoost (~0.88 AUC), FastAPI inference API, and Docker deployment . Trained on a Kaggle CRM dataset; handles categorical data, missing values, and leakage prevention . **Best for ML engineers** wanting a template for training and deploying a lead conversion model—but it is dataset-specific and not a complete qualification platform .



- **[lead-scoring-kan](https://github.com/jylee0912/lead-scoring-kan)**  

  Research code and datasets for a comparative analysis of **machine learning algorithms for lead scoring** (KAN—Kolmogorov-Arnold Networks) . Published August 2025, Python, active development . **Best for researchers** exploring novel ML architectures for lead scoring—not a production tool.



### Additional Strong Open-Source Options



- **growth-tools** — Open-source **automated lead capture** from Reddit, Discord, and GitHub with **hybrid LLM scoring** (0.5 × rule score + 0.5 × LLM intent score) and outreach drafts . **Best for developer-tool companies** wanting to capture leads from developer communities—not a general-purpose lead scoring platform for existing CRM leads .

- **leadEngine** — Open-source **AI-powered lead automation platform** with a Chrome extension for scraping public business data, AI scoring (0–100 with reasons), workflow automation, and CRM integrations . **Best for outbound prospecting** from public data sources—but it is pre-1.0 and focused on lead *discovery* rather than scoring existing leads .

- **Cantrip** — Open-source **GTM lead research and scoring tool** that takes attendee CSVs or GitHub searches, scores leads best-first, and generates outreach drafts . **Best for event follow-up and GitHub-based prospecting**—but it is a CLI/browser tool rather than a CRM-integrated scoring platform .



**Frameworks for building custom systems**: For **product-led SaaS teams wanting self-hosted MadKudu-style signal detection**, Beton provides the most complete open-source alternative . For a **comprehensive scoring engine with 136 features and local LLM reasoning**, ai-lead-scoring-engine . For a **practical AI qualification pipeline with n8n automation**, ai-lead-agent . For a **transparent rules-based baseline**, looot-score . **No open-source project trains a predictive model on your closed-won deals** like MadKudu does—the predictive moat remains commercial. Choose based on whether you need signal detection (Beton), feature-rich scoring (ai-lead-scoring-engine), or a quick AI pipeline (ai-lead-agent).



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Predictive lead scoring platforms handling lead and behavioral data must comply with applicable privacy regulations (GDPR, CCPA) and data governance policies; **scoring models can encode bias and should be audited for fairness**—especially when trained on historical conversion data that may reflect past discriminatory practices.

- **Open-source predictive lead scoring is emerging but fundamentally limited by the absence of your outcome data**—Beton provides LLM-powered signal detection , and ai-lead-scoring-engine provides feature-rich rules and local LLM reasoning . However, **no open-source project trains a predictive model on your own closed-won deals** like MadKudu does—one open-source rebuild explicitly lists this as a left-out feature . Organizations requiring true predictive scoring trained on their specific conversion patterns should evaluate commercial platforms or invest in custom model development.

- Verify license terms for commercial use; Beton is open-source (AGPLv3) , looot-score is MIT , and ai-lead-scoring-engine is open-source (check repository) .



---



**Made for revenue operations leaders, sales analysts, and teams building lead qualification infrastructure.**  

Let's make predictive lead scoring more open, but with clear eyes about the outcome-data gap that makes true predictive modeling a commercial advantage.
