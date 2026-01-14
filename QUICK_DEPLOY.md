# ⚡ Quick Deploy to Render - 5 Minutes

## Your GitHub Repo is Ready! ✅
**Repository:** https://github.com/thaungsunyein/repa

---

## Step-by-Step Deployment

### 1. Go to Render Dashboard
👉 **https://dashboard.render.com**

### 2. Create New Web Service
- Click **"New +"** button (top right)
- Select **"Web Service"**

### 3. Connect GitHub
- Click **"Connect GitHub"** (if not already connected)
- Authorize Render to access your repositories
- Select repository: **`thaungsunyein/repa`**
- Click **"Connect"**

### 4. Configure Service

**Basic Settings:**
- **Name:** `repa` (or leave default)
- **Region:** Choose closest (e.g., Frankfurt for Europe)
- **Branch:** `main`
- **Root Directory:** (leave empty)
- **Runtime:** `Python 3`
- **Build Command:** `pip install -r requirements.txt` ✅ (auto-filled)
- **Start Command:** `uvicorn app:app --host 0.0.0.0 --port $PORT` ✅ (auto-filled)

**Plan:**
- Select **"Free"** ✅

### 5. Add Environment Variables

Click **"Advanced"** → Scroll to **"Environment Variables"**

Add these **5 required variables** (get from your `.env` file):

```
OPENAI_API_KEY
FIRECRAWL_API_KEY  
SUPABASE_URL
SUPABASE_KEY
SUPABASE_SERVICE_KEY
```

**How to add:**
1. Click **"Add Environment Variable"**
2. Enter **Key:** `OPENAI_API_KEY`
3. Enter **Value:** (paste your API key from `.env`)
4. Click **"Add"**
5. Repeat for all 5 variables

**Optional (but recommended):**
```
JWT_SECRET
CORS_ORIGINS=https://repa.onrender.com
```

### 6. Deploy!

- Click **"Create Web Service"** button (bottom)
- Wait ~5-10 minutes for first deployment
- Watch the build logs (they'll show progress)

### 7. Get Your URL

Once deployment completes:
- You'll see: **"Your service is live at: https://repa-xxxx.onrender.com"**
- Copy this URL! 📋

### 8. Test It!

1. Visit your URL
2. Wait ~1 minute if first visit (cold start)
3. Try registering a new account
4. Test the chat feature

---

## 🎯 Your Deployment URL Will Be:

**`https://repa-xxxx.onrender.com`** (or similar)

*(Render will show you the exact URL after deployment)*

---

## ✅ Quick Checklist

Before deploying, make sure you have:
- [x] GitHub repo connected ✅
- [ ] All 5 environment variables ready (from `.env`)
- [ ] Supabase database set up
- [ ] API keys ready (OpenAI, Firecrawl)

---

## 🆘 Need Help?

**Common Issues:**
- **Build fails?** Check `requirements.txt` syntax
- **Service won't start?** Verify start command uses `$PORT`
- **Database errors?** Check Supabase credentials
- **CORS errors?** Add `CORS_ORIGINS` environment variable

**Full Guide:** See `RENDER_DEPLOYMENT_GUIDE.md`

---

## 📧 After Deployment

Share with your team:
- **URL:** `https://repa-xxxx.onrender.com`
- **Note:** First request after 15 min inactivity takes ~1 min
- **Testing:** See `TESTING_GUIDE.md`

---

**Ready?** Go to https://dashboard.render.com and start! 🚀







