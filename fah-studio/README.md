# FAH Studio — Roongfah AI Muse

Internal content tool for **Fah** — Roongfah's AI brand persona.  
Generates captions, video scripts, and carousel copy in her authentic Thai voice.

---

## Quick Deploy to Vercel (Team Setup)

### Step 1 — Push to GitHub
```bash
git init
git add .
git commit -m "FAH Studio v1"
git remote add origin https://github.com/YOUR_USERNAME/fah-studio.git
git push -u origin main
```

### Step 2 — Import on Vercel
1. Go to [vercel.com](https://vercel.com) → **New Project**
2. Import from GitHub → select `fah-studio`
3. Framework: **Other** (static)
4. Click **Deploy**

### Step 3 — Add API Key (one-time)
1. In Vercel → your project → **Settings → Environment Variables**
2. Add: `ANTHROPIC_API_KEY` = `sk-ant-...`
3. Get your key at [console.anthropic.com](https://console.anthropic.com) → API Keys
4. **Redeploy** once after adding the key

### Step 4 — Share URL with Team
Your team URL will be: `https://fah-studio-xxx.vercel.app`  
Anyone on your team opens this URL and generates content — no setup needed.

---

## Local Testing (no Vercel)

Open `index.html` in browser → go to **Settings** tab → add your API key there.

Or use a local server:
```bash
npx serve .
# or
python3 -m http.server 3000
```

Note: Local API calls go directly from browser to Anthropic. Fine for testing, but key is visible in browser storage. Use Vercel for production.

---

## File Structure

```
fah-studio/
├── index.html          ← Main app (Studio, Bible, Calendar, Settings)
├── api/
│   └── generate.js     ← Vercel serverless function (API key stays server-side)
├── vercel.json         ← Vercel config
└── README.md           ← This file
```

---

## Content Types Available

| Type | Output | Use for |
|------|--------|---------|
| Morning Routine | Caption + hashtags | Monday reels |
| Product Demo | Caption + hashtags | Mid-week posts |
| Ingredient Spotlight | Carousel text | Educational content |
| Lifestyle Caption | Caption + hashtags | Fill days |
| Before / After | Caption + hashtags | Results posts |
| Thai Beauty Tip | Caption + hashtags | Saturday tip posts |
| Product Review | Caption + hashtags | Deep review content |
| Video Script (HeyGen) | Full spoken script | Paste into HeyGen |

---

## Fah Character Quick Reference

- **Age / Location:** 28, Bangkok
- **Personality:** Warm, grounded, never salesy
- **Voice:** Casual Bangkok Thai + natural English
- **Story:** Had dull skin, found real skincare, Roongfah is her ritual
- **NOT:** A model, brand rep, or corporate spokesperson

---

## Monthly Cost Estimate

| Tool | Cost |
|------|------|
| Midjourney (images) | You own it |
| ElevenLabs (voice) | You own it |
| HeyGen (video avatar) | ฿1,050–3,500/mo |
| CapCut (editing) | Free |
| FAH Studio (this) | Claude API credits |

**Total new spend to launch Fah: ฿1,050–3,500/month**

---

Built for Roongfah team · June 2026  
Powered by Claude (claude-sonnet-4-6)
