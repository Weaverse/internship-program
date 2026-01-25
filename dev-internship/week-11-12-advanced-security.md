# Week 11-12: Advanced Topics & Security

|                 |                                                                                                          |
| :-------------- | :------------------------------------------------------------------------------------------------------- |
| Learning Topics | Schema validation with Zod, Authentication & Authorization, Security best practices, React Router        |
| Objectives      | Implement secure authentication system, Add comprehensive validation, Build advanced e-commerce features |

## Zod Schema Validation
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

## React Router Advanced Patterns
1. Get to know React Router:
   - What it is and why it's used
   - Basic routing concepts
   - Dynamic routing with parameters
   - Nested routes and layouts
2. Read [React Router Documentation](https://reactrouter.com/en/main/start/overview)
3. Complete [React Router Tutorial](https://reactrouter.com/en/main/start/tutorial)

## Assignment

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

[← Back to Overview](./README.md) | [Previous: Week 9-10](./week-09-10-react.md) | [Next: Week 13 →](./week-13-shopify.md)
