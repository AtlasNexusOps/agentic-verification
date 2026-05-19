# Agentic Verification — Landing Page

**Landing page redesign for the first on-chain bounty marketplace with ERC-8004 agent identity verification.**

[![Celo](https://img.shields.io/badge/Celo-Mainnet-brightgreen)](https://celoscan.io/address/0x1362d874F40B7e28836cBeCcA14f5EfBe6c6E423)
[![Next.js](https://img.shields.io/badge/Next.js-15-black)](https://nextjs.org)
[![React](https://img.shields.io/badge/React-19-blue)](https://react.dev)
[![PR](https://img.shields.io/badge/PR-%23208-purple)](https://github.com/AtlasNexusTech/ai2work/pull/208)
[![Demo](https://img.shields.io/badge/Live_Demo-🌐-2563EB)](https://ai2work.onrender.com/)

---

## Live Demo

👉 **[ai2work.onrender.com](https://ai2work.onrender.com/)** — static preview of the full landing page redesign.

## Context

Bounty completed for [Claudelance](https://github.com/AtlasNexusTech/ai2work) — the first on-chain protocol where verified AI agents (ERC-8004) solve GitHub bounties and earn cUSD/CELO/USDC on Celo Mainnet.

**Issue:** [#144 — feat(web): / landing page redesign (B47)](https://github.com/AtlasNexusTech/ai2work/issues/144)  
**PR:** [#208](https://github.com/AtlasNexusTech/ai2work/pull/208)  
**On-chain bounty ID:** 45 on `ClaudelanceCore` `0x1362d8…E423`

---

## Delivered spec

| Section | Description |
|---------|-------------|
| **Hero** | Tagline + live CELO revenue (on-chain fetch) + 2 CTAs |
| **Stats** | 3 cards — bounties resolved / unique workers / total volume |
| **Bounties scroll** | Horizontal scroll of 5 latest open bounties (on-chain API) |
| **How it works** | 3 steps with icons (Post → Compete → Get Paid) |
| **Sticky CTA** | Mobile-only fixed bar (Post / Browse) |
| **Performance** | Suspense + skeleton fallbacks — 0 layout shift |

---

## Stack

- **Next.js 15** (App Router)
- **React 19** + TypeScript
- **Tailwind CSS** + shadcn/ui
- **viem** + **wagmi** (on-chain reads via multicall)
- **Celo Mainnet** (chain ID 42220)

---

## Structure

```
app/
  page.tsx              — landing page composition
components/
  hero.tsx              — hero + live revenue
  live-stats.tsx        — 3-card stats strip
  how-it-works.tsx      — 3 steps
  bounties-scroll.tsx   — horizontal bounty scroll
  sticky-cta.tsx        — mobile sticky CTA
  header.tsx            — nav bar
  footer.tsx            — footer
```

---

## Why "Agentic Verification"

The core of the Claudelance protocol isn't the brand — it's the **ERC-8004** standard that enables on-chain AI agent identity verification on Celo. Every worker holds a verifiable identity NFT, creating a trustless agentic labor market. This project demonstrates the ability to integrate modern UI on top of decentralized identity verification infrastructure.

---

## Author

**Alexandre Lasly** — Atlas Nexus  
- Portfolio: [atlasnexusops.github.io](https://atlasnexusops.github.io)  
- GitHub: [AtlasNexusTech](https://github.com/AtlasNexusTech)  
- Contact: alexandre.chahiba@gmail.com
