# Nepak Point

Nepak Point is an e-commerce personal project dedicated to badminton enthusiasts,providing high-quality equipment, accessories, and apparel to enhance their game experience.
[Nepak Point](https://nepak-point.indahmutiah.com)

Table of Contents:

- [Nepak Point](#nepak-point)
  - [Technologies](#technologies)
  - [Links](#links)
  - [Features](#features)
  - [REST API Endpoints](#rest-api-endpoints)

## Technologies

- Frontend: React, Bun, TailwindCSS, ShadcnUI, Typescript, React Icons
- Backend: Bun, Hono, Typescript, Postgresql, Prisma ORM, Docker

## Links

- Website/Frontend: <https://nepak-point.indahmutiah.com>
  - Backend: <https://nepak-point-api.indahmutiah.com>
- Repositories:
  - General: <https://github.com/indahmutiah/nepak-point>
  - Backend: <https://github.com/indahmutiah/nepak-point-api>
  - Frontend: <https://github.com/indahmutiah/nepak-point-web>

Inspirations:

- <https://www.decathlon.co.id/c/olahraga-raket/badminton/perlengkapan-badminton.html#>
- <https://www.rumahflypower.id/>
- <https://www.planetsports.asia/equipment/eq-badminton.html>

## Features

- Home page
  - Hero section
  - Products catalogue. Example: <https://www.rumahflypower.id/products?CollectionItem=all&activePage=products>
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
  - Shipping address form
    Name, email, phone, address, province, city, postal code
- Place order / transaction is being processed

## REST API Endpoints

- Production: `https://nepak-point-api.indahmutiah.com`
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

more endopoints later

### Product

```json
{
  "id": "ULID123",
  "name": "Astec ",
  "series": "Storm Z9000 Badminton",
  "category": "racket",
  "price": 799000
}
```

### Add New Product

Request Body:

```json
{
  "name": "Samurai Shuttlecock",
  "series": "Speed 78 Semi Spin",
  "category": "accesories",
  "price": 135000
}
```

Response Body:

```json
{
  "id": "abc123",
  "name": "Samurai Shuttlecock",
  "series": "Speed 78 Semi Spin",
  "category": "accesories",
  "price": 120000
}
```
