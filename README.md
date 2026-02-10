# Pulse PWA — Deploy in 5 Minutes

## What's in this folder

```
pulse-pwa/
├── index.html      ← The entire app (single file, no build needed)
├── manifest.json   ← Tells phones this is an installable app
├── sw.js           ← Service worker (enables offline mode)
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
└── README.md       ← You are here
```

## Deploy to Vercel (Easiest — 5 minutes)

### Option 1: Drag and drop
1. Go to https://vercel.com and sign up (free)
2. Click "Add New Project"
3. Drag this entire `pulse-pwa` folder into the upload area
4. Click Deploy
5. You'll get a URL like `pulse-pwa.vercel.app`

### Option 2: Via GitHub
1. Create a GitHub account if you don't have one
2. Create a new repository (e.g., `pulse-app`)
3. Upload all files from this folder to the repo
4. Go to https://vercel.com → "Import Git Repository"
5. Select your repo → Deploy
6. Done! Updates auto-deploy when you push changes

## Deploy to Netlify (Alternative)

1. Go to https://netlify.com and sign up (free)
2. Drag this folder into the deploy area
3. Get your URL like `pulse-pwa.netlify.app`

## Deploy to Cloudflare Pages (Best for censorship resistance)

1. Go to https://pages.cloudflare.com
2. Connect your GitHub repo or direct upload
3. Deploy — Cloudflare's global network makes it very hard to block

## Custom Domain (Optional)

1. Buy a domain (e.g., `pulse.ge` or `pulsege.org`)
   - Recommended registrars: Cloudflare, Namecheap, Porkbun
2. In Vercel/Netlify/Cloudflare: Settings → Domains → Add your domain
3. Update DNS records as instructed
4. SSL certificate is automatic and free

## How Users Install It

### iPhone (Safari)
1. Open the URL in Safari
2. Tap the Share button (square with arrow)
3. Scroll down → "Add to Home Screen"
4. The app appears as an icon, opens fullscreen like a native app

### Android (Chrome)
1. Open the URL in Chrome
2. Chrome shows "Add to Home Screen" banner automatically
3. Or: tap ⋮ menu → "Install app"

## Updating the App

Just edit `index.html` and re-deploy. Users get the update next time they open the app.
To force an immediate update, change `CACHE_NAME` in `sw.js` (e.g., `pulse-v2`).

## Making It Harder to Block

If the Georgian government tries to block the domain:
- **Multiple domains**: Deploy to 2-3 different URLs
- **Cloudflare**: Their network is extremely difficult to block entirely
- **Share via QR codes**: Print physical QR codes pointing to the URL
- **IPFS deployment**: Use Fleek.co to deploy to IPFS (decentralized, uncensorable)
- **Tor hidden service**: For maximum censorship resistance

## Next Steps to Make It Real

1. **Real news feeds**: Replace demo data with RSS from Civil.ge, OC Media
2. **Real-time chat**: Integrate Matrix protocol (matrix.org)
3. **Real maps**: Add Leaflet.js or Mapbox for actual GPS mapping
4. **Push notifications**: Add Firebase Cloud Messaging
5. **Bluetooth mesh**: Add WebBluetooth API for offline P2P
