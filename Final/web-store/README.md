# Nuxt Store App

A beautiful, type‑safe Nuxt 3 storefront that fetches products from the public **Fake Store API** and displays them with a clean, responsive UI.

---

## Features
- **Type‑safe data fetching** with TypeScript generics (`useFetch<Product[]>`).
- Reusable **product card component** (`components/productCard.vue`).
- Dynamic product detail page (`pages/[id].vue`).
- Responsive layout using CSS Grid/Flexbox – works on desktop, tablet and mobile.
- Scoped CSS and modern design utilities (dark‑mode ready, glass‑morphism ready for future enhancements).

---

## Tech Stack
- **Nuxt 3** (Vue 3, Vite) – server‑side rendering & file‑based routing.
- **TypeScript** – full type safety across the app.
- **SCSS/CSS** – custom styling, no external UI framework.
- **Fake Store API** – `https://fakestoreapi.com` (demo product data).

---

## Prerequisites
- **Node.js** ≥ 18 (LTS recommended)
- **pnpm** (or npm / yarn – just change the install command)

---

## Getting Started
```bash
# Clone the repo (if you haven't already)
git clone https://github.com/rukkyoo/nuxt-store-app.git
cd nuxt-store-app/Final/web-store

# Install dependencies
pnpm install   # or `npm i` / `yarn`

# Run the development server
pnpm dev       # `npm run dev` or `yarn dev`
```
Open **http://localhost:3000** in your browser. You should see a grid of products fetched from the API.

---

## Build for Production
```bash
pnpm build   # or `npm run build`
pnpm start   # serves the built app
```
The generated static files live in the `.output` directory.

---

## Project Structure
```
app/
├─ components/          # Reusable UI components (e.g., productCard.vue)
├─ pages/               # File‑based routes (index, [id].vue)
├─ styles/ (optional)  # Global styles, if any
└─ ...
```
Key files:
- `components/productCard.vue` – displays a product card; typed with the `Product` interface.
- `pages/[id].vue` – shows a single product’s details, also fully typed.
- `app.vue` – root layout (you can extend with a header/footer).

---

## TypeScript Interfaces
```ts
interface Product {
  id: number;
  title: string;
  price: number;
  description: string;
  image: string;
  // add other fields from the API as needed
}
```
All data fetching uses this interface to guarantee compile‑time safety.

---

## Contributing
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/awesome‑feature`).
3. Commit your changes with clear messages.
4. Open a Pull Request.

Please keep the code TypeScript‑safe and run `pnpm lint` before submitting.

---

## License
This project is licensed under the MIT License – see the `LICENSE` file for details.
