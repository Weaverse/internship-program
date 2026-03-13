# Week 11-12: React Router & GraphQL

> [!IMPORTANT]
> **DO NOT** use AI tools to write code for you. You come here to **LEARN**, the goal of this program is to build
> your programming skills through **hands-on** practice. AI assistants can help explain
> concepts or debug issues, but writing the code yourself is **essential** for learning.

---

|                 |                                                                                                                            |
| :-------------- | :------------------------------------------------------------------------------------------------------------------------- |
| Learning Topics | React Router Framework Mode, File-based routing, Route modules, Data loading, Actions, GraphQL fundamentals                |
| Objectives      | Master React Router Framework Mode, Learn GraphQL data fetching, Build a Pokedex Explorer app                              |

## Understanding React Router Modes

> [!IMPORTANT]
> React Router v7 has three modes: **Declarative**, **Data**, and **Framework**. We will focus on **Framework Mode** because it is what Shopify Hydrogen uses. Do NOT learn the Declarative (`<BrowserRouter>`) or Data (`RouterProvider`) patterns — they are different architectures.

1. Read [Picking a Mode](https://reactrouter.com/start/modes) to understand the differences
2. We use **Framework Mode** because it provides:
   - Type-safe routing with file-based route configuration
   - Built-in data loading (`loader`) and mutations (`action`)
   - Server-side rendering (SSR), static pre-rendering, and SPA strategies
   - Automatic code splitting
   - This is the same architecture used by Hydrogen (Shopify's React framework)

## React Router Framework Mode

### Installation & Setup
1. Read [Framework Mode Installation](https://reactrouter.com/start/framework/installation)
2. Set up a new project:
   ```bash
   npx create-react-router@latest my-app
   ```

### Routing (Days 1-2)
1. Read [Routing](https://reactrouter.com/start/framework/routing)
2. Learn how routes are defined in `routes.ts`:
   ```typescript
   // app/routes.ts
   import { index, route, layout, prefix } from "@react-router/dev/routes"

   export default [
     index("./routes/home.tsx"),
     route("pokemon", "./routes/pokemon/index.tsx"),
     route("pokemon/:id", "./routes/pokemon/detail.tsx"),
     layout("./routes/layouts/browse-layout.tsx", [
       route("type/:name", "./routes/type.tsx"),
       route("search", "./routes/search.tsx"),
     ]),
   ]
   ```
3. Key concepts:
   - `routes.ts` as the single source of truth
   - Index routes, dynamic params, layout routes
   - Nested routes and `<Outlet />`
   - Type-safe params via Route Module types

### Route Modules (Days 3-4)
1. Read [Route Module](https://reactrouter.com/start/framework/route-module)
2. Understand the Route Module API:
   ```typescript
   // app/routes/pokemon/detail.tsx
   import type { Route } from "./+types/detail"

   // Loader - runs on the server to fetch data
   export async function loader({ params }: Route.LoaderArgs) {
     const pokemon = await fetchPokemon(params.id)
     if (!pokemon) throw new Response("Not Found", { status: 404 })
     return { pokemon }
   }

   // Component - renders with type-safe loaderData
   export default function PokemonDetail({ loaderData }: Route.ComponentProps) {
     const { pokemon } = loaderData
     return <h1>{pokemon.name}</h1>
   }

   // Meta - sets page title and meta tags
   export function meta({ data }: Route.MetaArgs) {
     return [
       { title: data.pokemon.name },
       { name: "description", content: `Stats and details for ${data.pokemon.name}` },
     ]
   }
   ```
3. Key exports to learn:
   - `loader` — server-side data loading
   - `default` — the React component
   - `meta` — page metadata
   - `ErrorBoundary` — error handling per route
   - `headers` — HTTP response headers

### Data Loading & Actions (Days 5-6)
1. Read [Data Loading](https://reactrouter.com/start/framework/data-loading) and [Actions](https://reactrouter.com/start/framework/actions)
2. Learn data loading patterns:
   ```typescript
   // Loader for a search page
   export async function loader({ request }: Route.LoaderArgs) {
     const url = new URL(request.url)
     const query = url.searchParams.get("q")
     const type = url.searchParams.get("type")
     const results = await searchPokemon(query, type)
     return { results, query, type }
   }
   ```
3. Learn form actions:
   ```typescript
   // Action for handling form submissions
   export async function action({ request }: Route.ActionArgs) {
     const formData = await request.formData()
     const pokemonId = formData.get("pokemonId")
     await addToFavorites(pokemonId)
     return { success: true }
   }
   ```
4. Key concepts:
   - Loaders run before the component renders
   - Actions handle form submissions (POST, PUT, DELETE)
   - `useLoaderData` and `useActionData` hooks
   - `useFetcher` for non-navigation mutations

### Navigation & Pending UI (Days 7-8)
1. Read [Navigating](https://reactrouter.com/start/framework/navigating) and [Pending UI](https://reactrouter.com/start/framework/pending-ui)
2. Learn navigation patterns:
   - `<Link>` and `<NavLink>` components
   - `useNavigate` hook for programmatic navigation
   - `useNavigation` for pending/loading states
   - `<Form>` component for data mutations

### Rendering Strategies (Day 9)
1. Read [Rendering Strategies](https://reactrouter.com/start/framework/rendering)
2. Understand the options:
   - **SSR** (Server-Side Rendering) — default, renders on each request
   - **SPA** (Single Page App) — client-only rendering
   - **Static Pre-rendering** — generates HTML at build time
3. Configure in `react-router.config.ts`

### Tutorials
1. Complete the [Quick Start](https://reactrouter.com/tutorials/quickstart) tutorial
2. Complete the [Address Book](https://reactrouter.com/tutorials/address-book) tutorial — this covers the full Framework Mode workflow

## GraphQL Fundamentals (Day 10)

1. Learn what GraphQL is and how it differs from REST:
   - REST: multiple endpoints, fixed data shape
   - GraphQL: single endpoint, client decides what data to fetch
2. Read [GraphQL Introduction](https://graphql.org/learn/)
3. Key concepts:
   - Queries (reading data)
   - Variables and arguments
   - Fragments (reusable field sets)
   - Using a GraphQL playground/explorer
4. Explore the [PokeAPI GraphQL Playground](https://beta.pokeapi.co/graphql/v1beta):
   ```graphql
   # Example: Fetch Pokemon with their types and stats
   query GetPokemon($limit: Int, $offset: Int) {
     pokemon_v2_pokemon(limit: $limit, offset: $offset) {
       id
       name
       pokemon_v2_pokemontypes {
         pokemon_v2_type {
           name
         }
       }
       pokemon_v2_pokemonstats {
         base_stat
         pokemon_v2_stat {
           name
         }
       }
       pokemon_v2_pokemonsprites {
         sprites
       }
     }
   }
   ```

### PokeAPI GraphQL Resources
- [PokeAPI Documentation](https://pokeapi.co/docs/graphql)
- GraphQL endpoint: `https://beta.pokeapi.co/graphql/v1beta`
- No API key required — fully public

## Assignment: Pokedex Explorer

Build a Pokedex Explorer app using React Router Framework Mode and the [PokeAPI GraphQL endpoint](https://beta.pokeapi.co/graphql/v1beta):
- [ ] Set up project with `create-react-router`, TypeScript, and TailwindCSS
- [ ] Define routes in `routes.ts`:
  - **Home** (`/`) — list of Pokemon with loader
  - **Search** (`/search?q=...`) — search by name with URL params and loader
  - **Pokemon detail** (`/pokemon/:id`) — stats, types, abilities with loader
  - **Type** (`/type/:name`) — browse Pokemon by type (fire, water, etc.)
  - **Favorites** (`/favorites`) — saved favorites with action to add/remove
- [ ] Fetch all data using GraphQL queries in route `loader` functions
- [ ] Implement search using `<Form>` and URL search params
- [ ] Add/remove favorites using route `action` functions
- [ ] Use `<Link>` and `<NavLink>` for navigation
- [ ] Add pending UI states during navigation (loading indicators)
- [ ] Implement error boundaries for failed API requests
- [ ] Add pagination using GraphQL `limit` and `offset` variables
- [ ] Deploy to production

---

[← Back to Overview](./README.md) | [Previous: Week 9-10](./week-09-10-react.md) | [Next: Week 13 →](./week-13-shopify.md)
