# Aspirely / Skill Commerce Platform — real full-stack application

This repository is the application build, not a demo/test site.

Frontend: React + Vite
Backend: Node.js + Express
Database: PostgreSQL/Supabase

No real secret is stored in the repository.

## Supabase
Run database/001_schema.sql, then database/002_seed.sql in Supabase SQL Editor.

## Render backend
Root directory: backend
Build command: npm install
Start command: npm start

Environment:
NODE_ENV=production
PORT=5000
DATABASE_URL=<new rotated database URL>
JWT_SECRET=<new random secret>
JWT_EXPIRES_IN=7d
CORS_ORIGIN=<frontend production URL>

## Frontend
Root directory: frontend
Build command: npm install && npm run build
Publish directory: dist
VITE_API_URL=<backend URL>

## Commerce note
The current checkout is a real manual-payment-verification flow: order → payment reference → CEO verification → enrollment → eligible commission → points/level update. No frontend flag can mark an order paid.

Automated payment gateway, email/SMS and video providers are not faked; those require the real provider accounts and credentials.
