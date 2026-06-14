+++
date = '2026-04-07T00:00:00+01:00'
lastmod = '2026-06-13T00:00:00+01:00'
draft = false
title = 'MapaYCamión - SaaS de Gestión de Flotas y Facturación'
description = 'SaaS multitenant de logística que desarrollo de forma autónoma: planificación de rutas, gestión de flota y conductores y facturación VeriFactu'
tags = ['Django', 'DRF', 'React', 'Vite', 'TypeScript', 'PostgreSQL', 'Redis', 'Celery', 'Docker', 'SaaS']
image = '/images/projects/mapaycamion-logo.svg'
translationKey = 'mapaycamion'
+++

## Descripción

**MapaYCamión** es una plataforma de gestión logística y facturación que desarrollo **de forma autónoma como proyecto propio** (la empresa, en un principio, se llamará MapaYCamión). Es un SaaS multitenant orientado a empresas de transporte que necesitan planificar rutas, gestionar su flota y conductores y llevar la facturación desde una única herramienta.

Cada cliente funciona en su propio esquema aislado de PostgreSQL (un esquema por tenant), de forma que los datos quedan totalmente separados entre empresas. El cálculo de rutas se realiza sobre datos reales de OpenStreetMap con **GraphHopper**, las direcciones se resuelven con geocodificación **Photon** y la facturación es compatible con el sistema español **VeriFactu**.

### Características principales

- SaaS multitenant con un esquema de base de datos aislado por cliente
- Enrutado por subdominio (panel de administración vs. app por tenant)
- Planificación de rutas sobre datos de OpenStreetMap con GraphHopper
- Geocodificación de direcciones con Photon
- Gestión de flota, conductores, itinerarios y planificación
- Facturación compatible con VeriFactu
- Panel de administración para crear y gestionar tenants
- Tareas en segundo plano y planificación con Celery + Redis

### Tecnologías utilizadas

- Django + Django REST Framework
- django-tenants (multitenancy)
- React + Vite + TypeScript (integrado con django-vite)
- PostgreSQL + Redis
- Celery (workers + beat)
- GraphHopper (rutas OSM) + Photon (geocodificación)
- Docker y Docker Compose
