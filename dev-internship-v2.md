<div align="center">
  <img src="https://weaverse.io/static/images/logo.svg" alt="Weaverse Logo" width="180"/>
  
  # Weaverse Developer Internship Program
  
  A comprehensive 16-week curriculum designed to transform interns/freshers with basic programming knowledge into skilled full-stack developers specializing in modern e-commerce development.
  
  **[How to Apply](README.md#how-to-apply)** | **[Contact Us](README.md#contact)**
</div>

---

## Table of Contents

- [Program Overview](#program-overview)
- [About Weaverse](#about-weaverse)
- [Technology Stack](#technology-stack)
- [Pre-Program Requirements](#pre-program-requirements)
- [Week 1-2: JavaScript Fundamentals](#week-1-2-javascript-fundamentals)
- [Week 3-4: CSS & Modern Styling](#week-3-4-css--modern-styling)
- [Week 5-6: TypeScript & Build Tools](#week-5-6-typescript--build-tools)
- [Week 7-8: Node.js & Backend Development](#week-7-8-nodejs--backend-development)
- [Week 9-10: React Fundamentals](#week-9-10-react-fundamentals)
- [Week 11-12: Advanced Topics & Security](#week-11-12-advanced-topics--security)
- [Week 13-14: Shopify Development](#week-13-14-shopify-development)
- [Week 15-16: Weaverse Integration & Final Project](#week-15-16-weaverse-integration--final-project)

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

## Week 1-2: JavaScript Fundamentals

### Learning Objectives
- Master JavaScript basics and ES6+ features
- Understand asynchronous programming
- Practice problem-solving with coding exercises

### Week 1: JavaScript Basics

**Core JavaScript**
1. Register on [Exercism](https://exercism.org/tracks/javascript)
2. Complete these exercises in order:
   - Hello World
   - Two Fer
   - Resistor Color
   - Gigasecond
   - RNA Transcription

**Functions & Arrays**
- Complete Exercism exercises:
  - Space Age
  - Pangram
  - Matrix
  - Bob
  - Allergies

### Week 2: Advanced JavaScript

**Functional Programming**
1. Start [LearnRx Interactive Tutorial](https://reactivex.io/learnrx/)
2. Complete exercises 1-20 (Arrays and Functions)
3. Focus on:
   - Array methods (map, filter, reduce)
   - Function composition
   - Immutability concepts

**Asynchronous JavaScript**
- Complete LearnRx exercises 21-42
- Complete remaining Exercism "Easy" exercises
- Topics covered:
  - Promises
  - Async/Await
  - Event handling

### Week 1-2 Assignment

**Build a Task Manager CLI**
Create a command-line task manager with:
- Add/remove tasks
- Mark tasks as complete
- List all tasks
- Filter tasks by status
- Save tasks to JSON file

```javascript
// Example usage
node task-manager.js add "Learn JavaScript"
node task-manager.js list
node task-manager.js complete 1
node task-manager.js remove 1
```

---

## Week 3-4: CSS & Modern Styling

### Learning Objectives
- Master CSS layout techniques (Flexbox, Grid)
- Learn utility-first CSS with TailwindCSS
- Build responsive, modern interfaces

### Week 3: CSS Fundamentals

**Flexbox Mastery**
1. Complete all levels at [Flexbox Froggy](https://flexboxfroggy.com/)
2. Practice exercises:
   - Create a navigation bar
   - Build a card layout
   - Design a footer component

**CSS Grid**
1. Complete all levels at [Grid Garden](https://codepip.com/games/grid-garden/)
2. Practice exercises:
   - Create a photo gallery
   - Build a dashboard layout
   - Design a magazine-style layout

**Responsive Design**
- Media queries
- Mobile-first approach
- Viewport units and techniques

### Week 4: TailwindCSS

**TailwindCSS Basics**
1. Read [TailwindCSS Documentation](https://tailwindcss.com/docs)
2. Set up TailwindCSS in a project
3. Learn utility classes:
   - Layout & Spacing
   - Colors & Typography
   - Flexbox & Grid utilities

**Build FreshCart Clone**
- Reference: [FreshCart Template](https://freshcart-template.codescandy.com/)
- Requirements:
  - Fully responsive design
  - Use only TailwindCSS (no custom CSS)
  - Implement all major sections:
    - Header with navigation
    - Hero section
    - Product grid
    - Features section
    - Footer

### Week 3-4 Assignment

**Complete FreshCart Clone**
- All pages must be responsive
- Use TailwindCSS utilities only
- Include hover states and transitions
- Deploy to GitHub Pages

---

## Week 5-6: TypeScript & Build Tools

### Learning Objectives
- Understand TypeScript fundamentals
- Master modern build tools with Vite
- Build type-safe applications

### Week 5: TypeScript

**TypeScript Basics**
1. Read [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html):
   - Basic Types
   - Interfaces
   - Classes
   - Functions

**Advanced TypeScript**
- Generics
- Type inference
- Union and Intersection types
- Utility types

**TypeScript with DOM**
- DOM manipulation with types
- Event handling
- Type declarations

### Week 6: Vite & Project Building

**Vite Fundamentals**
1. Read [Vite Documentation](https://vitejs.dev/guide/)
2. Learn about:
   - Project scaffolding
   - Hot Module Replacement
   - Build optimization
   - Environment variables

**BudgetY App Project**
Build [BudgetY App](https://hta218.github.io/budget-y/) with:
- Vite + TypeScript + TailwindCSS
- Features to implement:
  - Add/edit/delete transactions
  - Category management
  - Monthly budget tracking
  - Data visualization
  - Local storage persistence

### Week 5-6 Assignment

**Complete BudgetY App**
```bash
# Project structure
budget-y/
├── src/
│   ├── types/
│   ├── utils/
│   ├── components/
│   └── main.ts
├── index.html
├── package.json
├── tsconfig.json
├── tailwind.config.js
└── vite.config.ts
```

Requirements:
- Full TypeScript implementation
- No type errors
- Responsive design
- Deploy to production

---

## Week 7-8: Node.js & Backend Development

### Learning Objectives
- Understand Node.js and npm ecosystem
- Build REST APIs with Express
- Work with databases using Prisma ORM

### Week 7: Node.js & Express

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

### Week 8: Database & Prisma

**Prisma Setup**
1. Follow [Prisma Getting Started](https://www.prisma.io/docs/getting-started/setup-prisma/start-from-scratch/relational-databases-typescript-postgresql)
2. Learn:
   - Schema definition
   - Migrations
   - CRUD operations

**Build Blog API**
Create a REST API with:
- User registration/login
- CRUD operations for posts
- Comments system
- Categories and tags

### Week 7-8 Assignment

**Blog API Project**
Endpoints to implement:
```
POST   /api/auth/register
POST   /api/auth/login
GET    /api/posts
GET    /api/posts/:id
POST   /api/posts
PUT    /api/posts/:id
DELETE /api/posts/:id
POST   /api/posts/:id/comments
```

Database schema:
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

## Week 9-10: React Fundamentals

### Learning Objectives
- Master React component development
- Understand hooks and state management
- Build interactive user interfaces

### Week 9: React Basics

**React Fundamentals**
1. Read [React Documentation](https://react.dev/learn)
2. Complete official tutorial
3. Learn:
   - Components and Props
   - State and Lifecycle
   - Handling Events
   - Conditional Rendering

**React Hooks**
- useState and useEffect
- useContext and useReducer
- Custom hooks
- Rules of hooks

### Week 10: Building with React

**React with TypeScript**
- Type-safe components
- Props interfaces
- Event handling types
- Generic components

**Blog Frontend**
Build a React frontend for your Blog API:
- Post listing and detail views
- User authentication
- Create/edit posts
- Comment system
- Search and filtering

### Week 9-10 Assignment

**Complete Blog Platform**
- Connect React frontend to Express API
- Implement all CRUD operations
- Add loading states and error handling
- Style with TailwindCSS
- Deploy frontend and backend

---

## Week 11-12: Advanced Topics & Security

### Learning Objectives
- Implement data validation with Zod
- Add authentication and security
- Master React Router for navigation

### Week 11: Validation & Security

**Zod Schema Validation**
1. Read [Zod Documentation](https://zod.dev)
2. Add validation to Blog API:
   ```typescript
   import { z } from 'zod';
   
   const PostSchema = z.object({
     title: z.string().min(1).max(200),
     content: z.string().min(10),
     published: z.boolean().optional()
   });
   ```

**Authentication & Security**
- JWT implementation
- Password hashing with bcrypt
- Protected routes
- Rate limiting
- CORS configuration

### Week 12: React Router & AI

**React Router**
1. Complete [React Router Tutorial](https://reactrouter.com/en/main/start/tutorial)
2. Implement in Blog frontend:
   - Nested routes
   - Protected routes
   - URL parameters
   - Navigation guards

**AI Integration**
1. Complete [Anthropic Prompt Engineering Tutorial](https://github.com/anthropics/prompt-eng-interactive-tutorial)
2. Add AI features to blog:
   - Content suggestions
   - Auto-tagging
   - Comment moderation

### Week 11-12 Assignment

**Secure Blog Platform**
- Implement full authentication flow
- Add input validation everywhere
- Create admin dashboard
- Include AI-powered features
- Write security documentation

---

## Week 13-14: Shopify Development

### Learning Objectives
- Understand Shopify ecosystem
- Set up development store
- Build with Shopify Hydrogen

### Week 13: Shopify Basics

**Shopify Setup**
1. Create partner account
2. Set up development store
3. Explore admin interface
4. Understand Shopify concepts:
   - Products and collections
   - Orders and customers
   - Themes and apps

**Shopify APIs**
- REST Admin API
- GraphQL Admin API
- Storefront API
- Webhook handling

### Week 14: Hydrogen Development

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

### Week 13-14 Assignment

**Shopify Storefront**
- Create custom Hydrogen storefront
- Implement product catalog
- Add cart functionality
- Style with TailwindCSS
- Deploy to Oxygen

---

## Week 15-16: Weaverse Integration & Final Project

### Learning Objectives
- Integrate Weaverse SDK
- Build visual components
- Complete capstone project

### Week 15: Weaverse Development

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

### Week 16: Capstone Project

**Final Project Requirements:**
Build a complete e-commerce site with:
1. **Shopify Integration**
   - Product catalog
   - Shopping cart
   - Customer accounts

2. **Weaverse Features**
   - Visual page building
   - Custom components
   - Theme settings

3. **Technical Requirements**
   - TypeScript throughout
   - Responsive design
   - Performance optimized
   - SEO friendly

### Final Assessment

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

### Next Steps
- Continue building with Weaverse
- Contribute to open source
- Apply for full-time positions
- Keep learning and growing!

Welcome to the Weaverse developer community!