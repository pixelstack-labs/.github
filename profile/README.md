
# 🚀 PixelStack Labs

**Enterprise E-Commerce Platform — Plugin Runtime, Local Cart, Modular Payments, Full‑Stack TypeScript**

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/pixelstack-labs/pixelstack?label=latest)](https://github.com/pixelstack-labs/pixelstack/releases)
[![Build](https://img.shields.io/badge/build-passing-brightgreen)]()
[![License](https://img.shields.io/badge/license-BSL-blue)](LICENSE)
[![PRs](https://img.shields.io/badge/PRs-private%20beta-red)](#contributing)

---

## 🌐 Overview

PixelStack is a **production‑ready e‑commerce platform** built from the ground up for high‑traffic, enterprise‑grade stores.  
It features a **local cart system** (30ms operations), a **modular payment gateway abstraction**, and **Artemis** — a custom React plugin runtime that executes components without a site rebuild.

---

## ✨ Key Highlights

| Feature | Description |
|--------|-------------|
| 🛒 **Local Cart** | PostgreSQL‑backed cart with 30ms add/update/remove. Guests & logged‑in users share the same fast path. |
| 🧩 **Artemis Runtime** | Run React components dynamically using a custom 9‑pass bundler (Challenger) — no redeploy required. |
| 💳 **Payment Abstraction** | Adapter‑based gateway system (Mock, COD, Stripe, ZarinPal). Add a new gateway by writing one file. |
| 🔍 **CQRS & Materialized Views** | All read paths (search, filters, product detail, SEO) go through PostgreSQL views — sub‑10ms queries. |
| 🔐 **Auth** | Independent JWT‑based auth with multiple login methods (password, OTP, Google, magic link). Lazy Saleor customer creation — only at first purchase. |
| ⚡ **Performance** | Multi‑tier caching (L1 in‑memory + L2 Redis Sentinel), Varnish full‑page cache, HTTP/2, ISR. |
| 🛡️ **Security** | Helmet, CSP, HSTS, CORS whitelist, rate limiting (Redis sliding window), input validation. |

---

## 🏗️ Architecture (simplified)

```
Browser → Next.js BFF → Express Custom API (CQRS)
                           ├─ Local Cart (PostgreSQL)
                           ├─ Payment Gateways (Adapter Pattern)
                           └─ Saleor GraphQL (only at checkout)
```

- **Write path**: Cart mutations, checkout → Saleor (minimal)
- **Read path**: Products, search, filters → Materialized Views in PostgreSQL (fast)

---

## 🧰 Tech Stack

- **Frontend**: Next.js 15, TypeScript, Tailwind CSS, Framer Motion
- **Backend**: Node.js, Express, TypeScript, Drizzle ORM
- **Databases**: PostgreSQL (primary + replicas), Redis Sentinel, ClickHouse (analytics)
- **Infra**: Docker (47 services), Traefik, HAProxy, Varnish, MinIO, Prometheus, Grafana, Jaeger
- **Commerce**: Saleor 3.x (headless GraphQL)

---

## 📦 Repositories

| Repository | Description |
|-----------|-------------|
| [pixelstack](https://github.com/pixelstack-labs/pixelstack) | Main monorepo — full platform |
| `artemis-engine` | Artemis plugin runtime & bundler (private) |
| `pixelstack-docs` | Architecture & API documentation (coming soon) |

---

## 🚀 Getting Started (Private)

> PixelStack is currently in **private beta**.  
> If you are a collaborator, check the [project setup guide](https://github.com/pixelstack-labs/pixelstack) in the main repo.

---

## 📖 Documentation

- 📘 [Cart System Reference](https://github.com/pixelstack-labs/pixelstack/blob/main/docs/cart-system.md)
- 🧪 [Artemis Developer Guide](https://github.com/pixelstack-labs/pixelstack/blob/main/docs/artemis_developer.md)
- 💳 [Payment Architecture](https://github.com/pixelstack-labs/pixelstack/blob/main/docs/payment-architecture.md)

---

## 👤 Author

Built with ❤️ by **[@matinsanei](https://github.com/matinsanei)**

---

## 📝 Contributing

We are not accepting public contributions at this stage.  
If you find a bug or have a suggestion, please open an issue in the relevant repository.

---

## 📄 License

This project is currently **source available**. A license for public use will be announced upon public release.

---

© 2026 PixelStack Labs. All rights reserved.
