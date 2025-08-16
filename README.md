# LokApp

B2B meal ordering for industrial-zone restaurants. Replaces unstructured WhatsApp orders and paper meal tickets with standardized flows, dynamic stock tracking, and transparent billing.

## Quick Start
**Watch (90s):** [youtube.com/watch?v=0OZnB6jDBDI](https://www.youtube.com/watch?v=0OZnB6jDBDI)  
**Live demo:** [lokapp-role-based-serhatyurdakuls-projects.vercel.app](https://lokapp-role-based-serhatyurdakuls-projects.vercel.app)

**Demo accounts** *(reset periodically)*
- **Restaurant** — Email: `testloksorumlu@gmail.com` · Password: `test1234`
- **Customer** — Email: `mehmetaka@gmail.com` · Password: `12345678`

> This repository is for showcase only; the application code lives in a private repository. Below are product screenshots and brief explanations of the main flows.

## Features
- **Role-based access**: Restaurant and Customer views with protected routes.
- **Company-grouped kitchen view**: Orders aggregated per company for faster prep and clear summaries.
- **Stock-aware menu**: Sold-out items disabled; one choice per category.
- **Mobile-first UI**: Responsive layouts for small and large screens.
- **Transparent billing**: Clear per-company order summaries support restaurant and company reconciliation.

## Tech Stack & Architecture
- **Frontend:** React, Redux Toolkit, React Router DOM, SCSS
- **API layer:** Centralized HTTP client with auth headers and 401 handling
- **Architecture:** Feature-based modules (auth, customer, restaurant), shared UI in `components/common`, centralized state in `store`

## Folder Structure (overview)

```
src/
  components/
    common/            # Shared UI components (Button, Modal, Loading, etc.)
  features/
    auth/              # Authentication & role flow
    customer/          # Employee-facing screens & state
    restaurant/        # Restaurant dashboard, menu, orders & state
  store/               # Redux store (root reducer)
  utils/               # API layer (axios + interceptors), helpers
  styles/              # Global SCSS
```

## Screenshots (Mobile)

<figure>
  <img src="docs/screenshots/login-register-1.png" width="820" alt="Login / Register" />
  <figcaption><strong>Login / Register</strong><br/>Field validation, password toggle, role-based redirect after login.</figcaption>
</figure>

<figure>
  <img src="docs/screenshots/customer-1.png" width="820" alt="Customer — Menu (mobile)" />
  <figcaption><strong>Customer — Menu (mobile)</strong><br/>One choice per category; sold-out disabled; sticky “Confirm Order”.</figcaption>
</figure>

<figure>
  <img src="docs/screenshots/customer-2.png" width="820" alt="Customer — QR & Profile" />
  <figcaption><strong>Customer — QR & Profile</strong><br/>Dine-in check-in flow; profile with company info and meal history.</figcaption>
</figure>

<figure>
  <img src="docs/screenshots/restaurant-2.png" width="820" alt="Restaurant — Menu Management & Add Meal" />
  <figcaption><strong>Restaurant — Menu Management & Add Meal</strong><br/>Category tabs/search; Remaining/Sold badges; Edit/Delete actions.</figcaption>
</figure>

<figure>
  <img src="docs/screenshots/restaurant-1.png" width="820" alt="Restaurant — Dashboard & Low Stock / Stock Update" />
  <figcaption><strong>Restaurant — Dashboard & Low Stock</strong><br/>Pending Orders, Low Stock list, mark as Sold-Out / update stock.</figcaption>
</figure>

<figure>
  <img src="docs/screenshots/restaurant-3.png" width="820" alt="Restaurant — Orders & Order Detail" />
  <figcaption><strong>Restaurant — Orders & Detail</strong><br/>Industrial-site tabs; per-company status; confirmation modal on complete.</figcaption>
</figure>

## Screenshots (Desktop)

<figure>
  <img src="docs/screenshots/restaurant-responsive-2.png" width="820" alt="Restaurant — Menu Management (desktop)" />
  <figcaption><strong>Restaurant — Menu Management (desktop)</strong></figcaption>
</figure>

<figure>
  <img src="docs/screenshots/restaurant-responsive-1.png" width="820" alt="Restaurant — Dashboard (desktop)" />
  <figcaption><strong>Restaurant — Dashboard (desktop)</strong></figcaption>
</figure>

<figure>
  <img src="docs/screenshots/restaurant-responsive-3.png" width="820" alt="Restaurant — Orders list (desktop)" />
  <figcaption><strong>Restaurant — Orders list (desktop)</strong></figcaption>
</figure>

<figure>
  <img src="docs/screenshots/folder-structure.png" width="820" alt="Folder Structure / Architecture" />
  <figcaption><strong>Architecture</strong><br/>Feature-based structure; protected routes; API overview.</figcaption>
</figure>

## Roadmap
- QR check-in integration and reporting (daily/monthly company totals)
