# 50 Beginner-Friendly MERN Backend Assignments (With DB, CRUD, Auth)

## LEVEL 1 — MongoDB + Basic CRUD (10)

1. Connect an Express app to MongoDB with Mongoose and verify connection.
2. Create a `User` model (name, email) and an endpoint to **create** a user (`POST /users`).
3. Add `GET /users` to return all users from MongoDB.
4. Add `GET /users/:id` to return a single user by ID.
5. Add `PUT /users/:id` to update a user (full replace or partial).
6. Add `DELETE /users/:id` to delete a user.
7. Create a `Product` model (name, price) and build CRUD endpoints for products.
8. Implement server-side validation in Mongoose (required fields) and return validation errors.
9. Create an endpoint to search users by name (case-insensitive) using Mongoose queries.
10. Add unique index on `email` and handle duplicate-key errors gracefully.

## LEVEL 2 — Auth Basics (10)

11. Add `password` to `User` model and implement **registration** (`POST /auth/register`) storing hashed password with bcrypt.
12. Implement **login** (`POST /auth/login`) that verifies password and returns a JWT.
13. Create auth middleware that protects routes by verifying JWT.
14. Protect `GET /users` so only authenticated requests can access it.
15. Implement **logout** using token blacklist (in-memory simple approach).
16. Create `PATCH /users/:id/password` route to change password (verify old + set new).
17. Add email format validation and password minimum length checks.
18. Create a `profile` route (`GET /me`) that returns logged-in user (decoded from token).
19. Implement refresh tokens: issue short-lived access token + long-lived refresh token, and `POST /auth/refresh`.
20. Add role field to User (`user` / `admin`) and middleware to restrict admin routes.

## LEVEL 3 — CRUD Features & Querying (10)

21. Add pagination for products (`GET /products?page=1&limit=10`) using skip/limit.
22. Add sorting/filtering (`?sort=price&min=100&max=500`) on product list.
23. Implement soft-delete for users (`isDeleted = true`) and add restore endpoint.
24. Add endpoint to upload a product image and save filename in DB (multer).
25. Create a `Category` model and link products to categories (ObjectId ref).
26. Create endpoint to fetch products by category with populated category data.
27. Use Mongoose aggregation to compute average product price per category.
28. Add endpoint to increment product likes (`POST /products/:id/like`) using `$inc`.
29. Implement bulk-insert endpoint for many products (`POST /products/bulk`).
30. Add full-text search on products using a text index.

## LEVEL 4 — Relations, Transactions & File Storage (10)

31. Create `Post` model & `Comment` model; allow creating comments linked to posts.
32. Add endpoint to fetch a post with populated comments.
33. Implement cascading delete: deleting a post removes its comments.
34. Use transactions to transfer stock between two products atomically.
35. Store uploaded file metadata in DB and create download endpoint.
36. Implement avatar upload for users and serve files from `/uploads/avatars`.
37. Add image type + size validation before saving upload.
38. Add favorite products: store product IDs in `User.favorites` with add/remove endpoints.
39. Create `Cart` model and endpoints to add/remove items.
40. Populate user cart with product data and compute total price.

## LEVEL 5 — Security, Testing & DevOps (10)

41. Add rate limiting using `express-rate-limit` or custom memory-based limiter.
42. Implement email verification using token + `/auth/verify?token=...`.
43. Implement password reset flow: forgot + reset endpoints with token.
44. Add input sanitization to prevent NoSQL injection (e.g., disallow `$` in queries).
45. Write Jest + Supertest tests for auth (register, login, protected route).
46. Write role-based access tests for admin-only routes.
47. Setup logging using `winston` including DB error logging & request IDs.
48. Add login attempt limiter (lockout after N failed attempts).
49. Dockerize app with `Dockerfile` + `docker-compose.yml` (app + MongoDB).
50. Add Swagger/OpenAPI docs for main endpoints and serve at `/api-docs`.
