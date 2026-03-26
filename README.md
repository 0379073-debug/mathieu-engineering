# Mathieu Engineering — Matrix Theme Template

A complete 5-page Matrix-themed website. Single HTML file, zero dependencies (fonts load from Google Fonts CDN).

---

## Files

```
mathieu-engineering-template/
├── index.html          ← The complete website (edit this)
├── README.md           ← You're reading it
└── wix-embed.html      ← Wix HTML iframe embed version
```

---

## Option 1: Deploy as a Standalone Site (Recommended)

This is the cleanest option — full design, all 5 pages, full Matrix rain effect.

### GitHub Pages (Free, 5 minutes)

1. Go to [github.com](https://github.com) and create a free account
2. Click **New Repository** → name it `mathieu-engineering` → set to **Public**
3. Click **Add file → Upload files** → drag in `index.html` → **Commit changes**
4. Go to **Settings → Pages → Source → Deploy from branch → main / root**
5. Your site will be live at `https://yourusername.github.io/mathieu-engineering/`

### Netlify (Free, 2 minutes — even easier)

1. Go to [netlify.com](https://netlify.com) → sign up free
2. Drag the `index.html` file directly onto the Netlify dashboard
3. Done — instant live URL like `https://random-name.netlify.app`
4. Optional: set a custom domain in Netlify settings

### Connect Your Own Domain

Once deployed on GitHub Pages or Netlify, you can connect `mathieuengineering.com` (or any domain) in their settings. Both support custom domains for free.

---

## Option 2: Embed in Wix

If you want to keep your existing Wix site and add this as a section:

1. Open the `wix-embed.html` file — it's a self-contained version optimized for iframe embedding
2. Host `wix-embed.html` on GitHub Pages or Netlify (same steps above)
3. In Wix Editor: **Add → Embed → HTML iFrame**
4. Set the iframe URL to your hosted `wix-embed.html` URL
5. Resize the iframe to fill the page (set height to 100vh or a fixed large value)

**Note:** Wix's free plan shows a Wix banner. The iframe approach works best on Wix Premium.

---

## Customizing the Template

All content is in `index.html`. Find these sections to edit:

### Your Projects (line ~300 in the JS section)
```javascript
const projects = [
  {
    id: 'p1',
    cat: 'engineering',        // Category: engineering / design / innovation / software
    title: 'Project_Alpha',    // ← Change this
    tag: 'Engineering',        // ← Change this
    year: '2024',              // ← Change this
    status: 'COMPLETE',        // COMPLETE or IN_PROGRESS
    desc: 'Short description', // ← Change this (shown in card)
    body: 'Full description',  // ← Change this (shown in modal popup)
    tags: ['hardware', 'custom'] // ← Change these
  },
  // ... more projects
];
```

### Your Blog Posts
```javascript
const posts = [
  {
    date: '2025-03-15',
    cat: 'mindset',
    title: 'Your Post Title',   // ← Change this
    excerpt: 'Post preview...'  // ← Change this
  },
];
```

### Your Skills (About page)
```javascript
const skills = [
  { name: 'Engineering Design', pct: 85 }, // ← Change name and percentage
  { name: 'Problem Solving',    pct: 92 },
];
```

### Stats Bar (Home page)
Search for `stat-num` in the HTML — there are 4 stat blocks. Change the numbers and labels.

### Contact Info
Search for `mathieu.engineering.company@gmail.com` — replace with your email.
Search for `patreon.com/mathieuengineering` — replace with your Patreon URL.

### Your Name / Brand
Search and replace `Mathieu_Engineering` with your brand name.
Search and replace `Mathieu Engineering` with the display version.

### Colors
At the top of the `<style>` block, find the `:root` section:
```css
:root {
  --matrix: #00ff41;     /* Main green — change to any color */
  --matrix-dim: #00cc33; /* Dimmer version of main color */
  --matrix-dark: #006618;/* Darkest version */
}
```
You can swap the green for any color — e.g. `#00bfff` for blue, `#ff6b35` for orange.

---

## Pages Included

| Page | Description |
|------|-------------|
| Home | Hero, services grid, featured projects, Patreon CTA |
| About | Bio, terminal box, animated skill bars, timeline |
| Portfolio | Filterable project grid with modal popups |
| Blog | Posts with sidebar, categories, subscribe form |
| Contact | Full contact form + info panel with availability status |

---

## Technical Notes

- **Single file** — everything is self-contained in `index.html`
- **No build step** — open the file in a browser and it works
- **Fonts** — loads Share Tech Mono + Orbitron from Google Fonts (requires internet)
- **Matrix rain** — rendered on HTML5 Canvas, runs at ~20fps, minimal CPU
- **Navigation** — pure JavaScript, no page reloads, smooth transitions
- **Mobile** — basic responsive, best viewed on desktop (engineering portfolio)

---

## License

Free to use for personal and commercial projects. No attribution required.
