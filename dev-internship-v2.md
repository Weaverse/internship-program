<div align="center">
  <img src="https://weaverse.io/static/images/logo.svg" alt="Weaverse Logo" width="180"/>
  
  # Weaverse Developer Internship Program
  
  A comprehensive curriculum designed to transform interns/freshers with basic programming knowledge into skilled full-stack developers specializing in modern e-commerce development.
  
  **[How to Apply](README.md#how-to-apply)** | **[Contact Us](README.md#contact)**
</div>

---

## Table of Contents

- [Weaverse Developer Internship Program](#weaverse-developer-internship-program)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
    - [Structure](#structure)
    - [Learning Outcomes](#learning-outcomes)
  - [Technology Stack](#technology-stack)
    - [Core Technologies](#core-technologies)
  - [Pre-Program Requirements](#pre-program-requirements)
    - [English for Developers (Self-Study, Recommended)](#english-for-developers-self-study-recommended)
    - [Orientation \& Setup](#orientation--setup)
  - [Week 1-2: JavaScript](#week-1-2-javascript)
    - [Assignment](#assignment)
  - [Week 3-4: CSS \& Modern Styling](#week-3-4-css--modern-styling)
    - [Assignment](#assignment-1)
  - [Week 5-6: TypeScript \& Build Tools](#week-5-6-typescript--build-tools)
    - [Assignment](#assignment-2)
  - [Week 7-8: Node.js \& Backend Development](#week-7-8-nodejs--backend-development)
    - [Assignment](#assignment-3)
  - [Week 9-10: React](#week-9-10-react)
    - [Assignment](#assignment-4)
  - [Week 11-12: Advanced Topics \& Security](#week-11-12-advanced-topics--security)
    - [Assignment](#assignment-5)
  - [Week 13: Shopify Development](#week-13-shopify-development)
  - [Week 14: Weaverse Integration](#week-14-weaverse-integration)
  - [Week 15-16: Final Project \& Internship Review](#week-15-16-final-project--internship-review)
  - [Graduation](#graduation)

---

## Overview

### Structure

- **Duration**: 12-16 weeks (3-4 months)
- **Schedule**: 30-36 hours per week
- **Format**: Hybrid learning with mentorship support
- **Focus**: Frontend, Backend, Integration & Tools

### Learning Outcomes

By completing this program, interns will:
- Build production-ready web applications using modern JavaScript frameworks
- Understand full-stack development with React and Node.js
- Create responsive, accessible user interfaces
- Work with databases and API development
- Deploy applications to production environments
- Specialize in Shopify and Weaverse development

---

## Technology Stack

### Core Technologies

| Category        | Technologies                | Purpose                    |
| --------------- | --------------------------- | -------------------------- |
| **Languages**   | JavaScript, TypeScript      | Core programming           |
| **Frontend**    | React, TailwindCSS          | User interface development |
| **Backend**     | Node.js, Express.js         | Server-side development    |
| **Database**    | PostgreSQL, Prisma ORM      | Data persistence           |
| **Build Tools** | Vite, npm, pnpm             | Development workflow       |
| **E-commerce**  | Shopify, Hydrogen, Weaverse | Headless commerce          |

---

## Pre-Program Requirements

### English for Developers (Self-Study, Recommended)

Before starting the official program, we recommend completing:
- [FreeCodeCamp English for Developers](https://www.freecodecamp.org/learn/b1-english-for-developers/)
- Study at home during your free time
- Essential for reading documentation and communicating with team members

### Orientation & Setup

1. **Company Introduction**
   - Explore Weaverse at [weaverse.io](https://weaverse.io)
   - Try the demo at [studio.weaverse.io/demo](https://studio.weaverse.io/demo)
   - Understand our mission and products

2. **Development Environment Setup**
   - Install [Brave Browser](https://brave.com/) or Chrome
   - Set up [iTerm2](https://iterm2.com/) (macOS) or Windows Terminal
   - Install [Git](https://git-scm.com/) and create [GitHub](https://github.com) account
   - Install [Node.js](https://nodejs.org/) (LTS version)
   - Choose IDE: [VS Code](https://code.visualstudio.com/) or [Cursor](https://cursor.sh/)

**Setup Checklist:**
```bash
# Verify installations
node --version  # Should show v18+ 
npm --version   # Should show v8+
git --version   # Should show 2.30+

# Configure Git
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

---

## Week 1-2: JavaScript & TypeScript

|                 |                                                                                                              |
| :-------------- | :----------------------------------------------------------------------------------------------------------- |
| Learning Topics | Core JavaScript, ES6+ features, Functional programming, TypeScript fundamentals, Type-safe development       |
| Objectives      | Complete 30 JS exercises, Master TypeScript basics, Build a type-safe CLI task manager with full TypeScript |

**Beginner JavaScript (Skip if already familiar)**
1. Complete [JavaScript Beginner Tutorial](https://www.w3schools.com/js/default.asp)

**Core JavaScript (Days 1-3)**
1. Register an account on [Exercism](https://exercism.org/tracks/javascript)
2. Complete the following exercises:
   - **15 Easy exercises** - Start with basics and build confidence
   - **10 Medium exercises** - Apply concepts in more complex scenarios
   - **5 Hard exercises** - Challenge yourself with advanced problems
3. Focus on understanding:
   - Variables and data types
   - Functions and scope
   - Arrays and objects
   - Control flow and loops
   - String manipulation

**Functional Programming (Days 4-5)**
1. Start [LearnRx Interactive Tutorial](https://reactivex.io/learnrx/)
2. Complete exercises 1-20 (Arrays and Functions)
3. Focus on:
   - Array methods (map, filter, reduce)
   - Function composition
   - Immutability concepts
   - Promises and Async/Await

**TypeScript Fundamentals (Days 6-10)**
1. Read [TypeScript Handbook - The Basics](https://www.typescriptlang.org/docs/handbook/2/basics.html)
2. Set up TypeScript environment:
   ```bash
   npm install -g typescript ts-node @types/node
   tsc --init
   ```
3. Learn essential TypeScript concepts:
   - Type annotations and inference
   - Interfaces and type aliases
   - Function types and generics basics
   - Union and intersection types
   - Enums and literal types
   - Type guards and narrowing

4. Practice with TypeScript exercises:
   ```typescript
   // Example: Type-safe task interface
   interface Task {
     id: string;
     title: string;
     completed: boolean;
     createdAt: Date;
     priority: 'low' | 'medium' | 'high';
   }
   
   // Type-safe function
   function filterTasksByPriority(tasks: Task[], priority: Task['priority']): Task[] {
     return tasks.filter(task => task.priority === priority);
   }
   ```

### Assignment

Build a Type-Safe Task Manager CLI in TypeScript:
- [ ] Set up TypeScript project with proper tsconfig.json
- [ ] Define interfaces for Task, User, and Project
- [ ] Create type-safe command-line interface using Commander.js
- [ ] Implement CRUD operations with full type safety:
  - Add tasks with validation
  - Remove tasks by ID
  - Update task status and priority
  - List and filter tasks
- [ ] Add project management features:
  - Create projects
  - Assign tasks to projects
  - View tasks by project
- [ ] Implement data persistence with type-safe JSON handling
- [ ] Add input validation using type guards
- [ ] Include error handling with custom error types
- [ ] Write at least 5 unit tests using Jest with TypeScript

**Required TypeScript features to demonstrate:**
- Interfaces and type aliases
- Generics for reusable functions
- Union types for command options
- Type guards for validation
- Proper typing for async operations

---

## Week 3-4: CSS & Modern Styling

|                 |                                                                                                          |
| :-------------- | :------------------------------------------------------------------------------------------------------- |
| Learning Topics | Flexbox, CSS Grid, Responsive design, TailwindCSS, Modern styling patterns                               |
| Objectives      | Complete Flexbox Froggy and Grid Garden, Build responsive FreshCart template clone with TailwindCSS only |

**Flexbox & Grid**
1. Complete all levels at [Flexbox Froggy](https://flexboxfroggy.com/)
2. Complete all levels at [Grid Garden](https://codepip.com/games/grid-garden/)

**TailwindCSS**

1. Read [TailwindCSS Documentation](https://tailwindcss.com/docs)
2. Set up TailwindCSS in a project
3. Learn utility classes:
   - Layout & Spacing
   - Colors & Typography
   - Flexbox & Grid utilities

### Assignment

Build [FreshCart Site](https://freshcart-template.codescandy.com/):
- [ ] Build fully responsive design
- [ ] Use only TailwindCSS (no custom CSS)
- [ ] Deploy to GitHub Pages

---

## Week 5-6: AI Integration & Build Tools

|                 |                                                                                                            |
| :-------------- | :--------------------------------------------------------------------------------------------------------- |
| Learning Topics | AI prompt engineering, IDE AI integration, Vite build system, Modern development workflow with AI          |
| Objectives      | Master AI-assisted development, Set up Google Gemini in IDE, Build AI-enhanced BudgetY app with TypeScript |

**AI Prompt Engineering (Days 1-3)**

1. Complete [Anthropic Prompt Engineering Tutorial](https://github.com/anthropics/prompt-eng-interactive-tutorial)
2. Learn key concepts:
   - Clear instruction formulation
   - Context provision strategies
   - Few-shot prompting
   - Chain-of-thought reasoning
   - Common pitfalls and best practices

**IDE AI Integration (Days 4-5)**

1. **Set up Google Gemini in VS Code/Cursor**
   ```bash
   # Install Continue extension for VS Code
   # Or use Cursor with built-in AI features
   ```

2. **Configure AI Assistant**
   - Set up API keys securely
   - Configure context awareness
   - Learn keyboard shortcuts
   - Practice AI-assisted coding patterns

3. **AI Development Workflows**
   - Code generation from comments
   - Refactoring with AI assistance
   - Debugging with AI insights
   - Documentation generation
   - Test case generation

**Build Tools with Vite (Days 6-7)**
1. Read [Vite Documentation](https://vitejs.dev/guide/)
2. Learn about:
   - Project scaffolding
   - Hot Module Replacement
   - Build optimization
   - Environment variables
   - Plugin ecosystem

**AI-Powered Development Practices**
```typescript
// Example: Using AI to generate TypeScript interfaces
// Prompt: "Generate TypeScript interfaces for a budget tracking app with transactions, categories, and monthly summaries"

interface Transaction {
  id: string;
  amount: number;
  category: Category;
  description: string;
  date: Date;
  type: 'income' | 'expense';
}

interface Category {
  id: string;
  name: string;
  icon: string;
  color: string;
  budget?: number;
}

interface MonthlySummary {
  month: string;
  year: number;
  totalIncome: number;
  totalExpenses: number;
  categoryBreakdown: Map<string, number>;
}
```

### Assignment

Build AI-Enhanced [BudgetY App](https://hta218.github.io/budget-y/) with:
- [ ] Set up project with Vite + TypeScript + TailwindCSS
- [ ] Configure AI assistant in your IDE
- [ ] Use AI to generate initial TypeScript interfaces and types
- [ ] Implement features with AI assistance:
  - Transaction CRUD operations
  - Category management
  - Budget tracking and alerts
  - Data visualization components
- [ ] Add AI-powered features:
  - Smart transaction categorization
  - Spending insights generation
  - Budget recommendations
- [ ] Document AI prompts used for each major feature
- [ ] Write unit tests (generate test cases with AI)
- [ ] Create a development journal documenting:
  - Effective prompts used
  - Time saved with AI assistance
  - Challenges and solutions
- [ ] Deploy to production

**AI Integration Requirements:**
- Use AI for at least 50% of code generation
- Document 10+ effective prompts in markdown file
- Generate all TypeScript types with AI assistance
- Create test cases using AI
- Use AI for code review and optimization

---

## Week 7-8: Node.js & Backend Development

|                 |                                                                                                       |
| :-------------- | :---------------------------------------------------------------------------------------------------- |
| Learning Topics | Node.js ecosystem, Express.js, REST APIs, Database design, Prisma ORM                                 |
| Objectives      | Build complete Blog API with authentication, Implement CRUD operations, Create database relationships |

**Node.js Fundamentals**
- Node.js basics and modules
- NPM package management
- File system operations
- Environment variables

**Express.js**
1. Read [Express Getting Started](https://expressjs.com/en/starter/installing.html)
2. Build a simple API:
   ```javascript
   // Basic Express setup
   const express = require('express');
   const app = express();
   
   app.use(express.json());
   
   app.get('/api/health', (req, res) => {
     res.json({ status: 'OK' });
   });
   
   app.listen(3000);
   ```

**Database & Prisma**

1. Register a free Database hosting service (Supabase, Railway, etc.)
1. Follow [Prisma Getting Started](https://www.prisma.io/docs/getting-started/setup-prisma/start-from-scratch/relational-databases-typescript-postgresql)
2. Learn:
   - Schema definition
   - Migrations
   - CRUD operations

### Assignment

Complete Blog API Project:
- [ ] Set up Node.js project with Express and TypeScript
- [ ] Configure Prisma with PostgreSQL database
- [ ] Implement JWT-based authentication (register/login)
- [ ] Create CRUD operations for posts
- [ ] Build comments system
- [ ] Add categories and tags functionality
- [ ] Deploy to production

**Required Endpoints:**
```
POST   /api/auth/register
POST   /api/auth/login
GET    /api/posts
GET    /api/posts/:id
POST   /api/posts
PUT    /api/posts/:id
DELETE /api/posts/:id
```

**Database Schema:**
```prisma
model User {
  id        String   @id @default(cuid())
  email     String   @unique
  name      String
  password  String
  posts     Post[]
  comments  Comment[]
  createdAt DateTime @default(now())
}

model Post {
  id        String    @id @default(cuid())
  title     String
  content   String
  published Boolean   @default(false)
  author    User      @relation(fields: [authorId], references: [id])
  authorId  String
  comments  Comment[]
  createdAt DateTime  @default(now())
  updatedAt DateTime  @updatedAt
}

model Comment {
  id        String   @id @default(cuid())
  content   String
  post      Post     @relation(fields: [postId], references: [id])
  postId    String
  author    User     @relation(fields: [authorId], references: [id])
  authorId  String
  createdAt DateTime @default(now())
}
```

---

## Week 9-10: React

|                 |                                                                                                                          |
| :-------------- | :----------------------------------------------------------------------------------------------------------------------- |
| Learning Topics | React components, Hooks, State management with Preact Signals, ShadcnUI components, TypeScript integration, Deployment |
| Objectives      | Master React fundamentals, Build complete Blog frontend with modern UI components, Deploy to production                  |

**React Basics**

1. Read [React Documentation](https://react.dev/learn)
2. Complete official tutorial
3. Learn:
   - Components and Props
   - State and Lifecycle
   - Handling Events
   - Conditional Rendering
   - useState and useEffect
   - Custom hooks
   - Rules of hooks

**Modern UI with ShadcnUI**

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

**State Management with Preact Signals**

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

### Assignment

Complete Blog Platform with Modern Stack:
- [ ] Set up React project with TypeScript, TailwindCSS, and ShadcnUI
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
- [ ] Implement comment system
- [ ] Add search and filtering features
- [ ] Connect to backend API with proper error handling
- [ ] Include form validation with react-hook-form
- [ ] Deploy to production:
  - Frontend to Vercel
  - Backend to Fly.io or Vercel Functions
  - Configure environment variables
  - Set up custom domain (optional)

**Deployment Steps:**
```bash
# Frontend deployment to Vercel
npm install -g vercel
vercel
# Follow prompts to configure project

# Backend deployment to Fly.io
curl -L https://fly.io/install.sh | sh
fly launch
fly deploy
# Configure DATABASE_URL and other secrets
fly secrets set JWT_SECRET=your-secret-here
```

---

## Week 11-12: Advanced Topics & Security

|                 |                                                                                                          |
| :-------------- | :------------------------------------------------------------------------------------------------------- |
| Learning Topics | Schema validation with Zod, Authentication & Authorization, Security best practices, React Router        |
| Objectives      | Implement secure authentication system, Add comprehensive validation, Build advanced e-commerce features |

**Zod Schema Validation**
1. Read [Zod Documentation](https://zod.dev)
2. Implement validation patterns:
   ```typescript
   import { z } from 'zod';
   
   // API validation schemas
   const UserSchema = z.object({
     email: z.string().email(),
     password: z.string().min(8).regex(/[A-Z]/, 'Must contain uppercase'),
     name: z.string().min(2).max(50)
   });
   
   const ProductSchema = z.object({
     title: z.string().min(1).max(200),
     price: z.number().positive(),
     category: z.enum(['electronics', 'clothing', 'books', 'other']),
     stock: z.number().int().min(0)
   });
   
   // Form validation with error messages
   const LoginSchema = z.object({
     email: z.string().email('Invalid email address'),
     password: z.string().min(1, 'Password is required')
   });
   ```

**Security Best Practices**
1. **Authentication & Authorization**
   - JWT implementation with refresh tokens
   - Role-based access control (RBAC)
   - Secure password hashing with bcrypt
   - Session management

2. **API Security**
   ```typescript
   // Rate limiting
   import rateLimit from 'express-rate-limit';
   
   const limiter = rateLimit({
     windowMs: 15 * 60 * 1000, // 15 minutes
     max: 100 // limit each IP to 100 requests per windowMs
   });
   
   // CORS configuration
   const corsOptions = {
     origin: process.env.FRONTEND_URL,
     credentials: true,
     optionsSuccessStatus: 200
   };
   
   // Input sanitization
   app.use(helmet());
   app.use(mongoSanitize());
   ```

**React Router Advanced Patterns**

1. Complete [React Router Tutorial](https://reactrouter.com/en/main/start/tutorial)
2. Learn advanced concepts:
   - Route guards and middleware
   - Lazy loading with code splitting
   - Nested layouts
   - Programmatic navigation
   - Route transitions

### Assignment

Build a Secure E-commerce Store with Advanced Features:
- [ ] Implement comprehensive authentication system:
  - User registration with email verification
  - Login with JWT tokens
  - Password reset functionality
  - Remember me option
- [ ] Create product catalog with advanced routing:
  - Category-based routes (`/products/electronics`)
  - Search with query parameters
  - Pagination and filtering
- [ ] Build secure admin dashboard:
  - Protected routes with role checking
  - Product CRUD operations
  - Order management
  - User management
- [ ] Add security features:
  - Rate limiting on API endpoints
  - Input validation with Zod on all forms
  - XSS protection
  - CSRF tokens
  - Secure headers with Helmet
- [ ] Implement shopping cart with:
  - Persistent state (localStorage + backend)
  - Guest checkout option
  - Stock validation
- [ ] Add payment simulation:
  - Checkout flow with form validation
  - Order confirmation
  - Email notifications (mock)
- [ ] Performance optimizations:
  - Lazy load routes
  - Image optimization
  - API response caching

*Use the AI assistant you set up in Week 5-6 to help with complex implementations.*

---

## Week 13: Shopify Development

|                 |                                                                                                        |
| :-------------- | :----------------------------------------------------------------------------------------------------- |
| Learning Topics | Shopify ecosystem, Partner account, Admin APIs, Hydrogen framework, Headless commerce                  |
| Objectives      | Set up Shopify development environment, Build custom Hydrogen storefront, Implement cart functionality |

**Shopify Basics**
1. Create a partner account
2. Set up development store
3. Explore admin interface
4. Understand Shopify concepts:
   - Products and collections
   - Orders and customers
   - Themes and apps

**Shopify Hydrogen Development**

**Hydrogen Setup**
1. Read [Hydrogen Documentation](https://shopify.dev/docs/custom-storefronts/hydrogen)
2. Create Hydrogen project:
   ```bash
   npm create @shopify/hydrogen@latest
   ```

**Custom Storefront**
Build features:
- Product listing
- Product details
- Shopping cart
- Checkout redirect

---

## Week 14: Weaverse Integration

|                 |                                                                                                       |
| :-------------- | :---------------------------------------------------------------------------------------------------- |
| Learning Topics | Weaverse SDK, Visual components, Component schemas, Final project integration                         |
| Objectives      | Master Weaverse platform, Create custom visual components, Build complete e-commerce capstone project |

**Weaverse Setup**
1. Read [Weaverse Documentation](https://weaverse.io/docs)
2. Set up Weaverse project:
   ```bash
   npm create @weaverse/hydrogen@latest
   ```

**Component Development**
- Create custom sections
- Define component schemas
- Implement visual editing
- Test in Weaverse Studio

## Week 15-16: Final Project & Internship Review

Build a complete Weaverse Hydrogen theme:
- [ ] Set up Weaverse + Hydrogen project
- [ ] Create custom visual components with schemas
- [ ] Build product catalog with Shopify integration
- [ ] Implement shopping cart and checkout
- [ ] Add customer account management
- [ ] Create visual page builder experience
- [ ] Design responsive theme with TailwindCSS
- [ ] Implement SEO optimization
- [ ] Add performance monitoring
- [ ] Include comprehensive testing
- [ ] Deploy to production
- [ ] Write technical documentation
- [ ] Create deployment guide
- [ ] Prepare final presentation
- [ ] Document future improvements

**Presentation & Review**
- Live demo of project
- Code walkthrough
- Technical documentation
- Deployment guide
- Future improvements

---

## Graduation

Congratulations! You've completed the Weaverse Developer Internship Program. You're now equipped with:

- Modern JavaScript and TypeScript skills
- Full-stack development experience
- E-commerce platform expertise
- Production deployment knowledge
- Professional development practices

Happy learning and growing!

---

*The Weaverse Team 🤝*