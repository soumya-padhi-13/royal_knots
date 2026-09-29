Here it is as plain text:

---

**Royal Knots — Wedding Photography & Films**

A single-page, self-contained website for Royal Knots (formerly Digital Vision / Royal Knot Films), a wedding photography and cinematography studio based in Bhubaneswar, Odisha.

Live site: add your GitHub Pages link here once published

---

**What's in this repo**

royal-knots-website/
└── index.html ← the entire website (HTML + CSS + JS + all photos, one file)

That's it — no build step, no framework, no dependencies. Open index.html in a browser and the whole site runs.

**Why it's one file**

All portfolio photos and the logo are embedded directly in index.html as base64 data, instead of being separate image files. That makes the site:

- Portable — copy or share index.html alone and every photo still works
- Simple to host — no folder structure to keep in sync, no broken image links
- Slightly heavier to load — the file is currently ~1.9MB, which is fine for GitHub Pages but not as fast as separate, lazily-loaded images. If the site grows past 20–30 photos, it's worth switching to a real /assets image folder — ask and this can be restructured.

**Features**

- Custom "shutter" intro animation on load, branded with the Royal Knots logo
- Film-frame / sprocket-hole visual motif throughout (services, gallery)
- Sections: Hero, Services, Packages, Portfolio Gallery, Process, Testimonial, Contact
- Responsive layout (mobile, tablet, desktop)
- Scroll-triggered fade-in animations
- Respects prefers-reduced-motion for accessibility
- 11-photo masonry gallery pulled from real shoots

**How to publish (GitHub Pages)**

1. Go to the repo's Settings → Pages
2. Under Build and deployment, set Source to Deploy from a branch
3. Pick the main branch and / (root) folder → Save
4. Wait 1–2 minutes, then refresh — your live URL will appear at the top of that page, something like: https://<your-username>.github.io/<repo-name>/

**Customizing**

- Studio name / tagline → the `<title>` tag, and the hero `<h1>` text
- Phone number / email → footer section, near the bottom of the `<body>`
- Instagram / social links → footer `<a>` tags under "Follow"
- Package prices → `#packages` section, each `.pack` block
- Gallery photos → `#work` section — each `.gcell` has `style="background-image:url('...')"`. Replace the base64 string with a new photo, or swap in a normal image URL
- Colors → CSS variables at the top of the `<style>` block (--gold, --wine, --ink, etc.)

**Known limitations**

- The contact form is front-end only right now — it shows a "thanks" confirmation but doesn't actually send anywhere yet. To make it functional, connect it to an email service (e.g. Formspree, Getform) or a backend endpoint.
- Package pricing, address, and phone number are placeholders and should be double-checked before going live.

**Credits**

Design and development by NexeraTech.
