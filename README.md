# Buyer-Lead-Intake-
# 🏡 Mini Buyer Lead Intake App

A full-stack Next.js application to **capture, list, and manage buyer leads** with validation, search/filter, and CSV import/export.

---

## 🚀 Features

- Create, view, edit, and manage buyer leads
- Strong **validation** with Zod (client + server)
- **Server-side rendering (SSR)** with real pagination & sorting
- **Filters & debounced search** with URL sync
- **CSV import/export** (transactional import with row-level errors)
- Buyer history tracking (who changed what & when)
- Ownership enforcement (users can only edit their own leads)
- Basic authentication (magic link / demo login)

---

## 🛠️ Tech Stack

- **Frontend:** Next.js (App Router) + TypeScript
- **Database:** PostgreSQL / Supabase / SQLite with Prisma or Drizzle
- **Validation:** Zod
- **Auth:** Supabase auth (magic link) or demo login
- **Deployment:** Vercel (recommended)
- **Version Control:** Git with meaningful commits

---

## 📦 Data Model

### `buyers` (leads)
- `id`, `fullName`, `email`, `phone`, `city`, `propertyType`, `bhk`, `purpose`,  
  `budgetMin`, `budgetMax`, `timeline`, `source`, `status`, `notes`, `tags`,  
  `ownerId`, `updatedAt`

### `buyer_history`
- `id`, `buyerId`, `changedBy`, `changedAt`, `diff` (JSON of changed fields)

---

## 🔑 Key Flows

### 1. Create Lead – `/buyers/new`
- Form validation (Zod, both clien
