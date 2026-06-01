# Planora

Planora is a hospitality-focused ERP platform for workforce planning, legal-compliant scheduling, occupancy forecasting, and operational visualization.

This repository is currently aligned with a formal technical specification and follows a specification-first development approach.

## Project Goals

- Enforce labor constraints and role-based access in scheduling workflows.
- Improve staffing decisions using occupancy forecasting and optimization.
- Provide a 3D digital twin view for spatially-aware operations.
- Support offline-first employee workflows (PWA behavior).
- Maintain production-minded engineering quality, security, and traceability.

## Functional Scope

### Core Modules

1. ERP and legal compliance engine
2. Predictive AI and auto-scheduling
3. 3D digital twin and spatial mapping
4. Offline-first employee mobility

### Optional Module (Time-Permitting)

5. Network and connected objects extension (MQTT telemetry ingestion, gateway auth, dashboard freshness)

The optional network track is explicitly non-blocking for the baseline release.

## Target Architecture

- `planora-api` (Node.js/Express): business rules, RBAC, scheduling orchestration
- `planora-ai` (Python/FastAPI): forecasting and recommendation services
- `planora-db` (PostgreSQL): operational source of truth
- Frontend (React + TypeScript): manager dashboard and employee portal
- 3D layer (Three.js / React Three Fiber): interactive floor and assignment mapping
- Optional extension: MQTT broker + ingest service for edge telemetry

## Quality Targets (from Specification)

- Availability: `>= 99.5%` monthly uptime (excluding planned maintenance)
- API performance: p95 `< 300 ms` for core scheduling APIs
- Scheduler runtime: one-week draft generation `< 90 s` (baseline property size)
- Security baseline: JWT + RBAC, TLS in transit, least-privilege access, auditability
- Observability baseline: structured logs, trace IDs, and service metrics

## Delivery Roadmap (12 Weeks)

- `S1-S2`: Architecture foundation, security, and core API
- `S3-S4`: Frontend/PWA and AI integration
- `S5-S6`: 3D digital twin, hardening, and release preparation
- `QA` stream: cross-cutting validation and UAT
- `OPT` stream (optional): network extension only if baseline remains on track

## Security and Compliance Highlights

- Legal rest-window enforcement and immutable schedule audit trails
- Department-scoped RBAC controls
- Versioned model/scheduling metadata for traceability
- Explicit quality gates before production release

## Current Repository Status

- Specification-complete baseline (`PLAN-SPEC-004`)
- Implementation to follow sprint-by-sprint roadmap
- Optional network extension included as a conditional scope

## Specification Documents

- Main technical specification (LaTeX): `../docs/specs/planora_technical_spec_v3.tex`
- Main technical specification (PDF): `../docs/specs/planora_technical_spec_v3.pdf`

## Maintainer

Ali Akbar Shahriari Garaei

## License

Apache License 2.0 — see [LICENSE](LICENSE) for details.

Copyright 2026 Ali Akbar Shahriari Garaei
