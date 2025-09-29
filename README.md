# Amazing Safari (Batch 9)

[Amazing Safari](https://amazingsafari.haidar.dev) online store for zoo products merchandise.

## Links

- Frontend Web: <https://amazingsafari.haidar.dev>
- Backend API: <https://amazingsafari-api.haidar.dev>

Repositories:

- General: <https://github.com/bear-mentor/amazingsafari>
- Backend API: <https://github.com/bear-mentor/amazingsafari-api>
- Frontend Web: <https://github.com/bear-mentor/amazingsafari-web>

UI Designs:

- Figma: <https://figma.com/design/TC8pwzy5HpWoFAQWJpN6IJ/amazingsafari.haidar.dev>

Inspirations:

- <https://safariwonders.com>
- <https://tamansafari.com>
- <https://stlzoo.org/services/gift-shops/zoo-merchandise>

## Architecture & Tech Stack

### Client = Presentation Layer (UI)

- HTML
- CSS
  - Tailwind CSS
  - shadcn/ui
- JavaScript
- TypeScript
- React
- React Router
- Docker

### Server = Application Layer (Business Logic)

- JavaScript
- TypeScript
- Hono
- OpenAPI
- Zod
- Docker

### Data Access Layer (Database)

- Prisma
- PostgreSQL
- Docker

## Features

- Home page
  - Hero section
  - Products catalogue
  - Example: <https://safariwonders.com/product-animal>
- Product page
  - Image
  - SKU (stock keeping unit)
  - Name
  - Price
  - Description
  - Add to cart form: quantity input & add to cart button
- Shopping cart page
  - Product items to buy
    - Image, name, price, quantity, total (price x quantity)
    - Remove item
  - Link: continue shopping, go to products catalogue
  - Link: checkout
- Checkout page
  - Order summary
    - Product items to buy
    - Grand total of all product items to buy
- Place order / transaction is being processed

### Home Page

<img alt="Home Page" src="./designs/home.jpg" width="400" />

## Entity Relationship Diagram (ERD)

![ERD](./diagrams/erd.svg)

## REST API Endpoints

- Production: `https://amazingsafari.haidar.dev`
- Local: `http://localhost:3000`

| Endpoint         | HTTP     | Description               |
| ---------------- | -------- | ------------------------- |
| `/products`      | `GET`    | Get all products          |
| `/products/:id`  | `GET`    | Get product by id         |
| `/products/seed` | `POST`   | Seed all initial products |
| `/products`      | `POST`   | Add new product           |
| `/products`      | `DELETE` | Delete all products       |
| `/products/:id`  | `DELETE` | Delete product by id      |
| `/products/:id`  | `PUT`    | Update product by id      |

### Product

```json
{
  "id": "abc123",
  "slug": "panda-plush",
  "name": "Panda Plush",
  "price": 120000,
  "createdAt": "2025-09-29",
  "updatedAt": "2025-09-29"
}
```
