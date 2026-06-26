# Detailed Deployment Guide

## Option 1: Vercel + Railway (Easiest)

### Deploy Frontend to Vercel

1. https://vercel.com → Sign up
2. Click "New Project"
3. Select "Import" and choose your GitHub repo
4. Set root directory: `./frontend`
5. Add env var: `NEXT_PUBLIC_STRAPI_URL=https://your-backend.railway.app`
6. Deploy!

### Deploy Backend to Railway

1. https://railway.app → Sign up
2. New Project → Deploy from GitHub
3. Select repo, set root dir: `./cms`
4. Railway auto-creates PostgreSQL
5. Deploy!

---

## Option 2: Render + Vercel

### Deploy Backend to Render

1. https://render.com → Sign up
2. New Web Service
3. Connect GitHub
4. Set root directory: `./cms`
5. Add PostgreSQL database
6. Deploy!

---

## Environment Variables

### Frontend (.env.local)
```
NEXT_PUBLIC_STRAPI_URL=https://your-cms-url.com
NEXT_PUBLIC_API_URL=https://your-cms-url.com/api
```

### Backend (.env)
```
HOST=0.0.0.0
PORT=1337
DATABASE_URL=postgresql://...
JWT_SECRET=your-secret-key
ADMIN_JWT_SECRET=your-admin-secret
```

---

## Testing

### Local
```bash
cd frontend && npm run dev
cd cms && npm run develop
```

### Production
- Frontend: https://your-app.vercel.app
- CMS: https://your-cms.railway.app/admin

---

You're done! 🎉
