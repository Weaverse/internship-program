# Week 7-8: Node.js & Backend Development

> [!IMPORTANT]
> **DO NOT** use AI tools to write code for you. You come here to **LEARN**, the goal of this program is to build
> your programming skills through **hands-on** practice. AI assistants can help explain
> concepts or debug issues, but writing the code yourself is **essential** for learning.

---

|                 |                                                                                                   |
| :-------------- | :------------------------------------------------------------------------------------------------ |
| Learning Topics | Node.js ecosystem, Express.js, REST APIs, MySQL Database, Prisma ORM                              |
| Objectives      | Build complete Blog API with authentication, Master database operations, Create RESTful endpoints |

## Part 1: Node.js & Express Fundamentals

### Node.js Fundamentals
- Node.js basics and modules
- NPM package management
- File system operations
- Environment variables

### Project Setup

1. **Initialize the project**
   ```bash
   mkdir blog-api
   cd blog-api
   npm init -y
   ```

2. **Install dependencies**
   ```bash
   npm install express
   npm install -D typescript tsx @types/node @types/express
   ```

3. **Configure `package.json`**

   Add `"type": "module"` and dev scripts:
   ```json
   {
     "name": "blog-api",
     "type": "module",
     "scripts": {
       "dev": "tsx watch src/index.ts",
       "start": "tsx src/index.ts"
     }
   }
   ```

   - `"type": "module"` enables ES modules (`import`/`export` syntax) instead of CommonJS (`require`)
   - [`tsx`](https://tsx.is/) runs TypeScript directly without a separate compile step
   - `tsx watch` automatically restarts the server when you save file changes

4. **Configure TypeScript**

   Create `tsconfig.json`:
   ```json
   {
     "compilerOptions": {
       "target": "ESNext",
       "module": "NodeNext",
       "moduleResolution": "NodeNext",
       "strict": true,
       "esModuleInterop": true,
       "outDir": "dist"
     },
     "include": ["src"]
   }
   ```

5. **Create entry file**

   Create `src/index.ts` and start your server:
   ```typescript
   import express from 'express'

   const app = express()
   const PORT = 3000

   app.use(express.json())

   app.get('/api/health', (req, res) => {
     res.json({ status: 'OK' })
   })

   app.listen(PORT, () => {
     console.log(`Server running on http://localhost:${PORT}`)
   })
   ```

6. **Run the dev server**
   ```bash
   npm run dev
   ```
   Now any changes you save in `src/` will automatically restart the server.

### Express.js
1. Read [Express Getting Started](https://expressjs.com/en/starter/installing.html)
2. Learn Express core concepts:
   - Routing (`app.get`, `app.post`, `app.put`, `app.delete`)
   - Middleware (`app.use`)
   - Request object (`req.body`, `req.params`, `req.query`)
   - Response object (`res.json`, `res.status`)

### Test Your APIs

1. **Test in the browser**
   - Open `http://localhost:3000/api/health` in your browser
   - The browser can only test `GET` requests — for `POST`, `PUT`, `DELETE` you need an API client

2. **Install [Bruno](https://www.usebruno.com/)**
   - Bruno is a fast, open-source API client (alternative to Postman)
   - Download and install from [usebruno.com](https://www.usebruno.com/downloads)

3. **Test APIs in Bruno**
   - Create a new collection for your project
   - Add requests for each endpoint (GET, POST, PUT, DELETE)
   - Test the health endpoint and verify the response
   - Save your collection so you can reuse it as you build more endpoints

## Part 2: Database with MySQL

### MySQL Setup and Installation

1. **Introduction to MySQL**
   - MySQL is one of the most popular relational database management systems
   - We'll learn SQL fundamentals and how to integrate databases with Node.js applications
   - Understanding of tables, relationships, and SQL queries

2. **Install MySQL**
   ```bash
   # Check if MySQL is already installed
   mysql --version

   # If not installed, follow the installation guide:
   ```
   - macOS: [MySQL Installation Guide for macOS](https://dev.mysql.com/doc/refman/8.4/en/macos-installation.html)
   - Windows: Use MySQL Installer from the official website
   - Linux: Use package manager (apt, yum, etc.)

3. **Install SQL Client**
   Choose one of these SQL clients for visual database management:
   - [MySQL Workbench](https://dev.mysql.com/doc/workbench/en/) - Official MySQL GUI
   - [Beekeeper Studio](https://www.beekeeperstudio.io/) - Modern, lightweight SQL client
   - TablePlus, DBeaver, or any preferred SQL client

4. **Start Local MySQL Server**
   ```bash
   # Start MySQL service (macOS)
   brew services start mysql

   # Or using mysql.server
   mysql.server start

   # Connect to MySQL
   mysql -u root -p
   ```

5. **Connect MySQL with Node.js Express**
   ```typescript
   // Install mysql2 package
   // npm install mysql2

   import mysql from 'mysql2'

   // Create connection
   const connection = mysql.createConnection({
     host: 'localhost',
     user: 'root',
     password: 'your_password',
     database: 'blog_db'
   })

   // Connect to database
   connection.connect((err) => {
     if (err) {
       console.error('Error connecting to MySQL:', err)
       return
     }
     console.log('Connected to MySQL database')
   })
   ```

6. **Learn Basic CRUD Operations**
   ```typescript
   // CREATE - Insert data
   app.post('/api/users', (req, res) => {
    const { name, email } = req.body;
    const query = 'INSERT INTO users (name, email) VALUES (?, ?)';

     connection.execute(query, [name, email], (err, results) => {
       if (err) return res.status(500).json({ error: err.message });
       res.json({ id: results.insertId, name, email });
     });
   });

   // READ - Get data using query params
   app.get('/api/users', (req, res) => {
     // ...
   });

   // READ - Get single user by ID (using params)
   app.get('/api/users/:id', (req, res) => {
     // ...
   });

   // UPDATE
   app.put('/api/users/:id', (req, res) => {
     // ...
   });

   // DELETE
   app.delete('/api/users/:id', (req, res) => {
     // ...
   });
   ```

### Assignment: Database Integration

1. **Test All APIs**
   - Test all CRUD operations using Bruno
   - Save example requests for each endpoint
   - Test edge cases and error handling

2. **Update to [RESTful Standards](https://restfulapi.net/)**
   - [ ] Follow RESTful naming conventions:
     - GET /api/users (list all users)
     - GET /api/users/:id (get single user)
     - POST /api/users (create user)
     - PUT /api/users/:id (update entire user)
     - PATCH /api/users/:id (partial update)
     - DELETE /api/users/:id (delete user)
   - [ ] Implement proper HTTP status codes:
     - 200 OK for successful GET/PUT
     - 201 Created for successful POST
     - 204 No Content for successful DELETE
     - 400 Bad Request for validation errors
     - 404 Not Found for missing resources
     - 500 Internal Server Error for server issues

## Part 3: ORM with Prisma

### Introduction to ORMs

1. **What is an ORM?**
   - ORM (Object-Relational Mapping) is a technique that lets you query and manipulate data using an object-oriented paradigm
   - Benefits: Type safety, auto-completion, migrations, database agnostic code
   - Prisma is a modern ORM that provides excellent TypeScript support

### Add Prisma to Your Project

Follow the official guide: [Add Prisma to an existing project (MySQL)](https://www.prisma.io/docs/prisma-orm/add-to-existing-project/mysql)

1. **Install Prisma CLI**
   ```bash
   npm install prisma -D
   ```

2. **Initialize Prisma with MySQL**
   ```bash
   npx prisma init --datasource-provider mysql
   ```
   This creates:
   - `prisma/schema.prisma` — your database schema file
   - `.env` — with a `DATABASE_URL` placeholder

3. **Configure the database connection**

   Update the `DATABASE_URL` in your `.env` file to point to your local MySQL database:
   ```env
   DATABASE_URL="mysql://root:password@localhost:3306/blog_db"
   ```

4. **Introspect your existing database**

   Since you already have tables from Part 2, pull the existing schema into Prisma:
   ```bash
   npx prisma db pull
   ```
   This reads your database and generates the corresponding models in `prisma/schema.prisma`.

   Open `prisma/schema.prisma` and review the generated models — they should match your existing tables.

5. **Install and generate Prisma Client**
   ```bash
   npm install @prisma/client
   npx prisma generate
   ```
   - `@prisma/client` is the library you use in your code
   - `prisma generate` creates a type-safe client based on your schema

6. **Update your Express routes to use Prisma**
   ```typescript
   import { PrismaClient } from '@prisma/client'

   const prisma = new PrismaClient()

   // CREATE
   app.post('/api/users', async (req, res) => {
     const user = await prisma.user.create({
       data: req.body
     })
     res.status(201).json(user)
   })

   // READ with pagination
   app.get('/api/users', async (req, res) => {
     // ...
   })

   // UPDATE
   app.put('/api/users/:id', async (req, res) => {
     // ...
   })

   // DELETE
   app.delete('/api/users/:id', async (req, res) => {
     // ...
   })
   ```

   Compare this with the raw MySQL version from Part 2 — notice how much cleaner and type-safe Prisma queries are.

7. **Deploy to Cloud Database**
   - Register for a free database hosting service:
     - [Supabase](https://supabase.com/) - Generous free tier with PostgreSQL
     - [PlanetScale](https://planetscale.com/) - MySQL-compatible serverless database
     - [Railway](https://railway.app/) - Simple deployment with MySQL/PostgreSQL
     - [Aiven](https://aiven.io/) - Managed cloud databases
   - Update your `DATABASE_URL` to use the cloud database instead of local

## Part 4: Authentication with JWT

### Understanding JWT Authentication
1. What is JWT (JSON Web Token) and how it works
2. Authentication flow: Register → Login → Access protected routes
3. Read [JWT Introduction](https://jwt.io/introduction)

### Implementation
```typescript
import bcrypt from 'bcrypt'
import jwt from 'jsonwebtoken'

const JWT_SECRET = process.env.JWT_SECRET || 'your-secret-key'

// Register - hash password before storing
app.post('/api/auth/register', async (req, res) => {
  const { email, password, name } = req.body
  const hashedPassword = await bcrypt.hash(password, 10)

  const user = await prisma.user.create({
    data: { email, password: hashedPassword, name }
  })

  res.status(201).json({ message: 'User registered successfully' })
})

// Login - verify password and issue token
app.post('/api/auth/login', async (req, res) => {
  const { email, password } = req.body
  const user = await prisma.user.findUnique({ where: { email } })

  if (!user || !(await bcrypt.compare(password, user.password))) {
    return res.status(401).json({ error: 'Invalid credentials' })
  }

  const token = jwt.sign({ userId: user.id }, JWT_SECRET, { expiresIn: '7d' })
  res.json({ token })
})

// Auth middleware - protect routes
function authenticate(req, res, next) {
  const token = req.headers.authorization?.split(' ')[1]
  if (!token) return res.status(401).json({ error: 'Token required' })

  try {
    const decoded = jwt.verify(token, JWT_SECRET)
    req.userId = decoded.userId
    next()
  } catch {
    res.status(401).json({ error: 'Invalid token' })
  }
}

// Protected route example
app.post('/api/posts', authenticate, async (req, res) => {
  const post = await prisma.post.create({
    data: { ...req.body, authorId: req.userId }
  })
  res.status(201).json(post)
})
```

### Key Concepts
- Password hashing with bcrypt (never store plain passwords)
- JWT signing and verification
- Auth middleware pattern for protecting routes
- Storing tokens on the client side (Authorization header)

## Final Assignment: Complete Blog API

Build a complete Blog API with all the concepts learned:

- [ ] Set up Node.js project with Express and TypeScript
- [ ] Start with raw MySQL queries to understand SQL fundamentals
- [ ] Migrate to Prisma ORM for better developer experience
- [ ] Configure Prisma with cloud database (MySQL or PostgreSQL)
- [ ] Implement JWT-based authentication (register/login)
- [ ] Create RESTful CRUD operations for:
  - Posts (with pagination, search, filtering by category)
  - Comments (nested under posts)
  - Categories and Tags (many-to-many relationships)
  - User profiles
- [ ] Add proper validation using middleware
- [ ] Implement error handling and logging
- [ ] Create API documentation using Postman or Swagger
- [ ] Deploy to production (Vercel, Railway, or Render)

### Required Endpoints
```
Auth:
POST   /api/auth/register
POST   /api/auth/login
POST   /api/auth/refresh
POST   /api/auth/logout

Users:
GET    /api/users/:id
PUT    /api/users/:id
DELETE /api/users/:id

Posts:
GET    /api/posts          (with pagination, search, filter)
GET    /api/posts/:id
POST   /api/posts
PUT    /api/posts/:id
DELETE /api/posts/:id

Comments:
GET    /api/posts/:postId/comments
POST   /api/posts/:postId/comments
PUT    /api/comments/:id
DELETE /api/comments/:id

Categories & Tags:
GET    /api/categories
POST   /api/categories
GET    /api/tags
POST   /api/tags
```

### Database Schema
```prisma
model User {
  id        String   @id @default(cuid())
  email     String   @unique
  name      String
  password  String
  posts     Post[]
  comments  Comment[]
  createdAt DateTime @default(now())
  updatedAt DateTime @updatedAt
}

model Post {
  id         String     @id @default(cuid())
  title      String
  slug       String     @unique
  content    String     @db.Text
  published  Boolean    @default(false)
  author     User       @relation(fields: [authorId], references: [id])
  authorId   String
  category   Category?  @relation(fields: [categoryId], references: [id])
  categoryId String?
  tags       Tag[]
  comments   Comment[]
  createdAt  DateTime   @default(now())
  updatedAt  DateTime   @updatedAt
}

model Comment {
  id        String   @id @default(cuid())
  content   String   @db.Text
  post      Post     @relation(fields: [postId], references: [id], onDelete: Cascade)
  postId    String
  author    User     @relation(fields: [authorId], references: [id])
  authorId  String
  createdAt DateTime @default(now())
}

model Category {
  id    String @id @default(cuid())
  name  String @unique
  posts Post[]
}

model Tag {
  id    String @id @default(cuid())
  name  String @unique
  posts Post[]
}
```

---

[← Back to Overview](./README.md) | [Previous: Week 5-6](./week-05-06-build-tools.md) | [Next: Week 9-10 →](./week-09-10-react.md)
