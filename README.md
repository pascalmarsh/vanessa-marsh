
# Vanessa Marsh — Portfolio Site

## Deploying to Vercel

### Option 1: Vercel CLI (fastest)
```bash
npm install -g vercel
cd vanessa-marsh
vercel
```
Follow the prompts. Your site will be live at a `*.vercel.app` URL instantly.

### Option 2: Vercel Dashboard (no code needed)
1. Go to [vercel.com](https://vercel.com) and sign in
2. Click **"Add New Project"**
3. Drag and drop the `vanessa-marsh` folder into the upload area
4. Click **Deploy**
5. Your site is live!

### Option 3: GitHub → Vercel (auto-deploy on every update)
1. Push this folder to a GitHub repo
2. Connect the repo on vercel.com → "Add New Project" → Import from GitHub
3. Every push to `main` automatically redeploys the site

## Connecting vanessamarsh.com
1. After deploying, go to your Vercel project → **Settings → Domains**
2. Add `vanessamarsh.com` and `www.vanessamarsh.com`
3. Update your domain's DNS records (Vercel will show you exactly what to add)

## What's in the site
- Full hero with mosaic of real artwork images
- 12-product shop grid (all sourced from Big Cartel)
- Live shopping cart with bundle discounts (10% / 18% / 25%)
- Checkout redirects to Big Cartel, Vinted, Instagram
- Platform directory (Big Cartel, Vinted, Instagram, Commission)
- About section with full bio from vanessamarsh.com
- Commission request form (medium, size, budget, brief)
- Custom cursor, scroll animations, mobile responsive

## Updating Products
Edit the `products` array in the `<script>` section of `index.html`.
Each product has: title, price, img (BigCartel CDN URL), medium, size, tags, desc, platformUrl, available.

## Email for Commission Form
The form currently shows a success message. To wire it to a real email:
- Use [Formspree](https://formspree.io) (free) — replace the form's `onsubmit` with a fetch to your Formspree endpoint
- Or use Netlify Forms if you switch hosting

## Notes
- All images load directly from BigCartel's CDN — no image hosting needed
- The site is fully static HTML/CSS/JS — zero dependencies, zero build step
- Bundle discounts are applied client-side; the checkout redirects to the platform for actual payment
