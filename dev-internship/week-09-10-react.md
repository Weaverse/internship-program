# Week 9-10: React

> [!IMPORTANT]
> **DO NOT** use AI tools to write code for you. You come here to **LEARN**, the goal of this program is to build
> your programming skills through **hands-on** practice. AI assistants can help explain
> concepts or debug issues, but writing the code yourself is **essential** for learning.

---

|                 |                                                                                                                        |
| :-------------- | :--------------------------------------------------------------------------------------------------------------------- |
| Learning Topics | React components, Hooks, Data fetching, State management with Preact Signals, ShadcnUI components                     |
| Objectives      | Master React fundamentals, Learn data fetching patterns, Build complete Blog frontend with modern UI                   |

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

3. **Connecting to your backend API (cross-origin)**

   Your React app (e.g., `localhost:5173`) and your backend API (e.g., `localhost:5000`) run on different ports. Browsers block these cross-origin requests by default. The simplest solution is Vite's built-in proxy — add this to your Vite config and all `/api` requests will be forwarded to your backend:
   ```typescript
   // vite.config.ts
   export default defineConfig({
     plugins: [react()],
     server: {
       proxy: {
         '/api': 'http://localhost:5000'
       }
     }
   })
   ```
   Now `fetch('/api/posts')` in your React code will automatically proxy to `http://localhost:5000/api/posts` during development — no CORS issues, no backend changes needed.

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

## Assignment

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

---

[← Back to Overview](./README.md) | [Previous: Week 7-8](./week-07-08-nodejs-backend.md) | [Next: Week 11-12 →](./week-11-12-react-router.md)
