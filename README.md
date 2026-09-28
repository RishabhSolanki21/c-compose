# Chat & Text-Editing App: Docker Compose

Runs the frontend, backend and PostgreSQL together with one command.

## Requirements

- Docker Desktop (includes Docker Compose)
- Git

## Setup

Clone all three repos **into the same parent folder**:

```bash
mkdir chat-app && cd chat-app
git clone https://github.com/RishabhSolanki21/FrontendChat.git
git clone https://github.com/RishabhSolanki21/WebChat.git
git clone https://github.com/RishabhSolanki21/c-compose.git
```

Resulting layout:

```
chat-app/
├── FrontendChat/
├── WebChat/
└── c-compose/
```

## Configure

```bash
cd c-compose
cp .env.example .env        # Windows PowerShell: Copy-Item .env.example .env
```

Edit `.env` and set your own values:

```env
POSTGRES_USER=your_user
POSTGRES_PASSWORD=your_password
POSTGRES_DB=chatappdb
SPRING_DATASOURCE_URL=jdbc:postgresql://postgres:5432/chatappdb
```

## Run

```bash
docker compose up --build
```

- Frontend: http://localhost:5173
- Backend: http://localhost:8080

Stop with docker compose down
