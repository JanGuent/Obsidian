---

tags: [learning, fullstack, meal-planner]

created: 2026-10-04

---

  

# Meal Planner: Full-Stack Learning Plan

  

**Goal:** Build a weekly meal planner PWA (ingredients, recipes, nutrients, shopping list) and become comfortable building and hosting full-stack apps professionally.

  

**Stack:** Vue 3 + TypeScript + Vite, Pinia, Dexie, Cloudflare Pages, later Spring Boot + Postgres + Docker.

  

**Principle:** One new thing at a time. Rough estimates assume steady progress; evenings-only learning will take longer.

  

---

  

## Phase 1: Git and GitHub (3-4 days)

  

**Resources**

- [Pro Git book](https://git-scm.com/book) (chapters 1-3)

- [GitHub Skills](https://skills.github.com) (hands-on courses)

  

**Tasks**

- [ ] Read Pro Git chapters 1-3

- [ ] Complete one GitHub Skills course

- [ ] Create the project repo on GitHub

- [ ] Commit in small steps with meaningful messages

- [ ] Create a branch, open a pull request against my own repo, merge it

  

**Done when**

- [ ] I can branch, open a PR and merge without looking anything up

  

---

  

## Phase 2: JavaScript, TypeScript and the browser (1-2 weeks)

  

**Resources**

- [javascript.info](https://javascript.info) (first two parts)

- [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)

- [MDN](https://developer.mozilla.org) (reference)

  

**Tasks**

- [ ] Work through javascript.info: basics, functions, objects

- [ ] Learn async/await, promises and `fetch`

- [ ] Learn modules (`import` / `export`)

- [ ] Practice array methods (`map`, `filter`, `reduce`)

- [ ] Learn DOM basics

- [ ] Work through the TypeScript Handbook (types, interfaces, generics, unions)

  

**Done when**

- [ ] I wrote a small TS script that fetches data from a public API and renders it to a page, without a framework

  

---

  

## Phase 3: HTML and CSS basics (1 week)

  

**Resources**

- [web.dev Learn HTML](https://web.dev/learn/html) and [Learn CSS](https://web.dev/learn/css)

- [Flexbox Froggy](https://flexboxfroggy.com) and [Grid Garden](https://cssgridgarden.com)

- [Tailwind docs](https://tailwindcss.com/docs) (only after the basics)

  

**Tasks**

- [ ] Semantic HTML

- [ ] The box model

- [ ] Flexbox (finish Flexbox Froggy)

- [ ] Grid (finish Grid Garden)

- [ ] Responsive design with media queries

- [ ] Add Tailwind and rebuild one small layout with it

  

**Done when**

- [ ] I can build a mobile-friendly layout by hand

  

---

  

## Phase 4: Vue 3 fundamentals (2 weeks)

  

**Resources**

- [Vue tutorial and guide](https://vuejs.org)

- [Vue Router](https://router.vuejs.org)

- [Pinia](https://pinia.vuejs.org)

  

**Tasks**

- [ ] Scaffold a project with Vite

- [ ] Do the official Vue tutorial

- [ ] Learn the Composition API with `<script setup>`

- [ ] Reactivity: `ref`, `reactive`, `computed`, `watch`

- [ ] Props and emits

- [ ] Vue Router: routes, params, navigation

- [ ] Pinia: stores, state, getters, actions

  

**App milestone**

- [ ] Ingredient list with add / edit / delete, state in memory only (data lost on refresh is fine)

  

---

  

## Phase 5: Build the core app locally (2-3 weeks)

  

In-memory state in Pinia only. Focus on design decisions, not polish.

  

**Tasks**

- [ ] Data model in TypeScript (Ingredient, Recipe, RecipeIngredient, MealPlanEntry)

- [ ] Normalize amounts to grams / ml

- [ ] Recipe CRUD (recipes made of ingredients)

- [ ] Nutrient calculation per recipe as a `computed`

- [ ] Weekly planner view (days x meal slots)

- [ ] Per-meal and per-day nutrient totals

- [ ] Shopping list generated from the plan (aggregated, scaled by servings)

- [ ] Check-off on shopping list items

  

**Done when**

- [ ] The full feature set works in the browser, even if it is ugly

  

---

  

## Phase 6: Persistence and deployment (1 week)

  

**Resources**

- [Dexie](https://dexie.org)

- [Cloudflare Pages docs](https://developers.cloudflare.com/pages/)

- [GitHub Actions docs](https://docs.github.com/en/actions)

  

**Tasks**

- [ ] Store data in IndexedDB with Dexie

- [ ] Deploy the static build to Cloudflare Pages (or Netlify) from GitHub

- [ ] Add a GitHub Actions workflow: type check and build on every push

- [ ] Refactor Pinia stores to read/write through Dexie

  

**Done when**

- [ ] The app is live at a URL

- [ ] Data survives a page refresh

- [ ] Every push is checked automatically

  

---

  

## Phase 7: PWA and offline (1 week)

  

**Resources**

- [web.dev PWA course](https://web.dev/learn/pwa)

- [vite-plugin-pwa docs](https://vite-pwa-org.netlify.app)

  

**Tasks**

- [ ] Understand manifest and service worker (read the web.dev course)

- [ ] Add `vite-plugin-pwa`

- [ ] Add icons and manifest details

- [ ] Inspect the service worker in the browser Application tab

- [ ] Install the app on my phone

  

**Done when**

- [ ] The shopping list works in airplane mode

  

---

  

## Phase 8: Add the Spring Boot backend (2-3 weeks)

  

**Resources**

- [TanStack Query for Vue](https://tanstack.com/query/latest/docs/framework/vue/overview)

- [springdoc-openapi](https://springdoc.org)

  

**Tasks**

- [ ] REST API: ingredients, recipes, plan entries, shopping list state

- [ ] Postgres + Flyway migrations

- [ ] OpenAPI spec and generated TypeScript client

- [ ] CORS (understand why it happens, then configure it)

- [ ] Session-based auth with Spring Security

- [ ] Replace Dexie calls with API calls via TanStack Query

- [ ] Optional: keep Dexie as an offline cache and queue check/uncheck actions

  

**Done when**

- [ ] The app reads and writes through my backend

  

---

  

## Phase 9: Backend hosting and testing (2 weeks)

  

**Resources**

- [Docker: Get Started](https://docs.docker.com/get-started/)

- [Caddy docs](https://caddyserver.com/docs/)

- [Vitest](https://vitest.dev)

- [Playwright](https://playwright.dev)

  

**Tasks**

- [ ] Dockerize the Spring Boot app

- [ ] Docker Compose: app + Postgres + Caddy

- [ ] Deploy to Oracle Always Free (or a cheap VPS)

- [ ] HTTPS working via Caddy

- [ ] Nightly `pg_dump` backups stored off the server

- [ ] Deploy pipeline with GitHub Actions

- [ ] Vitest tests for nutrient and shopping list logic

- [ ] One or two Playwright end-to-end flows

  

**Done when**

- [ ] The full app runs on my own hosting with backups and automated checks

  

---

  

## Working with Claude as a mentor

  

- [ ] Try each task first, then ask for a review

- [ ] Ask for hints, not solutions

- [ ] Ask for a quiz at the end of each phase

- [ ] Ask "what would a senior dev criticize here?" before moving on

- [ ] Start conversations with: "Don't give me full code, guide me with questions"

  

---

  

## Progress log

  

| Phase | Started | Finished | Notes |

|---|---|---|---|

| 1 Git/GitHub | | | |

| 2 JS/TS | | | |

| 3 HTML/CSS | | | |

| 4 Vue | | | |

| 5 Core app | | | |

| 6 Persistence + deploy | | | |

| 7 PWA | | | |

| 8 Spring Boot backend | | | |

| 9 Hosting + testing | | | |