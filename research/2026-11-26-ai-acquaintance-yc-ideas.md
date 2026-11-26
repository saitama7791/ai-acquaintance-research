# AI Acquaintance — what YC just funded in people, relationships and warm intros, and the ten products worth building on this domain

**Research date:** 26 November 2026 · **Scope:** YC batches W25, S25, F25, W26, S26, F26 (1,138 companies) · **Founder profile:** solo, India, 14 years performance marketing, AI automation, cold outreach
**Owner of the domain:** AI Acquaintance

---

## 1. Executive summary

The people layer is being rebuilt, but not where the name suggests.

YC's last six batches contain **no company whose core product is a warm-introduction engine**. What YC funded instead is the raw material for one: people-data APIs (Ploid, Autumn, CLODO), AI-native CRMs (item, Fixture), recruiting systems that rank candidates but never say *who can reach them* (Elip, Perfectly, Spott), community platforms that match members crudely (Bubble Lab at $99–$1,499/mo), and personal assistants whose main churn driver is failing to remember people (Pally, Pickle, Caddy).

The gap is consistent across all eight themes I grouped: **everyone can find a person; almost nobody can prove a path to them.** That is exactly what "acquaintance" means, and it is the one thing a marketer with a cold-outreach machine can sell before the product is finished.

**Recommendation: build Idea 1 (Acquaintance Graph, 8.5/10) and use Idea 2 (Conference Acquaintance, 8.4/10) as the wedge.** Same engine — a person-to-person graph with path scoring — sold first to event organisers, whose attendee lists are handed over as CSV (no OAuth review, no scraping), then to revenue teams at $149/seat/month. Two buyers, one codebase, and a proprietary dataset that compounds every event.

The two scores are within noise; the sequencing decision is about **data access, not market size**.

**The credit stack is real, and it is mostly fast.** Verified on 26 Nov 2026: Cloudflare $10k (live website is the gate), Google for Startups $2k self-serve, AWS Activate Founders $1k–$5k, Microsoft $200–$1,000 starter, MongoDB $15k, ElevenLabs $5,500+ in voice. That is a **$13.2k floor and a ~$38.5k ceiling** of usable infrastructure for a solo founder with a live MVP and no funding. OpenAI and Anthropic are closed to him (partner-VC-gated and cohort-full respectively) — do not plan around them.

---

## 2. Method and what was verified

| Step | What was done | Result |
|---|---|---|
| Data | YC directory dataset (6,409 companies, fields incl. batch, one-liner, tags, team size) pulled 26 Nov 2026 from `yc-oss.github.io` mirror of the YC directory | 1,138 companies in the six batches (W25 164, S25 166, F25 146, W26 198, S26 226, F26 238) |
| Filter | Two-layer keyword scan over one-liner, long description, tags, industry | 203 core hits, 433-company pool → **56 manually triaged** (28 core, 28 adjacent) |
| Liveness | Every shortlisted company's website fetched with a browser user agent | **56/56 returned HTTP 200** on 26 Nov 2026; page titles recorded and used to catch pivots |
| Enrichment | Funding + traction per core company (press, App Store API, GitHub, pricing pages, Launch YC) | 31 rows; **5 with public funding**; the rest honestly `not public` |
| Demand | 21 verbatim quotes across 7 pain clusters (Reddit, Capterra) | All 7 clusters covered; 5 quotes re-verified by me directly against the live thread |
| Credits | 12 programs read on the vendor's own page | 12 verified; 2 effectively closed (OpenAI, Anthropic) |

**Verification note.** Subagent output was treated as claims, not facts. I re-fetched and confirmed: the Pally $5.2M round (Business Insider), Pocket's $11M and 130,000+ units (TechCrunch), Artificial Societies' $5.35M (Business Insider), Ploid's $200/$600 pricing, Autumn's $20–$2,400 pricing, Bubble Lab's four tiers, CLODO's customer page, Cloudflare's $10k Tier 3, MongoDB's $15k ceiling, ElevenLabs' 33M characters, and five Reddit quotes used as evidence below. Anything I could not confirm is labelled `not public` or `not verified`.

**Known limits.** Most YC companies never announce funding, so "funding not public" does not mean unfunded. Reddit hides vote counts on many threads, so engagement is often `not visible`. G2 blocks automated reads (CAPTCHA), so review evidence comes from Capterra and Reddit. My keyword scan can miss a company whose one-liner avoids the vocabulary — the 12-company "additional" pass found only 3 that survived verification, which suggests the shortlist is close to complete, not that it is perfect.

---

## 3. Step 1 — the YC scan

### 3.1 Core: people, relationships, memory, introductions (29 companies, 28 shortlisted + 1 added on review)

| Company | Batch | One-line pitch | Funding | Traction signal (verified) |
|---|---|---|---|---|
| **Autumn** | W26 | The people-intelligence company — "an index of every person in the world: relationships, work history, contact info" | not public | Live pricing $20–$2,400/mo; claims Brex, Rippling, PostHog in production (company claim) |
| **Ploid** | F26 | The people data company for the agent era — "the living index of people" | not public | Live pricing: $200/mo Growth, $600/mo Scale; API + MCP + CLI |
| **CLODO** | S25 | Planet-scale people discovery | not public | "1000+ organizations" on customer page; Mercor, Ergo, Flagright, Antler-backed founders quoted |
| **item** | F25 | The AI-native CRM that works for you | not public | Named customer testimonials on homepage (AgentMail, Wordware) |
| **Fixture** | W26 | An agentic CRM built for startups | not public | Product live behind login; no pricing or logos public |
| **Minro** | F25 | Identify churn risk and stay close to users at scale | not public | Self-reported uplift stats only; no named customers |
| **Caddy** | F25 | Personal AI that lives in your texts | not public | iOS app live, 47 App Store ratings |
| **Logical** | F25 | Proactive AI that knows what's important | LKR 150M+ (USD undisclosed) | Launch YC post live |
| **Char** | S25 | AI notepad that knows and works for you | not public | **Pivoted** — char.com now serves "Char Is Now Anarlog" (May 2026) |
| **Epicenter** | S25 | Portable, open memory for AI | not public | 4,844 GitHub stars; local-first |
| **Pally** | S25 | Personal AI assistant you text | **$5.2M** (Aug 2026), $30M valuation | Pro ~$25/mo, $200/mo tier; free base tier |
| **Pickle** | W25 | Personal AI agent network for Asia | **~$4.42M** (6B KRW, Jun 2025) | Base Ventures led; avatar user base grew 5× in a month (same article) |
| **Oki** | W25 | The memory computer for your digital life | not public | Hardware pre-orders $2,299; ships Q1 2027 |
| **Pocket** | W26 | Take notes in the real world | **$11M** (Jun 2026) | 130,000+ units sold; $129 device + $200/yr plan |
| **Vexo** | F26 | AI bracelet that remembers your day | not public | Pre-orders $99 (from $199); ships 30 Jan 2027 |
| **Liva AI** | S25 | Building socially intelligent AI | not public | Launch YC post; site is a JS shell |
| **Artificial Societies** | W25 | Foundational model of human societies | **$5.35M** (Aug 2025) | Point72 Ventures led; sells simulation research |
| **A1Base** | W25 | The social network layer for AI apps | not public | Site is a shell; no pricing or customers readable |
| **Maywood** | W26 | Proactive AI that tracks relationships across LinkedIn, news, conferences | not public | Request-access only |
| **Bubble Lab** | W26 | Intelligence layer for communities and events | not public | Live pricing $99 / $499 / $799 / from $1,499 per month + 1% of payments |
| **Lyon** | F26 | Foundation models on enterprise event data | not public | Minimal site |
| **Elip AI** | W25 | "Good matches have reasons" — AI career agent | not public | Live pricing: candidates free, companies pay 10% of first-year salary |
| **Perfectly** | W26 | The AI-native recruiting OS | not public (founder post claims $25M valuation) | Launch YC post; claims Giga, Corgi, LlamaIndex, Porter |
| **Spott** | W25 | AI-native ATS/CRM for recruiting firms | not public | 50-person team |
| **Contrario** | W25 | AI hiring platform powered by expert recruiters | not public | 20-person team |
| **Sorce** | F25 | Tinder for jobs | not public | Live paid plan $14.99/week or $39.99/month |
| **RealRoots** | S25 | IRL friendship app for women | not public | 1,269 App Store ratings; $289 paid 7-week programme |
| **Quippy** | F26 | "The gym, but for your social life" | not public | 99 App Store ratings; 4 open roles |
| **Yam** | F26 | AI romance sims for women | not public | In-app purchases $0.99–$19.99; 24 ratings |

Adjacent but strategically important: **OneStop** (S25, local social, 7 ratings, NYC-only), **Anywhere** (F26, "the map of your life" built by the Zenly/Bump team), **Blue** (S25, $1,299 phone that reads every message and drafts replies), **Locata** (S25, AI referral automation in primary care), **Ergo** (W25, "context layer that helps revenue teams close"), **Cedar** (W25, mid-funnel sales workspace), **Clean** (F26), **Frontrunner** (F26), **Cardinal** (W26), **GatherHQ** (F26) — the revenue-context cluster that will compete for the same buyer as any warm-intro product.

Full 56-row list with page titles and HTTP status: `data/yc-scan-56.csv`. Enrichment: `data/yc-funding-traction.csv`.

### 3.2 What the scan says about the six batches

- **W25** was the CRM-and-memory batch: item, Minro, Logical, Oki, Pickle, A1Base, Spott, Contrario, Elip.
- **S25** was people-search and consumer social: CLODO, Pally, Epicenter, RealRoots, OneStop, Char (later folded), Locata.
- **F25** was thin on this space — one CRM (item), one job-marketplace (Sorce), one assistant (Caddy), one relationship tracker that is really GTM tooling (Minro).
- **W26** produced the two most direct competitors: **Autumn** (people-intelligence API) and **Fixture** (agentic CRM), plus **Bubble Lab** (communities) and the recruiting OS **Perfectly**.
- **S26** had almost nothing in relationships; its people-adjacent output is agent infrastructure (Mosaic, Artil, Inkbox) and career agents (Pluto).
- **F26** is the people-data batch: **Ploid** (living index of people), **Maywood** (relationship tracking), **Lantern** (recruiting), **Anywhere** (personal map), **Quippy** and **Yam** (consumer).

**Nobody shipped the intro.** Eleven companies find people; two store relationships; zero route a warm path between two humans with proof of the connection.

---

## 4. Step 2 — patterns: eight themes, and what is still unsolved

### T1. People-data infrastructure — "the index of everyone" (6 companies: Autumn, Ploid, CLODO, The Hog, Leadbay, Bystreet)
**Investors are betting** that agents, not humans, will be the main buyers of people data, so the winning product is an API with credits and an MCP endpoint, not a UI. Autumn's own copy says it plainly: *"People research as a primitive."*
**Still unsolved:** depth of relationship. These indexes know where someone worked; they do not know who trusts them, who introduced them, or whether an intro would be welcome. Coverage outside the US is patchy — a real opening for an India-based founder.
**Who pays:** sales teams ($200–$2,400/mo), recruiters, investors doing deal sourcing, risk teams.

### T2. Relationship memory for individuals (10: item, Fixture, Minro, Caddy, Char, Epicenter, Pocket, Vexo, Oki, Logical)
**Betting on** passive capture — hardware (Pocket 130k units, Oki $2,299), wearables (Vexo), iMessage (Caddy), desktop copilots (Logical) — because manual CRM entry always dies.
**Still unsolved:** the admin problem. The most upvoted advice in the personal-CRM threads is that a tool *"has to be easy enough to update right after meeting someone. The second it starts feeling like admin work, it's probably gonna get abandoned."* And the memory itself is unreliable: a paid companion user's complaint is that *"it has terrible memory, it can't remember anything we talked about in the past except for my name."*
**Who pays:** prosumers at $15–$25/mo (Pally), hardware buyers at $129–$2,299, teams at $20–$850/mo (Autumn, item).

### T3. Warm introductions and the who-knows-whom graph (4: A1Base, Maywood, Ergo, Cedar — none of them actually an intro engine)
**Betting on** context as a sales weapon, but building it as a personal assistant or a data layer.
**Still unsolved:** the org-level question. From r/sales, four days before this report: *"The problem was that nobody on the team knew who knew whom. Our contacts lived in phones, LinkedIn, inboxes and mostly in our heads. So warm intros happened by luck, not by process."* No funded product answers that with a ranked path and a ready-to-forward blurb.
**Who pays:** the first sales hire and the founder who is still selling; later, heads of sales at $100–$200/seat.

### T4. Recruiting through the network (11: Elip, Perfectly, Spott, Contrario, Vela, Lantern, Sorce, Outship, Ovlo, Pluto, G LNK)
**Betting on** agency-style economics — Elip charges 10% of first-year salary, which means the buyer already pays five figures per hire and will pay for a better path.
**Still unsolved:** warm paths into passive candidates. Recruiters say it themselves: *"In a tight niche, I get way more out of referrals from people who said no than from any search tool"*, and the best-performing recruiters start with their own database, *"This step alone has helped me close roles faster than any cold sourcing channel."* The graph is the product; the profile is a commodity.
**Who pays:** boutique agencies ($500–$2,000/recruiter/mo), in-house TA ($20k–$100k/yr).

### T5. Communities and events (7: Bubble Lab, Lyon, OneStop, Anywhere, RealRoots, Quippy, TryNearby)
**Betting on** the IRL revival and on operators who already monetise membership. Bubble Lab's price ladder — $99 to $1,499/mo plus 1% of payments — proves community operators pay real money for member intelligence.
**Still unsolved:** matching quality and cross-event memory. Organisers report attendees *"had difficulty identifying others from similar work fields"* even at a 150–250 person event, and the buying conversation in community circles is still "is random matching good enough?" (Donut $59/mo, Intros $199/mo).
**Who pays:** community operators, event organisers, sponsors buying qualified meetings.

### T6. Companions and agents that know you (7: Pally, Pickle, Yam, Quippy, Moonshot, Sentient OS, Blue)
**Betting on** text/voice as the interface and memory as the moat. Pally raised $5.2M at a $30M valuation on exactly that thesis: *"Relationships are the single most important thing in our lives."*
**Still unsolved:** trust and retention. The cancellation threads are public inventories of broken memory and billing complaints; consumer AI churn is 5–8%/month territory.
**Who pays:** consumers, $15–$200/mo. High volume, thin margins, brutal CAC.

### T7. Agent identity, inboxes and messaging (7: A1Base, Artil, Agent Relay, Mosaic, Inkbox, AgentMail, ZeroSettle)
**Betting on** agents needing their own phone numbers, inboxes and social presence before they can act on a human's behalf.
**Still unsolved:** consent and reputation. If my agent talks to your agent, who authorised the introduction, and what stops it from becoming spam at machine speed? Nobody in this batch sells "agent-safe introductions" — a plausible 2027 wedge.
**Who pays:** developers, then revenue teams.

### T8. Revenue context and meeting prep (11: Ergo, Cedar, Caretta, Peppr, GatherHQ, Nex, Quotain, Nixo, Cardinal, Clean, Frontrunner)
**Betting on** the pre-call and in-call moment. Reps describe the job in their own words: *"After an hour or two, I have 30 or 40 tabs open"*, and the top-voted answer to "what do you do before every meeting" is *"Research. Know everything you can about the people you're meeting with."*
**Still unsolved:** the *person's* history with your company. These tools brief on the account; none of them say "you met her at Web Summit in 2023, she asked about pricing, and Ravi introduced you."
**Who pays:** sales orgs, $30–$100/seat, often bundled into the CRM budget.

### The one-line conclusion from the patterns

> YC has funded the **supply** of people data and the **storage** of relationships. It has not funded the **routing** of relationships. That is a product-shaped hole, and it is the literal meaning of the domain.

---

## 5. Step 3 — ten products for AI Acquaintance, scored

**Scoring:** six dimensions, 0–10 each, weighted — name fit 10%, YC proof 20%, MVP-in-14-days 20%, credit-program fit 10%, founder edge 20%, willingness to pay 20%. Equal weighting would not change the top three. Full per-idea detail (pitch, buyer, evidence, competitors, model, MVP, edge, risks) is in `data/ai-acquaintance-ideas-scored.csv`.

| # | Idea | Type | Score /10 | Name | YC proof | MVP | Credits | Edge | WTP | Verdict |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Acquaintance Graph | B2B | **8.5** | 9 | 9 | 7 | 8 | 9 | 9 | Build this |
| 2 | Conference Acquaintance | B2B | **8.4** | 10 | 8 | 8 | 8 | 10 | 7 | Fastest cash |
| 3 | Warm Path Recruiting | B2B | **8.0** | 8 | 9 | 7 | 8 | 8 | 8 | Vertical of #1 |
| 4 | Community Member Memory | B2B | **7.7** | 9 | 8 | 7 | 8 | 8 | 7 | Fast proof |
| 5 | Customer Referral Graph | B2B | **7.4** | 8 | 7 | 8 | 8 | 7 | 7 | Expansion module |
| 6 | WhatsApp Personal CRM | Prosumer | **7.2** | 8 | 7 | 8 | 6 | 9 | 5 | Consumer bet |
| 7 | Founder Warm Paths | B2B2C | **7.0** | 9 | 6 | 9 | 7 | 6 | 6 | Lead magnet |
| 8 | Acquaintance Companion | B2C | **6.9** | 10 | 7 | 7 | 5 | 8 | 5 | Weakest |
| 9 | People Memory API | B2B | **6.8** | 7 | 8 | 9 | 9 | 4 | 5 | Internal only |
| 10 | Alumni & Accelerator Network OS | B2B2C | **6.8** | 9 | 6 | 7 | 7 | 7 | 6 | Slow, trusted |

### 5.1 Idea 1 — Acquaintance Graph (8.5/10) · *the recommendation*

**Pitch.** The who-knows-who graph for a revenue team: ask which colleague can warm-intro you to a target buyer, and get a ranked path plus a two-line blurb the connector can forward in ten seconds.

**Customer.** B2B. Seed-to-Series-B SaaS with 5–50 quota carriers, a CRM full of dead contacts, and a first sales hire who is already trying to do this in Slack by asking "does anyone know someone at X?"

**Problem and evidence.** From r/sales (22 Nov 2026): *"The problem was that nobody on the team knew who knew whom… So warm intros happened by luck, not by process."* From r/SalesOperations: SDR teams *"spending like 4 hours a day just verifying if contacts were still valid"* — the substitute behaviour is manual list-work, not a product. The paying alternative, CLODO, has 1,000+ organisations and quotes customers closing $1M+ ARR from one hyper-specific outreach (`clodo.ai/customers`) — proof the buyer exists, without proving the *path*.

**Competition.** CLODO (people search), Autumn (people-intelligence API), Maywood (relationship tracking + outreach drafts), Ergo (revenue context), item and Fixture (CRM). Differentiation: **they index people, we rank relationships.** The unit of output is not a profile, it is a ranked path with an owner, a strength score and a draft intro — and it lives in Slack where the ask already happens.

**Model.** $149/seat/month; $999/month for a 10-seat team; $2,000 one-off data setup. Land with 5 seats, expand by team.

**MVP in 10–14 days.** CSV/LinkedIn-export and CRM-export upload → entity resolution into one person record → graph edges from shared employer, school, past deal, past email thread → Slack slash-command `who can intro me to <person/company>` → ranked paths with evidence ("worked together at Freshworks 2019–2021") → intro draft. No OAuth in v1: uploads only, which removes the single biggest schedule risk.

**Founder edge.** He sells to exactly this buyer already and can run 300 cold emails plus a LinkedIn ad set for under $500. The measurable funnel (intro requested → accepted → meeting) is a performance-marketing artefact, and publishing those benchmarks monthly becomes the content moat.

**Risks.** Google/Microsoft restricted-scope verification (CASA) if OAuth is added later — weeks, not days; LinkedIn scraping violates ToS if used; employee graphs are sensitive personal data (GDPR, India DPDP Act 2023) requiring per-user consent, encryption, retention limits and deletion; one spammy intro campaign can burn the brand permanently, so intros must be human-sent by design.

### 5.2 Idea 2 — Conference Acquaintance (8.4/10) · *the wedge*

**Pitch.** Attendee-list intelligence for organisers and sponsors: who in this room should meet whom, and the intro that makes it happen.

**Customer.** B2B. Event organisers of 200–2,000 person B2B events, and the sponsors who pay for qualified meetings.

**Problem and evidence.** An organiser of a 150–250 person networking event reports *"the difficulty attendees had identifying others from similar work fields"* (r/EventProduction). Before the event, buyers cannot even see the room: *"How do you even know who's going unless the event publishes a full list which most don't?"* (r/Entrepreneurs). On the sell side, Bubble Lab's live pricing shows community and event operators paying $99–$1,499/month for member intelligence, and exhibitors are told they *"spend thousands on booth space but won't invest a few hundred in proper lead follow-up"* (r/b2bmarketing) — the gap is follow-up and matching, not booth space.

**Competition.** Bubble Lab (W26), Lyon (F26), OneStop (S25), plus Donut ($59/mo) and Intros AI ($199/mo) in community matching. Differentiation: they run the community or the event page; we **score the pair** and hand both sides a reason to meet. Output is a per-attendee "meet these five" brief and a sponsor report of meetings booked.

**Model.** $499–$1,499 per event; $2,500–$10,000 sponsor meeting package. Paid per event, which suits both the buyer's budget cycle and a solo founder's cash needs.

**MVP in 7–10 days.** Upload Luma/Eventbrite/CSV → enrich (role, company, links) → goal capture at registration (3 chips: "hiring", "raising", "selling", "learning") → pair scoring → attendee brief + organiser dashboard + sponsor report.

**Founder edge.** Event organisers are a listable, cold-emailable ICP, and his paid-social playbook works on them. He can also run his own 50-person paid event as a live demo, which doubles as content and as graph seed data.

**Risks.** Attendee data makes the organiser the controller and him the processor — needs a DPA and opt-in for matching; budgets are seasonal (Sept–Nov, Feb–May); if match quality is poor, organisers churn after one event, so the first three events must be hand-curated.

### 5.3 Idea 3 — Warm Path Recruiting (8.0/10)

**Pitch.** For boutique recruiters: the warm path into a passive candidate, computed from the firm's own placements, alumni and client network.
**Customer.** B2B — boutique recruiting firms and in-house TA filling niche technical roles.
**Evidence.** *"In a tight niche, I get way more out of referrals from people who said no than from any search tool"* (r/RecruitmentAgencies); *"This step alone has helped me close roles faster than any cold sourcing channel"* (r/recruiting, on starting with the internal database).
**Competition.** Elip (10% of first-year salary), Perfectly, Spott, Contrario, Vela, Lantern. They source and rank candidates; none ranks **who inside the firm can reach them**.
**Model.** $799–$999/recruiter/month. One placement pays for a year.
**MVP.** ATS export → co-employment and submission history → path ranking for a candidate URL → referral-ask drafts → path-conversion log. 10–14 days.
**Edge.** Recruiting firms are a classic cold-email ICP and a 20-firm pilot produces a defensible case study in six weeks.
**Risks.** Fast churn, candidate-data compliance (GDPR), and dependence on ATS hygiene. Best run as a vertical of Idea 1 rather than a separate company.

### 5.4 Idea 4 — Community Member Memory (7.7/10)

**Pitch.** Member memory and matchmaking for paid communities: know every member, who they should meet, and who is drifting away.
**Customer.** B2B — operators of paid Slack/Discord/WhatsApp communities, 200–5,000 members.
**Evidence.** Community operators already buy matching at *"Intros charge $199/mo (or $169/mo if billed annually). Donut is $59/mo"* (r/CommunityManager), and the thread debates whether random matching is good enough. Bubble Lab's $99–$799 tiers prove the budget line.
**Competition.** Bubble Lab, Donut, Intros AI, Circle and Discord native features.
**Model.** $149–$499/month by member count.
**MVP.** Slack app (channels only, never DMs) + CSV import → member profiles from messages and onboarding → weekly "these five should meet" digest → 30-day drift alerts → intro drafts in the operator's voice.
**Edge.** Community operators are creators and course sellers — his paid-social and cold-DM playbook is built for this buyer, and India's cost base supports done-with-you setup.
**Risks.** Slack app review, member consent to profiling, and a single wrong digest kills trust.

### 5.5 Idea 5 — Customer Referral Graph (7.4/10)

**Pitch.** Turn happy customers into warm intros to target accounts: which customer already knows the buyer you want.
**Customer.** B2B — account-based SaaS and services firms with 50–500 customers.
**Evidence.** Same r/sales warm-intro thread; Cedar, Ergo, Cardinal and Clean all sell adjacent revenue context, none sells customer-to-prospect paths.
**Model.** $499–$1,500/month by customer count.
**MVP.** Customer + target lists → two-sided enrichment → edge scoring → "do you know X?" draft → intro/meeting log to CRM.
**Edge.** Advocacy and referral asks are marketing motions, so he can sell to CMOs, not just sales ops.
**Risks.** Customer-list access needs a DPA; overlap may be thin; fragments focus from Idea 1. Best as an expansion module.

### 5.6 Idea 6 — WhatsApp Personal CRM (7.2/10)

**Pitch.** A personal CRM that lives in WhatsApp: forward a chat, and it remembers the person, the promise and the follow-up.
**Customer.** Prosumer — founders, consultants and salespeople in India, UAE and Singapore who run their network on WhatsApp.
**Evidence.** *"I forget how I met someone, what we discussed, or why I planned to follow up"* (r/CRMSoftware); the top reply warns the tool *"has to be easy enough to update right after meeting someone."* Pally proves the price point: ~$25/mo pro, $200/mo with its own number.
**Model.** $12/month or ₹499/month; $99/year.
**MVP.** WhatsApp Cloud API number → forward/CC a chat or voice note → LLM extracts person, context, promises, dates → person card → weekly follow-up digest → natural-language search.
**Edge.** Consumer subscription growth on Meta is literally his 14-year job: creative testing, CAC discipline, a WhatsApp-native funnel. India's cost base makes ₹499 viable where a US competitor cannot go.
**Risks.** WhatsApp Business API policy on assistant use, DPDP consent, low Indian ARPU forcing volume, and memory errors that damage real relationships.

### 5.7 Idea 7 — Founder Warm Paths (7.0/10)

**Pitch.** For founders raising: map your network to the funds you are targeting and show the shortest warm path to each partner.
**Customer.** B2B2C — pre-seed and seed founders raising in the next 90 days.
**Evidence.** Conference and network-visibility pain (r/Entrepreneurs); YC's own fundraising stories show how much of the outcome is who introduces you (Artificial Societies' founders simulated their own raise before pitching — Business Insider).
**Competition.** OpenVC, NFX Signal, VC newsletters — no YC company in the six batches owns this.
**Model.** $49/month during a raise; $199 one-off report. No success fees, ever.
**MVP.** Contact upload → seeded fund/partner list → path scoring → intro drafts → ask tracker. 7–9 days.
**Edge.** A free "who can intro you to <fund>" tool is a perfect lead magnet in his content + paid-acquisition motion.
**Risks.** 2–3 month customer lifetime, spam optics, thin moat. Treat as top-of-funnel, not the company.

### 5.8 Idea 8 — Acquaintance Companion (6.9/10)

**Pitch.** A companion that remembers your real people: it keeps the thread with friends and family warm and tells you what to say next.
**Customer.** B2C — busy 28–45 professionals with large, decaying social circles (US/UK first).
**Evidence.** The churn reason for paid companions is memory: *"it has terrible memory, it can't remember anything we talked about in the past except for my name"* (r/ReplikaOfficial); *"I'm done paying for an app that constantly lets me down"* (r/CharacterAI, 563-point top reply).
**Model.** $15/month, $99/year.
**MVP.** Onboard 10 key people → log catch-ups by voice → weekly "reach out to these three" with a drafted message → memory Q&A.
**Edge.** Paid social for emotional consumer products is his exact skillset and India builds the creative cheaply.
**Risks.** CAC, 5–8% monthly churn, app-store policy, duty of care. The weakest credit-program and fundability story of the ten.

### 5.9 Idea 9 — People Memory API (6.8/10)

**Pitch.** A memory-of-people layer any agent can call: remember who someone is, how you met, what they care about, when to follow up.
**Customer.** B2B — AI product teams that need persistent people context.
**Evidence.** Epicenter (4,844 stars), A1Base (social layer for AI apps) and Nessie (shared context across Claude/ChatGPT/Cursor) all show demand for portable context; none is a people-specific memory primitive.
**Model.** Free 1k records; $99/month for 25k lookups; $0.02/record.
**MVP.** MCP server + REST: `upsert_person`, `add_interaction`, `recall`, `due_followups`; Postgres + pgvector; deletion endpoint; three demo clients. 7–9 days — the fastest build here.
**Risks.** Near-zero switching cost, labs ship memory natively, and he has no developer audience. **Build it as the internal core of Idea 1, open it later.**

### 5.10 Idea 10 — Alumni & Accelerator Network OS (6.8/10)

**Pitch.** A living who-knows-whom map for accelerators, universities and alumni networks, with member-requested warm intros.
**Customer.** B2B2C — accelerators, incubators, university alumni offices, founder networks (200–20,000 members).
**Evidence.** Consultants describe wanting exactly this for their own network — *"I'm not incredibly good at remembering the names and personal details of people"* (r/consulting) — and CLODO's customer proof shows people-search budgets exist inside programmes.
**Competition.** PeopleGrove, Graduway, Handshake (incumbents); no YC company in the six batches targets this segment.
**Model.** $6k–$20k/year.
**MVP.** Member import + enrichment → cohort/employer/city graph → member intro-request form → operator approval queue → monthly network-density report.
**Edge.** A free "network density audit" is a strong opener to a small, listable buyer set; one accelerator logo validates the company.
**Risks.** 6–9 month sales cycles, procurement, member consent. Good for logos, bad for 30-day cash.

---

## 6. Credit programs: what he can actually get

Verified against each vendor's own page on 26 November 2026. Full table with quoted eligibility language: `data/credit-programs.csv`.

| Program | What is actually available to a solo, unfunded, India-based founder | Speed | Fit |
|---|---|---|---|
| **Cloudflare for Startups** | **$10k** Tier 3, "no minimum funding required"; needs a live public website and public LinkedIn/X/GitHub | 48h review (program FAQ) | 5/5 |
| **Google for Startups Cloud** | **$2k** Start tier (MVP + founded within 24 months); same application is the on-ramp to $200k–$350k after a round | not published | 5/5 |
| **AWS Activate** | **$1,000** self-serve Founders tier, "select participants up to $5,000"; $200k is partner-gated | 5–10 business days | 4/5 |
| **Microsoft for Startups** | **$200** starter without an investor code, $1,000 with one; up to $150k over time with usage | 3 business days | 4/5 |
| **MongoDB for Startups** | up to **$15k** Atlas credits; 7 years or younger, Series B or earlier, live site + LinkedIn | 5 business days | 4/5 |
| **ElevenLabs Grants** | **33M characters / 12 months**, "more than $5,500+ in value", under 25 employees | 1 week | 3/5 (only if the product speaks) |
| **Notion for Startups** | 3 months free with a company domain (6 months needs a partner); under-10-employee founders are routed to 1 month | not published | 2/5 |
| **Vercel for Startups** | up to **$30k** platform credit, but eligibility is hidden behind a contact form / partner network | not published | 2/5 |
| **Stripe Atlas** | **$2.5k** Stripe credits + $500 Treasury bonus, costs $500, creates a US Delaware entity | ~1 business day to incorporate | 3/5 |
| **Supabase** | **$300** and VC-backed only — he does not qualify | 5 days | 1/5 |
| **OpenAI for Startups** | no self-serve path, no published amount; credits route through partner VCs | — | 1/5 |
| **Anthropic Claude Startups** | cohort **closed**, "not accepting new applications"; $100k API credits only via a partner VC | — | 1/5 |

**Week-one application stack (nothing here needs funding, a deck or a referrer):** Cloudflare $10k → Google $2k → AWS $1k → Microsoft $200–$1,000 → MongoDB $15k (only if the product actually uses Atlas) → ElevenLabs (only if voice is in the product). Realistic usable total: **$13.2k floor, ~$38.5k ceiling**, most of it approved inside two weeks. Add Stripe Atlas the moment a US customer or investor needs a Delaware entity.

**How the product story helps.** A people-graph product is a good citizen of these programs: it needs a database with vector search (MongoDB), edge compute and object storage (Cloudflare), an always-on web app (Google/AWS/Azure), and — if voice intros or call notes are in scope — a voice API (ElevenLabs). That maps cleanly onto the tiers that are actually self-serve. A pure consumer companion app maps worse: it mostly consumes model tokens, which is the one category every vendor gates.

---

## 7. The 14-day build plan (Idea 1 + 2, shared engine)

| Days | Ship | Definition of done |
|---|---|---|
| 1–2 | Schema + entity resolution | people, edges (type, evidence, confidence), events, intros; dedupe across CSV sources |
| 3–4 | Enrichment pipeline | role/company/links for 500 attendees in under 10 minutes; cost per 1,000 records logged |
| 5–6 | Matching engine | pair scoring with a stated reason per match; eval set of 50 hand-labelled pairs, precision reported honestly |
| 7–8 | Attendee brief + organiser dashboard | "meet these five" page; sponsor report PDF |
| 9–10 | Slack slash-command | `who can intro me to X` returns ranked paths + drafts |
| 11 | Stripe checkout + per-event pricing | one live paying event or a signed pilot |
| 12 | Instrumentation | intro requested → accepted → meeting, tracked per event |
| 13–14 | Credit applications + public launch post | Cloudflare, Google, AWS, Microsoft submitted; demo event page live |

**Kill criteria, written down before starting:** if 3 of 5 pilot organisers do not get at least one meeting they attribute to the product, the matching thesis is wrong and the build stops. If a revenue team will not pay $149/seat after seeing the Slack demo, the B2B price is wrong, not the product.

---

## 8. Risks that decide whether this is a company

1. **Personal data.** A graph of who knows whom is a graph of personal relationships. GDPR (EU/UK) and India's DPDP Act 2023 both require a lawful basis, purpose limitation, deletion and breach process. Design: per-user consent for contact uploads, organiser as controller for attendee data, no scraping of private data, no training on customer data, published retention.
2. **Platform dependency.** LinkedIn's terms prohibit scraping at scale; Google and Microsoft restricted scopes require a security assessment before OAuth. The CSV-first MVP is a deliberate hedge — but it caps growth until the OAuth path is cleared.
3. **Consent and reputation.** Warm intros are a trust transaction. Machine-generated intros at volume turn the product into a spam cannon and kill the brand in one quarter. Intros must be human-approved, rate-limited, and never sent by the AI on the user's behalf.
4. **Incumbent squeeze.** Autumn and Ploid can add relationship scoring to an API that already has distribution; Bubble Lab can add matching to a platform organisers already run. The defence is the proprietary graph (who met whom, at which event, with what outcome) — which is why the event wedge matters.
5. **Solo-founder concentration.** One founder, one codebase, two buyers. The 14-day plan deliberately ships the event product first because it needs no security review, and holds the Slack product for week three.

---

## 9. What I could not verify

- **Funding for 23 of 28 core companies** — not announced publicly. Their YC standard deal is not company-specific funding and is not reported as such here.
- **Most engagement counts** on Reddit threads (hidden by the platform) and G2 reviews (CAPTCHA-blocked). Capterra and visible comment scores were used instead.
- **Claimed traction**: Autumn's Brex/Rippling/PostHog usage, Perfectly's $25M valuation, Yam's "3+ hours per DAU" — all company or founder claims, marked as such.
- **Cloudflare's 48-hour review claim** appeared in the program FAQ quoted by the researcher; the extract I re-read did not show that line. Treat as "days, not weeks" rather than a guarantee.
- **Whether any YC company in these batches is building a warm-intro engine quietly** — one-liners can hide it. My 1,138-company scan and a second pass found none; that is evidence, not proof.

---

## 10. Sources

**YC data:** `yc-oss.github.io/api/companies/all.json` (6,409 companies, pulled 26 Nov 2026); company sites and pricing pages fetched individually (see `data/yc-scan-56.csv` for the HTTP status of each).
**Funding:** Business Insider — Pally $5.2M (Aug 2026) and Artificial Societies $5.35M (Aug 2025); TechCrunch — Pocket $11M (29 Jun 2026); BusinessKorea — Pickle 6B KRW (Jun 2025); Ada Derana — Logical LKR 150M+ (Jul 2026).
**Demand evidence:** Reddit threads in r/sales, r/SalesOperations, r/salestechniques, r/CRMSoftware, r/CRM, r/consulting, r/recruiting, r/RecruitmentAgencies, r/CommunityManager, r/EventProduction, r/Entrepreneurs, r/b2bmarketing, r/ReplikaOfficial, r/CharacterAI, r/aipartners; Capterra Apollo reviews. Every URL is in `data/market-signals.csv`.
**Credits:** aws.amazon.com/activate, cloud.google.com/startup, microsoft.com/en-us/startups, openai.com/startups, anthropic.com/startups, elevenlabs.io/startup-grants, vercel.com/startups, cloudflare.com/forstartups, mongodb.com/startups, supabase.com, notion.com/startups, stripe.com/atlas — all read 26 Nov 2026.

*Prepared for the owner of AI Acquaintance. Facts are sourced; the ranking, the recommendation and the kill criteria are judgement calls and are labelled as such.*
