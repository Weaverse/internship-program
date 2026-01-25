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

### Express.js
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
   ```javascript
   // Install mysql2 package
   // npm install mysql2

   const mysql = require('mysql2');

   // Create connection
   const connection = mysql.createConnection({
     host: 'localhost',
     user: 'root',
     password: 'your_password',
     database: 'blog_db'
   });

   // Connect to database
   connection.connect((err) => {
     if (err) {
       console.error('Error connecting to MySQL:', err);
       return;
     }
     console.log('Connected to MySQL database');
   });
   ```

6. **Learn Basic CRUD Operations**
   ```javascript
   // CREATE - Insert data
   app.post('/api/users', (req, res) => {
    const { name, email } = req.query;
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

1. **Install API Client**
   - Install [Postman](https://www.postman.com/downloads/) or any preferred API client
   - Alternative options: Insomnia, Thunder Client (VS Code extension), HTTPie

2. **Test All APIs**
   - Create a Postman collection for your API
   - Test all CRUD operations using the API client
   - Save example requests for each endpoint
   - Test edge cases and error handling

3. **Update to [RESTful Standards](https://restfulapi.net/)**
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

### Learn Prisma

1. **Install and Initialize Prisma**
   ```bash
   npm install prisma @prisma/client
   npx prisma init
   ```

2. **Configure Prisma with MySQL**
   Update your `.env` file:
   ```env
   DATABASE_URL="mysql://root:password@localhost:3306/blog_db"
   ```

3. **Define Prisma Schema**
   ```prisma
   // prisma/schema.prisma
   generator client {
     provider = "prisma-client-js"
   }

   datasource db {
     provider = "mysql"
     url      = env("DATABASE_URL")
   }

   model User {
     id        String   @id @default(cuid())
     email     String   @unique
     name      String
     password  String
     posts     Post[]
     comments  Comment[]
     createdAt DateTime @default(now())
   }
   ```

4. **Update Database Calls to Use Prisma**
   ```typescript
   import { PrismaClient } from '@prisma/client';
   const prisma = new PrismaClient();

   // CREATE
   app.post('/api/users', async (req, res) => {
     try {
       const user = await prisma.user.create({
         data: req.body
       });
       res.status(201).json(user);
     } catch (error) {
       res.status(400).json({ error: error.message });
     }
   });

   // READ with pagination
   app.get('/api/users', async (req, res) => {
     // ...
   });

   // UPDATE
   app.put('/api/users/:id', async (req, res) => {
     // ...
   });

   // DELETE
   app.delete('/api/users/:id', async (req, res) => {
     // ...
   });
   ```

5. **Deploy to Cloud Database**
   - Register for a free database hosting service:
     - [Supabase](https://supabase.com/) - Generous free tier with PostgreSQL
     - [PlanetScale](https://planetscale.com/) - MySQL-compatible serverless database
     - [Railway](https://railway.app/) - Simple deployment with MySQL/PostgreSQL
     - [Aiven](https://aiven.io/) - Managed cloud databases
   - Update your DATABASE_URL to use the cloud database instead of local

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

[← Back to Overview](./README.md) | [Previous: Week 5-6](./week-05-06-ai-build-tools.md) | [Next: Week 9-10 →](./week-09-10-react.md)
