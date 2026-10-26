# PixelStack Labs

Enterprise commerce platform and its client fleet, built end-to-end as a
proprietary stack: a Next.js 16 storefront, an Express BFF over Saleor and
PostgreSQL, the Artemis server-driven UI runtime, and Artemify - a native
Android social-commerce client.

## What we build

**PixelStack enterprise platform** - production commerce stack for
Ghaem Plastic: CQRS read paths over materialized views, local cart with
row-level locking, modular ZarinPal gateway with reconciliation cron,
multi-tier cache chain (NodeCache, Redis, Varnish, ISR), full checkout.

**Artemis** - server-driven UI runtime. Layouts are authored in Strapi;
transpiled, import-free React components are delivered at runtime and
executed client-side without a site rebuild.

**Artemify** - full Android client (Kotlin, Jetpack Compose): social feed,
native chat over rt.v1 realtime websocket, stickers, rich message bodies,
and storefront surfaces. Desktop remains the Tauri reference shell.

## Repositories

| Repository | Focus | Access |
|---|---|---|
| artemify-android | Native Android client + Tauri reference shell | private |
| pixelstack-platform | Enterprise orchestration repo (compose stack, super-repo) | private |
| pixelstack-web | Next.js 16 storefront | private |
| pixelstack-api | Express BFF, identity, payments, caching | private |
| artemis | Server-driven UI middleware | private |
| pixelstack-admin | Admin panel | private |
| pixelstack-cms | CMS configuration | private |
| pixelstack-hub | Hub service | private |
| pixelstack-infra | Infrastructure glue | private |
| telegram-gifts | Gift pack tooling | private |
| .github | Org profile and policies | public |

## Status

- Private development; repositories are proprietary, all rights reserved.
- Membership and contribution require an invitation from the org owner.
- English-only code comments, no-decorative-banners policy across all repos.

## Contact

- Owner: [matinsanei](https://github.com/matinsanei)
- Licensing and access: licensing@pixelstack.cloud

(c) 2026 PixelStack Labs. All rights reserved.
