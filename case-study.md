# Case Study: RAG-lite Telegram Q&A Bot — Notion/Sheets Knowledge Base + MCP + LangChain + Confidence Gate

**Client Type:** Any business with 50+ FAQs/docs in Notion/Sheets — support Q&A eats 1.5 hrs/day
**Timeline:** 2 hours
**Tools:** Telegram Bot API, Notion API / Sheets API, Gemini API, Groq, Slack API, Make.com, n8n, MCP, LangChain, RAG-lite, Confidence Gate
**Cost to Run:** $0/month free tiers (no Pinecone needed for 50-200 Q&As)

### Problem
Founder has 50+ Q&As in Notion/Sheets. Customers ask same 20 questions via Telegram. Founder manually searches Notion → copy-pastes answer → 5 min per question × 20/day = 1.5 hrs/day. Generic AI bot hallucinates, wrong answers, angers customers. No confidence gate, no escalation.

### Solution
Built RAG-lite + MCP + LangChain + Confidence Gate:

**RAG-lite = Free Stack RAG:** No expensive vector DB. Use Sheets/Notion API as knowledge base + Gemini for retrieval + generation — $0/month, works for 50-200 Q&As (perfect for small biz). For 1000+ Q&As, upgrade to Pinecone — I can build that too.

**MCP = Model Context Protocol:** Model (Gemini) + Context (Retrieved Q&A) + Protocol (Telegram reply or Slack escalation) — standard for advanced AI agents.

**LangChain Pattern:** Retrieve (Search Sheets/Notion for keywords) → Augment (Prompt with retrieved Q&A) → Generate (Gemini answer with confidence)

**Flow:**
1. Trigger: Telegram Bot User Question (Telegram Bot API + Webhook)
2. Retrieve: Search Sheets/Notion knowledge base for keywords (Sheets API / Notion API — RAG-lite Retrieve)
3. Augment + Generate: Gemini generates answer with confidence score + source (Gemini API + MCP + LangChain)
4. Deliver: Router Confidence Gate — ≥80% → Telegram reply with answer + source, <80% or ESCALATE → Slack #support-escalation alert + Telegram "Let me check with team"

### Results
- Time: 1.5 hrs/day → 15 min review, 80% auto-answered in <30 sec, 20% escalated
- Response: 5 min → 30 sec, consistent answers
- Trust: Confidence gate prevents hallucinations — AI escalates instead of guessing — MCP + RAG-lite + LangChain is what advanced founders search and pay $400-600 for
- No Vector DB Cost: RAG-lite uses Sheets/Notion + Gemini — $0/month for small KB

### What Client Gets
- Working scenario + n8n workflow (AI Agent nodes + IF nodes) + blueprint
- Knowledge base template: 20 Q&As in Sheets/Notion — client fills their own
- Loom walkthrough: how RAG-lite works vs RAG, how to add new Q&As, how to adjust confidence threshold, how MCP works
- Documentation: How to swap Sheets to Notion, how to upgrade to Pinecone for 1000+ Q&As, how to change escalation channel
- 7 days support

### Tools & Cost
- Telegram Bot API free, Notion API free, Sheets API free, Gemini free tier (15 req/min), Groq free fallback, Slack API free, Make.com free, n8n free
- Running cost $0 — no Pinecone needed for 50-200 Q&As — client pays for build + upkeep

### Why Premium $400-600
Founders searching "RAG chatbot", "MCP agent", "LangChain bot", "Telegram support bot", "Notion knowledge base bot", "AI support agent with escalation" want exactly this — RAG-lite + MCP + confidence gate + Telegram + Notion/Sheets. Most freelancers can't build RAG. You can, with free stack.

---
Demo: [Add Link] | Portfolio: github.com/aiagentbuilderhq/automation-portfolio
