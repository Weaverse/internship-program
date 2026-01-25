# Week 9-10: React

> [!IMPORTANT]
> **DO NOT** use AI tools to write code for you. You come here to **LEARN**, the goal of this program is to build
> your programming skills through **hands-on** practice. AI assistants can help explain
> concepts or debug issues, but writing the code yourself is **essential** for learning.

---

|                 |                                                                                                                        |
| :-------------- | :--------------------------------------------------------------------------------------------------------------------- |
| Learning Topics | React components, Hooks, State management with Preact Signals, ShadcnUI components, TypeScript integration, Deployment |
| Objectives      | Master React fundamentals, Build complete Blog frontend with modern UI components, Deploy to production                |

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

## Modern UI with ShadcnUI

1. Set up ShadcnUI in your project:
   ```bash
   npx shadcn-ui@latest init
   ```
2. Install essential components:
   ```bash
   npx shadcn-ui@latest add button card dialog form input label
   npx shadcn-ui@latest add dropdown-menu toast alert
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
   import { signal, computed } from '@preact/signals-react';

   export const currentUser = signal<User | null>(null);
   export const isAuthenticated = computed(() => currentUser.value !== null);

   // stores/blogStore.ts
   export const posts = signal<Post[]>([]);
   export const selectedPost = signal<Post | null>(null);
   export const isLoading = signal(false);
   ```
3. Learn signal patterns:
   - Creating reactive state
   - Computed values
   - Effects and subscriptions
   - No providers needed!

## Assignment

Complete Blog Platform with Modern Stack:
- [ ] Set up React project with TypeScript, Preact Signals, TailwindCSS, and ShadcnUI
- [ ] Use ShadcnUI components for:
  - Form inputs and validation
  - Cards for post display
  - Dialogs for confirmations
  - Toast notifications for user feedback
  - Dropdown menus for user actions
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

[← Back to Overview](./README.md) | [Previous: Week 7-8](./week-07-08-nodejs-backend.md) | [Next: Week 11-12 →](./week-11-12-advanced-security.md)
