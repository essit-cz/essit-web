# Enterprise Systems Services — Production Website

A research-backed, SEO-optimized, multi-page static website for Enterprise Systems Services, s.r.o. — an IT services company based in Prague, Czech Republic, targeting enterprise and mid-market clients across Central Europe (CZ, SK, PL, HU).

## What Changed in This Release

Built from competitive and web-presence landscape research covering Central European IT services providers:

- **SEO**: High-intent keyword meta tags, Schema.org structured data (ITService type), Open Graph tags, hreflang alternates, canonical URLs
- **Trust Signals**: Certification badges, compliance statements, metrics section, case study content
- **CTAs**: Intent-driven language ("Request Assessment," "Schedule Consultation," "Get a Break-Fix Quote") replacing generic "Contact Us"
- **Compliance**: GDPR and Czech Data Protection Act alignment on every service page
- **FAQ Sections**: Research-backed Q&A targeting buyer journey stages
- **Structure**: Service-first navigation with clear scope boundaries per enterprise procurement expectations

## Pages

| File | Description |
|------|-------------|
| `index.html` | Homepage — hero, trust bar, service overview, differentiation, metrics, compliance |
| `network-engineering.html` | L1/L2 support — SLA matrix, monitoring tools, escalation workflow, FAQ |
| `network-migration.html` | Migration projects — 5-phase methodology, pricing models, case study, FAQ |
| `server-break-fix.html` | Break-fix — process table, certifications, data preservation, pricing, FAQ |
| `contact.html` | Contact — multi-channel methods, service interest, coverage area, response guarantee |

## Before Going Live

- Replace `+420 XXX XXX XXX` with your real phone number
- Verify `info@enterprise-systems.cz` is correct
- Replace placeholder case studies with real client examples
- Add real vendor certification badge images (Cisco, Dell, HPE, etc.)
- Set up a contact form backend (Formspree, custom endpoint, etc.)
- Add Google Analytics / privacy policy
- Set up Czech language subfolder (`/cs/`) for hreflang

## Deployment

### Quick Deploy with Docker
```bash
docker compose up --build -d
# Access at http://localhost
```

### Static Server
```bash
# Any static server works:
python3 -m http.server 80
# or with nginx (see nginx-config)
```

### Cloudflare Setup
1. Add A record `@` → your server IP (orange cloud ON)
2. Add A record `www` → your server IP (orange cloud ON)
3. SSL/TLS mode: Full
4. Enable CDN, Brotli compression, security features

---

© 2026 Enterprise Systems Services, s.r.o.