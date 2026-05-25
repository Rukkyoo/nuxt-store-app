# Class Activity
 My younger brother broke a few things in here while using my pc, I desperately need your help with fixing them. I want you to go through the codebase and ensure that everything is working as expected.

# Instructions
- Remove the button element in `productCard.vue` and use a proper button element imported from `ui/Button.vue`, with the text "View Product", to replace it.

- On click, ensure the user is redirected to the `products/[id].vue` page and the page should display the product details. Tip: You can wrap the button with <NuxtLink> tag for navigation.

- Here's the product details endpoint for a specific product `('https://fakestoreapi.com/products/1')`.

- Styling has already been provided, functionality is the aim here.


# Nuxt Minimal Starter

Look at the [Nuxt documentation](https://nuxt.com/docs/getting-started/introduction) to learn more.

## Setup

Make sure to install dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
