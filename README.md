# The Void Store

A small storefront ("useless baubles that you do not need") built with Nuxt 3. It lists products from the public [Fake Store API](https://fakestoreapi.com) and has a details page for each one.

## Context

I built this in July 2023 as the technical assessment for a job interview, using Vue/Nuxt, which I had no real experience with at the time, so I learned what I needed along the way.

I don't work with Vue or Nuxt day to day. I'm keeping this repository because it's a concrete example of how I handle an unfamiliar stack: read the docs, figure out the framework's conventions, and build something functional with it. It isn't meant to show expertise in Vue or Nuxt.

## Stack

- [Nuxt 3](https://nuxt.com) (Vue 3, `<script setup>`)
- [Tailwind CSS](https://tailwindcss.com) via `@nuxtjs/tailwindcss`
- [Material Icons](https://fonts.google.com/icons)
- [Fake Store API](https://fakestoreapi.com) as the data source
- Deployed on Vercel

## What's implemented

- File-based routing: Home, About, a product list (`/products`) and a dynamic product page (`/products/[id]`).
- Data fetching with `useFetch`, rendered on the server.
- Two layouts (`default` and `products`), selected per page with `definePageMeta`.
- Reusable `ProductCard` and `ProductDetails` components that receive the product through props.
- A custom error page. Requesting a product that doesn't exist throws a 404 with `createError`, and the error page sends you back home with `clearError`.
- A page title per product using `<Head>` and `<Title>`.
- Shared `.btn` and `.card` styles built with Tailwind's `@apply`.

Some things were left unfinished: the Home and About pages still have placeholder text, the "Add to cart" button doesn't do anything, and the product page doesn't show the product's title or price.

## Live version

https://the-void-store.vercel.app

At the time of writing, the deployment is up but the product pages come up empty: the server-side requests to Fake Store API no longer return data, so the list is blank and the product pages return 404.

## Running locally

```bash
npm install
npm run dev
```

The app runs at `http://localhost:3000`. `npm run build` and `npm run preview` build and serve the production version.

## Status

Finished and no longer maintained. The repository is archived and kept as is.
