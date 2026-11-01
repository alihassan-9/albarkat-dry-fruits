<div align="center">

# AL-Barkat Dry Fruits

**A premium e-commerce storefront for dry fruits, nuts and gifting, built with Next.js 16, React 19 and Tailwind CSS 4.**

![Next.js](https://img.shields.io/badge/Next.js-16-000000?logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4-06B6D4?logo=tailwindcss&logoColor=white)
![Motion](https://img.shields.io/badge/Motion-animations-FF0055)

</div>

---

## Overview

AL-Barkat is an editorial-style online store for premium dates, nuts and dried fruits, aimed at customers in Pakistan. It covers the complete shopping journey: browsing by category or purpose, searching, wishlists, a cart drawer, and checkout with order confirmation. Motion is used for animations, and it respects reduced-motion preferences.

> **Status:** demo storefront. Checkout uses a demo configuration (Cash on Delivery, PKR pricing, flat-rate shipping with a free-shipping threshold) and no real payment gateway. Orders are stored client-side only.

## Features

- **Catalogue**: 7 categories (Dates, Almonds, Pistachios, Cashews, Walnuts, Raisins, Dried Fruits) plus a combined "Nuts" storefront group
- **Discovery**: shop-by-purpose (everyday, sharing, gifting, premium), category filters, and a global search overlay
- **Product pages**: dynamic `/product/[slug]` routes with a purchase panel and wishlist toggle
- **Cart and wishlist**: React Context and reducer state with a slide-out cart drawer
- **Checkout**: validated form, order summary, shipping calculation, and an order confirmation page
- **Content pages**: Our Story, Corporate Gifting, FAQ, Shipping Information, Returns & Refunds, Contact, Feedback
- **Polished UX**: reveal animations, an announcement marquee, responsive layout, and accessible components
- **Tested business logic**: unit tests for checkout pricing and order creation using the Node.js built-in test runner

## Tech Stack

| Area        | Technology                                       |
| ----------- | ------------------------------------------------ |
| Framework   | Next.js 16 (App Router), React 19, React Compiler |
| Language    | TypeScript 5                                     |
| Styling     | Tailwind CSS 4                                   |
| Animation   | Motion                                           |
| Icons       | Lucide                                           |
| Testing     | `node:test` + `node:assert`                      |
| Linting     | ESLint 9 (`eslint-config-next`)                  |

## Getting Started

### Prerequisites

- Node.js 20+

### Installation

```bash
git clone https://github.com/alihassan-9/albarkat-dry-fruits.git
cd albarkat-dry-fruits
npm install
npm run dev
```

Open http://localhost:3000.

### Scripts

| Command         | Description                         |
| --------------- | ----------------------------------- |
| `npm run dev`   | Start the development server        |
| `npm run build` | Create an optimised production build |
| `npm run start` | Serve the production build          |
| `npm run lint`  | Run ESLint                          |
| `npm test`      | Run the unit tests                  |

## Project Structure

```
albarkat-dry-fruits/
├── public/                  # product, category, hero and editorial imagery
├── src/
│   ├── app/                 # App Router pages
│   │   ├── shop/            # /shop and /shop/[category]
│   │   ├── product/[slug]/  # product detail pages
│   │   ├── checkout/        # checkout flow
│   │   ├── order-confirmation/
│   │   └── ...              # wishlist, faq, contact, our-story, policies
│   ├── components/          # UI grouped by feature
│   │   ├── ui/              # shared primitives (Button, Badge, Section, Reveal...)
│   │   ├── layout/          # Header, Footer, AnnouncementMarquee
│   │   ├── home/            # landing page sections
│   │   ├── shop/ product/ cart/ checkout/ wishlist/ search/
│   │   └── contact/ faq/ feedback/
│   └── lib/                 # catalogue data, state (cart, wishlist, search), pricing & validation
└── tests/                   # unit tests and test support
```

## Configuration

Business content lives in [`src/lib/site-config.ts`](src/lib/site-config.ts) and checkout rules in [`src/lib/checkout-config.ts`](src/lib/checkout-config.ts). Values marked `PLACEHOLDER` or `DEMO` must be replaced with confirmed business details before going live.

## License

© 2026 AL-Barkat Dry Fruits. All rights reserved.

## Author

Built by **Ali Hassan** · [LinkedIn](https://www.linkedin.com/in/ali-hassan-70bb9323b) · [GitHub](https://github.com/alihassan-9)
