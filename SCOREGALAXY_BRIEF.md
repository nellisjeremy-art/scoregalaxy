# SCOREGALAXY — Living Project Brief
> Paste this at the start of any new Claude conversation to instantly restore full context.
> Last updated: March 2026 · v1.0

---

## What Is ScoreGalaxy?

A **fan-first sports scores and community app** — a clean, calm alternative to ESPN and
the current ad-infested, gambling-centric sports media landscape. Built for fans who just
want to know if their team won, without being manipulated into staying longer.

**Tagline:** For the Fans. By the Fans.

---

## Core Philosophy (Non-Negotiable)

- **No ads. Ever.**
- **No gambling.** No odds, spreads, parlays, pick promotions. Banned forever.
- **No dark patterns.** No infinite scroll, streak counters, or anxiety-inducing badges.
- **Anti-addictive by design.** Optimize for usefulness per visit, not time-on-app.
- **Fan owned.** The community belongs to fans, not corporate voices.
- **No data brokering.**

**Elevator pitch:** "ESPN but simpler, faster, showing only what you care about."

**Design inspiration:** Basketball GM (play.basketball-gm.com) — utility-first,
dense data tables, monospace numbers, left sidebar nav, zero fluff. The data IS the design.

---

## Current Status

Phase 1 — NBA Web App (IN PROGRESS)

- DONE: PRD v2.0 written (originally FanTrack_PRD_v2.docx — needs rename to ScoreGalaxy)
- DONE: Working prototype → scoregalaxy.html (single file, no build step needed)
- DONE: Live ESPN API (scoreboard, box scores, standings)
- DONE: CORS proxy fallback (works when double-clicking locally)
- TODO: Upload scoregalaxy.html + SCOREGALAXY_BRIEF.md to GitHub repo named "scoregalaxy"
- TODO: Deploy to Vercel for a live public URL
- LATER: Convert to React + Vite project structure

---

## Tech Stack

Current: Single HTML file — vanilla JS, no framework, no build step.

Future:
- Framework: React + Vite
- Styling: Tailwind CSS
- Hosting: Vercel (free, auto-deploys from GitHub)
- Repo: GitHub, name "scoregalaxy"
- NBA live data: ESPN unofficial API (no key, free)
- NBA deep stats: Basketball Reference (tabled — historical/advanced stats)

ESPN API endpoints:
- Scoreboard: https://site.api.espn.com/apis/site/v2/sports/basketball/nba/scoreboard?dates=YYYYMMDD
- Box score:  https://site.web.api.espn.com/apis/site/v2/sports/basketball/nba/summary?event={id}
- Standings:  https://site.api.espn.com/apis/site/v2/sports/basketball/nba/standings?season=2025
- CORS proxy: https://corsproxy.io/?url={encodedURL}

---

## Design System

Aesthetic: Utility-first dark UI. Basketball GM meets Bloomberg Terminal.
Fonts: IBM Plex Mono (numbers/scores), IBM Plex Sans (body/nav)

CSS variables:
  --bg: #0f1117 | --bg2: #161922 | --bg3: #1e2330
  --border: #252c3d | --text: #e2e8f0 | --muted: #8892a4 | --dim: #4a5568
  --accent: #4f8ef7 (blue) | --live: #22c55e (green)

Rules: team color dots not logos · left sidebar nav · mono for all numbers ·
no infinite scroll · dark mode default · play-in line at standings row 6

---

## Features Built (v0.2)

- Live NBA scoreboard (real ESPN data)
- Date navigation prev/next
- Pulsing live game indicator
- Auto-refresh every 45s (today only)
- Favorite teams — starred, highlighted, saved to localStorage
- Edit favorites modal (all 30 teams)
- Box score modal — line scores + full player stats
- East/West standings (W/L/PCT/GB/L10/STRK)
- CORS proxy fallback
- Sidebar nav (Scoreboard / Standings)

---

## Full Roadmap

Phase 1 (Mo 1-2):   NBA MVP → GitHub → Vercel
Phase 2 (Mo 3-4):   NFL, MLB, NHL, MLS. Notifications.
Phase 3 (Mo 5-6):   Accounts (username only). Team forums.
Phase 4 (Mo 7-9):   Fan Persona system. Moderation.
Phase 5 (Mo 10-12): iOS app (React Native / Expo).
Phase 6 (Yr 2+):    College sports, international.

---

## Community Vision (Phase 3+)

- Username + password only. No email. Old-school Reddit.
- No social graph. No followers/following.
- Team forums with auto post-game threads.
- Upvote/downvote, no algorithmic amplification.
- Fan Persona tiers: Fan → Trusted Fan → Fan Correspondent → Mod → Legend
- Hard rules: no gambling, no sponsored content, no bots. Ban = permanent.

---

## Tabled Decisions

ESPN API vs Basketball Reference:
- ESPN = live/real-time. Basketball Reference = deep historical/advanced stats.
- Plan: use both eventually. Revisit when building player pages.

---

## Next Steps

1. Upload scoregalaxy.html + SCOREGALAXY_BRIEF.md to GitHub repo named "scoregalaxy"
2. Connect repo to Vercel → get live public URL
3. (Later) React + Vite conversion
4. (Later) Team pages
5. (Later) Player search

---

## Ideas Bank
> Updated via the dedicated ideas chat. Paste new ideas there.

- Old-school Reddit accounts for community (no email)
- Fan Correspondent verified persona — earned, not paid
- Community-governed sports personas (not follower-count driven)
- Clean design as deliberate anti-ESPN product statement
- Feels like a sports bar scoreboard, not a slot machine
- Dual data strategy: ESPN live + Basketball Reference depth
- "ScoreGalaxy" name opens up space/cosmos visual direction for branding — explore in ideas chat

---

## How To Use This Brief

TECHNICAL CHAT:
  "Here is my ScoreGalaxy project brief: [paste]. Today I want to [task]."

IDEAS/BRANDING CHAT:
  "Here is my ScoreGalaxy project brief: [paste]. Let's brainstorm [topic].
  Update the Ideas Bank with decisions and give me the full updated brief."

KEEPING CURRENT:
  End of each session: "Update the brief to reflect today's work and paste the full file."
  Replace the contents of SCOREGALAXY_BRIEF.md in your GitHub repo.

---

ScoreGalaxy · For the Fans. By the Fans. · Brief v1.0 · March 2026
