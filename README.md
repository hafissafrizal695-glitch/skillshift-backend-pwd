# SkillShift Backend

Career Portal API - Express + SQLite untuk SkillShift.

## Tech Stack

- **Express.js 5**
- **better-sqlite3**
- **Railway** untuk deployment

## Setup

```bash
# Install dependencies
npm install

# Development
npm run dev

# Production
npm start
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/health` | Health check |
| GET | `/api/jobs` | List semua lowongan |
| GET | `/api/jobs/:id` | Detail lowongan |
| POST | `/api/jobs` | Tambah lowongan |
| PUT | `/api/jobs/:id` | Update lowongan |
| DELETE | `/api/jobs/:id` | Hapus lowongan |
| POST | `/api/register` | Register mahasiswa |
| POST | `/api/login` | Login |
| GET | `/api/saved/:id_user` | List lowongan tersimpan |
| POST | `/api/saved` | Simpan lowongan |
| DELETE | `/api/saved/:id_user/:id_lowongan` | Hapus dari tersimpan |
| GET | `/api/accepted/:id_user` | List lowongan diterima |
| POST | `/api/accepted` | Tandai diterima |
| DELETE | `/api/accepted/:id_user/:id_lowongan` | Hapus dari diterima |
| GET | `/api/admin/accepted` | List semua accepted (admin) |

## Deploy ke Railway

1. Push ke GitHub repo
2. Import di [railway.app](https://railway.app)
3. Railway auto-detect Node.js
4. Set environment variable: `PORT = 3001`
5. Deploy!

## Database

Menggunakan SQLite yang tersimpan di folder `data/`. Untuk production, pertimbangkan migrate ke PostgreSQL.

## Akun Demo

| Role | Email | Password |
|------|-------|----------|
| Admin | `admin@skillshift.com` | `admin123` |
| Mahasiswa | `mahasiswa@skillshift.com` | `123456` |
