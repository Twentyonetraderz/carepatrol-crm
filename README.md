# CarePatrol CRM

A lightweight, brandable CRM for managing senior care leads.

## Features
- Sales pipeline (kanban board)
- Lead table with search
- CSV lead upload
- Internal messaging
- Lead detail panel with notes
- Data saved locally in the browser

## Deploy to Vercel (5 minutes)

### Option A — Drag & Drop (easiest)
1. Go to [vercel.com](https://vercel.com) and sign up / log in (free)
2. Click **"Add New Project"**
3. Choose **"Upload folder"** and drag this entire `carepatrol-crm` folder
4. Click **Deploy**
5. Vercel gives you a live URL instantly (e.g. `carepatrol-crm.vercel.app`)

### Option B — GitHub (recommended for updates)
1. Create a free GitHub account at [github.com](https://github.com)
2. Create a new repository called `carepatrol-crm`
3. Upload these two files (`index.html` and `vercel.json`)
4. Go to [vercel.com](https://vercel.com) → **Add New Project** → import your GitHub repo
5. Click **Deploy**
6. Every time you push changes to GitHub, Vercel auto-redeploys

### Custom Domain
1. In Vercel dashboard → your project → **Settings → Domains**
2. Add `crm.carepatrol.com` (or whatever you want)
3. Follow the DNS instructions Vercel gives you

## Automate Lead Input via Email (Zapier)

1. Sign up at [zapier.com](https://zapier.com) (free tier works)
2. Create a Zap: **Trigger** = new email in Gmail/Outlook matching a rule
3. **Action** = append a row to a Google Sheet with lead details
4. The CRM's CSV upload can then import that sheet export weekly

For real-time sync, ask your developer to add a small API backend.

## CSV Format for Upload

```
name,company,phone,email,value,source,stage
Mary Johnson,Sunrise Home Care,555-0101,mary@example.com,4500,Referral,New Lead
```

Valid stages: New Lead, Contacted, Qualified, Proposal Sent, Closed Won, Closed Lost
