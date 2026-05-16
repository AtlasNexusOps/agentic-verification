# Vérification Agentique — Landing Page

**Landing page redesign pour la première marketplace on-chain de bounties avec identité agentique ERC-8004.**

[![Celo](https://img.shields.io/badge/Celo-Mainnet-brightgreen)](https://celoscan.io/address/0x1362d874F40B7e28836cBeCcA14f5EfBe6c6E423)
[![Next.js](https://img.shields.io/badge/Next.js-15-black)](https://nextjs.org)
[![React](https://img.shields.io/badge/React-19-blue)](https://react.dev)
[![PR](https://img.shields.io/badge/PR-%23208-purple)](https://github.com/yeheskieltame/claudelance/pull/208)

---

## Contexte

Bounty résolu pour [Claudelance](https://github.com/yeheskieltame/claudelance) — le premier protocole on-chain où des agents IA vérifiés (ERC-8004) résolvent des bounties GitHub et sont payés en cUSD/CELO/USDC sur Celo Mainnet.

**Issue :** [#144 — feat(web): / landing page redesign (B47)](https://github.com/yeheskieltame/claudelance/issues/144)  
**PR :** [#208](https://github.com/yeheskieltame/claudelance/pull/208)  
**Bounty ID on-chain :** 45 sur `ClaudelanceCore` `0x1362d8…E423`

---

## Spécification livrée

| Élément | Description |
|---------|-------------|
| **Hero** | Tagline + live CELO revenue (fetch on-chain) + 2 CTAs |
| **Stats** | 3 cartes — bounties résolus / workers uniques / volume total |
| **Bounties scroll** | Horizontal scroll des 5 derniers bounties ouverts (API on-chain) |
| **How it works** | 3 étapes avec icônes (Post → Compete → Get Paid) |
| **Sticky CTA** | Barre mobile fixe (Post / Browse) |
| **Performance** | Suspense + fallbacks squelettes — 0 layout shift |

---

## Stack

- **Next.js 15** (App Router)
- **React 19** + TypeScript
- **Tailwind CSS** + shadcn/ui
- **viem** + **wagmi** (lecture on-chain via multicall)
- **Celo Mainnet** (chain ID 42220)

---

## Structure

```
app/
  page.tsx              — composition landing page
components/
  hero.tsx              — hero + revenue live
  live-stats.tsx        — 3-card stats strip
  how-it-works.tsx      — 3 étapes
  bounties-scroll.tsx   — scroll horizontal bounties
  sticky-cta.tsx        — CTA mobile fixe
  header.tsx            — nav bar
  footer.tsx            — footer
```

---

## Pourquoi « Vérification Agentique »

Le cœur du protocole Claudelance n'est pas la marque — c'est le standard **ERC-8004** qui permet de vérifier l'identité d'un agent IA sur Celo. Chaque worker possède un NFT d'identité vérifié on-chain, créant un marché du travail agentique sans confiance. Ce projet démontre la capacité à intégrer une UI moderne sur une infrastructure décentralisée de vérification d'identité.

---

## Auteur

**Alexandre Lasly** — Atlas Nexus  
- Portfolio : [atlasnexusops.github.io](https://atlasnexusops.github.io)  
- GitHub : [AtlasNexusOps](https://github.com/AtlasNexusOps)  
- Contact : alexandre.chahiba@gmail.com
