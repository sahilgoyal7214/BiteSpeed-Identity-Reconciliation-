# 🛂 Bitespeed Identity Reconciliation

An Express.js backend service to reconcile identities using email and phone numbers, built with **TypeScript**, **Prisma**, and **PostgreSQL**.

---

## 📌 Table of Contents

* [🚀 Features](#-features)
* [📮 API Endpoints](#-api-endpoints)
* [📦 Prerequisites](#-prerequisites)
* [⚙️ Getting Started](#-getting-started)

  * [🔁 Clone Repository](#1-clone-repository)
  * [🔐 Setup Environment Variables](#2-environment-variables)
  * [📥 Install Dependencies](#3-install-dependencies)
  * [⚒️ Generate Prisma Client](#4-generate-prisma-client)
  * [🧱 Database Migrations](#5-database-migrations)
  * [🧑‍💻 Run Locally](#6-run-locally)
* [📝 Available Scripts](#-available-scripts)

---

## 🚀 Features

* `/identify` endpoint to unify contacts based on email and/or phone.
* Robust input validation.
* Recursive linking logic for primary–secondary resolution.
* Uses transactions for consistent data handling.

---

## 📮 API Endpoints

| Method | Endpoint                                                                          | Description                                  |
| ------ | --------------------------------------------------------------------------------- | -------------------------------------------- |
| `POST` | [/identify](https://bitespeed-identity-reconciliation-bizn.onrender.com/identify) | Reconcile user identity based on email/phone |
| `GET`  | [/](https://bitespeed-identity-reconciliation-bizn.onrender.com)                  | Base health check route                      |

---

## 📦 Prerequisites

Ensure the following are installed:

* **Node.js** v18+
* **npm** v8+
* **PostgreSQL** database

---

## ⚙️ Getting Started

### 1. 🔁 Clone Repository

```bash
git clone https://github.com/sahilgoyal7214/Bitespeed-Identity-Reconciliation.git
cd Bitespeed-Identity-Reconciliation
```

### 2. 🔐 Setup Environment Variables

Create a `.env` file in the root directory:

```env
DATABASE_URL="postgresql://USER:PASSWORD@HOST:PORT/DATABASE"
```

### 3. 📥 Install Dependencies

```bash
npm install
```

### 4. ⚒️ Generate Prisma Client

```bash
npm run prisma:generate
```

### 5. 🧱 Database Migrations

* For **Development** (creates or resets schema):

  ```bash
  npm run prisma:migrate:dev -- --name init
  ```

* For **Production** (applies existing SQL migrations):

  ```bash
  npm run prisma:migrate:prod
  ```

### 6. 🧑‍💻 Run Locally

* Development (with hot-reload):

  ```bash
  npm run dev
  ```

* Build and start production:

  ```bash
  npm run build
  npm start
  ```

---

## 📝 Available Scripts

| Command                       | Description                    |
| ----------------------------- | ------------------------------ |
| `npm run dev`                 | Run with live reload (nodemon) |
| `npm run build`               | Compile TypeScript to `dist/`  |
| `npm start`                   | Run the compiled project       |
| `npm run prisma:generate`     | Generate Prisma client         |
| `npm run prisma:migrate:dev`  | Apply local dev migrations     |
| `npm run prisma:migrate:prod` | Apply production migrations    |

---
