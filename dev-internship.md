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
  - [Week 1-2: JavaScript \& TypeScript](#week-1-2-javascript--typescript)
      - [Beginner JavaScript (Skip if already familiar)](#beginner-javascript-skip-if-already-familiar)
      - [Core JavaScript (Days 1-3)](#core-javascript-days-1-3)
      - [Functional Programming (Days 4-5)](#functional-programming-days-4-5)
      - [TypeScript Fundamentals (Days 6-10)](#typescript-fundamentals-days-6-10)
      - [Building Command-Line Applications (Days 11-12)](#building-command-line-applications-days-11-12)
      - [Assignment](#assignment)
  - [Week 3-4: DOM, CSS \& Modern Styling](#week-3-4-dom-css--modern-styling)
      - [DOM Fundamentals (Days 1-4)](#dom-fundamentals-days-1-4)
      - [Flexbox \& Grid](#flexbox--grid)
      - [TailwindCSS](#tailwindcss)
      - [Assignment](#assignment-1)
  - [Week 5-6: AI Integration \& Build Tools](#week-5-6-ai-integration--build-tools)
      - [AI Prompt Engineering (Days 1-3)](#ai-prompt-engineering-days-1-3)
      - [IDE AI Integration (Days 4-5)](#ide-ai-integration-days-4-5)
      - [Build Tools with Vite (Days 6-7)](#build-tools-with-vite-days-6-7)
      - [AI-Powered Development Practices](#ai-powered-development-practices)
      - [Assignment](#assignment-2)
  - [Week 7-8: Node.js \& Backend Development](#week-7-8-nodejs--backend-development)
      - [Node.js Fundamentals](#nodejs-fundamentals)
      - [Express.js](#expressjs)
      - [Database \& Prisma](#database--prisma)
      - [Assignment](#assignment-3)
      - [Testing Your API:](#testing-your-api)
      - [Required Endpoints:](#required-endpoints)
      - [Database Schema:](#database-schema)
  - [Week 9-10: React](#week-9-10-react)
      - [React Basics](#react-basics)
      - [Modern UI with ShadcnUI](#modern-ui-with-shadcnui)
      - [State Management with Preact Signals](#state-management-with-preact-signals)
      - [Assignment](#assignment-4)
  - [Week 11-12: Advanced Topics \& Security](#week-11-12-advanced-topics--security)
      - [Zod Schema Validation](#zod-schema-validation)
      - [React Router Advanced Patterns](#react-router-advanced-patterns)
      - [Assignment](#assignment-5)
  - [Week 13: Shopify Development](#week-13-shopify-development)
      - [Shopify Basics](#shopify-basics)
      - [Assignment 1: Shopify Store Setup](#assignment-1-shopify-store-setup)
      - [Shopify Hydrogen Development](#shopify-hydrogen-development)
      - [Hydrogen Setup](#hydrogen-setup)
      - [Assignment 2: Hydrogen Storefront Development](#assignment-2-hydrogen-storefront-development)
      - [Example GraphQL Queries for Practice:](#example-graphql-queries-for-practice)
  - [Week 14: Weaverse Integration](#week-14-weaverse-integration)
      - [Weaverse Setup](#weaverse-setup)
      - [Component Development](#component-development)
  - [Week 15-16: Final Project \& Internship Review](#week-15-16-final-project--internship-review)
      - [Presentation \& Review](#presentation--review)
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
- [FreeCodeCamp English for Developers](https://www.freecodecamp.org/learn/b1-english-for-developers/) (B1 level, skip if already fluent)
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

|                 |                                                                                                             |
| :-------------- | :---------------------------------------------------------------------------------------------------------- |
| Learning Topics | Core JavaScript, ES6+ features, Functional programming, TypeScript fundamentals, Type-safe development      |
| Objectives      | Complete 30 JS exercises, Master TypeScript basics, Build a type-safe CLI task manager with full TypeScript |

#### Beginner JavaScript (Skip if already familiar)
1. Complete [JavaScript Beginner Tutorial](https://www.w3schools.com/js/default.asp)

#### Core JavaScript (Days 1-3)
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

#### Functional Programming (Days 4-5)
1. Start [LearnRx Interactive Tutorial](https://reactivex.io/learnrx/)
2. Complete exercises 1-20 (Arrays and Functions)
3. Focus on:
   - Array methods (map, filter, reduce)
   - Function composition
   - Immutability concepts
   - Promises and Async/Await

#### TypeScript Fundamentals (Days 6-10)
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

#### Building Command-Line Applications (Days 11-12)

**Prerequisites - Understanding the Terminal:**

Before diving into CLI development, it's essential to understand what a terminal is and how to use it effectively:

1. **What is a Terminal?**
   - A terminal (also called command line or shell) is a text-based interface to interact with your computer
   - It allows you to run commands, navigate files, and execute programs without a graphical interface
   - Essential for developers as many tools and scripts are designed for terminal use

2. **Basic Terminal Commands to Practice:**
   
   **For macOS/Linux (bash/zsh):**
   ```bash
   # Navigation
   pwd          # Print working directory (where you are)
   ls           # List files in current directory
   ls -la       # List all files with details
   cd folder    # Change directory to 'folder'
   cd ..        # Go up one directory
   cd ~         # Go to home directory
   
   # File Operations
   mkdir mydir  # Create a new directory
   touch file.txt   # Create an empty file
   cp file1 file2   # Copy file1 to file2
   mv file1 file2   # Move/rename file1 to file2
   rm file.txt      # Remove a file (use carefully!)
   cat file.txt     # Display file contents
   
   # Useful Commands
   clear        # Clear the terminal screen
   history      # Show command history
   echo "text"  # Print text to terminal
   which node   # Find where a program is installed
   ```
   
   **For Windows (Command Prompt/PowerShell):**
   ```powershell
   # Navigation
   pwd          # Print working directory (PowerShell) or use 'cd' (CMD)
   dir          # List files in current directory (or 'ls' in PowerShell)
   cd folder    # Change directory to 'folder'
   cd ..        # Go up one directory
   cd %USERPROFILE%  # Go to home directory (CMD) or cd ~ (PowerShell)
   
   # File Operations
   mkdir mydir  # Create a new directory
   type nul > file.txt   # Create empty file (CMD) or New-Item file.txt (PowerShell)
   copy file1 file2      # Copy file1 to file2
   move file1 file2      # Move/rename file1 to file2
   del file.txt          # Remove a file (use carefully!)
   type file.txt         # Display file contents (or 'cat' in PowerShell)
   
   # Useful Commands
   cls          # Clear the terminal screen
   doskey /h    # Show command history (CMD) or history (PowerShell)
   echo "text"  # Print text to terminal
   where node   # Find where a program is installed
   ```

3. **Practice Exercise:**
   - Open your terminal
   - Navigate to your home directory
   - Create a new directory called "cli-practice"
   - Create a file called "hello.txt" with some content
   - List the contents of the directory
   - Remove the file and directory

**Terminal Setup:**

Now let's set up a modern, developer-friendly terminal environment:

**Note for Windows Users:** While the instructions below focus on Zsh and Oh My Zsh (primarily for macOS/Linux), Windows users should:
- Install [WSL2 (Windows Subsystem for Linux)](https://learn.microsoft.com/en-us/windows/wsl/install) to run Linux commands natively
- After installing WSL2, you can follow the Zsh instructions below within your Linux environment
- Alternatively, use [Git Bash](https://git-scm.com/downloads) which provides Unix-like commands on Windows

1. **What is Zsh?**
   - Zsh (Z shell) is an extended version of the Bash shell with many improvements
   - More powerful auto-completion, better scripting capabilities, and enhanced customization
   - Default shell on macOS since Catalina, available on all platforms
   - Why prefer Zsh over Bash:
     - Smart tab completion (case-insensitive, partial matching)
     - Powerful globbing and pattern matching
     - Better command history search
     - Extensive theming and plugin ecosystem

2. **Install Zsh** (if not already installed):
   ```bash
   # Check if Zsh is installed
   zsh --version
   
   # Install on macOS (usually pre-installed)
   brew install zsh
   
   # Install on Ubuntu/Debian
   sudo apt update && sudo apt install zsh
   
   # Set Zsh as default shell
   chsh -s $(which zsh)
   ```
3. **What is Oh My Zsh?**
   - Oh My Zsh is a framework for managing Zsh configuration
   - Provides themes, plugins, and an auto-update tool
   - Makes Zsh easier to customize and extend
   - **The key difference**: Zsh is the shell itself, Oh My Zsh is a configuration framework that runs on top of Zsh

4. **Install Oh My Zsh**:
   ```bash
   # Install via curl
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   
   # Or via wget
   sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   ```
5. **Essential Oh My Zsh Plugins**:
   ```bash
   # Install zsh-autosuggestions for intelligent command completion
   git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
   
   # Install zsh-syntax-highlighting for command highlighting
   git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
   ```

6. **Configure Oh My Zsh**:
   Edit your `~/.zshrc` file:
   ```bash
   # Open the configuration file
   nano ~/.zshrc
   
   # Find the plugins line and update it to:
   plugins=(git zsh-autosuggestions zsh-syntax-highlighting node npm)
   
   # Optional: Change theme (default is robbyrussell)
   ZSH_THEME="agnoster"  # Or try "powerlevel10k/powerlevel10k"
   
   # Save and reload configuration
   source ~/.zshrc
   ```

7. **Verify Your Setup**:
   ```bash
   # Check shell
   echo $SHELL  # Should show /bin/zsh or similar
   
   # Test auto-suggestions (type a command you used before)
   # Test syntax highlighting (commands should be colored)
   # Test git plugin (type 'git' and press TAB)
   ```

**CLI Development Setup:**

1. Try Nodejs built-in prompt:
  ```js
  import readline from 'node:readline';

  const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout,
  });

  rl.question(`What's your name? `, name => {
    console.log(`Hi ${name}!`);
    rl.close();
  });
  ```

2. Install Commander.js for CLI development:
   ```bash
   npm install commander
   npm install --save-dev @types/node
   ```

3. Learn CLI basics:
   ```typescript
   // Basic CLI structure with Commander.js
   import { Command } from 'commander';
   
   const program = new Command();
   
   program
     .name('task-manager')
     .description('CLI task management application')
     .version('1.0.0');
   
   program
     .command('add <title>')
     .description('Add a new task')
     .option('-p, --priority <priority>', 'Set priority (low|medium|high)', 'medium')
     .action((title, options) => {
       console.log(`Adding task: ${title} with priority: ${options.priority}`);
     });
   
   program.parse(process.argv);
   ```

4. Essential CLI concepts:
   - Parsing command-line arguments
   - Creating interactive prompts with inquirer
   - Handling file system operations with fs/promises
   - Formatting console output with chalk
   - Creating help documentation
   - Error handling and user feedback

5. File persistence pattern:
   ```typescript
   import { promises as fs } from 'fs';
   import path from 'path';
   
   const DATA_FILE = path.join(process.cwd(), 'tasks.json');
   
   async function loadTasks(): Promise<Task[]> {
     try {
       const data = await fs.readFile(DATA_FILE, 'utf-8');
       return JSON.parse(data);
     } catch (error) {
       return []; // Return empty array if file doesn't exist
     }
   }
   
   async function saveTasks(tasks: Task[]): Promise<void> {
     await fs.writeFile(DATA_FILE, JSON.stringify(tasks, null, 2));
   }
   ```

#### Assignment

Build a Type-Safe Task Manager CLI in TypeScript:
- [ ] Set up TypeScript project with proper tsconfig.json
- [ ] Define interfaces for Task
- [ ] Create type-safe command-line interface using Commander.js
- [ ] Implement CRUD operations with full type safety:
  - Add tasks with validation
  - Remove tasks by ID
  - Update task status and priority
  - List and filter tasks
  - Save tasks to JSON file

---

## Week 3-4: DOM, CSS & Modern Styling

|                 |                                                                                                                        |
| :-------------- | :--------------------------------------------------------------------------------------------------------------------- |
| Learning Topics | DOM fundamentals, DOM manipulation, Event handling, Flexbox, CSS Grid, Responsive design, TailwindCSS                  |
| Objectives      | Master DOM manipulation, Complete CSS games, Build interactive FreshCart clone with TailwindCSS and vanilla JavaScript |

#### DOM Fundamentals (Days 1-4)

1. **Understanding the DOM**
   - Read [MDN: Introduction to the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
   - What is the DOM and how browsers create it
   - DOM tree structure: nodes, elements, and text
   - The document object and window object

2. **DOM Selection Methods**
   ```javascript
   // Element selection methods
   document.getElementById('myId')
   document.getElementsByClassName('myClass')
   document.getElementsByTagName('div')
   document.querySelector('.myClass')  // Returns first match
   document.querySelectorAll('.myClass')  // Returns all matches
   
   // Traversing the DOM
   element.parentElement
   element.children
   element.firstElementChild
   element.lastElementChild
   element.nextElementSibling
   element.previousElementSibling
   ```

3. **DOM Manipulation**
   ```javascript
   // Creating elements
   const newDiv = document.createElement('div')
   newDiv.textContent = 'Hello World'
   newDiv.className = 'my-class'
   newDiv.id = 'my-id'
   
   // Adding/removing elements
   parent.appendChild(newDiv)
   parent.insertBefore(newDiv, referenceNode)
   parent.removeChild(childNode)
   element.remove()  // Modern approach
   
   // Modifying attributes
   element.setAttribute('data-id', '123')
   element.getAttribute('data-id')
   element.removeAttribute('data-id')
   
   // Modifying styles
   element.style.color = 'red'
   element.style.backgroundColor = 'blue'
   element.classList.add('active')
   element.classList.remove('active')
   element.classList.toggle('active')
   element.classList.contains('active')
   ```

4. **Event Handling**
   ```javascript
   // Adding event listeners
   button.addEventListener('click', function(event) {
     console.log('Button clicked!')
   })
   
   // Common events
   // Mouse: click, dblclick, mouseenter, mouseleave, mousemove
   // Keyboard: keydown, keyup, keypress
   // Form: submit, change, input, focus, blur
   // Window: load, resize, scroll
   
   // Event object
   element.addEventListener('click', function(event) {
     event.preventDefault()  // Prevent default behavior
     event.stopPropagation()  // Stop event bubbling
     console.log(event.target)  // Element that triggered the event
     console.log(event.currentTarget)  // Element with the listener
   })
   
   // Event delegation
   document.getElementById('parent').addEventListener('click', function(event) {
     if (event.target.matches('.child-button')) {
       console.log('Child button clicked!')
     }
   })
   ```

#### Flexbox & Grid
1. Complete all levels at [Flexbox Froggy](https://flexboxfroggy.com/)
2. Complete all levels at [Grid Garden](https://codepip.com/games/grid-garden/)

#### TailwindCSS

1. Read [TailwindCSS Documentation](https://tailwindcss.com/docs)
2. Set up TailwindCSS in a project
3. Learn utility classes:
   - Layout & Spacing
   - Colors & Typography
   - Flexbox & Grid utilities

#### Assignment

**Part 1: DOM Manipulation Exercises (Days 5-7)**

Build these interactive components using vanilla JavaScript (no CSS needed):

1. **Interactive Todo List**
   - [ ] Add new todos with input field and button
   - [ ] Mark todos as complete (strike-through styling)
   - [ ] Delete todos with confirmation
   - [ ] Filter todos (all, active, completed)
   - [ ] Save todos to localStorage
   - [ ] Count of remaining todos
   - [ ] Deploy to GitHub Pages

**Part 2: FreshCart Site Clone (Days 8-14)**

Build [FreshCart Site](https://freshcart-template.codescandy.com/) with interactivity:
- [ ] Build fully responsive design with TailwindCSS
- [ ] Deploy to GitHub Pages

---

## Week 5-6: AI Integration & Build Tools

|                 |                                                                                                            |
| :-------------- | :--------------------------------------------------------------------------------------------------------- |
| Learning Topics | AI prompt engineering, IDE AI integration, Vite build system, Modern development workflow with AI          |
| Objectives      | Master AI-assisted development, Set up Google Gemini in IDE, Build AI-enhanced BudgetY app with TypeScript |

#### AI Prompt Engineering (Days 1-3)

1. Complete [Anthropic Prompt Engineering Tutorial](https://github.com/anthropics/prompt-eng-interactive-tutorial)
2. Learn key concepts:
   - Clear instruction formulation
   - Context provision strategies
   - Few-shot prompting
   - Chain-of-thought reasoning
   - Common pitfalls and best practices

#### IDE AI Integration (Days 4-5)

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

#### Build Tools with Vite (Days 6-7)
1. Read [Vite Documentation](https://vitejs.dev/guide/)
2. Learn about:
   - Project scaffolding
   - Hot Module Replacement
   - Build optimization
   - Environment variables
   - Plugin ecosystem

#### AI-Powered Development Practices
```áh
// Example: Using AI to generate TypeScript interfaces
// Prompt: "Generate TypeScript interfaces for a budget tracking app with transactions, categories, and monthly summaries"
```

#### Assignment

Build AI-Enhanced [BudgetY App](https://hta218.github.io/budget-y/) with:
- [ ] Set up project with Vite + TypeScript + TailwindCSS
- [ ] Configure AI assistant in your IDE
- [ ] Use AI to generate initial TypeScript interfaces and types
- [ ] Implement features:
  - Transaction CRUD operations
  - Category management
  - Budget tracking
- [ ] Deploy to production

---

## Week 7-8: Node.js & Backend Development

|                 |                                                                                                       |
| :-------------- | :---------------------------------------------------------------------------------------------------- |
| Learning Topics | Node.js ecosystem, Express.js, REST APIs, Database design, Prisma ORM                                 |
| Objectives      | Build complete Blog API with authentication, Implement CRUD operations, Create database relationships |

#### Node.js Fundamentals
- Node.js basics and modules
- NPM package management
- File system operations
- Environment variables

#### Express.js
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

#### Database & Prisma

1. Register a free Database hosting service (Supabase, Railway, etc.)
1. Follow [Prisma Getting Started](https://www.prisma.io/docs/getting-started/setup-prisma/start-from-scratch/relational-databases-typescript-postgresql)
2. Learn:
   - Schema definition
   - Migrations
   - CRUD operations

#### Assignment

Complete Blog API Project:
- [ ] Set up Node.js project with Express and TypeScript
- [ ] Configure Prisma with PostgreSQL database
- [ ] Implement JWT-based authentication (register/login)
- [ ] Create CRUD operations for posts
- [ ] Build comments system
- [ ] Add categories and tags functionality
- [ ] Deploy to production

#### Testing Your API:

Since this is an API-only project, you'll need a REST API client to test your endpoints. Install one of these tools:

1. **Postman** (Recommended for beginners)
   - Download from [postman.com](https://www.postman.com/downloads/)
   - Create collections for your API endpoints
   - Save example requests for documentation

#### Required Endpoints:
```
POST   /api/auth/register
POST   /api/auth/login
GET    /api/posts
GET    /api/posts/:id
POST   /api/posts
PUT    /api/posts/:id
DELETE /api/posts/:id
```

#### Database Schema:
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

|                 |                                                                                                                        |
| :-------------- | :--------------------------------------------------------------------------------------------------------------------- |
| Learning Topics | React components, Hooks, State management with Preact Signals, ShadcnUI components, TypeScript integration, Deployment |
| Objectives      | Master React fundamentals, Build complete Blog frontend with modern UI components, Deploy to production                |

#### React Basics

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

#### Modern UI with ShadcnUI

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

#### State Management with Preact Signals

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

#### Assignment

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

## Week 11-12: Advanced Topics & Security

|                 |                                                                                                          |
| :-------------- | :------------------------------------------------------------------------------------------------------- |
| Learning Topics | Schema validation with Zod, Authentication & Authorization, Security best practices, React Router        |
| Objectives      | Implement secure authentication system, Add comprehensive validation, Build advanced e-commerce features |

#### Zod Schema Validation
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

#### React Router Advanced Patterns
1. Get to know React Router:
   - What it is and why it's used
   - Basic routing concepts
   - Dynamic routing with parameters
   - Nested routes and layouts
2. Read [React Router Documentation](https://reactrouter.com/en/main/start/overview)
3. Complete [React Router Tutorial](https://reactrouter.com/en/main/start/tutorial)

#### Assignment

Build a Full-Featured Online Store with React Router:
- [ ] Set up project with React, TypeScript, React Router, and TailwindCSS
- [ ] Implement complete page structure with proper routing:
  - **Home page** (`/`) - Hero banner, featured products, categories
  - **Product listing** (`/products`) - Grid layout with filters
  - **Category pages** (`/collections/:category`) - Dynamic category routing
  - **Product detail** (`/products/:id`) - Gallery, variants, reviews
  - **Shopping cart** (`/cart`) - Cart items, quantity updates, totals
  - **Checkout** (`/checkout`) - Multi-step form with validation
  - **Order confirmation** (`/order/:id`) - Order summary and status
  - **Blog** (`/blog` and `/blog/:slug`) - Blog listing and articles
  - **About & Contact** pages - Company info and contact form
- [ ] Implement advanced routing features:
  - Nested routes for product categories
  - Breadcrumb navigation based on routes
  - 404 page for unknown routes
- [ ] Build reusable components:
  - Product card with hover effects
  - Cart drawer/modal
  - Search with autocomplete
  - Newsletter signup
- [ ] Add e-commerce functionality:
  - Add to cart
  - Product search and filtering
  - Recently viewed products
- [ ] Style with TailwindCSS and ShadcnUI:
  - Responsive design for all pages
  - Loading skeletons
- [ ] Add Zod validation for:
  - Checkout form fields
  - Contact form
  - Newsletter signup
- [ ] Deploy to production

*Use the AI assistant you set up in Week 5-6 to help with complex implementations.*

---

## Week 13: Shopify Development

|                 |                                                                                                        |
| :-------------- | :----------------------------------------------------------------------------------------------------- |
| Learning Topics | Shopify ecosystem, Partner account, Admin APIs, Hydrogen framework, Headless commerce                  |
| Objectives      | Set up Shopify development environment, Build custom Hydrogen storefront, Implement cart functionality |

#### Shopify Basics
1. Create a partner account
2. Set up development store
3. Explore admin interface
4. Understand Shopify concepts:
   - Products and collections
   - Orders and customers
   - Themes and apps

#### Assignment 1: Shopify Store Setup

Build a complete Shopify store using the admin interface:
- [ ] Create a Shopify Partner account at [partners.shopify.com](https://partners.shopify.com)
- [ ] Set up a development store with your company name
- [ ] Add content to your store:
  - Create at least 10 products across 3 collections
  - Add product descriptions, multiple images, and variants (size/color)
  - Create 3 blog posts in a "News" blog
  - Add essential pages: About Us, Contact, Shipping Policy, Privacy Policy
- [ ] Configure store appearance:
  - Install and customize a free theme (Dawn recommended)
  - Upload logo and favicon
  - Customize theme colors and typography
- [ ] Set up navigation:
  - Create main menu with Collections, About, Blog, Contact
  - Add footer menu with policies and social links
  - Configure search functionality
- [ ] Build full pages using theme customizer:
  - Homepage with hero banner, featured products, testimonials
  - Collection pages with filters
  - Product pages with related products
  - Blog page with categories
- [ ] Configure internationalization:
  - Set up at least 2 currencies (USD and your local currency)
  - Configure 2 markets (domestic and international)
  - Add language selector if applicable
- [ ] Test the complete customer journey from browsing to checkout

#### Shopify Hydrogen Development

#### Hydrogen Setup
1. Read [Hydrogen Documentation](https://shopify.dev/docs/custom-storefronts/hydrogen)
2. Create Hydrogen project:
   ```bash
   npm create @shopify/hydrogen@latest
   ```

#### Assignment 2: Hydrogen Storefront Development

Build a custom Hydrogen storefront connected to your Shopify store:
- [ ] Set up Hydrogen project:
  - Initialize new Hydrogen app
  - Connect to your development store using Storefront API
  - Configure environment variables
- [ ] Learn [GraphQL Storefront API](https://shopify.dev/docs/api/storefront):
  - Install [Shopify GraphiQL App](https://shopify-graphiql-app.shopifycloud.com/login)
  - Complete these query exercises:
    1. Query shop information (name, description, payment settings)
    2. Fetch first 10 products with title, price, and images
    3. Get a specific collection by handle with its products
    4. Query product variants and inventory levels
    5. Fetch blog articles with author and publish date
    6. Create a complex query combining products, collections, and metafields
    7. Practice pagination with products using cursor-based pagination
- [ ] Build homepage sections using Storefront API:
  - **Featured Products Section**:
    - Query products from a specific collection (e.g., "Featured" or "Best Sellers")
    - Display product grid with image, title, price
    - Implement hover effects and quick view
    - Add "Add to Cart" functionality
  - **Blog Articles Section**:
    - Query latest 3 articles from a specific blog
    - Display article cards with featured image, title, excerpt
    - Format publish dates properly
    - Add "Read More" links to full articles

#### Example GraphQL Queries for Practice:
```graphql
# Query 1: Shop Information
{
  shop {
    name
    description
    primaryDomain {
      url
    }
    paymentSettings {
      currencyCode
      supportedDigitalWallets
    }
  }
}

# Query 2: Products with Variants
{
  products(first: 10) {
    edges {
      node {
        id
        title
        handle
        priceRange {
          minVariantPrice {
            amount
            currencyCode
          }
        }
        images(first: 1) {
          edges {
            node {
              url
              altText
            }
          }
        }
        variants(first: 5) {
          edges {
            node {
              id
              title
              price {
                amount
              }
              availableForSale
            }
          }
        }
      }
    }
  }
}
```

---

## Week 14: Weaverse Integration

|                 |                                                                                                       |
| :-------------- | :---------------------------------------------------------------------------------------------------- |
| Learning Topics | Weaverse SDK, Visual components, Component schemas, Final project integration                         |
| Objectives      | Master Weaverse platform, Create custom visual components, Build complete e-commerce capstone project |

#### Weaverse Setup
1. Read [Weaverse Documentation](https://weaverse.io/docs)
2. Set up Weaverse project:
   ```bash
   npm create @weaverse/hydrogen@latest
   ```

#### Component Development
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

#### Presentation & Review
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