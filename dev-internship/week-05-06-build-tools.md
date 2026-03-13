# Week 5-6: Build Tools & Development Workflow

> [!IMPORTANT]
> **DO NOT** use AI tools to write code for you. You come here to **LEARN**, the goal of this program is to build
> your programming skills through **hands-on** practice. AI assistants can help explain
> concepts or debug issues, but writing the code yourself is **essential** for learning.

---

|                 |                                                                                                            |
| :-------------- | :--------------------------------------------------------------------------------------------------------- |
| Learning Topics | Package managers, Vite build system, Git workflows, Linting, Formatting, Environment configuration       |
| Objectives      | Master modern build tools, Learn collaborative Git workflows, Set up a professional dev environment, Build BudgetY app with TypeScript |

## Package Managers (Days 1-2)

1. Understand the role of package managers in modern JavaScript development
2. Learn [npm](https://docs.npmjs.com/about-npm) and [pnpm](https://pnpm.io/motivation):
   - Initializing projects (`npm init`, `pnpm init`)
   - Installing dependencies (`dependencies` vs `devDependencies`)
   - Understanding `package.json` and lock files
   - Running scripts (`npm run`, `pnpm run`)
   - Understanding semantic versioning (`^`, `~`, exact versions)
3. Learn about:
   - Global vs local packages
   - `npx` / `pnpm dlx` for running packages without installing
   - Monorepos and workspaces (overview)

## Vite (Days 3-5)

1. Read [Vite Documentation](https://vitejs.dev/guide/)
2. Learn about:
   - Why Vite? (ESM-based dev server vs traditional bundlers)
   - Project scaffolding (`npm create vite@latest`)
   - Development server & Hot Module Replacement (HMR)
   - Build optimization & production builds
   - Environment variables (`.env` files, `import.meta.env`)
   - Plugin ecosystem
   - Path aliases & project configuration (`vite.config.ts`)

## Code Quality Tools (Days 6-7)

### Linting & Formatting
1. Set up [Biome](https://biomejs.dev/) or [ESLint](https://eslint.org/) + [Prettier](https://prettier.io/)
2. Learn about:
   - Why linting and formatting matter
   - Configuring rules for your project
   - Auto-fix on save in your IDE
   - Running linters from the command line

### TypeScript Configuration
1. Understanding `tsconfig.json`:
   - `strict` mode and why it matters
   - `target` and `module` options
   - Path aliases with `baseUrl` and `paths`
2. Common TypeScript compiler options for frontend projects

## Git Workflows (Days 8-10)

> [!NOTE]
> If you're already comfortable with Git branching and pull requests, feel free to skip this section.

1. Read [Git Handbook](https://guides.github.com/introduction/git-handbook/)
2. Learn branching and merging:
   - Creating and switching branches (`git branch`, `git checkout`, `git switch`)
   - Merging branches and resolving conflicts
   - Rebasing vs merging (overview)
3. Learn collaborative workflows:
   - Forking and cloning repositories
   - Creating pull requests on GitHub
   - Code review process
   - Keeping your branch up to date (`git pull`, `git fetch`)
4. Practice:
   - Create a feature branch for your BudgetY app
   - Make changes, commit, and push to GitHub
   - Open a pull request and merge it
5. Learn useful Git commands:
   - `git stash` — temporarily save uncommitted changes
   - `git log --oneline` — view commit history
   - `git diff` — review changes before committing
   - `git reset` — undo commits (soft vs hard)

### Git Hooks (Optional)
- Pre-commit hooks with [Husky](https://typicode.github.io/husky/) + [lint-staged](https://github.com/lint-staged/lint-staged)
- Automating lint/format checks before commits

## Assignment

Build [BudgetY App](https://hta218.github.io/budget-y/) with:
- [ ] Set up project with Vite + TypeScript + TailwindCSS
- [ ] Configure linting and formatting
- [ ] Implement features:
  - Transaction CRUD operations
  - Category management
  - Budget tracking
- [ ] Deploy to production

---

[← Back to Overview](./README.md) | [Previous: Week 3-4](./week-03-04-dom-css-styling.md) | [Next: Week 7-8 →](./week-07-08-nodejs-backend.md)
