# Svastana Wellness — Website

Holistic naturopathy website for **Dr. G. Monica Sravanthi BNYS MBA MD Acupuncture**.

## 📁 Folder Structure

```
svastana-wellness/
├── index.html              ← Main website (single page)
├── netlify.toml            ← Netlify deployment config
├── .gitignore
└── assets/
    └── images/
        └── 8390CD77-EBEB-4FC6-9E44-10F103870F37.JPG   ← Doctor photo (add here)
```

## 🚀 Deploy to Netlify

### Option 1 — Drag & Drop (no GitHub needed)
1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag the entire `svastana-wellness` folder onto the Netlify dashboard
3. Done — your site is live!

### Option 2 — GitHub + Netlify (recommended)
1. Push this folder to a new GitHub repository
2. In Netlify → **Add new site → Import from Git**
3. Select your GitHub repo
4. Build settings:
   - **Publish directory:** `.` (a single dot)
   - **Build command:** *(leave empty)*
5. Click **Deploy site**

## 🖼️ Adding the Doctor Photo

Place the photo at exactly this path inside the project folder:

```
assets/images/8390CD77-EBEB-4FC6-9E44-10F103870F37.JPG
```

The image is already referenced in the HTML — just drop the file in place.

## ✏️ Customisation

| What to change | Where in `index.html` |
|---|---|
| Phone number | Search `8333888010` |
| WhatsApp number | Search `wa.me/91` |
| Email address | Search `svastanawellness8` |
| Clinic address | Search `#contact` section |
| Doctor photo | `assets/images/` folder |
| Logo image | `assets/images/` folder (currently uses same photo) |
