# Prisma Blog App

A backend blog application built with **Express.js**, **PostgreSQL**, and **Prisma**, featuring authentication using **Better Auth** with **Email/Password** and **Google OAuth**.

---

## 🚀 Tech Stack

- **Backend:** Express.js (Node.js)
- **Database:** PostgreSQL
- **ORM:** Prisma
- **Authentication:** Better Auth
  - Email & Password
  - Google OAuth
- **Language:** TypeScript
- **Runtime:** Node.js

---

## ✨ Features

- User authentication with email/password
- Google OAuth login
- Secure session handling using Better Auth
- Blog post CRUD operations
- PostgreSQL database with Prisma ORM
- Prisma migrations and generated client
- Environment-based configuration
- Scalable project structure

---

## 📁 Project Structure

```
blog-app/
├─ generated/
│  └─ prisma/
│     ├─ internal/
│     │  ├─ class.ts
│     │  ├─ prismaNamespace.ts
│     │  └─ prismaNamespaceBrowser.ts
│     ├─ models/
│     │  ├─ Account.ts
│     │  ├─ Comment.ts
│     │  ├─ Post.ts
│     │  ├─ Session.ts
│     │  ├─ User.ts
│     │  └─ Verification.ts
│     ├─ browser.ts
│     ├─ client.ts
│     ├─ commonInputTypes.ts
│     ├─ enums.ts
│     └─ models.ts
├─ prisma/
│  ├─ migrations/
│  │  ├─ 20251228060945_update/
│  │  │  └─ migration.sql
│  │  └─ migration_lock.toml
│  └─ schema.prisma
├─ resources/
│  ├─ erd.pdf
│  ├─ Project Requirement Document (PRD).pdf
│  └─ sd.png
├─ src/
│  ├─ lib/
│  │  ├─ auth.ts
│  │  └─ prisma.ts
│  ├─ middlewares/
│  │  └─ auth.ts
│  ├─ modules/
│  │  └─ post/
│  │     ├─ post.controller.ts
│  │     ├─ post.router.ts
│  │     └─ post.service.ts
│  ├─ app.ts
│  └─ server.ts
├─ .env
├─ .gitignore
├─ package-lock.json
├─ package.json
├─ pnpm-lock.yaml
├─ prisma.config.ts
├─ README.md
└─ tsconfig.json

```

## ⚙️ Environment Variables

Create a .env file in the project root:

```
PORT=3000

DATABASE_URL=postgresql://user:password@localhost:5432/prisma_blog

BETTER_AUTH_SECRET=your-secret-key
BETTER_AUTH_URL=http://localhost:3000

APP_USER=your-email
APP_PASS=your-password

GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret

```

## 🧱 Prisma Setup

Install dependencies:

```
npm install

```

Generate Prisma client:

```
npx prisma generate

```

Run database migrations:

```
npx prisma migrate dev

```

## 🔐 Authentication (Better Auth)

This project uses Better Auth for authentication with:

- Email & Password

- Google OAuth

Generate the Better Auth schema:

```
npx @better-auth/cli generate

```

## ▶️ Running the Application

Start development server:

```
npm run dev

```

## 🧪 Development Tools

Open Prisma Studio:

```
npx prisma studio

```

## 🛡️ Security

- Passwords are securely hashed

- OAuth tokens are never exposed to the client

- Trusted origins are enforced via Better Auth

- Sensitive configuration is stored in environment variables