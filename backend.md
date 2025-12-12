# 50 Beginner-Friendly MERN Backend Assignments (No DB, No Auth, No CRUD)

## LEVEL 1 — Basics (10 Tasks)

1. Create an Express server that returns "Hello World" on `/`.
2. Make a `/about` route that returns your name and hobby in JSON.
3. Build `/sum?a=5&b=10` that reads query params and returns their sum.
4. Add `/reverse/:word` that reverses the `:word` route parameter.
5. Create `/status` that returns `{ server: "running", time: "<iso-time>" }`.
6. Implement `/square/:n` that returns the square of `n`.
7. Write middleware that logs method, URL, and response time for every request.
8. Create a route that returns an array of 5 hard-coded student objects.
9. Add a route that returns the maximum number from a fixed array.
10. Build `/greet/:name` that returns `Hello <name>`.

## LEVEL 2 — Request Handling & Validation (10 Tasks)

11. Parse JSON body and validate required fields using middleware (no DB).
12. Implement input validation with Joi or express-validator for POST requests.
13. Build a route that accepts comma-separated numbers and returns mean/median.
14. Accept a CSV file upload (multer) and parse to JSON (in-memory).
15. Create a route that accepts a JSON array and returns it sorted by a field.
16. Implement content-type checking middleware to reject non-JSON POSTs.
17. Build a route that rate-limits requests per IP (in-memory counter).
18. Implement body-size-limiting middleware rejecting payloads above X KB.
19. Add a route that sanitizes HTML input and returns the cleaned version.
20. Create an endpoint that converts incoming JSON to YAML and returns the YAML.

## LEVEL 3 — File Handling & Streams (10 Tasks)

21. Implement file upload using multer and save files into a local `uploads/` folder.
22. Create a route that serves static files from a `public/` directory.
23. Build a file-download endpoint that streams a large file using `fs.createReadStream`.
24. Implement chunked file upload (reassemble chunks inside `/tmp`).
25. Create a route that streams a large CSV and counts rows without loading entire file.
26. Implement gzip compression for a text file and stream compressed content.
27. Build an image-resize route using Sharp (resize an uploaded image).
28. Create an endpoint that generates a PDF using pdfkit and returns it.
29. Build a route that zips multiple local files and streams the zip download.
30. Create a route that converts uploaded JSON file → CSV and returns the CSV.

## LEVEL 4 — Middleware, Error Handling & Logging (10 Tasks)

31. Create centralized error-handling middleware returning errors in JSON format.
32. Implement request logging using morgan and also save logs to a file.
33. Add helmet + CORS and create example routes to show their effects.
34. Write middleware to block requests from suspicious User-Agents.
35. Implement exponential backoff retry logic for an outbound HTTP request.
36. Build graceful shutdown handling SIGINT/SIGTERM (cleanup timers / jobs).
37. Add `/health/liveness` and `/health/readiness` monitoring endpoints.
38. Implement an in-memory LRU cache for expensive computations.
39. Create an endpoint demonstrating streaming JSON responses (SSE-style chunks).
40. Build a simple in-memory token-bucket rate limiter middleware.

## LEVEL 5 — Realtime, Scripts, Testing & DevOps (10 Tasks)

41. Implement a WebSocket echo server using the `ws` package.
42. Build a simple WebSocket mini-chat storing last 10 messages in memory.
43. Create a Server-Sent Events (SSE) endpoint sending current time every second.
44. Write a CLI script (`node scripts/report.js`) that reads a local file and prints stats.
45. Add Jest + Supertest unit tests for a simple route (success + error case).
46. Configure ESLint + Prettier and show linting/fixing on a sample file.
47. Create a `Dockerfile` and containerize your Express server.
48. Add a node-cron job that writes a timestamped file into `/tmp` every minute.
49. Build a proxy endpoint that forwards requests to an external API and logs them.
50. Add Swagger/OpenAPI documentation for 5 routes and serve it at `/docs`.
