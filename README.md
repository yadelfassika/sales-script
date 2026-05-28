# sales-script

A live, scrollable cold-call console. Single static `index.html` — no build, no framework, no dependencies. Open it in a browser and dial.

Built for [Echelon Advising](https://echelon-advising.com), an AI operations and infrastructure company. The script content is calibrated to a specific offer, but the structure (opener → bridge → translation → tactical moves → arsenal → bounces) is reusable for any B2B founder-led sales motion.

---

## The philosophy

> **Your only job in the first 30 seconds is to earn the next two minutes.**

Booked cold calls run around six minutes. Dead ones die at around three. The opener and bridge don't close — they buy minute two, and minute two is where the actual conversation starts. The whole console is built around that reframe.

Everything is written **for the ear**, not the eye. One idea per sentence. Contractions. No nested clauses. Periods where a writer would use commas. Pacing marks rendered inline so you know where to breathe and which word to land on.

---

## What's in it

### 01 — The Open

The first 10 seconds. A disarm-style permission opener that owns the call instead of apologizing for it. Built on Josh Braun's pattern (the self-deprecating ask) plus Chris Voss's no-oriented question construction. Two alternate variants: one for when you have a relevance hook, one for when you're truly dead-cold.

### 02 — The Bridge

The next 30–40 seconds. The line that decides how long they stay. Leads with the problem (a concrete scene they live every week), labels their reality back to them, and only *then* introduces what we do. Ends on a calibrated *which* question — open-ended, presupposes a bottleneck, gets them talking.

### 03 — Translation Grid

The four operational bottlenecks (inbound / follow-up / quoting / outbound) mapped four ways:
- What you say
- What it means to them
- What they say back (the predicted responses)
- Your move

Pull whichever row matches what they tell you in their answer to the calibrated question.

### 04 — Voss Moves

Four tactical patterns from Chris Voss's *Never Split the Difference*, adapted for live cold-call conversation:
- **Label** — "It sounds like…" / "It seems like…" / "It feels like…"
- **Mirror** — repeat their last 2–3 words as a question, then wait
- **Calibrated Question** — what / how questions that give them the illusion of control
- **No-Oriented Ask** — "Would you be opposed to…" frames the next-step ask so "no" is safe

This is the section to reach for when the conversation opens up and you need to keep them talking.

### 05 — Arsenal

Numbers that land (15–20 hrs/week recovered, 4–8 month payback, 25–35% dead-quote recovery, +31% same-day close lift, 90-day deployment).
Positioning lines in plain voice. Qualifier pills (ICP). The close, framed as a no-oriented ask.

### 06 — Quick Bounces

The six most common objections, each starting with a tactical empathy label *before* the redirect:

- It's too expensive
- We tried AI and it didn't work
- I don't have time
- Can't we just use ChatGPT
- Just send me some info
- Not interested

### 07 — Never Say

The phrases and patterns that statistically tank cold calls:

- "Is this a bad time?" (books under 1%)
- "How's your day going?"
- Hedges and filler ("real quick," "basically," "just," "kind of")
- Fear / scarcity framing
- "AI replaces your employees"
- "We advise / consult / hand it off"
- Buzzword soup
- Long sentences with stacked clauses

### Footer — the call math

Average conversation-to-meeting rate is roughly 1 in 20. Best windows: Wednesdays, 8–9am and 4–5pm. Rejection is the math, not you.

---

## Pacing key

The script lines render pacing marks inline so you don't read past your own breath:

- `/` — quick breath
- `//` — full stop, let it sit
- `[beat]` — deliberate silence
- **bold** — hit this word

---

## Sources

The methods and data behind the structure:

- **Gong Labs** — analysis of 300M+ recorded cold calls (opener success rates, call duration patterns, monologue length in winning calls)
- **HubSpot 2025 State of Cold Calling**
- **WHAM 2024 dataset**
- **Chris Voss** — *Never Split the Difference* (tactical empathy, labels, mirrors, calibrated questions, no-oriented questions)
- **Josh Braun** — disarm-style opener methodology
- **30 Minutes to President's Club** — the cold call framework
- **RAIN Group** — B2B buyer behavior data
- **Writing-for-the-ear craft** — Throughline Group, Columbia DS, speechwriting and voiceover practitioners

---

## Deploy

This is a single static HTML file. Any static host works; Vercel is fastest.

### Option A — Dashboard

1. Push this repo to GitHub.
2. Vercel → **Add New → Project** → import the repo.
3. Framework Preset: **Other**. Build/Output: leave empty.
4. Deploy. You'll get a `*.vercel.app` URL immediately.
5. Project → **Settings → Domains** → add your subdomain (e.g. `call.your-domain.com`). If your domain's DNS lives in Vercel, it auto-configures.
6. Optional: **Settings → Deployment Protection → Vercel Authentication** to gate access behind your Vercel login.

### Option B — CLI

```bash
git clone https://github.com/yadelfassika/sales-script.git
cd sales-script
vercel --prod
# attach a subdomain via the dashboard, or:
vercel domains add call.your-domain.com
```

### Local preview

Just open `index.html` in any browser. No server needed.

---

## Update workflow

1. Edit `index.html`.
2. Commit + push.
3. Vercel redeploys automatically.

The console is intentionally one file. Easier to audit, easier to fork, easier to keep current.

---

## Files

```
sales-script/
├── index.html      ← the entire console
├── vercel.json     ← cache + security headers, noindex tag
├── .gitignore
└── README.md
```

No `package.json`, no Node, no build step. By design.

---

## License

MIT. Adapt freely. If you ship something better, send it back.
