# Server Project

This project is a backend service built using **Fastify**, **Drizzle ORM**, and **TypeScript**.  
It was developed as part of my learning journey during **Rocketseat's NLW Agents** event.

---

## 🧱 Tech Stack

- **Fastify** – High-performance Node.js framework
- **Drizzle ORM** – SQL ORM with type safety
- **PostgreSQL** – Database used
- **Zod** – Runtime schema validation
- **TypeScript** – Static typing
- **Biome** – Code formatting and linting
- **Docker** – Containerized setup and environment consistency

---

## 📦 Why Docker?

Using Docker provides several benefits:

- ✅ **Environment consistency**: Same configuration for development, testing, and production.
- 🚀 **Easy setup**: Get up and running with a single command.
- 🧹 **No host machine pollution**: Keep your local machine clean.
- 📦 **Reproducible builds**: Version-controlled containerized services.
- ⚙️ **Database ready**: PostgreSQL runs in a container via `docker-compose`.

---

## 📁 Project Structure

Key files and folders:

- `package.json` – Project dependencies and scripts
- `tsconfig.json` – TypeScript configuration
- `drizzle.config.ts` – ORM configuration
- `docker-compose.yml` – Sets up PostgreSQL service
- `docker/setup.sql` – Initializes the database schema
- `.env.example` – Sample environment variables
- `client.http` – Sample HTTP requests for testing

---

## 🐳 Docker Setup

### 1. **Install Docker**

- Download and install Docker Desktop:
  - [Docker for Windows](https://www.docker.com/products/docker-desktop/)
  - [Docker for Mac](https://www.docker.com/products/docker-desktop/)
- Ensure Docker is running:
  ```bash
  docker --version
  ```

### 2. **Create a `.env` File**

Copy the example and modify as needed:

```bash
cp .env.example .env
```

### 3. **Start PostgreSQL Using Docker Compose**

```bash
docker-compose up -d
```

This will launch a PostgreSQL container and run the initialization script from `docker/setup.sql`.

---

## 🧪 Development Scripts

Run these using `npm run <script>`:

- `dev` – Start development server
- `start` – Start production build
- `db:seed` – Seed database with example data

---

## ⚙️ Local Development Setup (Optional without Docker)

1. Install dependencies:

   ```bash
   npm install
   ```

2. Configure the environment (`.env` file)

3. Run:

   ```bash
   npm run dev
   ```

---

## 🧼 Code Style

This project uses [Biome](https://biomejs.dev) for formatting and linting:

```bash
npx biome check .
npx biome format .
```

---

## 📚 Learning Credit

Project built while attending **NLW Agents** by [Rocketseat](https://www.rocketseat.com.br/).
