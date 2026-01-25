# Week 13: Shopify Development

> [!IMPORTANT]
> **DO NOT** use AI tools to write code for you. You come here to **LEARN**, the goal of this program is to build
> your programming skills through **hands-on** practice. AI assistants can help explain
> concepts or debug issues, but writing the code yourself is **essential** for learning.

---

|                 |                                                                                                        |
| :-------------- | :----------------------------------------------------------------------------------------------------- |
| Learning Topics | Shopify ecosystem, Partner account, Admin APIs, Hydrogen framework, Headless commerce                  |
| Objectives      | Set up Shopify development environment, Build custom Hydrogen storefront, Implement cart functionality |

## Shopify Basics
1. Create a partner account
2. Set up development store
3. Explore admin interface
4. Understand Shopify concepts:
   - Products and collections
   - Orders and customers
   - Themes and apps

## Assignment 1: Shopify Store Setup

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

## Shopify Hydrogen Development

### Hydrogen Setup
1. Read [Hydrogen Documentation](https://shopify.dev/docs/custom-storefronts/hydrogen)
2. Create Hydrogen project:
   ```bash
   npm create @shopify/hydrogen@latest
   ```

## Assignment 2: Hydrogen Storefront Development

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

### Example GraphQL Queries for Practice
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

[← Back to Overview](./README.md) | [Previous: Week 11-12](./week-11-12-advanced-security.md) | [Next: Week 14 →](./week-14-weaverse.md)
