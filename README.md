Enterprise Systems Services — Static Website Repository

A production-ready, multi-page static website for Enterprise Systems Services, s.r.o. — an IT services company targeting enterprise and mid-market clients across Central Europe.

## Pages

| File | Description |
|------|-------------|
| `index.html` | Homepage with hero, service overview, differentiation, resources |
| `network-engineering.html` | L1/L2 support page — SLA matrix, monitoring tools, escalation |
| `network-migration.html` | Migration page — 5-phase methodology, pricing, case studies |
| `server-break-fix.html` | Break-fix page — process table, certifications, turnaround SLAs |
| `contact.html` | Contact page — form, direct contact methods, coverage area |

## Design

- Hybrid dark/light: dark header + hero sections, light content sections
- Google Font: Inter (loaded via CDN)
- Fully responsive (mobile hamburger menu)
- Zero JavaScript dependencies — pure CSS
- SEO-ready semantic HTML

## Quick Deploy with Docker

```bash
# Build and run locally
docker compose up --build -d

# Access at http://localhost
```

## Deploy to Your Server

1. Copy all files to your server
2. Serve with any static server (nginx, Caddy, Apache, etc.)
3. Place behind Cloudflare for CDN/SSL/DDoS protection

### Minimal nginx config

```nginx
server {
    listen 80;
    server_name ess.example.com;
    root /var/www/ess-website;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

## Before Going Live

- Replace `+421 XXX XXX XXX` with your real phone number
- Verify `info@enterprise-systems.sk` is correct
- Replace placeholder case studies with real client examples
- Add real vendor certification badges (Cisco, Dell, HPE, etc.)
- Set up a contact form backend (Formspree, custom endpoint, etc.)
- Add Google Analytics / privacy policy

## Cloudflare Setup

1. Add A record `@` → your server IP (orange cloud ON)
2. Add A record `www` → your server IP (orange cloud ON)
3. SSL/TLS mode: Full
4. Enable CDN, Brotli compression, and security features

---

© 2025 Enterprise Systems Services, s.r.o.