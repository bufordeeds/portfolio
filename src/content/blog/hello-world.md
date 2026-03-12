---
title: 'Building My Own Cloud'
description: 'Why I moved off Vercel and Supabase onto a $5/mo VPS — and how you can too.'
pubDate: 'Mar 11 2026'
---

I just finished migrating my projects off of Vercel, Supabase, and Neon onto a single Hetzner VPS. Here's why.

## The Problem

Every new project meant another subscription. Vercel Pro, Supabase Pro, Neon — it adds up fast when you're an indie developer. I was spending ~$50-65/month on hosting alone, and each service had its own limits on projects, databases, and storage.

## The Solution

One VPS. $5.49/month. Unlimited projects.

The stack:
- **Caddy** for reverse proxy and automatic HTTPS
- **Docker Compose** to orchestrate everything
- **Postgres** for all my databases
- **MinIO** for S3-compatible object storage
- **Wildcard DNS** so any subdomain just works

Every new project is a `Dockerfile`, a `docker-compose.yml`, and a new block in the Caddyfile. Five minutes to deploy. Zero additional cost.

## What I Learned

The biggest surprise was how simple it all is. Caddy handles TLS certificates automatically. Docker keeps everything isolated. And having all my data on one box makes backups trivial.

More posts coming as I migrate each project and run into the inevitable edge cases.
