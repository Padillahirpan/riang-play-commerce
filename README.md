# RiangPlay

[RiangPlay](https://riang-play-fe.vercel.app//) is an online store for Kids and Babies wear.

Table of contents:

- [RiangPlay](#riangplay)
  - [Links](#links)
  - [Features](#features)
  - [UI Design](#ui-designs)
    - [Home Page](#home-page)
    - [Product](#products)
    - [Detail Product](#detail-product)
    - [Cart Page](#cart-page)
    - [Login Page](#login-page)
    - [Register Page](#register-page)

## Links

- Website/Frontend: <https://riang-play-fe.vercel.app/>
- Backend: <https://riang-play-be.onrender.com/>
- Repositories:
  - General: <hhttps://github.com/Padillahirpan/riang-play-commerce>
  - Backend: <https://github.com/Padillahirpan/riang-play-be>
  - Frontend: <https://github.com/Padillahirpan/riang-play-fe>

Inspirations:

- <https://symautilized.com/>

## Features

- Home Page
  - Navbar
  - Hero Section
  - Products New Arrivals
- Register Page
- Login Page
- Product Page
  - Image
  - SKU (stock keeping until)
  - Name
  - Price
  - Description
  - Add to cart form: quantity input & add to cart button
  - Shopping cart page
- Product items to buy
  - Image, name, price, quantity, total (price x quantity)
  - Remove items
- Profile Page
- Cart Page
- Link: continue shopping, go to products catalogue
- Link: checkout

## Entity Relationship Diagram (ERD)

![ERD](./diagrams/riang-play-erd.svg)

## REST API Endpoints

- Production: `https://riang-play-fe.vercel.app/`
- Local: `http://localhost:3000`

### API Product

| Endpoint          | HTTP     | Description               |
| ----------------- | -------- | ------------------------- |
| `/products`       | `GET`    | Get all products          |
| `/products/:slug` | `GET`    | Get product by slug       |
| `/products/seed`  | `POST`   | Seed all initial products |
| `/products`       | `POST`   | Add new product           |
| `/products`       | `DELETE` | Delete all products       |
| `/products/:id`   | `DELETE` | Delete product by id      |
| `/products/:id`   | `PATCH`  | Update product by id      |

### API Auth

| Endpoint          | HTTP     | Permission    | Description                          |
| ----------------- | -------- | ------------- | ------------------------------------ |
| `/auth/register`  | `POST`   | Public        | Register User                        |
| `/auth/login`     | `POST`   | Public        | Login User                           |
| `/auth/me`        | `GET`    | Authenticated | Get User Profile                     |
| `/cart`           | `GET`    | Authenticated | Get the current user's cart items    |
| `/cart/items`     | `POST`   | Authenticated | Add new item(s) to the cart          |
| `/cart/items/:id` | `DELETE` | Authenticated | Remove an item from the cart by ID   |
| `/cart/items/:id` | `PATCH`  | Authenticated | Update the quantity of an item by ID |
