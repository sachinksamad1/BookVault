# BookVault
A cross-platform Personal Book Library Management System (BookVault) that allows users to organise, analyse, and enrich their reading experience. The platform supports mobile (Flutter) and web (Angular) clients backed by a Node.js API, with optional AI/MCP integration for intelligent book insights

## 📌 Overview

- The Personal Library Platform enables users to:

- Create and manage personal book collections

- Store summaries, notes, and quotes

- Analyse fiction books with characters, tropes, and plot insights

- Search and explore books intelligently using AI assistance

- Access the platform seamlessly via mobile and web

The system is designed as a monorepo to ensure consistency, scalability, and maintainability across all platforms.

## 🏗️ Architecture Summary
```
Flutter Mobile App  ─┐
                     ├── REST / JSON APIs ── Node.js Backend ── Database
Angular Web App     ─┘                         │
                                               └── AI / MCP Integration

```
- Frontend (Web): Angular (latest stable), Angular Material

- Frontend (Mobile): Flutter

- Backend: Node.js + Express (TypeScript)

- AI Integration: MCP-based AI (e.g., Gemini MCP)

- Database: MongoDB (recommended) or PostgreSQL

- Deployment: Docker-ready (cloud-agnostic)

📁 Repository Structure
```
bookvault/
│
├── apps/
│   ├── mobile/            # Flutter mobile application
│   ├── web/               # Angular web application
│   └── backend/           # Node.js / Express API
│
├── packages/              # Shared contracts/models (future-ready)
│
├── docs/
│   ├── PRD-Mobile.md
│   ├── PRD-Web.md
│   ├── Architecture.md
│   ├── API-Spec.md
│   └── Roadmap.md
│
├── diagrams/              # Architecture & workflow diagrams
│
├── scripts/               # Setup and automation scripts
│
├── .github/
│   └── workflows/         # CI pipelines
│
├── README.md
├── .gitignore
└── LICENSE
```

## ✨ Key Features
Core Features

- Personal book library management

- Book metadata: title, author, genre, status

- Notes, highlights, and quotes

- Search and filtering

Fiction-Specific Features

- Story summary

- Character list and roles

- Plot and trope analysis

- Theme insights

AI-Powered Features

- Ask questions about a book

- Generate summaries and insights

- Compare books or authors

- Reading recommendations (future)

## 🚀 Getting Started
Prerequisites
| Tool | Version |
| -- | -- |
| Node.js |	≥ 24 (or latest) |
| npm / pnpm |	latest |
| Angular CLI |	21(or latest) |
| Flutter SDK |	stable |
| Docker | latest |


## 🔧 Backend Setup
```
cd apps/backend
npm install
cp .env.example .env
npm run dev
```

Backend runs by default on:
```
http://localhost:3000
```

## 🌐 Web App Setup (Angular)
```
cd apps/web
npm install
ng serve
```

Web app available at:
```
http://localhost:4200
```

## 📱 Mobile App Setup (Flutter)
```
cd apps/mobile
flutter pub get
flutter run
```

Supports Android emulator, iOS simulator, or physical device.

## 🔐 Environment Variables

Each application uses its own environment configuration.

Example (apps/backend/.env.example):
```
PORT=3000
DATABASE_URL=
AI_MCP_API_KEY=
JWT_SECRET=
```

Important: Never commit real `.env` files.

🧪 Testing (Planned / Optional)

- Backend: Jest

- Web: Angular TestBed

- Mobile: Flutter test framework

## 🔄 Branching Strategy
```
main        → production-ready
develop     → active development
feature/*   → new features
bugfix/*    → fixes
docs/*      → documentation updates
```

Commits follow Conventional Commits:
```
feat(web): add book detail view
feat(mobile): implement offline storage
fix(api): handle empty AI response
docs(prd): update mobile scope
```

## 📄 Documentation

All key documentation is maintained in `/docs`:

- PRD-Mobile.md – Mobile product requirements

- PRD-Web.md – Web product requirements

- Architecture.md – System design

- API-Spec.md – REST API contracts

- Roadmap.md – Feature planning

These documents are treated as a source of truth.

## 🧩 Roadmap (High Level)

- ✅ MVP (Library, Notes, Search)

- 🔄 AI Integration (Book Q&A, Summaries)

- 🔄 Authentication & Sync

- 🔄 Public Release (v1.0)

- 🔄 Social & Sharing Features

## 📦 Versioning

The project follows Semantic Versioning:
```
v0.1.0  MVP
v0.2.0  AI Features
v1.0.0  Public Release
```

## 🛡️ License

This project is licensed under the MIT License.
See the [LICENSE](LICENSE) file for details.

👤 Author

Sachin Samad
