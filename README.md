# 🗼 Watchtower System

> Full-stack security intelligence platform with real-time threat detection, SOC-grade audit logging, and MITRE ATT&CK mapping.

![Django](https://img.shields.io/badge/Django-4.2-092E20?style=flat&logo=django)
![Next.js](https://img.shields.io/badge/Next.js-14-000000?style=flat&logo=nextdotjs)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-4169E1?style=flat&logo=postgresql)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE-ATT%26CK-red?style=flat)

---

## Overview

Watchtower is a hospitality management system built with security-first architecture. Every user action, API call, and anomaly is logged in SIEM-compatible format and mapped to MITRE ATT&CK techniques — the same framework used by SOC analysts worldwide.

## Security Features

| Feature | Description | MITRE Coverage |
|---|---|---|
| Brute Force Detection | Auto-block after 5 failed logins/10min | T1110, T1110.001 |
| SQL Injection Prevention | Real-time regex scan in middleware | T1190 |
| XSS Protection | Input validation on every request | T1059.007 |
| Account Enumeration | Rate-limit on auth endpoints | T1087 |
| Audit Logging | Structured JSON/CEF export for SIEM | — |
| IP Blocking | Manual & automatic with expiry | — |

## Tech Stack

**Backend:** Django REST Framework · JWT Authentication · PostgreSQL · Custom Security Middleware

**Frontend:** Next.js 14 · TypeScript · Tailwind CSS · Recharts

**Security:** SIEM-compatible logging (Splunk/Elastic/QRadar) · CEF export · Real-time SOC dashboard

## Quick Start

```bash
# Backend
cd backend
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver

# Frontend
cd frontend
npm install
npm run dev
```

## SIEM Export

```bash
# JSON format (Splunk / Elastic)
GET /api/security/export/?format=json

# CEF format (QRadar / ArcSight)
GET /api/security/export/?format=cef
```

---

Built as a SOC Analyst portfolio project demonstrating defensive security concepts in a real-world application.
