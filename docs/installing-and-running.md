# Installation

NestJS Boilerplate supports [TypeORM](https://www.npmjs.com/package/typeorm) and [Mongoose](https://www.npmjs.com/package/mongoose) for working with databases. By default, TypeORM uses [PostgreSQL](https://www.postgresql.org/) as the main database, but you can use any relational database.

Switching between TypeORM and Mongoose is implemented based on the [Hexagonal Architecture](architecture.md#hexagonal-architecture). This makes it easy to choose the right database for your application.

---

## Table of Contents <!-- omit in toc -->

- [Comfortable development (PostgreSQL + TypeORM)](#comfortable-development-postgresql--typeorm)
  - [Video guideline (PostgreSQL + TypeORM)](#video-guideline-postgresql--typeorm)
- [Comfortable development (MongoDB + Mongoose)](#comfortable-development-mongodb--mongoose)
- [Quick run (PostgreSQL + TypeORM)](#quick-run-postgresql--typeorm)
- [Quick run (MongoDB + Mongoose)](#quick-run-mongodb--mongoose)
- [Links](#links)

---

## Comfortable development (PostgreSQL + TypeORM)

1. Clone repository

   ```bash
   git clone --depth 1 https://github.com/algorithm99129/nestjs-boilerplate.git my-app
   ```

2. Go to folder, and copy `env-example-relational` as `.env`.

   ```bash
   cd my-app/
   cp env-example-relational .env
   ```

3. Change `DATABASE_HOST=postgres` to `DATABASE_HOST=localhost`

   Change `MAIL_HOST=maildev` to `MAIL_HOST=localhost`

4. Run additional container:

   ```bash
   docker compose up -d postgres adminer maildev
   ```

5. Install dependency

   ```bash
   npm install
   ```

6. Run app configuration

   > You should run this command only the first time on initialization of your project, all next time skip it.

   > If you want to contribute to the boilerplate, you should NOT run this command.

   ```bash
   npm run app:config
   ```

7. Run migrations

   ```bash
   npm run migration:run
   ```

8. Run seeds

   ```bash
   npm run seed:run:relational
   ```

9. Run app in dev mode

   ```bash
   npm run start:dev
   ```

10. Open <http://localhost:3000>

### Video guideline (PostgreSQL + TypeORM)

<https://github.com/user-attachments/assets/136a16aa-f94a-4b20-8eaf-6b4262964315>

---

## Links

- Swagger (API docs): <http://localhost:3000/docs>
- Adminer (client for DB): <http://localhost:8080>
- MongoDB Express (client for DB): <http://localhost:8081/>
- Maildev: <http://localhost:1080>

---

Previous: [Introduction](introduction.md)

Next: [Architecture](architecture.md)
