# Amy Wang — Consulting Website

Personal consulting website for Amy Wang, AI Product & Automation Consultant.
Deployed via GitHub Pages at **https://phwamy.github.io/amywang-consulting/**

---

## Pages

| File | URL | Purpose |
|------|-----|---------|
| `index.html` | `/` | Main single-page site |
| `card.html` | `/card.html` | Mobile digital business card |

## Structure

```
├── index.html        # Main site (single file — all CSS + HTML)
├── card.html         # Digital business card (linked from QR code)
├── amy-wang.vcf      # vCard contact file (downloaded via "Save to Contacts")
├── photo.png         # Portrait photo used in hero and business card
└── README.md
```

## Sections (index.html)

- **Nav** — sticky, links to each section
- **Hero** — name, role, tagline, portrait photo
- **About** — background paragraph
- **Services** — 2×2 grid: AI Workflow Audit, Tool Setup & Automation, Custom App Development, Team Training
- **Selected Work** — 5 project cards with two badge types (Enterprise / Award|Personal)
- **Certifications** — AWS, Azure, Accenture badges linking to Credly
- **Contact** — email CTA + Cal.com inline booking widget (30 min / 60 min, Google Meet)
- **Footer** — LinkedIn, email links

## Integrations

| Service | Purpose | Where to update |
|---------|---------|----------------|
| **Cal.com** (`cal.com/phw.amy`) | Inline booking widget | Cal.com dashboard → Event Types |
| **Credly** | Certification badge images | Update image URLs in `index.html` if certs change |
| **QR Server API** | Generates QR code image for business card | URL in `index.html` and `card.html` |

## Updating content

All content lives in `index.html` (and `card.html` for the business card). After editing, push to `main` and GitHub Pages redeploys automatically within ~1 minute.

```bash
git add .
git commit -m "your message"
git push
```

### Common updates

**Change copy or add a project**
Edit the relevant section in `index.html` directly.

**Add a new certification**
Find the cert badge on [Credly](https://www.credly.com), copy the image URL, and add a new `.cert-card` block in the certifications section.

**Update contact info**
Search for `phw.amy@gmail.com` in both `index.html` and `card.html`.

**Update vCard**
Edit `amy-wang.vcf` with any new contact details, then push.

## Deployment

Hosted on **GitHub Pages** from the `main` branch, root folder (`/`).
No build step — push HTML files directly.

Settings: `github.com/phwamy/amywang-consulting` → Settings → Pages
