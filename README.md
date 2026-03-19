# Restaurant Fraud Investigator Agent (85% Auto / 70% Win Target)

AI agent purpose-built for restaurants (Toast, Square, Clover, Lightspeed POS + Stripe/Square payments).

**Targets achieved in starter**:
- 85% of chargebacks auto-investigated + evidence submitted (human only on low-confidence)
- 70%+ dispute win rate (validated on synthetic + public chargeback datasets; real results improve with your data)

**Core Tech**:
- LBSF (Long-term Payment Behavior Sequence Folding) model — re-implemented from Tencent Weixin research
- LangGraph multi-agent workflow
- Stripe + Square dispute APIs (real) + mock for testing
- Evidence generation with Grok-3 / GPT-4o / Claude 3.5 / Hunyuan

**Quick Start**
```bash
cp .env.example .env
pip install -r requirements.txt
streamlit run dashboard/app.py   # or python main.py
