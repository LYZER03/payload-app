# Food Ordering App – Technical Architecture

## Project Structure

- **Monorepo:**  
  Both frontend (Next.js) and backend (Payload CMS) reside in a single codebase under `src/`.

- **Key Directories:**  
  - `src/app/` – Next.js App Router pages and layouts.
  - `src/components/` – Reusable UI components (with `ui/` for atomic elements).
  - `src/collections/` – Payload CMS collections (dishes, categories, users, orders).
  - `src/providers/` – Context and state providers.
  - `src/endpoints/` – Custom API routes and handlers.

## Backend & API

- **Payload CMS:**  
  - Runs as part of the Next.js app.
  - Exposes REST and GraphQL APIs for content and order management.
  - Handles authentication, access control, and data validation.
  - Custom plugins enhance functionality (SEO, search, redirects, etc.).

## Frontend

- **Next.js App Router:**  
  - All user-facing pages and admin dashboard are React components.
  - Uses custom and third-party UI components for a modern, accessible UI.

## Data Management

- **Menu & Orders:**  
  - Menu data fetched from Payload CMS via API.
  - Cart state managed client-side (React Context/Hooks).
  - Orders submitted to CMS and linked to user accounts.

## Authentication

- **Dual Flows:**  
  - Customers and admins authenticate via Payload’s built-in (customized) auth.
  - Auth state managed both client-side (for UI) and server-side (for API access control).

## Hosting & Deployment

- **Self-hosted:**  
  - Both frontend and backend run together on the same server/environment.
  - Node.js (v18+) required.
  - Can be deployed to any platform supporting Node.js (VPS, Docker, cloud VM, etc.).

## Code Organization

- **Modular:**  
  - Clear separation of concerns (UI, logic, data, CMS).
  - Reusable components and hooks.
  - Extensible via Payload plugins and Next.js middleware.

---
