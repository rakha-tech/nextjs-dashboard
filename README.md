# 🧭 Next.js App Router Course — Summary (Chapters 1–16)

This repository contains everything learned throughout the **Next.js App Router Course**, from setup to advanced rendering techniques.  
Below is a summary of all important concepts covered in **Chapters 1–16**.

---

## 🏁 Chapter 1 — Getting Started

- Introduction to the **App Router** (`/app` directory).
- Difference between **Server Components** and **Client Components**.
- Project setup using **pnpm**, **TypeScript**, and **ESLint**.
- How routing works in Next.js using the **file system**.
- Introduction to the concept of **layouts**, **pages**, and **segments**.

---

## 🎨 Chapter 2 — CSS Styling

- Styling options in Next.js:
  - **Global CSS** (e.g., `globals.css`).
  - **CSS Modules** (`.module.css`) for component-scoped styles.
  - **Tailwind CSS** integration for utility-first design.
- Using the `className` prop for custom styling.

---

## 🧠 Chapter 3 — Optimizing Fonts and Images

- Using the built-in **`next/font`** for self-hosted Google Fonts.
- Using the **`next/image`** component for optimized images:
  - Automatic resizing, lazy loading, and responsive images.
- Performance benefit: reduced layout shift and faster LCP.

---

## 🧩 Chapter 4 — Creating Layouts and Pages

- Layouts define the **structure** shared between pages.
- Every route can have its own `layout.tsx`.
- **Root layout** = global scope  
  **Nested layout** = local to a specific route segment.
- Pages (`page.tsx`) represent the actual content per route.

---

## 🔗 Chapter 5 — Navigating Between Pages

- Using the **`Link`** component for client-side navigation.
- Difference between:
  - `Link` → instant navigation (no full page reload).
  - `useRouter()` → programmatic navigation.
- Maintaining SPA behavior with App Router.

---

## 🗄️ Chapter 6 — Setting Up Your Database

- Connected a database (e.g., **PostgreSQL**, **Supabase**, or **Firebase**).
- Importance of placing DB and app **in the same region** to reduce latency.
- Using **SQL queries** to retrieve only required data.

---

## 🔍 Chapter 7 — Fetching Data

- **Server Components** handle data fetching securely.
- Keep **database queries** and secrets on the server.
- Avoid fetching unnecessary data to optimize performance.
- Example pattern: `async function getData() { ... }`

---

## ⚡ Chapter 8 — Static and Dynamic Rendering

- **Static Rendering (SSG)** → pre-generated HTML at build time.
- **Dynamic Rendering (SSR)** → generated per request.
- When to use:
  - Static for rarely-changing data.
  - Dynamic for personalized or frequently-updated data.

---

## 🌊 Chapter 9 — Streaming

- Use **React Suspense** for streaming partial UI.
- Benefits:
  - Early UI rendering while waiting for data.
  - Better user experience with loading states.
- Loading UI can be defined with `loading.tsx`.

---

## 🧱 Chapter 10 — Partial Prerendering (PPR)

- **Experimental** feature (Next.js 14+).
- Combines **Static + Dynamic Rendering** in the same route.
- “Static shell” loads first, then **holes** (dynamic parts) stream asynchronously.
- Enabled via:
  - `ppr: 'incremental'` in `next.config.ts`
  - `export const experimental_ppr = true` in layout.

---

## 🔍 Chapter 11 — Adding Search and Pagination

- Implemented **server-side filtering** and **pagination**.
- Used **URL search params** (`searchParams`) to handle query state.
- Good UX: avoid reloading the entire page during searches.

---

## ✏️ Chapter 12 — Mutating Data

- Used **Server Actions** for POST/PUT/DELETE operations.
- Ensured security by keeping mutations server-side.
- Used **revalidation** or **cache invalidation** to update UI after mutations.

---

## 🚧 Chapter 13 — Handling Errors

- Error handling using:
  - `error.tsx` → for route-level errors.
  - `not-found.tsx` → for 404 pages.
- Prevented crashes and gave user-friendly feedback.

---

## ♿ Chapter 14 — Improving Accessibility

- Added semantic HTML elements and ARIA labels.
- Focus management for modals and forms.
- Ensured color contrast and keyboard navigation support.

---

## 🔐 Chapter 15 — Adding Authentication

- Implemented authentication via **NextAuth.js** or **custom Supabase auth**.
- Used middleware for route protection (`middleware.ts`).
- Separated **public routes** (e.g., `/login`) and **protected routes** (e.g., `/dashboard`).

---

## 🏷️ Chapter 16 — Adding Metadata

- Enhanced SEO and social sharing with Metadata API.
- Two main approaches:
  - **Config-based** via `export const metadata` in layouts/pages.
  - **File-based** (favicon, OG image, robots.txt, sitemap.xml).
- Used `title.template` for consistent branding:
  ```ts
  title: {
    template: '%s | Acme Dashboard',
    default: 'Acme Dashboard',
  }
  ```

## ✅ Final Summary

Through these 16 chapters, we learned to:

- Build scalable apps using **App Router architecture**.
- Manage data fetching, caching, and rendering efficiently.
- Improve performance with **streaming** and **PPR**.
- Add polish with **metadata**, **accessibility**, and **auth**.
- Deploy a production-ready dashboard with best practices.

## 🧠 Key Takeaways

- Move heavy logic to **server components**.
- Keep **UI fast** using streaming and suspense.
- Secure everything that touches the database.
- Optimize SEO and UX with proper metadata.
- Build modular, maintainable, and accessible applications.

## ⚙️ Tech Stack Recap

- Next.js 14+ (App Router)
- TypeScript
- Tailwind CSS
- PostgreSQL / Supabase
- NextAuth
