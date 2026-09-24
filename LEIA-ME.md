# Yso System v3

Um serviço só: o backend (Node + Postgres) também entrega o site (`backend/public/index.html`).

## Deploy no Render
1. Suba a pasta no GitHub (o `.gitignore` já barra o `.env`).
2. Render: New Web Service, Root Directory `backend`, Build `npm install`, Start `npm start`.
3. Variáveis de ambiente:
   - `DATABASE_URL` (Neon ou Supabase, só como Postgres)
   - `FRONTEND_URL` = a própria URL do Render
   - `ROBLOX_CLIENT_ID`, `ROBLOX_CLIENT_SECRET`
   - `ROBLOX_REDIRECT_URI` = `https://SEU-APP.onrender.com/api/auth/roblox/callback`
   - `ROBLOX_API_KEY`, `ROBLOX_GROUP_ID`
   - `ADMIN_ROBLOX_USER_ID` = seu ID numérico do Roblox (vira Creator no primeiro login)
   - `SEED_DEMO=false`
4. Cadastre a mesma Redirect URL no app OAuth do Roblox (escopos `openid` e `profile`).

## Rodar local
`cd backend`, copie `.env.example` para `.env`, `npm install`, `npm start`, abra http://localhost:4000
