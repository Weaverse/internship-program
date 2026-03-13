# Week 9-10: React & GraphQL

> [!IMPORTANT]
> **DO NOT** use AI tools to write code for you. You come here to **LEARN**, the goal of this program is to build
> your programming skills through **hands-on** practice. AI assistants can help explain
> concepts or debug issues, but writing the code yourself is **essential** for learning.

---

|                 |                                                                                                                                   |
| :-------------- | :-------------------------------------------------------------------------------------------------------------------------------- |
| Learning Topics | React components, Hooks, Data fetching, State management with Preact Signals, ShadcnUI, GraphQL fundamentals                     |
| Objectives      | Master React fundamentals, Learn data fetching patterns, Build Blog frontend, Learn GraphQL with Pokemon API                      |

## React Basics

1. Read [React Documentation](https://react.dev/learn)
2. Complete [official tutorial](https://react.dev/learn/tutorial-tic-tac-toe)
3. Learn:
   - Components and Props
   - State and Lifecycle
   - Handling Events
   - Conditional Rendering
   - useState and useEffect
   - Custom hooks
   - Rules of hooks

## Data Fetching

1. Learn how to fetch data in React:
   ```typescript
   // Basic fetch pattern
   function usePosts() {
     const [posts, setPosts] = useState<Post[]>([])
     const [loading, setLoading] = useState(true)
     const [error, setError] = useState<string | null>(null)

     useEffect(() => {
       async function fetchPosts() {
         try {
           const response = await fetch('/api/posts')
           if (!response.ok) throw new Error('Failed to fetch')
           const data = await response.json()
           setPosts(data)
         } catch (err) {
           setError(err.message)
         } finally {
           setLoading(false)
         }
       }
       fetchPosts()
     }, [])

     return { posts, loading, error }
   }
   ```
2. Key concepts:
   - The `fetch` API and handling responses
   - Loading, error, and success states
   - `useEffect` for data fetching on mount
   - Extracting reusable data fetching hooks
   - Handling API errors gracefully

## Modern UI with ShadcnUI

1. Set up ShadcnUI in your project:
   ```bash
   npx shadcn@latest init
   ```
2. Install essential components:
   ```bash
   npx shadcn@latest add button card dialog form input label
   npx shadcn@latest add dropdown-menu toast alert
   ```
3. Learn component customization with TailwindCSS
4. Understand the copy-paste component philosophy

## State Management with Preact Signals

1. Install Preact Signals:
   ```bash
   npm install @preact/signals-react
   ```
2. Create global state stores:
   ```typescript
   // stores/authStore.ts
   import { signal, computed } from '@preact/signals-react'

   export const currentUser = signal<User | null>(null)
   export const isAuthenticated = computed(() => currentUser.value !== null)

   // stores/blogStore.ts
   export const posts = signal<Post[]>([])
   export const selectedPost = signal<Post | null>(null)
   export const isLoading = signal(false)
   ```
3. Learn signal patterns:
   - Creating reactive state
   - Computed values
   - Effects and subscriptions
   - No providers needed!

## Assignment 1: Blog Frontend

> [!NOTE]
> Routing is **not required** for this assignment. You can manage all views using state (e.g., show/hide components conditionally). Routing will be covered in Week 11-12. If you already know React Router, feel free to use it as a nice-to-have.

Complete Blog Platform with Modern Stack:
- [ ] Set up React project with TypeScript, Preact Signals, TailwindCSS, and ShadcnUI
- [ ] Use ShadcnUI components for:
  - Form inputs and validation
  - Cards for post display
  - Dialogs for confirmations
  - Toast notifications for user feedback
  - Dropdown menus for user actions
- [ ] Implement data fetching:
  - Fetch posts, comments, and user data from the backend API (Week 7-8)
  - Handle loading and error states
- [ ] Implement state management with Preact Signals:
  - User authentication state
  - Blog posts and comments state
  - Loading and error states
  - Theme preferences
- [ ] Create responsive layout components
- [ ] Implement user authentication UI
- [ ] Build post listing and detail views
- [ ] Add create/edit post functionality
- [ ] Add search and filtering features
- [ ] Connect to backend API with proper error handling
- [ ] Include form validation with react-hook-form
- [ ] Deploy to production

## GraphQL Fundamentals

1. Learn what GraphQL is and how it differs from REST:
   - REST: multiple endpoints, fixed data shape
   - GraphQL: single endpoint, client decides what data to fetch
2. Read [GraphQL Introduction](https://graphql.org/learn/)
3. Key concepts:
   - Queries (reading data)
   - Variables and arguments
   - Fragments (reusable field sets)
   - Using a GraphQL playground/explorer
4. Practice with [PokeAPI GraphQL](https://pokeapi.co/docs/graphql):
   ```graphql
   # Example: Fetch a Pokemon with specific fields
   query GetPokemon($name: String!) {
     pokemon_v2_pokemon(where: { name: { _eq: $name } }) {
       name
       height
       weight
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
     }
   }
   ```

## Assignment 2: Pokemon Explorer (GraphQL)

> [!NOTE]
> This assignment focuses on learning GraphQL data fetching. UI/styling is **not the priority** — keep it simple and functional.

Build a Pokemon Explorer app using the [PokeAPI GraphQL endpoint](https://beta.pokeapi.co/graphql/v1beta):
- [ ] Set up a React + TypeScript project
- [ ] Fetch and display a list of Pokemon using a GraphQL query
- [ ] Implement Pokemon detail view (stats, types, abilities)
- [ ] Add search/filter by name or type using GraphQL variables
- [ ] Implement pagination or infinite scroll using GraphQL `limit` and `offset`
- [ ] Handle loading and error states
- [ ] Deploy to production

---

[← Back to Overview](./README.md) | [Previous: Week 7-8](./week-07-08-nodejs-backend.md) | [Next: Week 11-12 →](./week-11-12-advanced-react.md)
