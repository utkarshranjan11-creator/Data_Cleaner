# Intelligent Data Cleaning & Validation Bot

A backend system for cleaning and validating structured datasets (CSV/Excel) with deterministic rules, audit logs, and concurrent processing support.

---

## Overview

This project processes uploaded datasets and:

- Cleans data using rule-based logic
- Flags invalid or ambiguous values
- Generates:
  - Cleaned file
  - Logs file (audit trail)

---

## Tech Stack

- FastAPI
- PostgreSQL
- Redis + RQ (background jobs)
- Docker
- Python

---

## How It Works

1. Upload file via API  
2. Job is created  
3. Worker processes file in background  
4. Outputs generated:
   - Cleaned dataset
   - Logs file  
5. User downloads results  

---

## Key Features

- Deterministic cleaning (no guessing)
- Date normalization (YYYY-MM-DD)
- Location validation (controlled list)
- Coordinate validation
- Price normalization
- Duplicate handling with logs

---

## Concurrency & Reliability

- Background processing using Redis + RQ
- Deterministic job IDs (prevents duplicates)
- Atomic file writes
- Retry handling for failed jobs

---

## Security

- JWT authentication
- Rate limiting
- File size limits
- User-based access control

---

## Running Locally (Docker)

This project has been containerized and tested locally using Docker.



Note: Redis and PostgreSQL must be available for full functionality.

## Author

Built as part of learning and building real-world AI/backend systems.
> Note: Source code and internal architecture are not publicly shared.  
> All Credentials used are dummy and for demonstration/testing purposes only.
> The system is designed for enterprise deployment and can be provided as a Docker image upon request.