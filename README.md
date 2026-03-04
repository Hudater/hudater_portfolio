# hudater.dev

> [!NOTE]
> This is the staging branch for my portfolio site

Personal portfolio and infrastructure playground for Harshit Mani Tripathi.

This repository contains the source code and infrastructure configuration for hudater.dev.  
The project is designed to demonstrate reproducible infrastructure, CI/CD automation, and edge deployments.

---

## Architecture Overview

The project is structured to separate application logic from infrastructure provisioning.

```text
hudater_portfolio/
├── astro/ # Astro-based portfolio source
├── iac/ # OpenTofu infrastructure definitions
├── .github/ # CI/CD workflows
```

### Current State

- `hudater.dev` temporarily served via GitHub Pages
- DNS managed declaratively using OpenTofu
- Link hub available at `links.hudater.dev`

### Target State

- Astro site deployed via Cloudflare Workers
- DNS and routing managed via OpenTofu
- Automated CI/CD using GitHub Actions
- Preview environments per branch
- Zero-downtime production deployment

---

## Infrastructure Design Goals

- Reproducible DNS configuration
- Infrastructure as Code (OpenTofu)
- Automated deployment pipeline
- Staging and preview environments
- Clean rollback strategy
- Minimal manual configuration

---

## Technology Stack

- Astro
- Cloudflare Workers
- OpenTofu
- GitHub Actions
- GitHub Pages (temporary)

---

## Deployment Strategy

### Production

- Trigger: Push to `main`
- Build Astro
- Deploy to Cloudflare Worker
- Update production route

### Preview

- Trigger: Pull Request
- Deploy isolated preview instance
- Assign preview subdomain
- Destroy on PR close

---

## TODO

### Infrastructure

- [ ] Provision Cloudflare Worker via OpenTofu
- [ ] Provision Worker routes via OpenTofu
- [ ] Automate DNS record lifecycle
- [ ] Define staging environment in IaC
- [ ] Add rollback workflow
- [ ] Configure low TTL for controlled failover testing

### Application

- [ ] Complete Astro portfolio structure
- [ ] Add project documentation pages
- [ ] Add infrastructure case study section
- [ ] Add CI/CD documentation page
- [ ] Add architecture diagrams

### CI/CD

- [ ] Implement production deployment workflow
- [ ] Implement preview deployment workflow
- [ ] Auto-comment preview URL on PR
- [ ] Add smoke test after deploy
- [ ] Add build status badge

### Observability

- [ ] Add structured logging
- [ ] Explore Cloudflare analytics integration
- [ ] Add basic uptime monitoring
- [ ] Document incident handling process

### Polish

- [ ] Add Open Graph image
- [ ] Add custom error page
- [ ] Add security headers
- [ ] Write technical blog section
- [ ] Document migration from GitHub Pages to Workers

---

## Purpose

This repository is an evolving infrastructure project designed to demonstrate systems thinking, automation discipline, and production-oriented engineering practices.
