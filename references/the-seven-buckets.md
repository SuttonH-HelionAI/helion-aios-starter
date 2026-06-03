# The Seven Buckets: The Map of Your Business

> Before you wire anything, you map. Every business, whatever it sells, runs on the same seven buckets. Name what lives in each and your AIOS knows your whole business. Nothing important falls outside these seven.

These seven buckets are the **what** of your business. The four layers in `the-architecture.md` are the **how** your AIOS handles them. The buckets are also the seven domains in `connections.md`, the Reach layer made concrete.

---

## The seven buckets

| # | Bucket | What lives in it | Engine it feeds |
|---|---|---|---|
| 1 | **Revenue** | Where money lands and how you track it. Stripe, Shopify, bank, the spreadsheet you check. | Growth |
| 2 | **Customer** | Every touch with the people who pay you. CRM, support, reviews, DMs. | Growth |
| 3 | **Calendar** | What is scheduled and what is due. Your calendar and anything time-based. | Both |
| 4 | **Comms** | The inboxes and channels you live in. Email, Slack, DMs, phone. | Both |
| 5 | **Tasks** | Projects and to-dos, where work is tracked. ClickUp, Asana, Linear, a notebook. | Fulfillment |
| 6 | **Meetings** | Recordings, notes, and what got decided. Granola, Otter, Fireflies. | Fulfillment |
| 7 | **Knowledge** | Docs and files, the truth of the business. Drive, Notion, Dropbox. | Both |

---

## How the buckets fit the OS

The buckets are the what. The four layers are the how. Each layer does one job with every bucket.

- **Memory** knows what is in each bucket. Your business map. Lives in `context/business-map.md` once you fill it (or run `/onboard`).
- **Reach** connects the live tool behind each bucket. Lives in `connections.md` and `references/{tool}-api.md`.
- **Hands** does real work across the buckets, on command. Lives in `.claude/skills/`.
- **Pulse** runs the buckets while your laptop is closed. Scheduled and triggered work.

---

## The move: one bucket at a time

Do not connect all seven at once. That is how people stall.

1. **Pick the bucket that eats your week.** The one that costs you the most time or money right now.
2. **Map it in Memory.** Write what lives in it and which tool holds it.
3. **Wire it in Reach.** Connect that one tool, and save `references/{tool}-api.md`.
4. **Next bucket.** Repeat the loop.

`/audit` scores every bucket and names the biggest gap. `/level-up` scopes and ships the next one. One bucket a week and you cover all seven inside two months.

> A bucket is not "done" when the tool is connected. It is done when your AIOS can answer a real question from it faster and more correctly than you can. That is the litmus test, applied one bucket at a time.
