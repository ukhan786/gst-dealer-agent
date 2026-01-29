## Run the API locally

```bash
cd apps/api
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
uvicorn main:app --reload --port 8000

# GSTsandbox

GSTsandbox is a starter monorepo skeleton for a future API and web application stack.

## Directory Layout

- `apps/api`: FastAPI (or other Python API) application source.
- `apps/web`: Next.js (or other web frontend) application source.
- `data/synthetic`: Synthetic datasets and fixtures.
- `docs/consultative_models`: Documentation for consultative models.
- `scripts`: Utility scripts and local tooling.
