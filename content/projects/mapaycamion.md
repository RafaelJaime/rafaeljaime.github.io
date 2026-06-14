+++
date = '2026-04-07T00:00:00+01:00'
lastmod = '2026-06-13T00:00:00+01:00'
draft = false
title = 'MapaYCamión - Fleet Management & Invoicing SaaS'
description = 'Multi-tenant logistics SaaS I am building independently: route planning, fleet and driver management, and VeriFactu-compliant invoicing'
tags = ['Django', 'DRF', 'React', 'Vite', 'TypeScript', 'PostgreSQL', 'Redis', 'Celery', 'Docker', 'SaaS']
image = '/images/projects/mapaycamion-logo.svg'
translationKey = 'mapaycamion'
+++

## Description

**MapaYCamión** is a logistics management and invoicing platform I am building **independently as my own venture** (the company is, for now, named MapaYCamión). It is a multi-tenant SaaS aimed at transport and haulage companies that need to plan routes, manage their fleet and drivers, and handle billing in a single tool.

Each client runs in its own isolated PostgreSQL schema (schema-per-tenant), so data is fully separated between companies. Routing is computed over real OpenStreetMap data with **GraphHopper**, addresses are resolved with **Photon** geocoding, and invoicing is compliant with the Spanish **VeriFactu** e-invoicing system.

### Main Features

- Multi-tenant SaaS with an isolated database schema per client
- Subdomain-based routing (platform admin vs. per-tenant app)
- Route planning over OpenStreetMap data with GraphHopper
- Address geocoding with Photon
- Fleet, driver, itinerary and scheduling management
- VeriFactu-compliant invoicing
- Platform admin dashboard to create and manage tenants
- Background jobs and scheduling with Celery + Redis

### Technologies Used

- Django + Django REST Framework
- django-tenants (multi-tenancy)
- React + Vite + TypeScript (integrated via django-vite)
- PostgreSQL + Redis
- Celery (workers + beat)
- GraphHopper (OSM routing) + Photon (geocoding)
- Docker & Docker Compose
