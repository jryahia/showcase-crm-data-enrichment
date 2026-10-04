# CRM Data Enrichment

**Enrichment pipeline prototype: takes CRM records with only a name and email and fills in company, role and contact fields.**

> **This is a proprietary project. Source code is private. This page showcases the system's architecture and results.**

**Case study page:** [https://jryahia.github.io/showcase-crm-data-enrichment/](https://jryahia.github.io/showcase-crm-data-enrichment/)

![CRM Data Enrichment](assets/00-dashboard.png)

## Problem it solves

CRM records often arrive with just a name and an email. This prototype models the enrichment pipeline (domain extraction, company lookup, role prediction, confidence scoring) behind a single API and dashboard.

## Architecture

![Architecture](assets/architecture.svg)

1. Records arrive individually or in batches.
2. The email domain is extracted and used for company lookup.
3. Role and contact fields are filled in with a confidence score.
4. Enriched records and coverage stats are stored and shown.

## Key features

- Single and batch enrichment endpoints
- Confidence score per record
- Toggleable lookup sources
- Coverage dashboard
- Clearly flagged demo engine: no live Apollo or Clearbit calls

## Tech stack

![Python](https://img.shields.io/badge/Python-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![FastAPI](https://img.shields.io/badge/FastAPI-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![Jinja2](https://img.shields.io/badge/Jinja2-161b22?style=for-the-badge&labelColor=161b22&color=161b22)

## What it does in practice

- Prototype stage: enrichment currently uses a built-in demo engine with generated data, and every record is labelled as mock.

## Screenshots

**Enriched records with confidence (demo engine)**

![Enriched records with confidence (demo engine)](assets/00-dashboard.png)

**Enrichment sources and test enrichment (demo engine)**

![Enrichment sources and test enrichment (demo engine)](assets/10-sources.png)

---

Built by [Yahya Jarray](https://github.com/jryahia). Interested in a similar system? [Get in touch](mailto:yahiajarray43@gmail.com).

This repository contains no source code. It is a case study for a proprietary project. © Yahya Jarray.
