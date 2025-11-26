# Sistema X — Demo (React + Node + PostgreSQL + Playwright)


## Visão geral
Projeto mínimo para demonstração de CRUD com testes E2E usando Playwright.


## Pré-requisitos
- Node 18+ instalado
- Docker Desktop (recomendado)
- VS Code (recomendado)


## Como usar (com Docker) - passos rápidos
1. `docker-compose up --build`
2. Em outro terminal:
- `docker-compose exec backend npm run prisma:generate`
- `docker-compose exec backend npm run prisma:migrate`
- `docker-compose exec backend npm run seed`
3. Acesse frontend: `http://localhost:3000`
4. Backend health: `http://localhost:4000/health`
5. Rodar testes (localmente): `npx playwright test`


## Como usar (sem Docker) - passos resumidos
1. Configure Postgres local e atualize `backend/.env` com `DATABASE_URL`.
2. No `backend/`: `npm install`, `npx prisma generate`, `npx prisma migrate dev --name init`, `npm run seed`, `npm run dev`.
3. No `frontend/`: `npm install`, `npm run dev`.


## Estrutura
- `backend/` - API Express + Prisma
- `frontend/` - Vite + React
- `tests/` - Playwright E2E


## Comandos úteis
- `docker-compose up --build`
- `docker-compose down`
- `docker-compose exec backend sh`
- `npx playwright test`
-
- [frontend.zip](https://github.com/user-attachments/files/23780717/frontend.zip)



## Observações de segurança
As senhas/seed estão em texto apenas para demo. Em produção usar bcrypt e variáveis de ambiente seguras.


