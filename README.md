# 🚀 NovaOne — Unified SpaceTech Platform

**All of space technology — in one intelligent system.**

NovaOne is a next-generation spacetech web platform that unifies **mission tracking, satellite visualization, Earth observation analytics, AI image analysis, asteroid monitoring, interactive learning, and community networking** — all inside a single ecosystem.

---

## 🪐 Overview

NovaOne brings together seven core modules:

| Module | Description |
|--------|--------------|
| **LaunchDeck** | Real-time space mission tracker with countdowns, rockets, and payload insights. |
| **OrbIQ** | Live satellite dashboard with orbit visualization and pass predictions. |
| **AstroEdge** | Space data analytics and AI pipelines for Earth observation and research. |
| **StellarLearn** | Interactive education hub with 3D simulations, courses, and quizzes. |
| **NeoPulse** | Near-Earth object monitor with trajectory visualization and impact analysis. |
| **SpectraAI** | AI image analyzer for telescope and satellite imagery. |
| **GalaxNet** | Community and collaboration space for researchers and enthusiasts. |

---

## 🧩 Tech Stack

- **Frontend:** Next.js 15 + TypeScript + TailwindCSS + Framer Motion + CesiumJS + Three.js  
- **Backend:** FastAPI (Python) + Node/Fastify microservices via API Gateway  
- **Database:** PostgreSQL (multi-schema) + PostGIS + Redis + MinIO (S3)  
- **AI / ML:** PyTorch + TensorFlow + GDAL + Dask + OpenCV  
- **Infra:** Docker + Vercel + Fly.io + Upstash Redis + Neon Postgres  
- **Observability:** OpenTelemetry + Grafana + Loki + Tempo + Sentry  

---

## 🧠 Architecture

```

NovaOne
├── LaunchDeck      # Missions & launch analytics
├── OrbIQ           # Satellite & orbit dashboard
├── AstroEdge       # EO analytics & AI data pipelines
├── StellarLearn    # Space learning & simulations
├── NeoPulse        # NEO tracking & risk modeling
├── SpectraAI       # AI image analyzer
├── GalaxNet        # Social & collaboration layer
└── Core Services   # Auth, Search, Files, Notifications, Billing

````

All modules communicate via the **API Gateway** and **Redis Streams event bus**.  
Each service has its own Postgres schema for isolation.

---

## ⚙️ Local Setup

### Prerequisites
- Node.js ≥ 20  
- Python ≥ 3.10  
- Docker + Docker Compose  
- pnpm ≥ 9 (recommended)

### Clone & Install
```bash
git clone https://github.com/<your-username>/novaone.git
cd novaone
pnpm install
````

### Start Dev Environment

```bash
docker compose up -d
pnpm dev
```

Access:

* Frontend → [http://localhost:3000](http://localhost:3000)
* Gateway → [http://localhost:8080](http://localhost:8080)
* Postgres → localhost:5432
* Redis → localhost:6379

---

## 🛰️ Environment Variables

Create a `.env` in the project root:

```env
DATABASE_URL=postgresql://postgres:postgres@localhost:5432/novaone
REDIS_URL=redis://localhost:6379
MINIO_ENDPOINT=http://localhost:9000
MINIO_ACCESS_KEY=minio
MINIO_SECRET_KEY=minio123
NEXTAUTH_SECRET=<generate_one>
```

---

## 🧱 Project Structure

```
novaone/
├── apps/
│   ├── web/                # Next.js shell
│   ├── gateway/            # Fastify API gateway
│   ├── svc-launchdeck/     # Missions service
│   ├── svc-orbiq/          # Satellite service
│   ├── svc-astroedge/      # Analytics service
│   ├── svc-stellarlearn/   # Learning service
│   ├── svc-neopulse/       # NEO monitor
│   ├── svc-spectraai/      # AI image analyzer
│   ├── svc-galaxnet/       # Community network
│
├── packages/
│   ├── ui/                 # Shared shadcn UI components
│   ├── sdk/                # Typed API clients
│   ├── config/             # ESLint, Tailwind, tsconfig
│
└── infra/
    ├── docker/
    ├── k8s/
    └── terraform/
```

---

## 🧭 Roadmap

* [ ] LaunchDeck & OrbIQ MVP
* [ ] AstroEdge analytics & EO data ingestion
* [ ] NeoPulse asteroid tracker
* [ ] SpectraAI model upload & inference
* [ ] StellarLearn interactive courses
* [ ] GalaxNet feed & chat
* [ ] Unified dashboard & notifications
* [ ] API & SDK release

---

## 🤝 Contributing

Pull requests are welcome!
Please open an issue first to discuss significant changes.
Use `feat:`, `fix:`, or `chore:` prefixes in commit messages.

---

## 🌠 About

NovaOne is built to connect the dots between **space data, AI, and community** — empowering the next generation of space exploration and innovation.

> *“All of space, one platform.”*

```

---

want me to make a **badge-rich version** (with build status, tech logos, and shields.io tags for backend/frontend/modules)? it’ll make the GitHub page look more professional.
```
