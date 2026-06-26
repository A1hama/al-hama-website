# Al Hama Website — Complete Setup & Deployment Guide

## What You Have

✅ Beautiful Next.js frontend (your luxury brand design)
✅ Strapi CMS backend (easy content management)
✅ Ready to deploy to the internet

---

## Step 1: Test Locally First

### Setup Frontend

```bash
cd frontend
npm install
npm run dev
```

Visit http://localhost:3000

### Setup CMS Backend

In another terminal:

```bash
cd cms
npm install
npm run develop
```

Visit http://localhost:1337/admin

### Create Your First Content

1. Go to http://localhost:1337/admin
2. Create an admin account
3. Create a **HomePage** entry
4. Publish it
5. Visit http://localhost:3000 — content appears automatically!

---

## Step 2: Deploy Frontend to Vercel

1. Go to [vercel.com](https://vercel.com)
2. Click **New Project**
3. Import your GitHub repo `A1hama/al-hama-website`
4. Set **Root Directory** to `./frontend`
5. Add environment variable:
   ```
   NEXT_PUBLIC_STRAPI_URL=https://your-cms-backend.com
   ```
6. Click **Deploy** ✅

---

## Step 3: Deploy Backend to Railway

1. Go to [railway.app](https://railway.app)
2. Click **New Project**
3. Select **Deploy from GitHub**
4. Choose `A1hama/al-hama-website`
5. Click **Deploy**
6. Railway will ask for configuration:
   - Set **Root Directory** to `./cms`
   - Add **PostgreSQL** database
   - Set environment variables
7. Deploy! ✅

---

## Step 4: Connect Frontend to Backend

Once backend is live:

1. Copy your Railway backend URL
2. Go to Vercel → Your Project → Settings
3. Update `NEXT_PUBLIC_STRAPI_URL` to your Railway URL
4. Redeploy

✅ **Your website is now live!**

---

## Step 5: Start Managing Content

Now you can:

✅ Log into CMS: `https://your-railway-url.com/admin`
✅ Create/edit pages, services, team members
✅ Upload images
✅ **NO CODING NEEDED** — changes appear instantly!

---

## Helpful Links

- Vercel: https://vercel.com
- Railway: https://railway.app
- Next.js Docs: https://nextjs.org/docs
- Strapi Docs: https://strapi.io/documentation

---

## Troubleshooting

**Frontend can't reach backend?**
- Check `NEXT_PUBLIC_STRAPI_URL` is correct
- Ensure backend is running

**CMS won't start?**
- Check PostgreSQL database is connected
- Check environment variables are set

**Need more help?**
- Check deployment docs in `docs/` folder
- Contact Railway or Vercel support

---

## Next Steps

1. ✅ Test locally
2. ✅ Deploy to Vercel + Railway
3. ✅ Add your company content
4. ✅ Share with the world!

🚀 **You're ready to go!**
