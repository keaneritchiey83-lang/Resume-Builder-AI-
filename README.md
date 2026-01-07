# Resume-Builder-AI-
Building resumes with AI to help make it easier for building resumes and help perp for interview for successes  


Extended description (industry-agnostic)

Resume Builder AI is an evidence-first resume tailoring application that helps job seekers align their resume to any specific job description while maintaining accuracy and professional credibility. The tool ingests a resume (pasted text or file upload) and a target job description, then generates role-aligned bullet rewrites, a keyword coverage report, and explicit “evidence warnings” whenever a requested qualification is not supported by the resume content.

The core design principle is truthfulness by construction. Instead of generating free-form text, the system uses a structured output format (strict JSON) and enforces an evidence-first constraint: it rewrites and re-frames only what can be substantiated by the user’s provided resume. When the target role asks for tools, certifications, or experiences not present in the resume, the product flags those gaps and produces follow-up questions to help the user add legitimate evidence (projects, metrics, training, or validated responsibilities) rather than inventing claims.

From an engineering standpoint, Resume Builder AI is built as a reproducible, production-style pipeline. Inputs can be normalized into a stable schema (roles, achievements, skills, dates), each tailoring run can be versioned and logged (prompt/version + model metadata) for consistency, and the LLM provider is abstracted behind an interface to support swapping models without rewriting core logic. The system is designed to scale from a simple paste-and-generate experience to richer workflows such as resume version management, role-specific templates (e.g., federal resumes, academic CVs, sales resumes), and exportable artifacts (DOCX/PDF) that preserve formatting standards.

Because resumes often contain sensitive personal information, the product treats resume text as PII and is designed with privacy-aware defaults (e.g., minimized logging, secret management, and clear boundaries on stored artifacts). The roadmap includes stronger access controls, rate limiting for abuse prevention, and traceability features such as bullet-to-evidence mapping to increase user trust and reduce risk.


Medium description (portfolio / LinkedIn “Project” section)

Built Resume Builder AI, an evidence-first resume tailoring tool that works across industries. Users provide a resume and job description and receive tailored bullet points, ATS keyword coverage, gap analysis, and “evidence warnings” to prevent fabricated claims. The system uses structured outputs, run logging with prompt/version tracking, and a provider-agnostic LLM interface to improve reproducibility, maintainability, and responsible handling of sensitive resume data.


Resume-ready project bullets (any industry)

Resume Builder AI (Evidence-First Tailoring Tool)

Developed an AI-assisted resume tailoring workflow that generates role-aligned bullet rewrites, keyword coverage, and gap analysis across multiple industries while enforcing evidence-based claims.

Implemented structured JSON outputs and run logging (prompt/model versioning) to improve repeatability, auditability, and UI rendering reliability.

Designed a modular architecture with a provider-agnostic LLM client and privacy-aware handling of resume text (PII-safe defaults, minimized logging, secure configuration).

Optional tighter version (if space is limited):

Built an evidence-first AI resume tailor that produces truthful bullet rewrites, ATS keyword gap analysis, and reproducible run logs for any job category.


“Any industry” feature list

Paste/upload resume + paste job description

Generate:

Tailored bullet points (industry-appropriate language)

Keyword coverage (found vs missing)

Gap report (skills/tools/requirements not evidenced)

Evidence warnings (high-risk claims needing proof)

Follow-up questions to collect legitimate evidence

Export: DOCX (PDF optional)

Reliability:

Strict JSON schema for deterministic rendering

Prompt/version logging for reproducibility

Provider-agnostic LLM interface (swap models cleanly)


One-sentence value proposition (works in any field)

Tailor your resume to any job description with evidence-first rewrites, keyword coverage, and gap analysis—without inventing experience.”


Strategic questions to sharpen your positioning (optional, but high impact)

Are you optimizing primarily for speed (one-click tailoring) or accuracy and defensibility (evidence traceability and warnings)?

Will your default output be ATS-first (keyword alignment) or hiring-manager-first (clarity, impact, and narrative)?

Do you want the tool to support multiple formats (e.g., federal resume, academic CV, one-page private sector) as separate templates?

If you want, I can also provide a fully industry-agnostic JSON sample output (tailored bullets + gaps + warnings) that you can use as your mock API response in demos, independent of SOC/cybersecurity language.


1) GitHub README extended description (long, product-style)

Resume Builder AI is an evidence-first resume tailoring application that helps candidates align their resume to any job description—across industries—without compromising accuracy. Users provide a resume and a target job posting, and the system produces role-aligned bullet rewrites, keyword coverage (found vs missing), and explicit “evidence warnings” whenever a requested requirement is not supported by the resume text.

The core design principle is truthfulness by construction. Rather than generating unconstrained text, the application enforces a structured output contract (strict JSON) and applies evidence-first rules: it only reframes and improves claims that are already supported in the source resume. When the job description requests tools, credentials, or responsibilities that are not evidenced, the tool surfaces those gaps and generates targeted follow-up questions to help the user add legitimate proof (projects, quantified results, training, or clarified scope) instead of fabricating experience.

From an engineering standpoint, the system is implemented as a production-style pipeline. Inputs can be normalized into a stable schema (roles, achievements, skills, dates), every tailoring run can be logged with prompt/version identifiers and model metadata for reproducibility, and the LLM provider is abstracted behind a clean interface so models can be swapped without rewriting business logic. The architecture supports iterative resume versioning, role-specific templates, and exportable artifacts (DOCX/PDF) that preserve formatting standards.

Because resumes often contain sensitive personal information, the product treats resume content as PII and is designed with privacy-aware defaults (minimized logging, secure secret handling, and clear boundaries around artifact storage). The roadmap includes stronger access controls, rate limiting for abuse prevention, and bullet-to-evidence traceability to increase user trust and reduce risk.

Key capabilities

Tailored bullet rewrites grounded in source evidence

Keyword coverage + gap analysis (ATS and hiring-manager readability)

Evidence warnings + follow-up questions to prevent unsupported claims

Structured outputs for deterministic rendering and exports

Reproducible run logs (prompt/model versioning)

2) Resume project description (short, impact-focused)

Resume Builder AI (Evidence-First Resume Tailoring)

Built an AI-assisted resume tailoring tool that generates role-aligned bullet rewrites, keyword coverage, and gap analysis across industries while enforcing evidence-based claims.

Implemented structured JSON outputs and run logging (prompt/model versioning) to improve repeatability, auditability, and reliable UI rendering.

Designed a modular architecture with a provider-agnostic LLM interface and privacy-aware handling of resume text (PII-safe defaults, minimized logging, secure configuration).

If you need a tighter 2-bullet version:

Developed an evidence-first AI resume tailoring workflow that produces truthful rewrites plus keyword gap analysis for any job description.

Added reproducible run logging and structured outputs to support deterministic rendering and export.

3) LinkedIn “Project” description (medium, recruiter-friendly)

Built Resume Builder AI, an evidence-first resume tailoring tool that works across industries. Users paste a resume and job description to receive tailored bullet points, ATS keyword coverage, gap analysis, and “evidence warnings” that prevent fabricated claims. The system uses structured outputs, prompt/model versioning for reproducibility, and a provider-agnostic LLM interface to keep the pipeline maintainable and privacy-aware when handling sensitive resume data.

4) Interview intro (30–60 seconds) + deeper follow-up
30–60 second pitch

“I built Resume Builder AI, an evidence-first resume tailoring tool. You provide a resume and a job description, and it returns tailored bullet rewrites, keyword coverage, and explicit evidence warnings when a requirement isn’t supported by the resume. I structured the output as strict JSON for deterministic rendering and exports, and I log each run with prompt/model versioning for reproducibility. The main differentiator is that it’s designed to reduce hallucinations by treating the resume as the source of truth and turning missing requirements into follow-up questions rather than invented claims.”

2-minute technical follow-up (if they ask “how did you build it?”)

“It’s a simple pipeline: ingest resume and job text, normalize into a stable schema, extract target keywords and role signals, then generate constrained outputs under an evidence-first policy. The LLM provider sits behind an interface so the rest of the codebase isn’t coupled to one model. Each generation run is stored with prompt version and metadata so results are traceable and repeatable. Since resumes contain PII, I designed privacy-aware defaults—minimize logs, keep secrets in environment variables, and plan for access controls and rate limiting as it scales.”

Optional: One-line tagline (works everywhere)

“Tailor resumes to any job description with evidence-first rewrites, keyword coverage, and gap analysis—without inventing experience.”

Resume Builder AI

Resume Builder AI is an evidence-first resume tailoring application designed to help candidates align their resume to any job description—across industries—without compromising accuracy. Users provide a resume and a target job posting, and the system generates role-aligned bullet rewrites, ATS keyword coverage, and explicit “evidence warnings” whenever a requested qualification is not supported by the resume text.

Why this exists

Most resume “optimizers” are either (1) generic rewriters that don’t materially improve alignment, or (2) keyword stuffers that encourage unsupported claims. This project takes a different approach: truthfulness by construction. The resume is treated as the source of truth, and the tool only rewrites what is supported by evidence in the provided content.

What it does

Tailored bullet rewrites (evidence-first): Produces 6–12 job-aligned bullets grounded in the resume text (no invented tools, employers, certifications, or metrics).

ATS keyword coverage: Identifies keywords/skills requested by the job description and reports what is found vs missing.

Gap analysis + follow-up questions: Converts missing requirements into actionable questions so users can add legitimate proof (projects, outcomes, training) rather than fabricating.

Evidence warnings: Flags high-risk areas where the job asks for experience that the resume does not substantiate.

Exportable artifacts: Generates formatted outputs for submission (DOCX first; PDF optional later).

Key design principles

Evidence-first generation: Tailored bullets must remain supported by resume content.

Structured outputs: Responses are constrained to a strict JSON schema to enable deterministic UI rendering and downstream exports.

Reproducibility: Tailoring runs can be logged with prompt/version identifiers and model metadata for consistent, auditable results.

Privacy-aware defaults: Resume content is treated as sensitive data (PII). Logging is minimized and secrets are managed outside source control.

High-level architecture

Web UI: Candidate inputs (resume + job description), results view, export actions

API: Orchestrates parsing, keyword extraction, and evidence-first tailoring pipeline

Storage (optional in MVP): Resume versions, job postings, tailoring runs, and generated artifacts

LLM provider abstraction: A clean interface layer allows swapping models without rewriting business logic

Security & privacy notes

Resumes often contain personally identifiable information. The system is designed with privacy-aware defaults:

Avoid logging raw resume/job text by default (store only run IDs/metadata unless explicitly enabled)

Use environment variables for secrets (no secrets committed to the repo)

Roadmap includes access control for stored artifacts and rate limiting for abuse prevention

Roadmap

Resume parsing into a stable schema (roles, achievements, skills, dates)

Bullet-to-evidence traceability (show which resume lines support each bullet)

Template system for multiple formats (one-page, multi-page, federal resume, CV)

Evaluation metrics (relevance, readability, truthfulness) + regression tests for prompt changes

Async job processing and caching for scale


ReadME.md
# Resume Builder AI

Resume Builder AI is an evidence-first resume tailoring application designed to help candidates align their resume to any job description—across industries—without compromising accuracy. Users provide a resume and a target job posting, and the system generates role-aligned bullet rewrites, ATS keyword coverage, and explicit “evidence warnings” whenever a requested qualification is not supported by the resume text.

## Why this exists
Most resume “optimizers” are either (1) generic rewriters that don’t materially improve alignment, or (2) keyword stuffers that encourage unsupported claims. This project takes a different approach: **truthfulness by construction**. The resume is treated as the source of truth, and the tool only rewrites what is supported by evidence in the provided content.

## What it does
- **Tailored bullet rewrites (evidence-first):** Produces 6–12 job-aligned bullets grounded in the resume text (no invented tools, employers, certifications, or metrics).
- **ATS keyword coverage:** Identifies keywords/skills requested by the job description and reports what is **found vs missing**.
- **Gap analysis + follow-up questions:** Converts missing requirements into actionable questions so users can add legitimate proof (projects, outcomes, training) rather than fabricating.
- **Evidence warnings:** Flags high-risk areas where the job asks for experience that the resume does not substantiate.
- **Exportable artifacts:** Generates formatted outputs for submission (DOCX first; PDF optional later).

## Key design principles
- **Evidence-first generation:** Tailored bullets must remain supported by resume content.
- **Structured outputs:** Responses are constrained to a strict JSON schema to enable deterministic UI rendering and exports.
- **Reproducibility:** Tailoring runs can be logged with prompt/version identifiers and model metadata for consistent, auditable results.
- **Privacy-aware defaults:** Resume content is treated as sensitive data (PII). Logging is minimized and secrets are managed outside source control.

## Tech stack
- **Web:** Next.js (React, TypeScript)
- **API:** FastAPI (Python)
- **Database:** Postgres (Docker)
- **CI/Security:** GitHub Actions + CodeQL + Dependabot (recommended)

## Repo structure
```text
resume-builder-ai/
  apps/web
  services/api
  docs
  .github/workflows
  docker-compose.yml
Quickstart
Prerequisites
Node.js 20+

Python 3.11+

Docker + Docker Compose (recommended for Postgres)

Do not commit .env files. Use the provided *.example templates.

Option A: Run with Docker Postgres + Local Web/API (recommended)
1) Start Postgres
From repo root:

bash

docker compose up -d db
2) Configure API env


bash

cp services/api/.env.example services/api/.env
3) Run the API
bash

cd services/api
python -m venv .venv
# macOS/Linux:
source .venv/bin/activate
# Windows PowerShell:
# .\.venv\Scripts\Activate.ps1

pip install -r requirements.txt
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
API health check:

bash

curl http://localhost:8000/health
4) Configure Web env
Copy:

bash

cp apps/web/.env.local.example apps/web/.env.local
5) Run the Web
bash
Copy code
cd apps/web
npm ci
npm run dev
Open:

Web: http://localhost:3000

API: http://localhost:8000

Option B: Run everything locally (no Docker)
You can install Postgres locally and set DATABASE_URL accordingly in services/api/.env.
Then follow the same API and Web steps above.

Environment variables
API: services/api/.env.example
env

# App
ENV=dev
LOG_LEVEL=INFO

# Database (Docker compose default)
DATABASE_URL=postgresql+psycopg://rba:rba@localhost:5432/rba

# LLM provider configuration (choose one approach)
LLM_PROVIDER=mock  # mock | openai

# If LLM_PROVIDER=openai (optional until you wire it)
OPENAI_API_KEY=
OPENAI_MODEL=
Web: apps/web/.env.local.example
env

# Next.js can access this at build/runtime
NEXT_PUBLIC_API_BASE_URL=http://localhost:8000
Security & privacy notes
Resumes often contain personally identifiable information. This project is designed with privacy-aware defaults:

Avoid logging raw resume/job text (store run IDs + metadata unless explicitly enabled)

Keep secrets in environment variables (never commit secrets)

Roadmap includes access control for stored artifacts and rate limiting for abuse prevention

Roadmap
Resume parsing into a stable schema (roles, achievements, skills, dates)

Bullet-to-evidence traceability (show which resume lines support each bullet)

Template system for multiple formats (one-page, multi-page, federal resume, CV)

Evaluation metrics (relevance, readability, truthfulness) + regression tests for prompt changes

Async job processing and caching for scale

yaml


---

## Optional (high-value): add a simple `Makefile` at repo root
If you want one-command ergonomics, create `Makefile`:

```makefile
.PHONY: db-up db-down api web

db-up:
	docker compose up -d db

db-down:
	docker compose down

api:
	cd services/api && uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

web:
	cd apps/web && npm run dev


DATABASE_URL formats
A) SQLAlchemy + psycopg (recommended MVP)

Use this when your SQLAlchemy URL looks like postgresql+psycopg://...

DATABASE_URL=postgresql+psycopg://USER:PASSWORD@HOST:5432/DBNAME


Example:

DATABASE_URL=postgresql+psycopg://rba:rba@localhost:5432/rba

B) SQLAlchemy async + asyncpg

Use this when you’re doing async engine:

DATABASE_URL=postgresql+asyncpg://USER:PASSWORD@HOST:5432/DBNAME


Example:

DATABASE_URL=postgresql+asyncpg://rba:rba@localhost:5432/rba

C) If you are NOT using SQLAlchemy (raw driver / other libs)

Some frameworks expect:

DATABASE_URL=postgresql://USER:PASSWORD@HOST:5432/DBNAME


Example:

DATABASE_URL=postgresql://rba:rba@localhost:5432/rba


Assumed MVP configuration (recommended)

API port: 8000

Postgres: user rba, password rba, db rba

Host/port: localhost:5432

Driver: psycopg (sync)

ORM: SQLAlchemy

services/api/.env.example
ENV=dev
LOG_LEVEL=INFO

DATABASE_URL=postgresql+psycopg://rba:rba@localhost:5432/rba

LLM_PROVIDER=mock
OPENAI_API_KEY=
OPENAI_MODEL=

Matching docker-compose.yml (root)
services:
  db:
    image: postgres:16
    environment:
      POSTGRES_USER: rba
      POSTGRES_PASSWORD: rba
      POSTGRES_DB: rba
    ports:
      - "5432:5432"
    volumes:
      - rba_pg:/var/lib/postgresql/data

volumes:
  rba_pg:

Matching Python dependencies

If you’re using SQLAlchemy sync with psycopg, your services/api/requirements.txt should include:

fastapi
uvicorn[standard]
sqlalchemy
psycopg[binary]


(You can add Alembic later when you introduce migrations.)

If you later switch to asyncpg

Only the URL changes:

DATABASE_URL=postgresql+asyncpg://rba:rba@localhost:5432/rba


…and you’d replace psycopg[binary] with:

asyncpg


1) Final DATABASE_URL (SQLAlchemy + psycopg, sync)

Use this in services/api/.env (and keep it in .env.example as shown):

DATABASE_URL=postgresql+psycopg://rba:rba@localhost:5432/rba

2) Matching docker-compose.yml (repo root)
services:
  db:
    image: postgres:16
    environment:
      POSTGRES_USER: rba
      POSTGRES_PASSWORD: rba
      POSTGRES_DB: rba
    ports:
      - "5432:5432"
    volumes:
      - rba_pg:/var/lib/postgresql/data

volumes:
  rba_pg:


Run DB:

docker compose up -d db

3) Matching services/api/requirements.txt
fastapi
uvicorn[standard]
sqlalchemy
psycopg[binary]
python-dotenv

4) FastAPI + SQLAlchemy DB wiring (copy/paste)
services/api/app/core/config.py
import os
from dotenv import load_dotenv

load_dotenv()

DATABASE_URL = os.getenv("DATABASE_URL", "")
if not DATABASE_URL:
    raise RuntimeError("DATABASE_URL is not set")

services/api/app/services/storage/db.py
from sqlalchemy import create_engine
from sqlalchemy.orm import sessionmaker, DeclarativeBase
from app.core.config import DATABASE_URL

engine = create_engine(DATABASE_URL, pool_pre_ping=True)

SessionLocal = sessionmaker(autocommit=False, autoflush=False, bind=engine)

class Base(DeclarativeBase):
    pass

def get_db():
    db = SessionLocal()
    try:
        yield db
    finally:
        db.close()

Optional: DB check endpoint (proves connectivity in interviews)

services/api/app/routes/health.py

from fastapi import APIRouter, Depends
from sqlalchemy.orm import Session
from sqlalchemy import text
from app.services.storage.db import get_db

router = APIRouter()

@router.get("/health")
def health(db: Session = Depends(get_db)):
    db.execute(text("SELECT 1"))
    return {"status": "ok", "db": "ok"}

5) Your .env.example (API)

services/api/.env.example

ENV=dev
LOG_LEVEL=INFO

DATABASE_URL=postgresql+psycopg://rba:rba@localhost:5432/rba

LLM_PROVIDER=mock
OPENAI_API_KEY=
OPENAI_MODEL=

6) When you’re ready to switch to asyncpg

Only change the URL + dependency set:

URL

DATABASE_URL=postgresql+asyncpg://rba:rba@localhost:5432/rba


Dependencies

remove psycopg[binary]

add asyncpg

and you’ll use SQLAlchemy’s async engine/session pattern (different code).


1) Root docker-compose.yml
services:
  db:
    image: postgres:16
    environment:
      POSTGRES_USER: rba
      POSTGRES_PASSWORD: rba
      POSTGRES_DB: rba
    ports:
      - "5432:5432"
    volumes:
      - rba_pg:/var/lib/postgresql/data

volumes:
  rba_pg:

2) API env template: services/api/.env.example
ENV=dev
LOG_LEVEL=INFO

# SQLAlchemy sync engine (psycopg)
DATABASE_URL=postgresql+psycopg://rba:rba@localhost:5432/rba

# LLM wiring (safe defaults for MVP)
LLM_PROVIDER=mock  # mock | openai
OPENAI_API_KEY=
OPENAI_MODEL=


Create your actual env file:

cp services/api/.env.example services/api/.env

3) Web env template: apps/web/.env.local.example
NEXT_PUBLIC_API_BASE_URL=http://localhost:8000


Create your actual env file:

cp apps/web/.env.local.example apps/web/.env.local

4) API dependencies: services/api/requirements.txt
fastapi
uvicorn[standard]
sqlalchemy
psycopg[binary]
python-dotenv

5) FastAPI DB wiring (SQLAlchemy sync + psycopg)
services/api/app/core/config.py
import os
from dotenv import load_dotenv

load_dotenv()

ENV = os.getenv("ENV", "dev")
LOG_LEVEL = os.getenv("LOG_LEVEL", "INFO")

DATABASE_URL = os.getenv("DATABASE_URL", "")
if not DATABASE_URL:
    raise RuntimeError("DATABASE_URL is not set (check services/api/.env)")

services/api/app/services/storage/db.py
from sqlalchemy import create_engine
from sqlalchemy.orm import sessionmaker, DeclarativeBase
from app.core.config import DATABASE_URL

engine = create_engine(
    DATABASE_URL,
    pool_pre_ping=True,
)

SessionLocal = sessionmaker(
    autocommit=False,
    autoflush=False,
    bind=engine,
)

class Base(DeclarativeBase):
    pass

def get_db():
    db = SessionLocal()
    try:
        yield db
    finally:
        db.close()

services/api/app/routes/health.py (includes DB connectivity)
from fastapi import APIRouter, Depends
from sqlalchemy.orm import Session
from sqlalchemy import text
from app.services.storage.db import get_db

router = APIRouter()

@router.get("/health")
def health(db: Session = Depends(get_db)):
    db.execute(text("SELECT 1"))
    return {"status": "ok", "db": "ok"}

services/api/app/main.py
from fastapi import FastAPI
from app.routes import health

app = FastAPI(title="Resume Builder AI API", version="0.1.0")

app.include_router(health.router, tags=["health"])


Ensure services/api/app/routes/__init__.py exists (can be empty), or import modules directly.

6) README “Quickstart” section (exact for your setup)

Paste this into your README.md under Quickstart:

## Quickstart

### Prerequisites
- Node.js 20+
- Python 3.11+
- Docker + Docker Compose

### 1) Start Postgres
From repo root:
```bash
docker compose up -d db

2) Configure API
cp services/api/.env.example services/api/.env
cd services/api
python -m venv .venv
# macOS/Linux:
source .venv/bin/activate
# Windows PowerShell:
# .\.venv\Scripts\Activate.ps1

pip install -r requirements.txt
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000


Health check:

curl http://localhost:8000/health

3) Configure Web
cp apps/web/.env.local.example apps/web/.env.local
cd apps/web
npm ci
npm run dev


Open:

Web: http://localhost:3000

API: http://localhost:8000


---

## 7) Optional: root `Makefile` (one-command ergonomics)
```makefile
.PHONY: db-up db-down api web

db-up:
	docker compose up -d db

db-down:
	docker compose down

api:
	cd services/api && uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

web:
	cd apps/web && npm run dev

8) Smoke test (verifies DB + API quickly)

Start DB:

docker compose up -d db


Run API and test:

curl http://localhost:8000/health


Expected:

{"status":"ok","db":"ok"}


1) Install Alembic

Update services/api/requirements.txt:

fastapi
uvicorn[standard]
sqlalchemy
psycopg[binary]
python-dotenv
alembic


Then:

cd services/api
pip install -r requirements.txt

2) Initialize Alembic folder

From services/api:

alembic init alembic


This creates:

services/api/alembic.ini

services/api/alembic/

env.py

script.py.mako

versions/

3) Configure alembic.ini

Open services/api/alembic.ini and set a placeholder URL (it will be overridden in env.py):

sqlalchemy.url = driver://user:pass@localhost/dbname


(Keep the rest as generated.)

4) Wire Alembic to your app’s DATABASE_URL + Base metadata
A) Ensure your Base exists (you already have this)

You previously used:

services/api/app/services/storage/db.py:

from sqlalchemy import create_engine
from sqlalchemy.orm import sessionmaker, DeclarativeBase
from app.core.config import DATABASE_URL

engine = create_engine(DATABASE_URL, pool_pre_ping=True)
SessionLocal = sessionmaker(autocommit=False, autoflush=False, bind=engine)

class Base(DeclarativeBase):
    pass


That’s good.

B) Add a single import point for all models (important for autogenerate)

Create:

services/api/app/models/__init__.py

# Import all SQLAlchemy models here so Alembic can discover them.
from app.models.tables import *  # noqa


Now create a models file (even if minimal) so your first migration generates real tables.

5) Add example tables (so migrations generate something)

Create:

services/api/app/models/tables.py

from sqlalchemy import String, Text, DateTime, func
from sqlalchemy.orm import Mapped, mapped_column
from app.services.storage.db import Base

class ResumeVersion(Base):
    __tablename__ = "resume_versions"

    id: Mapped[int] = mapped_column(primary_key=True)
    title: Mapped[str] = mapped_column(String(200), default="Untitled")
    raw_text: Mapped[str] = mapped_column(Text)
    created_at: Mapped[DateTime] = mapped_column(DateTime(timezone=True), server_default=func.now())

class JobPosting(Base):
    __tablename__ = "job_postings"

    id: Mapped[int] = mapped_column(primary_key=True)
    title: Mapped[str] = mapped_column(String(200), default="Job Posting")
    raw_text: Mapped[str] = mapped_column(Text)
    created_at: Mapped[DateTime] = mapped_column(DateTime(timezone=True), server_default=func.now())

class TailorRun(Base):
    __tablename__ = "tailor_runs"

    id: Mapped[int] = mapped_column(primary_key=True)
    resume_version_id: Mapped[int] = mapped_column()
    job_posting_id: Mapped[int] = mapped_column()
    prompt_version: Mapped[str] = mapped_column(String(50), default="v1")
    model_name: Mapped[str] = mapped_column(String(100), default="mock")
    output_json: Mapped[str] = mapped_column(Text)
    created_at: Mapped[DateTime] = mapped_column(DateTime(timezone=True), server_default=func.now())


Note: This is a starter schema you can refine later (FKs, indexes, JSON type, etc.). It’s sufficient for proving migrations end-to-end.

6) Replace Alembic env.py to load .env, set URL, and discover metadata

Replace services/api/alembic/env.py with this:

from logging.config import fileConfig
import os
import sys

from alembic import context
from sqlalchemy import engine_from_config, pool
from dotenv import load_dotenv

# --- Make "app" importable ---
# This file lives in services/api/alembic/env.py
# Add services/api to sys.path so "from app..." works.
sys.path.append(os.path.abspath(os.path.join(os.path.dirname(__file__), "..")))

# Load environment variables from services/api/.env
load_dotenv(os.path.join(os.path.dirname(__file__), "..", ".env"))

# Alembic Config object
config = context.config

# Configure Python logging
if config.config_file_name is not None:
    fileConfig(config.config_file_name)

# Import Base + models so autogenerate can see metadata
from app.services.storage.db import Base  # noqa: E402
import app.models  # noqa: E402  (imports app/models/__init__.py which imports tables)

target_metadata = Base.metadata

def get_database_url() -> str:
    url = os.getenv("DATABASE_URL", "")
    if not url:
        raise RuntimeError("DATABASE_URL is not set. Check services/api/.env")
    return url

def run_migrations_offline() -> None:
    url = get_database_url()
    context.configure(
        url=url,
        target_metadata=target_metadata,
        literal_binds=True,
        compare_type=True,
        dialect_opts={"paramstyle": "named"},
    )

    with context.begin_transaction():
        context.run_migrations()

def run_migrations_online() -> None:
    # Override sqlalchemy.url from env
    configuration = config.get_section(config.config_ini_section) or {}
    configuration["sqlalchemy.url"] = get_database_url()

    connectable = engine_from_config(
        configuration,
        prefix="sqlalchemy.",
        poolclass=pool.NullPool,
        future=True,
    )

    with connectable.connect() as connection:
        context.configure(
            connection=connection,
            target_metadata=target_metadata,
            compare_type=True,
        )

        with context.begin_transaction():
            context.run_migrations()

if context.is_offline_mode():
    run_migrations_offline()
else:
    run_migrations_online()


Key points:

Loads services/api/.env

Sets the DB URL dynamically

Imports app.models so Alembic sees all tables for autogenerate

compare_type=True helps detect column type changes

7) Create your first migration

Make sure Postgres is running:

# from repo root
docker compose up -d db


Then generate revision:

cd services/api
alembic revision --autogenerate -m "create core tables"


Apply it:

alembic upgrade head

8) Verify migrations worked

Connect to Postgres (optional) and check that these exist:

alembic_version

resume_versions

job_postings

tailor_runs

Or run your API /health and optionally add a DB query endpoint.

9) Common issues (fast fixes)

“ModuleNotFoundError: app”
Your sys.path in env.py is wrong. Ensure it appends services/api (the parent of app/).

Autogenerate creates empty migration
Alembic can’t see your models. Ensure app/models/__init__.py imports tables.py.

DATABASE_URL not loaded
Confirm services/api/.env exists and contains your postgresql+psycopg://... string.


1) Dependencies

Update services/api/requirements.txt:

fastapi
uvicorn[standard]
sqlalchemy
psycopg[binary]
python-dotenv
alembic


Install:

cd services/api
pip install -r requirements.txt

2) Models (FKs, JSONB, indexes, relationships)
services/api/app/models/tables.py
import uuid
from sqlalchemy import (
    String,
    Text,
    DateTime,
    ForeignKey,
    Integer,
    Numeric,
    Index,
    func,
    text,
)
from sqlalchemy.orm import Mapped, mapped_column, relationship
from sqlalchemy.dialects.postgresql import UUID, JSONB

from app.services.storage.db import Base


class ResumeVersion(Base):
    __tablename__ = "resume_versions"

    id: Mapped[uuid.UUID] = mapped_column(
        UUID(as_uuid=True),
        primary_key=True,
        server_default=text("gen_random_uuid()"),
    )

    title: Mapped[str] = mapped_column(String(200), default="Untitled", nullable=False)
    raw_text: Mapped[str] = mapped_column(Text, nullable=False)

    # Parsed/structured representation of resume (optional early; very useful later)
    parsed_json: Mapped[dict] = mapped_column(JSONB, nullable=False, default=dict)

    created_at: Mapped[DateTime] = mapped_column(
        DateTime(timezone=True), server_default=func.now(), nullable=False
    )
    updated_at: Mapped[DateTime] = mapped_column(
        DateTime(timezone=True), server_default=func.now(), onupdate=func.now(), nullable=False
    )

    tailor_runs: Mapped[list["TailorRun"]] = relationship(
        back_populates="resume_version",
        cascade="all, delete-orphan",
        passive_deletes=True,
    )


class JobPosting(Base):
    __tablename__ = "job_postings"

    id: Mapped[uuid.UUID] = mapped_column(
        UUID(as_uuid=True),
        primary_key=True,
        server_default=text("gen_random_uuid()"),
    )

    title: Mapped[str] = mapped_column(String(200), default="Job Posting", nullable=False)
    company: Mapped[str | None] = mapped_column(String(200), nullable=True)
    location: Mapped[str | None] = mapped_column(String(200), nullable=True)

    raw_text: Mapped[str] = mapped_column(Text, nullable=False)

    # Normalized/structured representation of job posting (optional early; very useful later)
    normalized_json: Mapped[dict] = mapped_column(JSONB, nullable=False, default=dict)

    created_at: Mapped[DateTime] = mapped_column(
        DateTime(timezone=True), server_default=func.now(), nullable=False
    )

    tailor_runs: Mapped[list["TailorRun"]] = relationship(
        back_populates="job_posting",
        cascade="all, delete-orphan",
        passive_deletes=True,
    )


class TailorRun(Base):
    __tablename__ = "tailor_runs"

    id: Mapped[uuid.UUID] = mapped_column(
        UUID(as_uuid=True),
        primary_key=True,
        server_default=text("gen_random_uuid()"),
    )

    resume_version_id: Mapped[uuid.UUID] = mapped_column(
        UUID(as_uuid=True),
        ForeignKey("resume_versions.id", ondelete="CASCADE"),
        nullable=False,
        index=True,
    )
    job_posting_id: Mapped[uuid.UUID] = mapped_column(
        UUID(as_uuid=True),
        ForeignKey("job_postings.id", ondelete="CASCADE"),
        nullable=False,
        index=True,
    )

    prompt_version: Mapped[str] = mapped_column(String(50), default="v1", nullable=False)
    llm_provider: Mapped[str] = mapped_column(String(50), default="mock", nullable=False)
    model_name: Mapped[str] = mapped_column(String(100), default="mock", nullable=False)

    # Store LLM output as JSONB (much better than TEXT)
    output_json: Mapped[dict] = mapped_column(JSONB, nullable=False, default=dict)

    # Optional telemetry (great for interviews + ops)
    prompt_tokens: Mapped[int | None] = mapped_column(Integer, nullable=True)
    completion_tokens: Mapped[int | None] = mapped_column(Integer, nullable=True)
    total_tokens: Mapped[int | None] = mapped_column(Integer, nullable=True)
    estimated_cost_usd: Mapped[float | None] = mapped_column(Numeric(10, 4), nullable=True)

    created_at: Mapped[DateTime] = mapped_column(
        DateTime(timezone=True), server_default=func.now(), nullable=False
    )

    resume_version: Mapped["ResumeVersion"] = relationship(back_populates="tailor_runs")
    job_posting: Mapped["JobPosting"] = relationship(back_populates="tailor_runs")

    artifacts: Mapped[list["Artifact"]] = relationship(
        back_populates="tailor_run",
        cascade="all, delete-orphan",
        passive_deletes=True,
    )


class Artifact(Base):
    __tablename__ = "artifacts"

    id: Mapped[uuid.UUID] = mapped_column(
        UUID(as_uuid=True),
        primary_key=True,
        server_default=text("gen_random_uuid()"),
    )

    tailor_run_id: Mapped[uuid.UUID] = mapped_column(
        UUID(as_uuid=True),
        ForeignKey("tailor_runs.id", ondelete="CASCADE"),
        nullable=False,
        index=True,
    )

    kind: Mapped[str] = mapped_column(String(50), default="docx", nullable=False)  # docx | pdf | json
    content_type: Mapped[str] = mapped_column(String(100), default="application/octet-stream", nullable=False)
    file_path: Mapped[str] = mapped_column(String(500), nullable=False)
    file_size_bytes: Mapped[int | None] = mapped_column(Integer, nullable=True)

    created_at: Mapped[DateTime] = mapped_column(
        DateTime(timezone=True), server_default=func.now(), nullable=False
    )

    tailor_run: Mapped["TailorRun"] = relationship(back_populates="artifacts")


# Helpful indexes (add/adjust as you learn usage patterns)
Index("ix_resume_versions_created_at", ResumeVersion.created_at)
Index("ix_job_postings_created_at", JobPosting.created_at)
Index("ix_tailor_runs_created_at", TailorRun.created_at)

# Optional: JSONB GIN indexes (good if you plan to query inside JSON)
# These can be heavy; include if you anticipate JSONB queries.
Index("ix_resume_versions_parsed_json_gin", ResumeVersion.parsed_json, postgresql_using="gin")
Index("ix_job_postings_normalized_json_gin", JobPosting.normalized_json, postgresql_using="gin")
Index("ix_tailor_runs_output_json_gin", TailorRun.output_json, postgresql_using="gin")

services/api/app/models/__init__.py
# Ensure Alembic discovers your models during autogenerate
from app.models.tables import *  # noqa

3) Alembic initialization

From services/api:

alembic init alembic

4) Alembic env.py (loads .env, imports models, better diffing)

Replace services/api/alembic/env.py with:

from logging.config import fileConfig
import os
import sys

from alembic import context
from sqlalchemy import engine_from_config, pool
from dotenv import load_dotenv

# Make "app" importable
sys.path.append(os.path.abspath(os.path.join(os.path.dirname(__file__), "..")))

# Load services/api/.env
load_dotenv(os.path.join(os.path.dirname(__file__), "..", ".env"))

config = context.config

if config.config_file_name is not None:
    fileConfig(config.config_file_name)

from app.services.storage.db import Base  # noqa: E402
import app.models  # noqa: E402  (imports app/models/__init__.py)

target_metadata = Base.metadata


def get_database_url() -> str:
    url = os.getenv("DATABASE_URL", "")
    if not url:
        raise RuntimeError("DATABASE_URL is not set. Check services/api/.env")
    return url


def run_migrations_offline() -> None:
    url = get_database_url()
    context.configure(
        url=url,
        target_metadata=target_metadata,
        literal_binds=True,
        compare_type=True,
        compare_server_default=True,
        dialect_opts={"paramstyle": "named"},
    )

    with context.begin_transaction():
        context.run_migrations()


def run_migrations_online() -> None:
    configuration = config.get_section(config.config_ini_section) or {}
    configuration["sqlalchemy.url"] = get_database_url()

    connectable = engine_from_config(
        configuration,
        prefix="sqlalchemy.",
        poolclass=pool.NullPool,
        future=True,
    )

    with connectable.connect() as connection:
        context.configure(
            connection=connection,
            target_metadata=target_metadata,
            compare_type=True,
            compare_server_default=True,
        )

        with context.begin_transaction():
            context.run_migrations()


if context.is_offline_mode():
    run_migrations_offline()
else:
    run_migrations_online()

5) Create a downgrade-safe “initial” migration (recommended)

Autogenerate is fine, but for your first migration, a manual deterministic migration is the most reliable.

A) Create an empty revision
cd services/api
alembic revision -m "initial schema"


This creates a file under services/api/alembic/versions/XXXXXXXX_initial_schema.py.

B) Replace the revision content with this

Open the generated file and replace everything inside with:

"""initial schema

Revision ID: <KEEP_YOURS>
Revises:
Create Date: <KEEP_YOURS>
"""

from alembic import op
import sqlalchemy as sa
from sqlalchemy.dialects import postgresql

# revision identifiers, used by Alembic.
revision = "<KEEP_YOURS>"
down_revision = None
branch_labels = None
depends_on = None


def upgrade() -> None:
    # UUID generation function
    op.execute("CREATE EXTENSION IF NOT EXISTS pgcrypto")

    op.create_table(
        "resume_versions",
        sa.Column("id", postgresql.UUID(as_uuid=True), primary_key=True, server_default=sa.text("gen_random_uuid()")),
        sa.Column("title", sa.String(length=200), nullable=False, server_default="Untitled"),
        sa.Column("raw_text", sa.Text(), nullable=False),
        sa.Column("parsed_json", postgresql.JSONB(astext_type=sa.Text()), nullable=False, server_default=sa.text("'{}'::jsonb")),
        sa.Column("created_at", sa.DateTime(timezone=True), nullable=False, server_default=sa.text("now()")),
        sa.Column("updated_at", sa.DateTime(timezone=True), nullable=False, server_default=sa.text("now()")),
    )
    op.create_index("ix_resume_versions_created_at", "resume_versions", ["created_at"])
    op.create_index("ix_resume_versions_parsed_json_gin", "resume_versions", ["parsed_json"], postgresql_using="gin")

    op.create_table(
        "job_postings",
        sa.Column("id", postgresql.UUID(as_uuid=True), primary_key=True, server_default=sa.text("gen_random_uuid()")),
        sa.Column("title", sa.String(length=200), nullable=False, server_default="Job Posting"),
        sa.Column("company", sa.String(length=200), nullable=True),
        sa.Column("location", sa.String(length=200), nullable=True),
        sa.Column("raw_text", sa.Text(), nullable=False),
        sa.Column("normalized_json", postgresql.JSONB(astext_type=sa.Text()), nullable=False, server_default=sa.text("'{}'::jsonb")),
        sa.Column("created_at", sa.DateTime(timezone=True), nullable=False, server_default=sa.text("now()")),
    )
    op.create_index("ix_job_postings_created_at", "job_postings", ["created_at"])
    op.create_index("ix_job_postings_normalized_json_gin", "job_postings", ["normalized_json"], postgresql_using="gin")

    op.create_table(
        "tailor_runs",
        sa.Column("id", postgresql.UUID(as_uuid=True), primary_key=True, server_default=sa.text("gen_random_uuid()")),
        sa.Column("resume_version_id", postgresql.UUID(as_uuid=True), nullable=False),
        sa.Column("job_posting_id", postgresql.UUID(as_uuid=True), nullable=False),
        sa.Column("prompt_version", sa.String(length=50), nullable=False, server_default="v1"),
        sa.Column("llm_provider", sa.String(length=50), nullable=False, server_default="mock"),
        sa.Column("model_name", sa.String(length=100), nullable=False, server_default="mock"),
        sa.Column("output_json", postgresql.JSONB(astext_type=sa.Text()), nullable=False, server_default=sa.text("'{}'::jsonb")),
        sa.Column("prompt_tokens", sa.Integer(), nullable=True),
        sa.Column("completion_tokens", sa.Integer(), nullable=True),
        sa.Column("total_tokens", sa.Integer(), nullable=True),
        sa.Column("estimated_cost_usd", sa.Numeric(10, 4), nullable=True),
        sa.Column("created_at", sa.DateTime(timezone=True), nullable=False, server_default=sa.text("now()")),
        sa.ForeignKeyConstraint(["resume_version_id"], ["resume_versions.id"], ondelete="CASCADE"),
        sa.ForeignKeyConstraint(["job_posting_id"], ["job_postings.id"], ondelete="CASCADE"),
    )
    op.create_index("ix_tailor_runs_created_at", "tailor_runs", ["created_at"])
    op.create_index("ix_tailor_runs_resume_version_id", "tailor_runs", ["resume_version_id"])
    op.create_index("ix_tailor_runs_job_posting_id", "tailor_runs", ["job_posting_id"])
    op.create_index("ix_tailor_runs_output_json_gin", "tailor_runs", ["output_json"], postgresql_using="gin")

    op.create_table(
        "artifacts",
        sa.Column("id", postgresql.UUID(as_uuid=True), primary_key=True, server_default=sa.text("gen_random_uuid()")),
        sa.Column("tailor_run_id", postgresql.UUID(as_uuid=True), nullable=False),
        sa.Column("kind", sa.String(length=50), nullable=False, server_default="docx"),
        sa.Column("content_type", sa.String(length=100), nullable=False, server_default="application/octet-stream"),
        sa.Column("file_path", sa.String(length=500), nullable=False),
        sa.Column("file_size_bytes", sa.Integer(), nullable=True),
        sa.Column("created_at", sa.DateTime(timezone=True), nullable=False, server_default=sa.text("now()")),
        sa.ForeignKeyConstraint(["tailor_run_id"], ["tailor_runs.id"], ondelete="CASCADE"),
    )
    op.create_index("ix_artifacts_tailor_run_id", "artifacts", ["tailor_run_id"])


def downgrade() -> None:
    # Drop in reverse dependency order (downgrade-safe)
    op.drop_index("ix_artifacts_tailor_run_id", table_name="artifacts")
    op.drop_table("artifacts")

    op.drop_index("ix_tailor_runs_output_json_gin", table_name="tailor_runs")
    op.drop_index("ix_tailor_runs_job_posting_id", table_name="tailor_runs")
    op.drop_index("ix_tailor_runs_resume_version_id", table_name="tailor_runs")
    op.drop_index("ix_tailor_runs_created_at", table_name="tailor_runs")
    op.drop_table("tailor_runs")

    op.drop_index("ix_job_postings_normalized_json_gin", table_name="job_postings")
    op.drop_index("ix_job_postings_created_at", table_name="job_postings")
    op.drop_table("job_postings")

    op.drop_index("ix_resume_versions_parsed_json_gin", table_name="resume_versions")
    op.drop_index("ix_resume_versions_created_at", table_name="resume_versions")
    op.drop_table("resume_versions")

    # Optional: keep extension (usually safe to leave installed).
    # If you want to remove it, do it last:
    # op.execute("DROP EXTENSION IF EXISTS pgcrypto")


Important: Keep your generated revision and Create Date header values; only replace the function bodies/content.

6) Apply migrations

Make sure DB is up:

# repo root
docker compose up -d db


Run upgrade:

cd services/api
alembic upgrade head

7) Add a README migration section (recommended)

Add this under your Quickstart:

### Migrations
Create a new migration:
```bash
cd services/api
alembic revision -m "your change"
# or if safe to autogenerate:
alembic revision --autogenerate -m "your change"


Apply migrations:

alembic upgrade head


Rollback one migration:

alembic downgrade -1


---

## 8) One operational tip (prevents 80% of Alembic issues)
Whenever you add a new SQLAlchemy model file, ensure it is imported by `app/models/__init__.py`. If Alembic can’t “see” it, `--autogenerate` will miss it.

---


1) Pydantic schemas (API contracts)
services/api/app/models/schemas.py
from __future__ import annotations

from pydantic import BaseModel, Field
from typing import Any, Optional
from uuid import UUID


# ---------- Resume ----------
class ResumeCreate(BaseModel):
    title: str = Field(default="Untitled", max_length=200)
    raw_text: str = Field(min_length=50)
    parsed_json: dict[str, Any] = Field(default_factory=dict)

class ResumeOut(BaseModel):
    id: UUID
    title: str
    raw_text: str
    parsed_json: dict[str, Any]

    class Config:
        from_attributes = True


# ---------- Job Posting ----------
class JobCreate(BaseModel):
    title: str = Field(default="Job Posting", max_length=200)
    company: Optional[str] = Field(default=None, max_length=200)
    location: Optional[str] = Field(default=None, max_length=200)
    raw_text: str = Field(min_length=50)
    normalized_json: dict[str, Any] = Field(default_factory=dict)

class JobOut(BaseModel):
    id: UUID
    title: str
    company: Optional[str] = None
    location: Optional[str] = None
    raw_text: str
    normalized_json: dict[str, Any]

    class Config:
        from_attributes = True


# ---------- Tailor ----------
class TailorRequest(BaseModel):
    resume_text: str = Field(min_length=50)
    job_text: str = Field(min_length=50)
    prompt_version: str = Field(default="v1", max_length=50)

class TailorRunOut(BaseModel):
    id: UUID
    resume_version_id: UUID
    job_posting_id: UUID
    prompt_version: str
    llm_provider: str
    model_name: str
    output_json: dict[str, Any]

    class Config:
        from_attributes = True


# ---------- Artifact ----------
class ArtifactOut(BaseModel):
    id: UUID
    tailor_run_id: UUID
    kind: str
    content_type: str
    file_path: str
    file_size_bytes: Optional[int] = None

    class Config:
        from_attributes = True

2) Repository layer (single place for DB operations)
services/api/app/services/storage/repos.py
from __future__ import annotations

from sqlalchemy.orm import Session
from sqlalchemy import select
from uuid import UUID

from app.models.tables import ResumeVersion, JobPosting, TailorRun, Artifact


class ResumeRepo:
    def create(self, db: Session, *, title: str, raw_text: str, parsed_json: dict) -> ResumeVersion:
        obj = ResumeVersion(title=title, raw_text=raw_text, parsed_json=parsed_json)
        db.add(obj)
        db.commit()
        db.refresh(obj)
        return obj

    def get(self, db: Session, resume_id: UUID) -> ResumeVersion | None:
        return db.get(ResumeVersion, resume_id)

    def list(self, db: Session, limit: int = 20, offset: int = 0) -> list[ResumeVersion]:
        stmt = select(ResumeVersion).order_by(ResumeVersion.created_at.desc()).limit(limit).offset(offset)
        return list(db.execute(stmt).scalars().all())


class JobRepo:
    def create(
        self,
        db: Session,
        *,
        title: str,
        company: str | None,
        location: str | None,
        raw_text: str,
        normalized_json: dict,
    ) -> JobPosting:
        obj = JobPosting(
            title=title,
            company=company,
            location=location,
            raw_text=raw_text,
            normalized_json=normalized_json,
        )
        db.add(obj)
        db.commit()
        db.refresh(obj)
        return obj

    def get(self, db: Session, job_id: UUID) -> JobPosting | None:
        return db.get(JobPosting, job_id)

    def list(self, db: Session, limit: int = 20, offset: int = 0) -> list[JobPosting]:
        stmt = select(JobPosting).order_by(JobPosting.created_at.desc()).limit(limit).offset(offset)
        return list(db.execute(stmt).scalars().all())


class TailorRunRepo:
    def create(
        self,
        db: Session,
        *,
        resume_version_id: UUID,
        job_posting_id: UUID,
        prompt_version: str,
        llm_provider: str,
        model_name: str,
        output_json: dict,
        prompt_tokens: int | None = None,
        completion_tokens: int | None = None,
        total_tokens: int | None = None,
        estimated_cost_usd: float | None = None,
    ) -> TailorRun:
        obj = TailorRun(
            resume_version_id=resume_version_id,
            job_posting_id=job_posting_id,
            prompt_version=prompt_version,
            llm_provider=llm_provider,
            model_name=model_name,
            output_json=output_json,
            prompt_tokens=prompt_tokens,
            completion_tokens=completion_tokens,
            total_tokens=total_tokens,
            estimated_cost_usd=estimated_cost_usd,
        )
        db.add(obj)
        db.commit()
        db.refresh(obj)
        return obj

    def get(self, db: Session, run_id: UUID) -> TailorRun | None:
        return db.get(TailorRun, run_id)

    def list(self, db: Session, limit: int = 20, offset: int = 0) -> list[TailorRun]:
        stmt = select(TailorRun).order_by(TailorRun.created_at.desc()).limit(limit).offset(offset)
        return list(db.execute(stmt).scalars().all())


class ArtifactRepo:
    def create(
        self,
        db: Session,
        *,
        tailor_run_id: UUID,
        kind: str,
        content_type: str,
        file_path: str,
        file_size_bytes: int | None = None,
    ) -> Artifact:
        obj = Artifact(
            tailor_run_id=tailor_run_id,
            kind=kind,
            content_type=content_type,
            file_path=file_path,
            file_size_bytes=file_size_bytes,
        )
        db.add(obj)
        db.commit()
        db.refresh(obj)
        return obj

    def list_for_run(self, db: Session, run_id: UUID) -> list[Artifact]:
        stmt = select(Artifact).where(Artifact.tailor_run_id == run_id).order_by(Artifact.created_at.desc())
        return list(db.execute(stmt).scalars().all())

3) Routes (CRUD + tailor run orchestration)
services/api/app/routes/resumes.py
from fastapi import APIRouter, Depends, HTTPException
from sqlalchemy.orm import Session
from uuid import UUID

from app.models.schemas import ResumeCreate, ResumeOut
from app.services.storage.db import get_db
from app.services.storage.repos import ResumeRepo

router = APIRouter()
repo = ResumeRepo()

@router.post("/resumes", response_model=ResumeOut)
def create_resume(payload: ResumeCreate, db: Session = Depends(get_db)):
    return repo.create(db, title=payload.title, raw_text=payload.raw_text, parsed_json=payload.parsed_json)

@router.get("/resumes/{resume_id}", response_model=ResumeOut)
def get_resume(resume_id: UUID, db: Session = Depends(get_db)):
    obj = repo.get(db, resume_id)
    if not obj:
        raise HTTPException(status_code=404, detail="Resume not found")
    return obj

@router.get("/resumes", response_model=list[ResumeOut])
def list_resumes(limit: int = 20, offset: int = 0, db: Session = Depends(get_db)):
    return repo.list(db, limit=limit, offset=offset)

services/api/app/routes/jobs.py
from fastapi import APIRouter, Depends, HTTPException
from sqlalchemy.orm import Session
from uuid import UUID

from app.models.schemas import JobCreate, JobOut
from app.services.storage.db import get_db
from app.services.storage.repos import JobRepo

router = APIRouter()
repo = JobRepo()

@router.post("/jobs", response_model=JobOut)
def create_job(payload: JobCreate, db: Session = Depends(get_db)):
    return repo.create(
        db,
        title=payload.title,
        company=payload.company,
        location=payload.location,
        raw_text=payload.raw_text,
        normalized_json=payload.normalized_json,
    )

@router.get("/jobs/{job_id}", response_model=JobOut)
def get_job(job_id: UUID, db: Session = Depends(get_db)):
    obj = repo.get(db, job_id)
    if not obj:
        raise HTTPException(status_code=404, detail="Job not found")
    return obj

@router.get("/jobs", response_model=list[JobOut])
def list_jobs(limit: int = 20, offset: int = 0, db: Session = Depends(get_db)):
    return repo.list(db, limit=limit, offset=offset)

4) Tailor route that persists resume/job + stores output

This is the “money endpoint” for demos.

services/api/app/routes/tailor.py
from fastapi import APIRouter, Depends
from sqlalchemy.orm import Session

from app.models.schemas import TailorRequest, TailorRunOut
from app.services.storage.db import get_db
from app.services.storage.repos import ResumeRepo, JobRepo, TailorRunRepo
from app.services.llm.mock import MockLLMClient

router = APIRouter()

resume_repo = ResumeRepo()
job_repo = JobRepo()
run_repo = TailorRunRepo()

llm = MockLLMClient()

@router.post("/tailor", response_model=TailorRunOut)
def tailor(payload: TailorRequest, db: Session = Depends(get_db)):
    # 1) Persist inputs (versioned)
    resume = resume_repo.create(db, title="Resume (auto)", raw_text=payload.resume_text, parsed_json={})
    job = job_repo.create(db, title="Job (auto)", company=None, location=None, raw_text=payload.job_text, normalized_json={})

    # 2) Run LLM (mock for now)
    system = "You are an evidence-first resume tailoring engine. Never invent experience."
    user = f"RESUME:\n{payload.resume_text}\n\nJOB:\n{payload.job_text}\n"
    output = llm.generate_json(system=system, user=user)

    # 3) Persist run output
    run = run_repo.create(
        db,
        resume_version_id=resume.id,
        job_posting_id=job.id,
        prompt_version=payload.prompt_version,
        llm_provider="mock",
        model_name="mock",
        output_json=output,
    )

    return run

5) Register routes in main.py
services/api/app/main.py
from fastapi import FastAPI
from app.routes import health, resumes, jobs, tailor

app = FastAPI(title="Resume Builder AI API", version="0.1.0")

app.include_router(health.router, tags=["health"])
app.include_router(resumes.router, prefix="/v1", tags=["resumes"])
app.include_router(jobs.router, prefix="/v1", tags=["jobs"])
app.include_router(tailor.router, prefix="/v1", tags=["tailor"])

6) Migrate + run

If you haven’t yet:

# root
docker compose up -d db

# services/api
alembic upgrade head
uvicorn app.main:app --reload --port 8000

7) Test quickly (curl)
curl http://localhost:8000/health


Tailor:

curl -X POST http://localhost:8000/v1/tailor \
  -H "Content-Type: application/json" \
  -d '{"resume_text":"Example resume text ...","job_text":"Example job text ...","prompt_version":"v1"}'


List runs (add this route if you want; repo already supports it):

You can easily add /v1/tailor-runs and /v1/tailor-runs/{id}.


1) Add dependency

Update services/api/requirements.txt:

python-docx


Then:

cd services/api
pip install -r requirements.txt

2) Config: artifact storage directory

Add to services/api/app/core/config.py:

import os
from pathlib import Path

# ... existing config ...

ARTIFACT_DIR = Path(os.getenv("ARTIFACT_DIR", "var/artifacts"))
ARTIFACT_DIR.mkdir(parents=True, exist_ok=True)


Optional: add to services/api/.env.example:

ARTIFACT_DIR=var/artifacts

3) Extend ArtifactRepo (get by id)

Update services/api/app/services/storage/repos.py (add this method inside ArtifactRepo):

from uuid import UUID

# ... existing ArtifactRepo ...

    def get(self, db: Session, artifact_id: UUID) -> Artifact | None:
        return db.get(Artifact, artifact_id)

4) DOCX exporter (service function)

Create services/api/app/services/export/docx_exporter.py:

from __future__ import annotations

from docx import Document
from typing import Any


def build_docx_from_tailor_output(output: dict[str, Any]) -> Document:
    """
    Builds a DOCX from the TailorRun.output_json schema.
    Expected keys (best-effort):
      - role_summary
      - tailored_bullets
      - ats_keywords_found
      - ats_keywords_missing
      - keyword_gaps
      - evidence_warnings
      - follow_up_questions
    """
    doc = Document()

    doc.add_heading("Resume Builder AI — Tailored Output", level=1)

    role_summary = output.get("role_summary")
    if role_summary:
        doc.add_heading("Role Summary", level=2)
        doc.add_paragraph(str(role_summary))

    def add_list_section(title: str, items: list[str] | None):
        if not items:
            return
        doc.add_heading(title, level=2)
        for item in items:
            doc.add_paragraph(str(item), style="List Bullet")

    add_list_section("Tailored Bullets", output.get("tailored_bullets"))
    add_list_section("ATS Keywords Found", output.get("ats_keywords_found"))
    add_list_section("ATS Keywords Missing", output.get("ats_keywords_missing"))
    add_list_section("Keyword Gaps", output.get("keyword_gaps"))
    add_list_section("Evidence Warnings", output.get("evidence_warnings"))
    add_list_section("Follow-up Questions", output.get("follow_up_questions"))

    return doc

5) Run list + run detail + artifact list routes

Create services/api/app/routes/runs.py:

from fastapi import APIRouter, Depends, HTTPException
from sqlalchemy.orm import Session
from uuid import UUID

from app.services.storage.db import get_db
from app.services.storage.repos import TailorRunRepo, ArtifactRepo
from app.models.schemas import TailorRunOut, ArtifactOut

router = APIRouter()
run_repo = TailorRunRepo()
artifact_repo = ArtifactRepo()


@router.get("/tailor-runs", response_model=list[TailorRunOut])
def list_runs(limit: int = 20, offset: int = 0, db: Session = Depends(get_db)):
    limit = min(max(limit, 1), 100)
    offset = max(offset, 0)
    return run_repo.list(db, limit=limit, offset=offset)


@router.get("/tailor-runs/{run_id}", response_model=TailorRunOut)
def get_run(run_id: UUID, db: Session = Depends(get_db)):
    run = run_repo.get(db, run_id)
    if not run:
        raise HTTPException(status_code=404, detail="Tailor run not found")
    return run


@router.get("/tailor-runs/{run_id}/artifacts", response_model=list[ArtifactOut])
def list_run_artifacts(run_id: UUID, db: Session = Depends(get_db)):
    run = run_repo.get(db, run_id)
    if not run:
        raise HTTPException(status_code=404, detail="Tailor run not found")
    return artifact_repo.list_for_run(db, run_id)

6) Export DOCX + download artifact routes

Create services/api/app/routes/export.py:

from __future__ import annotations

import os
from pathlib import Path
from uuid import UUID, uuid4

from fastapi import APIRouter, Depends, HTTPException
from fastapi.responses import FileResponse
from sqlalchemy.orm import Session

from app.core.config import ARTIFACT_DIR
from app.services.storage.db import get_db
from app.services.storage.repos import TailorRunRepo, ArtifactRepo
from app.services.export.docx_exporter import build_docx_from_tailor_output

router = APIRouter()

run_repo = TailorRunRepo()
artifact_repo = ArtifactRepo()


@router.post("/tailor-runs/{run_id}/export/docx")
def export_run_docx(run_id: UUID, db: Session = Depends(get_db)):
    run = run_repo.get(db, run_id)
    if not run:
        raise HTTPException(status_code=404, detail="Tailor run not found")

    # Build DOCX
    doc = build_docx_from_tailor_output(run.output_json or {})

    # Save to disk
    filename = f"{run_id}_{uuid4().hex}.docx"
    file_path = Path(ARTIFACT_DIR) / filename
    doc.save(str(file_path))

    size = os.path.getsize(file_path)

    # Persist artifact row
    artifact = artifact_repo.create(
        db,
        tailor_run_id=run.id,
        kind="docx",
        content_type="application/vnd.openxmlformats-officedocument.wordprocessingml.document",
        file_path=str(file_path),
        file_size_bytes=size,
    )

    return {
        "artifact_id": str(artifact.id),
        "tailor_run_id": str(run.id),
        "kind": artifact.kind,
        "content_type": artifact.content_type,
        "file_size_bytes": artifact.file_size_bytes,
        "download_url": f"/v1/artifacts/{artifact.id}/download",
    }


@router.get("/artifacts/{artifact_id}/download")
def download_artifact(artifact_id: UUID, db: Session = Depends(get_db)):
    artifact = artifact_repo.get(db, artifact_id)
    if not artifact:
        raise HTTPException(status_code=404, detail="Artifact not found")

    path = Path(artifact.file_path)
    if not path.exists():
        raise HTTPException(status_code=404, detail="Artifact file missing on disk")

    # FileResponse sets appropriate headers for download
    return FileResponse(
        path=str(path),
        media_type=artifact.content_type,
        filename=path.name,
    )

7) Register the new routes

Update services/api/app/main.py:

from fastapi import FastAPI
from app.routes import health, resumes, jobs, tailor, runs, export

app = FastAPI(title="Resume Builder AI API", version="0.1.0")

app.include_router(health.router, tags=["health"])
app.include_router(resumes.router, prefix="/v1", tags=["resumes"])
app.include_router(jobs.router, prefix="/v1", tags=["jobs"])
app.include_router(tailor.router, prefix="/v1", tags=["tailor"])

# NEW
app.include_router(runs.router, prefix="/v1", tags=["runs"])
app.include_router(export.router, prefix="/v1", tags=["export"])

8) Quick test (curl)

Create a run (your existing /v1/tailor endpoint):

curl -X POST http://localhost:8000/v1/tailor \
  -H "Content-Type: application/json" \
  -d '{"resume_text":"Example resume text ...","job_text":"Example job text ...","prompt_version":"v1"}'


List runs:

curl http://localhost:8000/v1/tailor-runs


Export DOCX (replace <RUN_ID>):

curl -X POST http://localhost:8000/v1/tailor-runs/<RUN_ID>/export/docx


Download artifact (replace <ARTIFACT_ID>):

curl -L -o tailored.docx http://localhost:8000/v1/artifacts/<ARTIFACT_ID>/download


0) Dependencies (add PDF support)

Update services/api/requirements.txt:

python-docx
reportlab


Then:

cd services/api
pip install -r requirements.txt

1) Auth-ready user scoping (dependency)

Create services/api/app/core/security.py:

from __future__ import annotations

from fastapi import Header
from uuid import UUID

# Fixed demo user for local/dev if header not supplied
DEMO_USER_ID = UUID("00000000-0000-0000-0000-000000000001")

def get_current_user_id(x_user_id: str | None = Header(default=None, alias="X-User-Id")) -> UUID:
    """
    Auth-ready placeholder:
    - In MVP/dev: accept X-User-Id header OR default to DEMO_USER_ID.
    - Later: replace with JWT verification and return the authenticated user's UUID.
    """
    if not x_user_id:
        return DEMO_USER_ID
    return UUID(x_user_id)


Usage: every route scopes reads/writes to this UUID.

2) Model updates: add user_id + deleted_at

Update your SQLAlchemy tables in services/api/app/models/tables.py:

A) Add these imports (if not already present)
from sqlalchemy import DateTime
from sqlalchemy.dialects.postgresql import UUID
from sqlalchemy import ForeignKey
from sqlalchemy.orm import Mapped, mapped_column
from sqlalchemy import func
import uuid

B) Add user_id + deleted_at columns to each table

Add to ResumeVersion, JobPosting, TailorRun, Artifact:

user_id: Mapped[uuid.UUID] = mapped_column(UUID(as_uuid=True), nullable=False, index=True)

deleted_at: Mapped[DateTime | None] = mapped_column(DateTime(timezone=True), nullable=True, index=True)


Example (ResumeVersion excerpt):

class ResumeVersion(Base):
    __tablename__ = "resume_versions"

    # ... existing columns ...

    user_id: Mapped[uuid.UUID] = mapped_column(UUID(as_uuid=True), nullable=False, index=True)
    deleted_at: Mapped[DateTime | None] = mapped_column(DateTime(timezone=True), nullable=True, index=True)


Do the same for JobPosting, TailorRun, Artifact.

C) Add stable ordering indexes (recommended)

Add indexes to support the list queries:

from sqlalchemy import Index

Index("ix_resume_versions_user_created", ResumeVersion.user_id, ResumeVersion.created_at.desc(), ResumeVersion.id.desc())
Index("ix_job_postings_user_created", JobPosting.user_id, JobPosting.created_at.desc(), JobPosting.id.desc())
Index("ix_tailor_runs_user_created", TailorRun.user_id, TailorRun.created_at.desc(), TailorRun.id.desc())
Index("ix_artifacts_user_created", Artifact.user_id, Artifact.created_at.desc(), Artifact.id.desc())

3) Migration: add users + user_id + soft deletes

Create a new Alembic revision:

cd services/api
alembic revision -m "add user scoping and soft deletes"


Replace the body of the new revision file with the following (keep your revision header IDs):

from alembic import op
import sqlalchemy as sa
from sqlalchemy.dialects import postgresql

DEMO_USER_ID = "00000000-0000-0000-0000-000000000001"

def upgrade() -> None:
    # Create users table (minimal; auth-ready)
    op.create_table(
        "users",
        sa.Column("id", postgresql.UUID(as_uuid=True), primary_key=True),
        sa.Column("created_at", sa.DateTime(timezone=True), nullable=False, server_default=sa.text("now()")),
    )

    # Ensure demo user exists for backfill
    op.execute(f"INSERT INTO users (id) VALUES ('{DEMO_USER_ID}') ON CONFLICT DO NOTHING")

    # Add user_id + deleted_at to existing tables (nullable first for backfill)
    for table in ("resume_versions", "job_postings", "tailor_runs", "artifacts"):
        op.add_column(table, sa.Column("user_id", postgresql.UUID(as_uuid=True), nullable=True))
        op.add_column(table, sa.Column("deleted_at", sa.DateTime(timezone=True), nullable=True))

        op.create_index(f"ix_{table}_user_id", table, ["user_id"])
        op.create_index(f"ix_{table}_deleted_at", table, ["deleted_at"])

        # Backfill existing rows to demo user (dev safety)
        op.execute(f"UPDATE {table} SET user_id = '{DEMO_USER_ID}' WHERE user_id IS NULL")

        # Set NOT NULL after backfill
        op.alter_column(table, "user_id", nullable=False)

    # Add stable ordering indexes (user_id + created_at + id)
    op.create_index(
        "ix_resume_versions_user_created", "resume_versions",
        ["user_id", sa.text("created_at DESC"), sa.text("id DESC")]
    )
    op.create_index(
        "ix_job_postings_user_created", "job_postings",
        ["user_id", sa.text("created_at DESC"), sa.text("id DESC")]
    )
    op.create_index(
        "ix_tailor_runs_user_created", "tailor_runs",
        ["user_id", sa.text("created_at DESC"), sa.text("id DESC")]
    )
    op.create_index(
        "ix_artifacts_user_created", "artifacts",
        ["user_id", sa.text("created_at DESC"), sa.text("id DESC")]
    )

def downgrade() -> None:
    # Drop indexes + columns in reverse
    for name, table in (
        ("ix_artifacts_user_created", "artifacts"),
        ("ix_tailor_runs_user_created", "tailor_runs"),
        ("ix_job_postings_user_created", "job_postings"),
        ("ix_resume_versions_user_created", "resume_versions"),
    ):
        op.drop_index(name, table_name=table)

    for table in ("artifacts", "tailor_runs", "job_postings", "resume_versions"):
        op.drop_index(f"ix_{table}_deleted_at", table_name=table)
        op.drop_index(f"ix_{table}_user_id", table_name=table)
        op.drop_column(table, "deleted_at")
        op.drop_column(table, "user_id")

    op.drop_table("users")


Apply it:

alembic upgrade head

4) PII minimization: list schemas without raw_text

Update services/api/app/models/schemas.py by adding summary outputs (no raw_text) and shared pagination models:

from pydantic import BaseModel
from typing import Any, Optional
from uuid import UUID
from datetime import datetime

class PaginationMeta(BaseModel):
    limit: int
    offset: int
    total: int
    has_more: bool
    next_offset: int | None

# --- Resume ---
class ResumeSummaryOut(BaseModel):
    id: UUID
    title: str
    created_at: datetime
    updated_at: datetime

    class Config:
        from_attributes = True

class ResumeOut(ResumeSummaryOut):
    raw_text: str
    parsed_json: dict[str, Any]

# --- Job ---
class JobSummaryOut(BaseModel):
    id: UUID
    title: str
    company: Optional[str] = None
    location: Optional[str] = None
    created_at: datetime

    class Config:
        from_attributes = True

class JobOut(JobSummaryOut):
    raw_text: str
    normalized_json: dict[str, Any]

# --- Runs ---
class TailorRunSummaryOut(BaseModel):
    id: UUID
    resume_version_id: UUID
    job_posting_id: UUID
    prompt_version: str
    llm_provider: str
    model_name: str
    created_at: datetime

    class Config:
        from_attributes = True

class TailorRunOut(TailorRunSummaryOut):
    output_json: dict[str, Any]

# --- Artifacts ---
class ArtifactOut(BaseModel):
    id: UUID
    tailor_run_id: UUID
    kind: str
    content_type: str
    file_size_bytes: int | None = None
    created_at: datetime

    class Config:
        from_attributes = True

# --- Paginated responses ---
class ResumeListResponse(BaseModel):
    items: list[ResumeSummaryOut]
    meta: PaginationMeta

class JobListResponse(BaseModel):
    items: list[JobSummaryOut]
    meta: PaginationMeta

class RunListResponse(BaseModel):
    items: list[TailorRunSummaryOut]
    meta: PaginationMeta

5) Repository layer: enforce user scoping + soft delete filtering

Update services/api/app/services/storage/repos.py to:

require user_id

filter deleted_at IS NULL

add list totals

Example: ResumeRepo (pattern applies to all)
from sqlalchemy import select, func as sa_func
from uuid import UUID
from sqlalchemy.orm import Session
from app.models.tables import ResumeVersion

class ResumeRepo:
    def create(self, db: Session, *, user_id: UUID, title: str, raw_text: str, parsed_json: dict) -> ResumeVersion:
        obj = ResumeVersion(user_id=user_id, title=title, raw_text=raw_text, parsed_json=parsed_json)
        db.add(obj)
        db.commit()
        db.refresh(obj)
        return obj

    def get(self, db: Session, *, user_id: UUID, resume_id: UUID) -> ResumeVersion | None:
        stmt = select(ResumeVersion).where(
            ResumeVersion.id == resume_id,
            ResumeVersion.user_id == user_id,
            ResumeVersion.deleted_at.is_(None),
        )
        return db.execute(stmt).scalar_one_or_none()

    def list(self, db: Session, *, user_id: UUID, limit: int = 20, offset: int = 0):
        base = select(ResumeVersion).where(
            ResumeVersion.user_id == user_id,
            ResumeVersion.deleted_at.is_(None),
        )

        total = db.execute(select(sa_func.count()).select_from(base.subquery())).scalar_one()

        stmt = base.order_by(ResumeVersion.created_at.desc(), ResumeVersion.id.desc()).limit(limit).offset(offset)
        items = list(db.execute(stmt).scalars().all())
        return items, total

    def soft_delete(self, db: Session, *, user_id: UUID, resume_id: UUID) -> bool:
        obj = self.get(db, user_id=user_id, resume_id=resume_id)
        if not obj:
            return False
        obj.deleted_at = sa_func.now()
        db.commit()
        return True


Apply the same pattern to JobRepo, TailorRunRepo, ArtifactRepo:

include user_id column on create

filter by user_id and deleted_at is null on get/list

For artifacts, add soft_delete() and hard_delete() (see DELETE endpoints below).

6) Routes updates: scope by user + PII-safe list responses + pagination meta
A) Resumes list returns summaries only

Update routes/resumes.py:

from fastapi import APIRouter, Depends, HTTPException
from sqlalchemy.orm import Session
from uuid import UUID

from app.core.security import get_current_user_id
from app.services.storage.db import get_db
from app.services.storage.repos import ResumeRepo
from app.models.schemas import ResumeCreate, ResumeOut, ResumeListResponse, PaginationMeta, ResumeSummaryOut

router = APIRouter()
repo = ResumeRepo()

@router.post("/resumes", response_model=ResumeOut)
def create_resume(payload: ResumeCreate, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    return repo.create(db, user_id=user_id, title=payload.title, raw_text=payload.raw_text, parsed_json=payload.parsed_json)

@router.get("/resumes/{resume_id}", response_model=ResumeOut)
def get_resume(resume_id: UUID, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    obj = repo.get(db, user_id=user_id, resume_id=resume_id)
    if not obj:
        raise HTTPException(status_code=404, detail="Resume not found")
    return obj

@router.get("/resumes", response_model=ResumeListResponse)
def list_resumes(limit: int = 20, offset: int = 0, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    limit = min(max(limit, 1), 100)
    offset = max(offset, 0)
    items, total = repo.list(db, user_id=user_id, limit=limit, offset=offset)
    has_more = (offset + limit) < total
    return {
        "items": [ResumeSummaryOut.model_validate(i) for i in items],
        "meta": PaginationMeta(limit=limit, offset=offset, total=total, has_more=has_more, next_offset=(offset + limit if has_more else None)),
    }

@router.delete("/resumes/{resume_id}")
def delete_resume(resume_id: UUID, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    ok = repo.soft_delete(db, user_id=user_id, resume_id=resume_id)
    if not ok:
        raise HTTPException(status_code=404, detail="Resume not found")
    return {"status": "deleted"}


Repeat this approach for jobs.py and runs.py:

list endpoints return SummaryOut

include meta

7) Run list + run detail (scoped + soft delete)

Update routes/runs.py to:

list returns RunListResponse

detail returns TailorRunOut (includes output_json)

Add a run delete endpoint:

@router.delete("/tailor-runs/{run_id}")
def delete_run(run_id: UUID, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    ok = run_repo.soft_delete(db, user_id=user_id, run_id=run_id)
    if not ok:
        raise HTTPException(status_code=404, detail="Tailor run not found")
    return {"status": "deleted"}


(Implement TailorRunRepo.soft_delete() similar to ResumeRepo.)

8) Export DOCX + PDF and persist Artifact rows (scoped)
A) Exporter: PDF

Create services/api/app/services/export/pdf_exporter.py:

from __future__ import annotations

from io import BytesIO
from typing import Any
from reportlab.pdfgen import canvas
from reportlab.lib.pagesizes import LETTER

def build_pdf_bytes_from_tailor_output(output: dict[str, Any]) -> bytes:
    buf = BytesIO()
    c = canvas.Canvas(buf, pagesize=LETTER)
    width, height = LETTER

    y = height - 72
    c.setFont("Helvetica-Bold", 14)
    c.drawString(72, y, "Resume Builder AI — Tailored Output")
    y -= 28

    def draw_section(title: str, items: list[str] | None):
        nonlocal y
        if not items:
            return
        c.setFont("Helvetica-Bold", 12)
        c.drawString(72, y, title)
        y -= 18
        c.setFont("Helvetica", 10)
        for item in items:
            # simple wrap behavior
            text = f"• {str(item)}"
            if y < 72:
                c.showPage()
                y = height - 72
                c.setFont("Helvetica", 10)
            c.drawString(78, y, text[:120])  # MVP: truncate; can implement wrapping later
            y -= 14
        y -= 10

    role_summary = output.get("role_summary")
    if role_summary:
        c.setFont("Helvetica-Bold", 12)
        c.drawString(72, y, "Role Summary")
        y -= 18
        c.setFont("Helvetica", 10)
        c.drawString(72, y, str(role_summary)[:140])
        y -= 24

    draw_section("Tailored Bullets", output.get("tailored_bullets"))
    draw_section("ATS Keywords Found", output.get("ats_keywords_found"))
    draw_section("ATS Keywords Missing", output.get("ats_keywords_missing"))
    draw_section("Keyword Gaps", output.get("keyword_gaps"))
    draw_section("Evidence Warnings", output.get("evidence_warnings"))
    draw_section("Follow-up Questions", output.get("follow_up_questions"))

    c.save()
    return buf.getvalue()

B) Export routes: add PDF endpoint + scope and user_id

Update routes/export.py:

Ensure you pass user_id into artifact creation

Add:

@router.post("/tailor-runs/{run_id}/export/pdf")
def export_run_pdf(run_id: UUID, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    run = run_repo.get(db, user_id=user_id, run_id=run_id)
    if not run:
        raise HTTPException(status_code=404, detail="Tailor run not found")

    pdf_bytes = build_pdf_bytes_from_tailor_output(run.output_json or {})

    filename = f"{run_id}_{uuid4().hex}.pdf"
    file_path = Path(ARTIFACT_DIR) / filename
    file_path.write_bytes(pdf_bytes)

    size = file_path.stat().st_size

    artifact = artifact_repo.create(
        db,
        user_id=user_id,
        tailor_run_id=run.id,
        kind="pdf",
        content_type="application/pdf",
        file_path=str(file_path),
        file_size_bytes=size,
    )

    return {
        "artifact_id": str(artifact.id),
        "download_url": f"/v1/artifacts/{artifact.id}/download",
    }


(You will need to update ArtifactRepo.create() to accept user_id and persist it.)

9) DELETE endpoints: artifact cleanup + optional hard delete and file purge

Add to routes/export.py:

@router.delete("/artifacts/{artifact_id}")
def delete_artifact(
    artifact_id: UUID,
    hard: bool = False,
    purge_file: bool = True,
    db: Session = Depends(get_db),
    user_id: UUID = Depends(get_current_user_id),
):
    artifact = artifact_repo.get(db, user_id=user_id, artifact_id=artifact_id)
    if not artifact:
        raise HTTPException(status_code=404, detail="Artifact not found")

    # optionally delete file on disk
    if purge_file:
        path = Path(artifact.file_path)
        if path.exists():
            path.unlink()

    if hard:
        artifact_repo.hard_delete(db, user_id=user_id, artifact_id=artifact_id)
        return {"status": "hard_deleted"}

    artifact_repo.soft_delete(db, user_id=user_id, artifact_id=artifact_id)
    return {"status": "deleted"}


Repository methods you’ll add to ArtifactRepo:

get(db, user_id, artifact_id) filtered by user + not deleted

soft_delete(...) sets deleted_at = now()

hard_delete(...) does db.delete(obj)

10) Update the “tailor” orchestration to store user_id everywhere

In routes/tailor.py, change create calls:

resume = resume_repo.create(db, user_id=user_id, title="Resume (auto)", raw_text=payload.resume_text, parsed_json={})
job = job_repo.create(db, user_id=user_id, title="Job (auto)", company=None, location=None, raw_text=payload.job_text, normalized_json={})
run = run_repo.create(db, user_id=user_id, resume_version_id=resume.id, job_posting_id=job.id, ...)


And ensure TailorRunRepo.create() / JobRepo.create() / ResumeRepo.create() accept and persist user_id.

11) Test quickly (curl)

Use default demo user (no header), or set a specific user:

curl -H "X-User-Id: 00000000-0000-0000-0000-000000000001" http://localhost:8000/v1/tailor-runs


Export DOCX:

curl -X POST http://localhost:8000/v1/tailor-runs/<RUN_ID>/export/docx


Export PDF:

curl -X POST http://localhost:8000/v1/tailor-runs/<RUN_ID>/export/pdf


Delete artifact:

curl -X DELETE "http://localhost:8000/v1/artifacts/<ARTIFACT_ID>?hard=false&purge_file=true"


1) Add auth-ready user scoping
services/api/app/core/security.py
from __future__ import annotations

from fastapi import Header
from uuid import UUID

# Dev/demo default user (replace later with JWT-authenticated user id)
DEMO_USER_ID = UUID("00000000-0000-0000-0000-000000000001")

def get_current_user_id(x_user_id: str | None = Header(default=None, alias="X-User-Id")) -> UUID:
    """
    MVP auth-ready dependency.
    - If X-User-Id header is present, use it.
    - Otherwise, default to a stable demo user.
    Later: replace this with JWT verification and return the authenticated user's UUID.
    """
    if not x_user_id:
        return DEMO_USER_ID
    return UUID(x_user_id)

2) Update models: add user_id and deleted_at

In services/api/app/models/tables.py, add two columns to each table (ResumeVersion, JobPosting, TailorRun, Artifact):

import uuid
from sqlalchemy import DateTime
from sqlalchemy.dialects.postgresql import UUID
from sqlalchemy.orm import Mapped, mapped_column
from sqlalchemy import func


Then in each class:

user_id: Mapped[uuid.UUID] = mapped_column(UUID(as_uuid=True), nullable=False, index=True)
deleted_at: Mapped[DateTime | None] = mapped_column(DateTime(timezone=True), nullable=True, index=True)


Example (add inside each table class):

user_id: Mapped[uuid.UUID] = mapped_column(UUID(as_uuid=True), nullable=False, index=True)
deleted_at: Mapped[DateTime | None] = mapped_column(DateTime(timezone=True), nullable=True, index=True)


You do not need to add relationships for this hardening step; it’s purely scoping/filtering.

3) Migration: users + user_id + soft deletes + indexes

Create the revision:

cd services/api
alembic revision -m "add user scoping and soft deletes"


Replace the upgrade/downgrade bodies with the following (keep your revision header IDs as-is):

from alembic import op
import sqlalchemy as sa
from sqlalchemy.dialects import postgresql

DEMO_USER_ID = "00000000-0000-0000-0000-000000000001"

def upgrade() -> None:
    # Create users table (auth-ready placeholder)
    op.create_table(
        "users",
        sa.Column("id", postgresql.UUID(as_uuid=True), primary_key=True),
        sa.Column("created_at", sa.DateTime(timezone=True), nullable=False, server_default=sa.text("now()")),
    )

    # Ensure demo user exists for backfill
    op.execute(f"INSERT INTO users (id) VALUES ('{DEMO_USER_ID}') ON CONFLICT DO NOTHING")

    # Add columns to existing tables (nullable -> backfill -> set NOT NULL for user_id)
    for table in ("resume_versions", "job_postings", "tailor_runs", "artifacts"):
        op.add_column(table, sa.Column("user_id", postgresql.UUID(as_uuid=True), nullable=True))
        op.add_column(table, sa.Column("deleted_at", sa.DateTime(timezone=True), nullable=True))

        op.create_index(f"ix_{table}_user_id", table, ["user_id"])
        op.create_index(f"ix_{table}_deleted_at", table, ["deleted_at"])

        op.execute(f"UPDATE {table} SET user_id = '{DEMO_USER_ID}' WHERE user_id IS NULL")
        op.alter_column(table, "user_id", nullable=False)

    # Stable ordering indexes (Postgres-specific; deterministic ordering)
    op.execute("""
      CREATE INDEX IF NOT EXISTS ix_resume_versions_user_created
      ON resume_versions (user_id, created_at DESC, id DESC)
    """)
    op.execute("""
      CREATE INDEX IF NOT EXISTS ix_job_postings_user_created
      ON job_postings (user_id, created_at DESC, id DESC)
    """)
    op.execute("""
      CREATE INDEX IF NOT EXISTS ix_tailor_runs_user_created
      ON tailor_runs (user_id, created_at DESC, id DESC)
    """)
    op.execute("""
      CREATE INDEX IF NOT EXISTS ix_artifacts_user_created
      ON artifacts (user_id, created_at DESC, id DESC)
    """)

def downgrade() -> None:
    # Drop composite indexes
    op.execute("DROP INDEX IF EXISTS ix_artifacts_user_created")
    op.execute("DROP INDEX IF EXISTS ix_tailor_runs_user_created")
    op.execute("DROP INDEX IF EXISTS ix_job_postings_user_created")
    op.execute("DROP INDEX IF EXISTS ix_resume_versions_user_created")

    # Drop per-table indexes + columns
    for table in ("artifacts", "tailor_runs", "job_postings", "resume_versions"):
        op.drop_index(f"ix_{table}_deleted_at", table_name=table)
        op.drop_index(f"ix_{table}_user_id", table_name=table)
        op.drop_column(table, "deleted_at")
        op.drop_column(table, "user_id")

    op.drop_table("users")


Apply it:

alembic upgrade head

4) Pydantic schemas: summary vs detail + pagination metadata
Replace services/api/app/models/schemas.py with:
from __future__ import annotations

from pydantic import BaseModel, Field
from typing import Any, Optional
from uuid import UUID
from datetime import datetime


# ---------- Pagination ----------
class PaginationMeta(BaseModel):
    limit: int
    offset: int
    total: int
    has_more: bool
    next_offset: int | None


# ---------- Resume ----------
class ResumeCreate(BaseModel):
    title: str = Field(default="Untitled", max_length=200)
    raw_text: str = Field(min_length=50)
    parsed_json: dict[str, Any] = Field(default_factory=dict)

class ResumeSummaryOut(BaseModel):
    id: UUID
    title: str
    created_at: datetime
    updated_at: datetime

    class Config:
        from_attributes = True

class ResumeOut(ResumeSummaryOut):
    raw_text: str
    parsed_json: dict[str, Any]

class ResumeListResponse(BaseModel):
    items: list[ResumeSummaryOut]
    meta: PaginationMeta


# ---------- Job Posting ----------
class JobCreate(BaseModel):
    title: str = Field(default="Job Posting", max_length=200)
    company: Optional[str] = Field(default=None, max_length=200)
    location: Optional[str] = Field(default=None, max_length=200)
    raw_text: str = Field(min_length=50)
    normalized_json: dict[str, Any] = Field(default_factory=dict)

class JobSummaryOut(BaseModel):
    id: UUID
    title: str
    company: Optional[str] = None
    location: Optional[str] = None
    created_at: datetime

    class Config:
        from_attributes = True

class JobOut(JobSummaryOut):
    raw_text: str
    normalized_json: dict[str, Any]

class JobListResponse(BaseModel):
    items: list[JobSummaryOut]
    meta: PaginationMeta


# ---------- Tailor ----------
class TailorRequest(BaseModel):
    resume_text: str = Field(min_length=50)
    job_text: str = Field(min_length=50)
    prompt_version: str = Field(default="v1", max_length=50)

class TailorRunSummaryOut(BaseModel):
    id: UUID
    resume_version_id: UUID
    job_posting_id: UUID
    prompt_version: str
    llm_provider: str
    model_name: str
    created_at: datetime

    class Config:
        from_attributes = True

class TailorRunOut(TailorRunSummaryOut):
    output_json: dict[str, Any]

class RunListResponse(BaseModel):
    items: list[TailorRunSummaryOut]
    meta: PaginationMeta


# ---------- Artifacts ----------
class ArtifactOut(BaseModel):
    id: UUID
    tailor_run_id: UUID
    kind: str
    content_type: str
    file_size_bytes: int | None = None
    created_at: datetime

    class Config:
        from_attributes = True

5) Repository layer: enforce user scoping + deleted filtering + totals
Replace services/api/app/services/storage/repos.py with:
from __future__ import annotations

from uuid import UUID
from sqlalchemy.orm import Session
from sqlalchemy import select, func as sa_func, update

from app.models.tables import ResumeVersion, JobPosting, TailorRun, Artifact


def _count_from_select(db: Session, stmt):
    subq = stmt.subquery()
    return db.execute(select(sa_func.count()).select_from(subq)).scalar_one()


class ResumeRepo:
    def create(self, db: Session, *, user_id: UUID, title: str, raw_text: str, parsed_json: dict) -> ResumeVersion:
        obj = ResumeVersion(user_id=user_id, title=title, raw_text=raw_text, parsed_json=parsed_json)
        db.add(obj)
        db.commit()
        db.refresh(obj)
        return obj

    def get(self, db: Session, *, user_id: UUID, resume_id: UUID) -> ResumeVersion | None:
        stmt = select(ResumeVersion).where(
            ResumeVersion.id == resume_id,
            ResumeVersion.user_id == user_id,
            ResumeVersion.deleted_at.is_(None),
        )
        return db.execute(stmt).scalar_one_or_none()

    def list(self, db: Session, *, user_id: UUID, limit: int, offset: int):
        base = select(ResumeVersion).where(
            ResumeVersion.user_id == user_id,
            ResumeVersion.deleted_at.is_(None),
        )
        total = _count_from_select(db, base)
        stmt = base.order_by(ResumeVersion.created_at.desc(), ResumeVersion.id.desc()).limit(limit).offset(offset)
        items = list(db.execute(stmt).scalars().all())
        return items, total

    def soft_delete(self, db: Session, *, user_id: UUID, resume_id: UUID) -> bool:
        obj = self.get(db, user_id=user_id, resume_id=resume_id)
        if not obj:
            return False
        obj.deleted_at = sa_func.now()
        db.commit()
        return True


class JobRepo:
    def create(
        self,
        db: Session,
        *,
        user_id: UUID,
        title: str,
        company: str | None,
        location: str | None,
        raw_text: str,
        normalized_json: dict,
    ) -> JobPosting:
        obj = JobPosting(
            user_id=user_id,
            title=title,
            company=company,
            location=location,
            raw_text=raw_text,
            normalized_json=normalized_json,
        )
        db.add(obj)
        db.commit()
        db.refresh(obj)
        return obj

    def get(self, db: Session, *, user_id: UUID, job_id: UUID) -> JobPosting | None:
        stmt = select(JobPosting).where(
            JobPosting.id == job_id,
            JobPosting.user_id == user_id,
            JobPosting.deleted_at.is_(None),
        )
        return db.execute(stmt).scalar_one_or_none()

    def list(self, db: Session, *, user_id: UUID, limit: int, offset: int):
        base = select(JobPosting).where(
            JobPosting.user_id == user_id,
        JobPosting.deleted_at.is_(None),
        )
        total = _count_from_select(db, base)
        stmt = base.order_by(JobPosting.created_at.desc(), JobPosting.id.desc()).limit(limit).offset(offset)
        items = list(db.execute(stmt).scalars().all())
        return items, total

    def soft_delete(self, db: Session, *, user_id: UUID, job_id: UUID) -> bool:
        obj = self.get(db, user_id=user_id, job_id=job_id)
        if not obj:
            return False
        obj.deleted_at = sa_func.now()
        db.commit()
        return True


class TailorRunRepo:
    def create(
        self,
        db: Session,
        *,
        user_id: UUID,
        resume_version_id: UUID,
        job_posting_id: UUID,
        prompt_version: str,
        llm_provider: str,
        model_name: str,
        output_json: dict,
        prompt_tokens: int | None = None,
        completion_tokens: int | None = None,
        total_tokens: int | None = None,
        estimated_cost_usd: float | None = None,
    ) -> TailorRun:
        obj = TailorRun(
            user_id=user_id,
            resume_version_id=resume_version_id,
            job_posting_id=job_posting_id,
            prompt_version=prompt_version,
            llm_provider=llm_provider,
            model_name=model_name,
            output_json=output_json,
            prompt_tokens=prompt_tokens,
            completion_tokens=completion_tokens,
            total_tokens=total_tokens,
            estimated_cost_usd=estimated_cost_usd,
        )
        db.add(obj)
        db.commit()
        db.refresh(obj)
        return obj

    def get(self, db: Session, *, user_id: UUID, run_id: UUID) -> TailorRun | None:
        stmt = select(TailorRun).where(
            TailorRun.id == run_id,
            TailorRun.user_id == user_id,
            TailorRun.deleted_at.is_(None),
        )
        return db.execute(stmt).scalar_one_or_none()

    def list(self, db: Session, *, user_id: UUID, limit: int, offset: int):
        base = select(TailorRun).where(
            TailorRun.user_id == user_id,
            TailorRun.deleted_at.is_(None),
        )
        total = _count_from_select(db, base)
        stmt = base.order_by(TailorRun.created_at.desc(), TailorRun.id.desc()).limit(limit).offset(offset)
        items = list(db.execute(stmt).scalars().all())
        return items, total

    def soft_delete(self, db: Session, *, user_id: UUID, run_id: UUID) -> bool:
        run = self.get(db, user_id=user_id, run_id=run_id)
        if not run:
            return False

        # Soft delete the run
        run.deleted_at = sa_func.now()

        # Soft delete all artifacts for the run (so they disappear too)
        db.execute(
            update(Artifact)
            .where(
                Artifact.user_id == user_id,
                Artifact.tailor_run_id == run_id,
                Artifact.deleted_at.is_(None),
            )
            .values(deleted_at=sa_func.now())
        )

        db.commit()
        return True


class ArtifactRepo:
    def create(
        self,
        db: Session,
        *,
        user_id: UUID,
        tailor_run_id: UUID,
        kind: str,
        content_type: str,
        file_path: str,
        file_size_bytes: int | None = None,
    ) -> Artifact:
        obj = Artifact(
            user_id=user_id,
            tailor_run_id=tailor_run_id,
            kind=kind,
            content_type=content_type,
            file_path=file_path,
            file_size_bytes=file_size_bytes,
        )
        db.add(obj)
        db.commit()
        db.refresh(obj)
        return obj

    def get(self, db: Session, *, user_id: UUID, artifact_id: UUID) -> Artifact | None:
        stmt = select(Artifact).where(
            Artifact.id == artifact_id,
            Artifact.user_id == user_id,
            Artifact.deleted_at.is_(None),
        )
        return db.execute(stmt).scalar_one_or_none()

    def list_for_run(self, db: Session, *, user_id: UUID, run_id: UUID) -> list[Artifact]:
        stmt = select(Artifact).where(
            Artifact.user_id == user_id,
            Artifact.tailor_run_id == run_id,
            Artifact.deleted_at.is_(None),
        ).order_by(Artifact.created_at.desc(), Artifact.id.desc())
        return list(db.execute(stmt).scalars().all())

    def soft_delete(self, db: Session, *, user_id: UUID, artifact_id: UUID) -> bool:
        obj = self.get(db, user_id=user_id, artifact_id=artifact_id)
        if not obj:
            return False
        obj.deleted_at = sa_func.now()
        db.commit()
        return True

    def hard_delete(self, db: Session, *, user_id: UUID, artifact_id: UUID) -> bool:
        obj = self.get(db, user_id=user_id, artifact_id=artifact_id)
        if not obj:
            return False
        db.delete(obj)
        db.commit()
        return True

6) Update list endpoints: summary only + pagination meta + stable ordering
Runs list/detail + artifacts list + run delete
Replace services/api/app/routes/runs.py
from fastapi import APIRouter, Depends, HTTPException
from sqlalchemy.orm import Session
from uuid import UUID

from app.core.security import get_current_user_id
from app.services.storage.db import get_db
from app.services.storage.repos import TailorRunRepo, ArtifactRepo
from app.models.schemas import (
    RunListResponse, TailorRunSummaryOut, TailorRunOut,
    ArtifactOut, PaginationMeta,
)

router = APIRouter()
run_repo = TailorRunRepo()
artifact_repo = ArtifactRepo()


@router.get("/tailor-runs", response_model=RunListResponse)
def list_runs(
    limit: int = 20,
    offset: int = 0,
    db: Session = Depends(get_db),
    user_id: UUID = Depends(get_current_user_id),
):
    limit = min(max(limit, 1), 100)
    offset = max(offset, 0)

    items, total = run_repo.list(db, user_id=user_id, limit=limit, offset=offset)
    has_more = (offset + limit) < total

    return {
        "items": [TailorRunSummaryOut.model_validate(i) for i in items],
        "meta": PaginationMeta(
            limit=limit,
            offset=offset,
            total=total,
            has_more=has_more,
            next_offset=(offset + limit if has_more else None),
        ),
    }


@router.get("/tailor-runs/{run_id}", response_model=TailorRunOut)
def get_run(
    run_id: UUID,
    db: Session = Depends(get_db),
    user_id: UUID = Depends(get_current_user_id),
):
    run = run_repo.get(db, user_id=user_id, run_id=run_id)
    if not run:
        raise HTTPException(status_code=404, detail="Tailor run not found")
    return run


@router.get("/tailor-runs/{run_id}/artifacts", response_model=list[ArtifactOut])
def list_run_artifacts(
    run_id: UUID,
    db: Session = Depends(get_db),
    user_id: UUID = Depends(get_current_user_id),
):
    # Ensure run exists and belongs to user
    run = run_repo.get(db, user_id=user_id, run_id=run_id)
    if not run:
        raise HTTPException(status_code=404, detail="Tailor run not found")

    return artifact_repo.list_for_run(db, user_id=user_id, run_id=run_id)


@router.delete("/tailor-runs/{run_id}")
def delete_run(
    run_id: UUID,
    db: Session = Depends(get_db),
    user_id: UUID = Depends(get_current_user_id),
):
    ok = run_repo.soft_delete(db, user_id=user_id, run_id=run_id)
    if not ok:
        raise HTTPException(status_code=404, detail="Tailor run not found")
    return {"status": "deleted"}

Resumes list/detail + delete (PII-safe list)
Replace services/api/app/routes/resumes.py
from fastapi import APIRouter, Depends, HTTPException
from sqlalchemy.orm import Session
from uuid import UUID

from app.core.security import get_current_user_id
from app.services.storage.db import get_db
from app.services.storage.repos import ResumeRepo
from app.models.schemas import ResumeCreate, ResumeOut, ResumeListResponse, ResumeSummaryOut, PaginationMeta

router = APIRouter()
repo = ResumeRepo()


@router.post("/resumes", response_model=ResumeOut)
def create_resume(payload: ResumeCreate, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    return repo.create(db, user_id=user_id, title=payload.title, raw_text=payload.raw_text, parsed_json=payload.parsed_json)


@router.get("/resumes/{resume_id}", response_model=ResumeOut)
def get_resume(resume_id: UUID, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    obj = repo.get(db, user_id=user_id, resume_id=resume_id)
    if not obj:
        raise HTTPException(status_code=404, detail="Resume not found")
    return obj


@router.get("/resumes", response_model=ResumeListResponse)
def list_resumes(limit: int = 20, offset: int = 0, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    limit = min(max(limit, 1), 100)
    offset = max(offset, 0)

    items, total = repo.list(db, user_id=user_id, limit=limit, offset=offset)
    has_more = (offset + limit) < total

    return {
        "items": [ResumeSummaryOut.model_validate(i) for i in items],
        "meta": PaginationMeta(limit=limit, offset=offset, total=total, has_more=has_more, next_offset=(offset + limit if has_more else None)),
    }


@router.delete("/resumes/{resume_id}")
def delete_resume(resume_id: UUID, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    ok = repo.soft_delete(db, user_id=user_id, resume_id=resume_id)
    if not ok:
        raise HTTPException(status_code=404, detail="Resume not found")
    return {"status": "deleted"}

Jobs list/detail + delete (PII-safe list)
Replace services/api/app/routes/jobs.py
from fastapi import APIRouter, Depends, HTTPException
from sqlalchemy.orm import Session
from uuid import UUID

from app.core.security import get_current_user_id
from app.services.storage.db import get_db
from app.services.storage.repos import JobRepo
from app.models.schemas import JobCreate, JobOut, JobListResponse, JobSummaryOut, PaginationMeta

router = APIRouter()
repo = JobRepo()


@router.post("/jobs", response_model=JobOut)
def create_job(payload: JobCreate, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    return repo.create(
        db,
        user_id=user_id,
        title=payload.title,
        company=payload.company,
        location=payload.location,
        raw_text=payload.raw_text,
        normalized_json=payload.normalized_json,
    )


@router.get("/jobs/{job_id}", response_model=JobOut)
def get_job(job_id: UUID, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    obj = repo.get(db, user_id=user_id, job_id=job_id)
    if not obj:
        raise HTTPException(status_code=404, detail="Job not found")
    return obj


@router.get("/jobs", response_model=JobListResponse)
def list_jobs(limit: int = 20, offset: int = 0, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    limit = min(max(limit, 1), 100)
    offset = max(offset, 0)

    items, total = repo.list(db, user_id=user_id, limit=limit, offset=offset)
    has_more = (offset + limit) < total

    return {
        "items": [JobSummaryOut.model_validate(i) for i in items],
        "meta": PaginationMeta(limit=limit, offset=offset, total=total, has_more=has_more, next_offset=(offset + limit if has_more else None)),
    }


@router.delete("/jobs/{job_id}")
def delete_job(job_id: UUID, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    ok = repo.soft_delete(db, user_id=user_id, job_id=job_id)
    if not ok:
        raise HTTPException(status_code=404, detail="Job not found")
    return {"status": "deleted"}

7) Exports: add PDF + artifact deletes
Add PDF exporter
services/api/app/services/export/pdf_exporter.py
from __future__ import annotations

from io import BytesIO
from typing import Any
from reportlab.pdfgen import canvas
from reportlab.lib.pagesizes import LETTER


def build_pdf_bytes_from_tailor_output(output: dict[str, Any]) -> bytes:
    buf = BytesIO()
    c = canvas.Canvas(buf, pagesize=LETTER)
    width, height = LETTER

    y = height - 72
    c.setFont("Helvetica-Bold", 14)
    c.drawString(72, y, "Resume Builder AI — Tailored Output")
    y -= 28

    def new_page():
        nonlocal y
        c.showPage()
        y = height - 72
        c.setFont("Helvetica", 10)

    def draw_paragraph(text: str):
        nonlocal y
        # MVP wrap: split into chunks
        for line in _wrap(text, 95):
            if y < 72:
                new_page()
            c.drawString(72, y, line)
            y -= 14

    def draw_section(title: str, items: list[str] | None):
        nonlocal y
        if not items:
            return
        if y < 90:
            new_page()
        c.setFont("Helvetica-Bold", 12)
        c.drawString(72, y, title)
        y -= 18
        c.setFont("Helvetica", 10)
        for item in items:
            for line in _wrap(f"• {str(item)}", 95):
                if y < 72:
                    new_page()
                c.drawString(72, y, line)
                y -= 14
        y -= 10

    role_summary = output.get("role_summary")
    if role_summary:
        c.setFont("Helvetica-Bold", 12)
        c.drawString(72, y, "Role Summary")
        y -= 18
        c.setFont("Helvetica", 10)
        draw_paragraph(str(role_summary))
        y -= 10

    draw_section("Tailored Bullets", output.get("tailored_bullets"))
    draw_section("ATS Keywords Found", output.get("ats_keywords_found"))
    draw_section("ATS Keywords Missing", output.get("ats_keywords_missing"))
    draw_section("Keyword Gaps", output.get("keyword_gaps"))
    draw_section("Evidence Warnings", output.get("evidence_warnings"))
    draw_section("Follow-up Questions", output.get("follow_up_questions"))

    c.save()
    return buf.getvalue()


def _wrap(text: str, max_len: int) -> list[str]:
    words = text.split()
    lines: list[str] = []
    cur: list[str] = []
    for w in words:
        if sum(len(x) for x in cur) + len(cur) + len(w) > max_len:
            lines.append(" ".join(cur))
            cur = [w]
        else:
            cur.append(w)
    if cur:
        lines.append(" ".join(cur))
    return lines

Replace services/api/app/routes/export.py with (DOCX + PDF + download + delete)
from __future__ import annotations

import os
from pathlib import Path
from uuid import UUID, uuid4

from fastapi import APIRouter, Depends, HTTPException
from fastapi.responses import FileResponse
from sqlalchemy.orm import Session

from app.core.config import ARTIFACT_DIR
from app.core.security import get_current_user_id
from app.services.storage.db import get_db
from app.services.storage.repos import TailorRunRepo, ArtifactRepo
from app.services.export.docx_exporter import build_docx_from_tailor_output
from app.services.export.pdf_exporter import build_pdf_bytes_from_tailor_output

router = APIRouter()
run_repo = TailorRunRepo()
artifact_repo = ArtifactRepo()


@router.post("/tailor-runs/{run_id}/export/docx")
def export_run_docx(
    run_id: UUID,
    db: Session = Depends(get_db),
    user_id: UUID = Depends(get_current_user_id),
):
    run = run_repo.get(db, user_id=user_id, run_id=run_id)
    if not run:
        raise HTTPException(status_code=404, detail="Tailor run not found")

    doc = build_docx_from_tailor_output(run.output_json or {})

    filename = f"{run_id}_{uuid4().hex}.docx"
    file_path = Path(ARTIFACT_DIR) / filename
    doc.save(str(file_path))

    size = os.path.getsize(file_path)

    artifact = artifact_repo.create(
        db,
        user_id=user_id,
        tailor_run_id=run.id,
        kind="docx",
        content_type="application/vnd.openxmlformats-officedocument.wordprocessingml.document",
        file_path=str(file_path),
        file_size_bytes=size,
    )

    return {
        "artifact_id": str(artifact.id),
        "download_url": f"/v1/artifacts/{artifact.id}/download",
    }


@router.post("/tailor-runs/{run_id}/export/pdf")
def export_run_pdf(
    run_id: UUID,
    db: Session = Depends(get_db),
    user_id: UUID = Depends(get_current_user_id),
):
    run = run_repo.get(db, user_id=user_id, run_id=run_id)
    if not run:
        raise HTTPException(status_code=404, detail="Tailor run not found")

    pdf_bytes = build_pdf_bytes_from_tailor_output(run.output_json or {})

    filename = f"{run_id}_{uuid4().hex}.pdf"
    file_path = Path(ARTIFACT_DIR) / filename
    file_path.write_bytes(pdf_bytes)

    size = file_path.stat().st_size

    artifact = artifact_repo.create(
        db,
        user_id=user_id,
        tailor_run_id=run.id,
        kind="pdf",
        content_type="application/pdf",
        file_path=str(file_path),
        file_size_bytes=size,
    )

    return {
        "artifact_id": str(artifact.id),
        "download_url": f"/v1/artifacts/{artifact.id}/download",
    }


@router.get("/artifacts/{artifact_id}/download")
def download_artifact(
    artifact_id: UUID,
    db: Session = Depends(get_db),
    user_id: UUID = Depends(get_current_user_id),
):
    artifact = artifact_repo.get(db, user_id=user_id, artifact_id=artifact_id)
    if not artifact:
        raise HTTPException(status_code=404, detail="Artifact not found")

    path = Path(artifact.file_path)
    if not path.exists():
        raise HTTPException(status_code=404, detail="Artifact file missing on disk")

    return FileResponse(
        path=str(path),
        media_type=artifact.content_type,
        filename=path.name,
    )


@router.delete("/artifacts/{artifact_id}")
def delete_artifact(
    artifact_id: UUID,
    hard: bool = False,
    purge_file: bool = True,
    db: Session = Depends(get_db),
    user_id: UUID = Depends(get_current_user_id),
):
    artifact = artifact_repo.get(db, user_id=user_id, artifact_id=artifact_id)
    if not artifact:
        raise HTTPException(status_code=404, detail="Artifact not found")

    if purge_file:
        path = Path(artifact.file_path)
        if path.exists():
            path.unlink()

    if hard:
        ok = artifact_repo.hard_delete(db, user_id=user_id, artifact_id=artifact_id)
        if not ok:
            raise HTTPException(status_code=404, detail="Artifact not found")
        return {"status": "hard_deleted"}

    ok = artifact_repo.soft_delete(db, user_id=user_id, artifact_id=artifact_id)
    if not ok:
        raise HTTPException(status_code=404, detail="Artifact not found")
    return {"status": "deleted"}

8) Update tailor orchestration to store user_id
Update services/api/app/routes/tailor.py to include user_id dependency and pass it into repo creates
from fastapi import APIRouter, Depends
from sqlalchemy.orm import Session
from uuid import UUID

from app.core.security import get_current_user_id
from app.models.schemas import TailorRequest, TailorRunOut
from app.services.storage.db import get_db
from app.services.storage.repos import ResumeRepo, JobRepo, TailorRunRepo
from app.services.llm.mock import MockLLMClient

router = APIRouter()

resume_repo = ResumeRepo()
job_repo = JobRepo()
run_repo = TailorRunRepo()
llm = MockLLMClient()

@router.post("/tailor", response_model=TailorRunOut)
def tailor(payload: TailorRequest, db: Session = Depends(get_db), user_id: UUID = Depends(get_current_user_id)):
    resume = resume_repo.create(db, user_id=user_id, title="Resume (auto)", raw_text=payload.resume_text, parsed_json={})
    job = job_repo.create(db, user_id=user_id, title="Job (auto)", company=None, location=None, raw_text=payload.job_text, normalized_json={})

    system = "You are an evidence-first resume tailoring engine. Never invent experience."
    user = f"RESUME:\n{payload.resume_text}\n\nJOB:\n{payload.job_text}\n"
    output = llm.generate_json(system=system, user=user)

    run = run_repo.create(
        db,
        user_id=user_id,
        resume_version_id=resume.id,
        job_posting_id=job.id,
        prompt_version=payload.prompt_version,
        llm_provider="mock",
        model_name="mock",
        output_json=output,
    )
    return run

9) Ensure exports directory config exists

If you haven’t already:

services/api/app/core/config.py (add)
import os
from pathlib import Path

ARTIFACT_DIR = Path(os.getenv("ARTIFACT_DIR", "var/artifacts"))
ARTIFACT_DIR.mkdir(parents=True, exist_ok=True)

10) Register routes
Update services/api/app/main.py
from fastapi import FastAPI
from app.routes import health, resumes, jobs, tailor, runs, export

app = FastAPI(title="Resume Builder AI API", version="0.1.0")

app.include_router(health.router, tags=["health"])
app.include_router(resumes.router, prefix="/v1", tags=["resumes"])
app.include_router(jobs.router, prefix="/v1", tags=["jobs"])
app.include_router(tailor.router, prefix="/v1", tags=["tailor"])
app.include_router(runs.router, prefix="/v1", tags=["runs"])
app.include_router(export.router, prefix="/v1", tags=["export"])

11) Quick test commands
Use default demo user (no header)
curl http://localhost:8000/v1/tailor-runs

Or specify a user explicitly
curl -H "X-User-Id: 00000000-0000-0000-0000-000000000001" http://localhost:8000/v1/tailor-runs

Export PDF
curl -X POST http://localhost:8000/v1/tailor-runs/<RUN_ID>/export/pdf

Download artifact
curl -L -o output.pdf http://localhost:8000/v1/artifacts/<ARTIFACT_ID>/download

Delete artifact (soft delete + purge file)
curl -X DELETE "http://localhost:8000/v1/artifacts/<ARTIFACT_ID>?hard=false&purge_file=true"


## MVP Hardening Checklist (Auth-Ready + PII-Safe)

This project treats resumes and job postings as sensitive data (PII). The following checklist hardens the API with:
- auth-ready user scoping (`user_id`)
- soft deletes (`deleted_at`)
- PII-minimized list endpoints (no `raw_text` by default)
- paginated responses with stable ordering
- export artifacts (DOCX/PDF) with controlled download + deletion

### 1) Add `get_current_user_id()` (auth-ready)
**Goal:** Endpoints accept `X-User-Id` and scope data per user.

**Done checks**
- `X-User-Id` header is accepted without errors
- Requests without `X-User-Id` still work (demo user fallback)

**Test**
```bash
curl -i http://localhost:8000/v1/tailor-runs
curl -i -H "X-User-Id: 00000000-0000-0000-0000-000000000001" http://localhost:8000/v1/tailor-runs
2) Update models + migration + upgrade (user_id, deleted_at)
Goal: All tables include user_id and deleted_at, and a minimal users table exists.

Done checks

Migration applies successfully: alembic upgrade head

Columns exist in Postgres: user_id, deleted_at

Test (Postgres)

bash
Copy code
# If you have psql available:
psql "postgresql://rba:rba@localhost:5432/rba" -c "\d resume_versions"
psql "postgresql://rba:rba@localhost:5432/rba" -c "\d job_postings"
psql "postgresql://rba:rba@localhost:5432/rba" -c "\d tailor_runs"
psql "postgresql://rba:rba@localhost:5432/rba" -c "\d artifacts"
psql "postgresql://rba:rba@localhost:5432/rba" -c "\d users"
3) Update repos (enforce user scoping + deleted_at filtering)
Goal: Cross-user reads/writes are blocked; soft-deleted rows disappear.

Done checks

Fetching another user’s resource returns 404

Soft-deleted resources stop appearing in list endpoints

Test

bash
Copy code
# Create a run as USER A
RUN_JSON=$(curl -s -X POST http://localhost:8000/v1/tailor \
  -H "Content-Type: application/json" \
  -H "X-User-Id: 00000000-0000-0000-0000-0000000000aa" \
  -d '{"resume_text":"Resume text example ...","job_text":"Job text example ...","prompt_version":"v1"}')

RUN_ID=$(python -c "import json,sys; print(json.loads(sys.argv[1])['id'])" "$RUN_JSON")
echo "RUN_ID=$RUN_ID"

# Attempt to read it as USER B (should be 404)
curl -i -H "X-User-Id: 00000000-0000-0000-0000-0000000000bb" \
  http://localhost:8000/v1/tailor-runs/$RUN_ID
4) Update list endpoints (PII minimization + pagination metadata)
Goal: List endpoints return summary objects (no raw_text) + meta with paging info.

Done checks

/v1/resumes, /v1/jobs, /v1/tailor-runs return { items: [...], meta: {...} }

List results do NOT include raw_text

Ordering is stable: (created_at DESC, id DESC)

Test

bash
Copy code
curl -s http://localhost:8000/v1/resumes | python -m json.tool
curl -s http://localhost:8000/v1/jobs | python -m json.tool
curl -s http://localhost:8000/v1/tailor-runs | python -m json.tool

# Verify raw_text is NOT in list payload
curl -s http://localhost:8000/v1/resumes | grep -i raw_text && echo "ERROR: raw_text leaked in list"
5) Add DELETE endpoints (soft delete by default)
Goal: Deletions hide items from lists without destroying data immediately.

Done checks

DELETE /v1/tailor-runs/{id} returns success

Deleted run no longer appears in list

Related artifacts are soft-deleted when run is deleted

Test

bash
Copy code
curl -X DELETE -i http://localhost:8000/v1/tailor-runs/$RUN_ID \
  -H "X-User-Id: 00000000-0000-0000-0000-0000000000aa"

curl -s -H "X-User-Id: 00000000-0000-0000-0000-0000000000aa" \
  http://localhost:8000/v1/tailor-runs | python -m json.tool
6) Add PDF export (and ensure artifact row + file download)
Goal: Export creates an Artifact row and returns a download URL.

Done checks

POST /v1/tailor-runs/{id}/export/pdf returns { artifact_id, download_url }

Download endpoint returns a real PDF

Artifact list shows the exported file

Test

bash
Copy code
# Create a fresh run first (since prior may be deleted)
RUN_JSON=$(curl -s -X POST http://localhost:8000/v1/tailor \
  -H "Content-Type: application/json" \
  -H "X-User-Id: 00000000-0000-0000-0000-0000000000aa" \
  -d '{"resume_text":"Resume text example ...","job_text":"Job text example ...","prompt_version":"v1"}')

RUN_ID=$(python -c "import json,sys; print(json.loads(sys.argv[1])['id'])" "$RUN_JSON")

EXPORT_JSON=$(curl -s -X POST http://localhost:8000/v1/tailor-runs/$RUN_ID/export/pdf \
  -H "X-User-Id: 00000000-0000-0000-0000-0000000000aa")

ARTIFACT_ID=$(python -c "import json,sys; print(json.loads(sys.argv[1])['artifact_id'])" "$EXPORT_JSON")
DOWNLOAD_URL=$(python -c "import json,sys; print(json.loads(sys.argv[1])['download_url'])" "$EXPORT_JSON")

echo "ARTIFACT_ID=$ARTIFACT_ID"
echo "DOWNLOAD_URL=$DOWNLOAD_URL"

# Download the file
curl -L -o tailored.pdf -H "X-User-Id: 00000000-0000-0000-0000-0000000000aa" \
  http://localhost:8000$DOWNLOAD_URL

# Confirm artifacts list shows it
curl -s -H "X-User-Id: 00000000-0000-0000-0000-0000000000aa" \
  http://localhost:8000/v1/tailor-runs/$RUN_ID/artifacts | python -m json.tool


CONTRIBUTING.md
# Contributing

Thank you for your interest in contributing to Resume Builder AI.

This project is built to be:
- **Evidence-first** (no invented experience)
- **PII-aware** (resumes and job postings contain sensitive data)
- **Auth-ready** (user scoping is required even before full auth is added)
- **Testable** (changes should be verifiable via repeatable checks)

## Code of Conduct
Be respectful and professional. Harassment or discrimination of any kind is not tolerated.

## Development Setup

### Prerequisites
- Node.js 20+
- Python 3.11+
- Docker + Docker Compose

### Start Postgres
From repo root:
```bash
docker compose up -d db

API
cd services/api
cp .env.example .env
python -m venv .venv
source .venv/bin/activate   # Windows: .\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
alembic upgrade head
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

Web
cd apps/web
cp .env.local.example .env.local
npm ci
npm run dev

Branching and PR Policy
One PR per unit of work

Prefer small PRs that are easy to review and revert. If a change touches DB schema, routes, repos, and docs, that is usually too large—split it.

Branch naming

Use one of:

feature/<short-name>

fix/<short-name>

chore/<short-name>

docs/<short-name>

Examples:

feature/user-scoping

feature/pdf-export

fix/alembic-env-imports

Commit message conventions

Use concise, imperative subjects:

Add user scoping and soft deletes

Return paginated list metadata

Add artifact delete endpoint

PII & Security Requirements
PII minimization defaults

List endpoints must not return raw resume/job text by default.

Prefer summary representations and provide detail endpoints for full content.

Logging restrictions

Do not log raw resumes or job postings.

Do not log full request payloads that could contain PII.

Use request IDs, row IDs, or metadata instead.

User scoping (auth-ready)

Until JWT auth is added, the API uses X-User-Id as a development placeholder.
All data access must be scoped by user_id.

Future auth note: replace X-User-Id with JWT-based authentication and return the authenticated subject ID (sub) as user_id.

Database Migrations

Use Alembic for schema changes.

Every schema change must include a migration and be reversible (downgrade-safe where practical).

Common commands:

cd services/api
alembic revision -m "describe change"
alembic revision --autogenerate -m "describe change"
alembic upgrade head
alembic downgrade -1

Definition of Done (DoD)

A PR is considered complete when:

It includes or updates relevant documentation

It includes acceptance checks (curl commands, notes, or tests)

It maintains user scoping and PII-safe defaults

It does not break alembic upgrade head

Proposed PR series for MVP Hardening

Add get_current_user_id() dependency (accept X-User-Id)

Add user_id + deleted_at + migration (upgrade-safe)

Enforce user scoping in repos (cross-user reads blocked)

PII-safe list endpoints + pagination metadata

DELETE endpoints (soft delete by default)

PDF export + artifact download/delete


---

## GitHub Issue Templates

### 1) `/.github/ISSUE_TEMPLATE/01-mvp-hardening-step.md`
```md
---
name: MVP Hardening Step
about: Implement one hardening checklist step as a single PR
title: "[Hardening] Step X: <short title>"
labels: ["hardening", "mvp"]
assignees: []
---

## Goal
Describe the change in one or two sentences.

## Scope (must stay small)
- [ ] API changes
- [ ] Repo changes
- [ ] DB migration (if needed)
- [ ] Docs updates

## Acceptance Criteria
- [ ] User scoping enforced where applicable (`user_id`)
- [ ] PII-safe defaults maintained (no raw_text in list endpoints)
- [ ] Stable ordering where listing applies (`created_at DESC, id DESC`)
- [ ] Migration upgrades cleanly (if included): `alembic upgrade head`

## Done Checks (copy/paste commands)
```bash
# Add the exact curl / commands that prove it works

Notes / Risks

List any risks, edge cases, or follow-up work.


### 2) `/.github/ISSUE_TEMPLATE/02-bug-report.md`
```md
---
name: Bug Report
about: Report a reproducible issue
title: "[Bug] <short summary>"
labels: ["bug"]
assignees: []
---

## Summary
What happened vs what you expected.

## Steps to Reproduce
1.
2.
3.

## Actual Result
Paste output or describe behavior.

## Expected Result
What should have happened.

## Environment
- OS:
- Python version:
- Node version:
- Docker version:
- API commit/branch:

## Logs / Stack Trace
```text
paste here


---

## Optional but Recommended: PR template

### `/.github/PULL_REQUEST_TEMPLATE.md`
```md
## Summary
What does this PR change, and why?

## Changes
- [ ] API
- [ ] DB migration
- [ ] Docs
- [ ] Tests

## PII / Security
- [ ] List endpoints do not return raw resume/job text by default
- [ ] No sensitive data logged
- [ ] User scoping enforced (`user_id`)

## Verification (paste commands + results)
```bash
# Provide curl commands or test commands used

Screenshots (if UI)

Attach screenshots or recordings if applicable.

Notes / Follow-ups

Anything reviewers should pay attention to.


---

## Notes for future auth (for README or docs)
You can paste this verbatim anywhere you document auth:
> `X-User-Id` is a development placeholder. Replace it with JWT-based authentication and return the authenticated subject ID (`sub`) as `user_id`.

---

If you want, I can also generate a **GitHub Projects-friendly roadmap** (as `docs/roadmap.md`) that maps each checklist step to an issue, a PR, and a release tag (e.g., `v0.2.0-hardening-1`, `v0.3.0-hardening-2`).


1) CONTRIBUTING.md (repo root)
# Contributing

Thanks for contributing to Resume Builder AI.

This project is designed to be:
- **PII-aware** (resumes and job postings are sensitive data)
- **Evidence-first** (no invented experience)
- **Auth-ready** (user scoping enforced even before full auth is added)
- **Maintainable** (small PRs, clear acceptance criteria)

---

## Quickstart (Dev)

### Prerequisites
- Node.js 20+
- Python 3.11+
- Docker + Docker Compose

### Start Postgres
From repo root:
```bash
docker compose up -d db

API
cd services/api
cp .env.example .env
python -m venv .venv
source .venv/bin/activate   # Windows: .\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
alembic upgrade head
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

Web
cd apps/web
cp .env.local.example .env.local
npm ci
npm run dev

Workflow: One PR per Step

We prefer small PRs that are easy to review and revert. For MVP hardening, implement one checklist step per PR.

Branch naming

Use:

feature/<short-name>

fix/<short-name>

chore/<short-name>

docs/<short-name>

Examples:

feature/user-scoping

feature/pagination-meta

feature/pdf-export

Commit messages

Use concise, imperative titles:

Add user scoping and soft deletes

Return paginated list metadata

Add artifact delete endpoint

PII & Security Requirements
PII minimization defaults

List endpoints must not return raw resume/job text by default.

Use summary list responses + separate detail endpoints for full content.

Logging restrictions

Do not log raw resumes or job postings.

Do not log full request payloads that could contain PII.

Auth-ready user scoping

Until JWT is implemented, the API uses X-User-Id as a development placeholder.

Note (future auth): Replace X-User-Id with JWT-based authentication and return the authenticated subject ID (sub) as user_id.

Database Migrations

All schema changes must include an Alembic migration.

cd services/api
alembic revision -m "describe change"
alembic revision --autogenerate -m "describe change"
alembic upgrade head
alembic downgrade -1

Definition of Done (DoD)

A PR is done when:

Documentation updated (README and/or docs)

Acceptance checks included (curl commands or tests)

User scoping enforced (user_id)

PII-safe list defaults preserved (no raw_text in lists)

alembic upgrade head succeeds (if migrations are involved)

MVP Hardening PR Series (Recommended)

Add get_current_user_id() dependency (accept X-User-Id)

Add user_id + deleted_at columns + migration + upgrade

Update repos (user scoping + deleted_at filtering)

Update list endpoints (summary responses + pagination meta + stable ordering)

Add DELETE endpoints (soft delete default)

Add PDF export (artifact row + download)


---

## 2) GitHub Issue Templates

### A) `/.github/ISSUE_TEMPLATE/01-hardening-step.md`
```md
---
name: Hardening Step (One PR)
about: Implement one MVP hardening step as a single PR with verifiable checks
title: "[Hardening] Step X: <short title>"
labels: ["hardening", "mvp"]
assignees: []
---

## Goal
Describe the objective in 1–2 sentences.

## Scope (keep small)
- [ ] DB migration
- [ ] Repo layer updates
- [ ] API routes / schemas
- [ ] Documentation updates

## Acceptance Criteria
- [ ] User scoping enforced (`user_id`) where applicable
- [ ] Soft deletes respected (`deleted_at`) where applicable
- [ ] PII-safe defaults: list endpoints do not return `raw_text`
- [ ] Stable ordering for lists: `(created_at DESC, id DESC)`
- [ ] If a migration is included: `alembic upgrade head` succeeds

## Done Checks (copy/paste)
```bash
# Add exact commands proving the change works
# Example:
# curl -i -H "X-User-Id: <uuid>" http://localhost:8000/v1/tailor-runs

Notes / Risks

Anything reviewers should be aware of.


### B) `/.github/ISSUE_TEMPLATE/02-bug-report.md`
```md
---
name: Bug Report
about: Report a reproducible bug with logs and steps
title: "[Bug] <short summary>"
labels: ["bug"]
assignees: []
---

## Summary
What happened vs what you expected.

## Steps to Reproduce
1.
2.
3.

## Actual Result
Paste output or describe behavior.

## Expected Result
What should have happened.

## Environment
- OS:
- Python:
- Node:
- Docker:
- Branch/commit:

## Logs / Stack Trace
```text
paste here


---

## 3) Optional PR Template (strongly recommended)

### `/.github/PULL_REQUEST_TEMPLATE.md`
```md
## Summary
What does this PR change and why?

## Changes
- [ ] API
- [ ] DB migration
- [ ] Docs
- [ ] Tests / verification commands

## PII / Security Checklist
- [ ] List endpoints do not return raw resume/job text by default
- [ ] No sensitive data logged
- [ ] User scoping enforced (`user_id`)
- [ ] Soft deletes respected (`deleted_at`) where applicable

## Verification (commands + output)
```bash
# Paste the exact commands used to verify

Notes / Follow-ups

Anything reviewers should pay attention to.


---

## 4) Suggested Issue Titles for Your “One PR per Step” Series
- `[Hardening] Step 1: Add get_current_user_id dependency`
- `[Hardening] Step 2: Add user_id + deleted_at migration`
- `[Hardening] Step 3: Enforce user scoping + deleted filtering in repos`
- `[Hardening] Step 4: Pagination metadata + stable ordering + PII-safe lists`
- `[Hardening] Step 5: Add DELETE endpoints (soft delete default)`
- `[Hardening] Step 6: Add PDF export + artifact download/delete`

---

If you tell me your current default branch name (`main` or `master`) and whether you use GitHub Actions, I can also add a minimal **CI workflow** that runs: `pip install`, `alembic upgrade head`, and a couple of curl smoke checks—great for signaling engineering maturity in interviews.



