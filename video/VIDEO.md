# Sentinel Protocol — Video Pitch Narrative

Script guide for the hackathon submission video (target: 3–5 minutes).
Each slide has an intro line (what to say as the slide appears) and a description (the talking points to cover). Speak naturally — this is a guide, not a teleprompter.

---

## Slide 1 — Cover

**Intro:** "Hey, I'm [your name], and this is Sentinel Protocol."

**Description:**
Open strong. Say the one-liner out loud: "We're building the open-source governance standard for AI agents on Solana." Pause for a beat to let it land. Then deliver the value proposition: "We help developers and DAOs control and govern autonomous AI agents through on-chain permissions, spending limits, and auditing." Don't linger — the cover slide is a handshake, not a speech. Move to the next slide within 10–15 seconds.

---

## Slide 2 — The problem

**Intro:** "Here's the problem we're solving."

**Description:**
Walk through the three stat cards left to right, building urgency with each one. Start with the Drift hack: "Two days ago, Drift Protocol lost $280 million. Not because of a code exploit — because of a governance failure. The multisig was misconfigured, timelocks were missing, and an attacker escalated privileges in minutes." Move to the middle card: "Meanwhile, Solana has already processed over 15 million transactions from AI agents. These agents hold treasuries, execute trades, make autonomous decisions." Finish with the third card: "And yet there are zero standardized protocols for governing what these agents can actually do. That's the gap." Let the "Keys > Code" quote sit for a moment. Total time: about 30–40 seconds.

---

## Slide 3 — Our insights

**Intro:** "We spent months studying this space. Three things became clear."

**Description:**
Cover each insight card as a mini-revelation. First: "Agents in 2026 aren't simple bots. They own wallets, manage liquidity pools, form DAOs. They're economic entities that need governance the same way a company needs a board." Second: "The ecosystem already has identity — Solana's Agent Registry tells you who an agent is. But nobody tells you what it's allowed to do. Identity without governance is like having an ID card in a country with no laws." Third: "And here's the strategic insight — Metaplex didn't win by building the best NFT marketplace. It won by becoming the standard. Whoever defines how agents are governed captures the entire ecosystem, not just one product." Keep this conversational. About 40–50 seconds.

---

## Slide 4 — Market

**Intro:** "Let me show you how big this opportunity is."

**Description:**
Start with the TAM/SAM/SOM circles on the left. Point to them as you speak: "The global agentic economy is projected at $47 billion by 2028. Solana's share of that — agents operating specifically on this chain — is around $8.2 billion." Then shift to the right side: "Here's our math. Solana processes about 15 million agent transactions per month today. Projections show 500 million by 2028. If just 5% of active agents adopt on-chain governance — that's 25,000 paying agents. With an average ticket of $1,370 per month from protocol fees and staking, our addressable market is roughly $410 million a year." The key here is showing you did the work — you didn't just pull a number from a report. About 30–40 seconds.

---

## Slide 5 — Current landscape

**Intro:** "We're not the first to notice this problem. But everyone is solving only a piece of it."

**Description:**
Walk through the four competitor cards quickly — don't bash anyone, just show the gaps. "Agent Registry gives agents identity and reputation, but has no permission system, no spending limits, no kill-switch. SAID Protocol does identity and discovery, but no governance, no timelocks. ElizaOS is a great agent framework, but each agent is an island — no shared governance layer, no auditing. SPL Governance handles DAO voting, but it wasn't built for AI agents — no circuit breakers, nothing AI-specific." Then hit the teal bar at the bottom: "Sentinel combines all of this — identity, governance, permissions, circuit breakers, and auditing — into one composable standard." This is the moment the audience should feel the gap clicking shut. About 30 seconds.

---

## Slide 6 — Why Sentinel stands out

**Intro:** "Here's what we actually built."

**Description:**
Go through the six feature cards. Don't read them — explain them like you're talking to a developer friend. "Permission Framework — granular control over which protocols, tokens, and actions each agent can access. Circuit Breakers — automatic kill-switches that freeze the agent when something looks wrong. Immutable Audit Trail — every action logged on-chain, tied to the agent's verified identity. Spending Policies — daily limits, per-transaction caps, rate limits, all programmable. Multi-sig and Timelocks — critical changes need multiple approvals and a mandatory delay. And the whole thing is composable through our SDK — plugins for ElizaOS, GOAT, ZerePy. Governance in a few lines of code." Speed through these — the next slide is the demo. About 25–30 seconds.

---

## Slide 7 — Risks and mitigations

**Intro:** "We're realistic about the challenges."

**Description:**
Cover each risk/strategy pair honestly. "The biggest risk is slow adoption — developers might resist adding another layer. Our answer: the SDK is drop-in. Three lines of code. We're also partnering directly with ElizaOS and GOAT for native integration." Second: "There's competitive risk — the Solana Foundation could expand Agent Registry into governance. We're positioned as complementary, not competitive. Open-source from day one, and we contribute actively to the ecosystem." Third: "Technical complexity — on-chain governance could add latency. We use a hybrid model: critical validations on-chain, routine checks off-chain with cryptographic proofs. Everything optimized for Solana's sub-400ms finality." Being upfront about risks builds credibility. About 25–30 seconds.

---

## Slide 8 — Sentinel Protocol SDK

**Intro:** "Let me show you what it looks like in practice."

**Description:**
This is the product demo moment. Walk through the code on screen line by line: "You import SentinelGovernor from sentinel-sdk. You create a new governor with your agent's public key. Set a spending limit — 100 USDC per day. Define which protocols the agent can interact with — Jupiter, Raydium. Set a circuit breaker — freeze if losses exceed 5%. Add multisig — two out of three signers must approve critical changes. That's it. Three lines and your agent is governed on-chain." If you have a live demo of the MVP on devnet, this is where you switch to it. Show the agent trying to exceed its limit, getting blocked, circuit breaker activating. The code slide is the fallback if you don't have a live demo ready. About 20–30 seconds for the slide, or 45–60 seconds if you do a live demo.

---

## Slide 9 — Making it happen (use cases)

**Intro:** "Here's how this plays out across different timelines."

**Description:**
Walk through the three columns briefly. "Right now, the immediate use case is trading bot governance — spending limits and kill-switches for the bots already operating on Solana. Plus permissions for x402 payment agents." Move to the middle: "Near future — DAO-governed agent swarms where the DAO votes on what agents can do. Agent marketplaces with trust scores based on governance history." Then the right column: "Long term — cross-chain governance via Wormhole, and automated insurance pools where stakers cover losses from governed agents." The point is showing a path from hackathon MVP to a full ecosystem. About 20 seconds.

---

## Slide 10 — Our traction

**Intro:** "Here's where we are today."

**Description:**
Cover the three metric cards: "We have a working MVP — an Anchor program on devnet with the permission framework and circuit breakers functional. We have three integrations planned for ElizaOS, GOAT, and ZerePy. And we're open-source from day one under Apache 2.0." Then walk the milestone timeline at the bottom: "Research and design — done. Anchor program v0.1 on devnet — done. Next up: TypeScript SDK alpha, then ElizaOS integration." Be honest about what's built and what's planned. Judges can smell fake traction. If you have any additional metrics by recording time — GitHub stars, devnet transactions, community members — mention them here. About 20 seconds.

---

## Slide 11 — Why now

**Intro:** "You might ask — why is now the right time?"

**Description:**
This slide has a split layout. Start with the purple left side to set the frame: "The timing for AI agent governance has never been this clear." Then go through the five reason cards on the right: "Solana has processed over 15 million agent transactions — this economy is real, it's not theoretical. The Drift hack two days ago — $280 million gone because of governance failure — made the need impossible to ignore. The Solana Foundation is actively prioritizing AI infrastructure — Agent Registry, skill files, a developer platform built for agents. Vibhu Norby from Solana Foundation publicly predicted that 99.9% of all on-chain transactions will come from agents by 2028. And ElizaOS has over 17,600 stars on GitHub — the demand for agent tooling has exploded." The "why now" slide is about creating urgency. Don't rush it. About 30–35 seconds.

---

## Slide 12 — Team

**Intro:** "And we're the right team to build this."

**Description:**
Start with the Unfair Advantage card on the left: "Our team has deep experience building Solana programs in Anchor and Rust, background in smart contract security and auditing, and we're active members of Superteam Brazil." Then introduce each team member briefly — name, role, one relevant credential. Don't read bios — just the one thing that makes each person credible for this specific project. "This isn't our first time building on Solana, and it's not our first time thinking about security. We understand the problem because we've lived it." Keep this tight — about 15–20 seconds. Judges care more about what you built than who you are.

---

## Slide 13 — Business model

**Intro:** "Here's how we make money."

**Description:**
Walk through the three revenue pillars: "40% from protocol fees — a minimal fee per governed transaction, about 0.001 SOL. This scales automatically with adoption. 35% from premium tiers — advanced governance features like custom policies, insurance, analytics dashboards for teams managing fleets of agents. And 25% from staking and validator fees — third-party validators stake tokens to audit agent behavior and earn fees for it." Point to the revenue chart at the bottom: "Our projection shows a path to meaningful revenue by month 12, scaling from protocol fees as the number of governed agents grows." Don't oversell the numbers — judges know projections are speculative. About 20 seconds.

---

## Slide 14 — Roadmap

**Intro:** "Here's our plan for the next 12 months."

**Description:**
Walk the timeline left to right, top boxes then bottom boxes. "Q2 2026 — that's now. MVP on devnet, permission framework, circuit breakers. Hackathon submission. Q3 — TypeScript SDK v1, ElizaOS integration, audit trail. Goal: first 10 agents governed. Q4 — mainnet beta, GOAT and ZerePy plugins, governance dashboard. Target: 100+ agents with $50K+ in total value governed. Q1 2027 — token launch, validator network, insurance pools v1. Goal: 1,000+ agents and a self-sustaining ecosystem." Keep this brisk — the roadmap is a reference, not a deep dive. About 20 seconds.

---

## Slide 15 — The ask

**Intro:** "Here's what we need to make this happen."

**Description:**
Be direct. "We're seeking a seed round of $500K, plus the hackathon prize. This capital gets us to 100+ governed agents on mainnet within six months, and to $50K monthly recurring revenue within twelve months." Cover the smart money line: "Beyond capital, we're looking for connections to the Solana Foundation, Multicoin Capital, and the teams building ElizaOS, GOAT, and ZerePy. The right introductions accelerate adoption faster than any amount of code." Close with the note at the bottom: "Every dollar goes toward results — more agents governed, more integrations shipped." About 15–20 seconds.

---

## Slide 16 — Impact phrase

**Intro:** Let the slide speak. Pause for a beat, then read the quote.

**Description:**
Read the quote slowly and deliberately: "If AI agents will control billions in on-chain assets, someone needs to set the rules." Pause. Then: "That someone is us." This is the emotional peak of the pitch. Don't rush it. Don't add anything after. Let it sit for 2–3 seconds of silence before moving to the final slide.

---

## Slide 17 — Contact / closing

**Intro:** "Thank you. Let's talk."

**Description:**
Close with your name, role, and how to reach you. "I'm [your name], founder of Sentinel Protocol. You can reach me at sol-sentinel-protocol@proton.me, follow us at @sln_sentinel_ai on X, or check out the code on GitHub." End with the tagline: "Let's govern the future of the agentic economy — together." Smile. Stop recording.

---

## Production notes

**Total target time:** 3:30 to 4:30. If you're running long, cut time from slides 9 (use cases), 13 (business model), and 14 (roadmap) first — those are reference slides. Never cut time from slides 2 (problem), 8 (product demo), 11 (why now), or 16 (impact phrase) — those are the emotional core.

**Pacing:** Speak slower than you think you should. Hackathon judges watch dozens of videos. The ones that land are the ones where the speaker sounds calm and confident, not like they're racing through material.

**If you have a working demo:** Replace slide 8 with a screen recording of the actual MVP on devnet. Show an agent trying to exceed its spending limit and getting blocked. Show the circuit breaker triggering. Show the audit log entry. A working demo is worth more than any number of slides.

**Recording setup:** Record in a quiet room. Use a decent microphone — laptop mics sound hollow. Screen-record the slide deck in presentation mode and overlay your voiceover. If you appear on camera, keep it to the intro and closing — the slides should be the focus for the middle section.
