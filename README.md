# Restaurant Fraud Investigator Agent

**Purpose-built AI agent for restaurants to fight chargebacks and win more disputes**

Automatically investigates incoming chargebacks, scores fraud likelihood using a long-sequence behavior model inspired by Tencent Weixin's LBSF architecture, gathers compelling evidence from POS + payment data, generates professional dispute responses, and — when confidence is high — submits responses automatically.

**Core goals**

- **85% automation rate** — most straightforward / high-confidence cases handled without human touch
- **≥70% dispute win rate** — realistic target when using rich POS metadata + strong behavioral scoring
- Focused on restaurant-typical fraud patterns: “I didn’t order this”, “item missing”, friendly fraud, account takeover after delivery, etc.

**Technology highlights**

- Fraud scoring engine: re-implemented **LBSF** (Long-term Payment Behavior Sequence Folding) — very effective at detecting anomalous long-term customer behavior
- Agent framework: **LangGraph** multi-step reasoning & tool-calling workflow
- LLM: Grok / GPT-4o / Claude / Hunyuan for natural-language evidence writing
- Integrations: Stripe Disputes API, Square Disputes, Toast / Clover / Lightspeed order lookup (API or CSV)
- Optional: Streamlit dashboard for monitoring & manual review queue

Status: starter implementation + demo flow — ready to connect real POS & payment data

```text

restaurant-fraud-investigator-agent/
├── README.md
├── requirements.txt
├── .env.example
├── config.py
├── main.py
├── models/
│   └── lbsf_model.py
├── agents/
│   └── fraud_investigator_agent.py
├── tools/
│   ├── payment_integrations.py
│   ├── evidence_generator.py
│   └── dispute_submitter.py
├── utils.py
├── data/
│   └── sample_transactions.csv
└── dashboard/
    └── app.py
