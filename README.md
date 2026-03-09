# Task: World Monitor–Style Intelligence Dashboard

**Reference:** [koala73/worldmonitor](https://github.com/koala73/worldmonitor)  
**Deadline:** 12 March  
**Reviewer (GitHub):** @enghamzasalem

---

## Objective

Build a **real application** that produces the **same kind of output** as World Monitor:

- **Unified dashboard** — news aggregation and situational awareness
- **Interactive map** — toggleable layers or a single clear map view
- **AI-synthesized briefs** — e.g. “World Brief” using **Ollama** and/or **Qwen** (lightweight LLMs)
- **Real architecture** — database, API layer, optional cache
- **Live deployment** — app reachable online
- **LLM on server** — Ollama or Qwen running on a VPS (or equivalent) and used by your API

You may deliver a **simplified subset** (fewer feeds, one map mode, one brief type) but it must be a **working, deployed system** with DB + API + LLM.

---

## Must Have

| # | Requirement | Acceptance |
|---|-------------|------------|
| 1 | **Database** | Persistent store (PostgreSQL, SQLite, Supabase, etc.) for feeds metadata, cached headlines/digests, and optionally briefs. |
| 2 | **API** | REST (or RPC) endpoints: feed digest (news), map data (layers/events), **AI brief** calling your LLM. |
| 3 | **Ollama / Qwen** | Backend calls **Ollama** (local or VPS) and/or **Qwen** (e.g. Qwen2-1.5B/7B) for summarization/briefs. |
| 4 | **Same output type** | Dashboard shows: aggregated news by category/source, map (or geo view), and **AI-generated brief** text like World Monitor’s “World Brief”. |
| 5 | **Live deployment** | App (frontend + API) deployed and reachable (Vercel, Railway, Fly.io, VPS). |
| 6 | **LLM on server** | Document and show **Ollama** or **Qwen** running on a server and used by your API (e.g. `OLLAMA_HOST` or Qwen API URL). |

---

## Optional

- Multiple variants (World / Tech / Finance) or tabs
- Redis/Upstash caching for digest and briefs
- PWA / installable frontend
- Use a **hidden/private branch** and add **@enghamzasalem** as reviewer so the fork is not exposed publicly

---

## Deliverables

1. **Repo (or fork)** with:
   - App code (frontend + API + DB)
   - DB schema or migrations / setup instructions
   - `.env.example` (API URL, DB URL, Ollama/Qwen endpoint)

2. **Docs:**
   - How to run locally (DB, API, frontend, Ollama/Qwen)
   - How the app was deployed (live URL)
   - How Ollama or Qwen was deployed on the server (VPS steps or link)

3. **Pull request (or submission)** with:
   - Short architecture summary (DB, API, LLM)
   - Live app URL and LLM API URL if applicable
   - Screenshot or short video: news digest + map + AI brief

4. **Reviewer:** Add **enghamzasalem** on GitHub with access to the repo/branch.

---

## “Same output” definition

- **News:** Headlines (and optional descriptions) grouped by source or category (like World Monitor’s RSS panels).
- **Map:** Geographic view (2D or 3D) with at least one data layer (events, feeds, or one global layer).
- **AI brief:** One panel with **LLM-generated text** summarizing recent headlines or a topic (same *type* as World Monitor’s World Brief), from Ollama or Qwen via your backend.

---

## Constraints

- **Deadline:** 16 March
- **LLM:** Use lightweight models (e.g. Ollama `llama3.2`, `qwen2:1.5b`, or small Qwen on VPS)
- **Visibility:** Code can live in a **hidden/private branch**; share with @enghamzasalem for review only

---

## Submission checklist

- [ ] DB in use (schema or migrations documented)
- [ ] API: feed digest, map data, AI brief (calling Ollama/Qwen)
- [ ] Frontend: dashboard with news + map + AI brief
- [ ] App deployed and live (URL in PR/README)
- [ ] Ollama or Qwen deployed on server and documented; API uses it
- [ ] @enghamzasalem added for review
- [ ] PR includes: architecture summary, live URL, screenshot/video
