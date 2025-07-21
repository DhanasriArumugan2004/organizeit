# 🚀 Getting Started with OrganizeIT

**Integrated Collaboration and IT Operations Platform**

This guide walks you through setting up, developing, and contributing to OrganizeIT—your all-in-one IT operations and team collaboration platform.

---

## 📁 Project Structure

organizeit/
├── backend/ # NestJS backend (API server)
├── frontend/ # Next.js frontend (UI with Tailwind CSS)
├── devops/ # Dockerfiles, deployment, and infra scripts
├── docs/ # Documentation files (like this one)
├── .github/ # GitHub Actions for CI/CD
├── docker-compose.yml # Docker setup for full stack
└── README.md # General overview

text

---

## ⚙️ Prerequisites

Before starting, make sure you have:

- **[Node.js (v20+)](https://nodejs.org/)**
- **[npm (v9+)** or yarn
- **[Docker Desktop](https://www.docker.com/products/docker-desktop)**
- **Git & GitHub CLI**
- Code Editor (e.g., [VS Code](https://code.visualstudio.com/))

---

## 🚧 Local Development (No Docker)

### 1. Frontend (Next.js + Tailwind)

cd frontend
npm install
npm run dev

text

Visit: [http://localhost:3000](http://localhost:3000)

### 2. Backend (NestJS)

cd backend
npm install
npm run start:dev

text

Visit: [http://localhost:4000](http://localhost:4000)

---

## 🐳 Docker Workflow

### Run Entire App with Docker Compose:

docker-compose up --build

text

- Frontend → http://localhost:3000  
- Backend → http://localhost:4000

### Stop containers:

Ctrl+C # To stop containers
docker-compose down

text

You can also run containers in the background:

docker-compose up -d

text

---

## 🌐 Environment Variables

You’ll create `.env` files in both apps as needed. For example:

**For Backend:**
PORT=3000
DATABASE_URL=your_postgres_url
JWT_SECRET=your_jwt_secret

text

**For Frontend:**
NEXT_PUBLIC_API_URL=http://localhost:4000

text

> ⚠️ Never commit `.env` files to GitHub. Add them to `.gitignore`.

---

## 🧪 Scripts (Frontend and Backend)

### Lint, Format, and Build

npm run lint # Lint code
npm run format # Format with Prettier
npm run build # Production build

text

### To run tests (when implemented):

npm run test

text

---

## 🚀 CI/CD with GitHub Actions

- Located in: `.github/workflows/ci.yml`
- Runs on `push` & `pull_request` to `main` branch
- What it does:
  - Installs dependencies
  - Runs lint & build for frontend and backend
  - (Optional: Extend it with test and deploy steps)

**✅ Check build logs:**
Go to GitHub → Actions tab → Click latest workflow run to inspect logs.

---

## ✅ Agile Development Checklist

We use a **solo-friendly Kanban** flow (Trello, Notion, GitHub Projects) with these columns:

- Backlog
- In Progress
- Done

### Initial Feature Tickets:

- [x] Scaffold frontend (Next.js + Tailwind)
- [x] Scaffold backend (NestJS)
- [x] Set up CI/CD with GitHub Actions
- [x] Set up Docker Compose for full stack
- [ ] Implement user login/register (JWT)
- [ ] Create dashboard UI for projects/tasks

---

## 📌 Useful Resources

- [Next.js Docs](https://nextjs.org/docs)
- [NestJS Docs](https://docs.nestjs.com/)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
- [Docker Compose](https://docs.docker.com/compose/)
- [GitHub Actions Docs](https://docs.github.com/en/actions)

---

## 📖 Contributing (even for yourself)

1. Create a new Git branch
2. Write or change code
3. Run `npm run lint && npm run format`
4. Commit your work and push:
git add .
git commit -m "feat: add new feature"
git push

text

---

## ✍️ Author

Made with ❤️ by [Your Name] as a solo developer project.

---

## ✅ Keep Evolving

Use this file as a living knowledge base. Log known issues, endpoints, config behaviors, or infra notes as you scale.
