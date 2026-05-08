# Market-Intelligence
A backend-focused **Market Intelligence** platform built with **FastAPI**, **SQLModel**, and **PostgreSQL-oriented tooling** for managing datasets, tags, reports, and infography analytics endpoints.
## Tech Stack
- **Language:** Python
- **Framework:** FastAPI
- **ORM / DB Layer:** SQLModel + SQLAlchemy
- **Migrations:** Alembic
- **Validation:** Pydantic v2
- **Server:** Uvicorn
- **Data/Analytics:** Pandas, NumPy, PyArrow, DuckDB

#Project Structure

Market-Intelligence/
├── FastApiBackend/
│   ├── backend/
│   │   ├── app/
│   │   │   ├── infography/
│   │   │   │   ├── routers.py
│   │   │   │   ├── models.py
│   │   │   │   └── query_engine.py
│   │   │   ├── database.py
│   │   │   └── ...
│   │   ├── requirements.txt
│   │   └── ...
│   └── venv/
└── ...
Features
Dataset upload and validation
Category/tag management
Report and report-topic management
Relationship-rich nested read models
Query engine endpoints for analytics/chart-related use cases
File handling for dataset storage and parquet workflows
Getting Started
1) Clone repository
git clone <your-repo-url>
cd Market-Intelligence
2) Create and activate virtual environment
Windows (PowerShell)

python -m venv FastApiBackend\venv
.\FastApiBackend\venv\Scripts\Activate.ps1
3) Install dependencies
pip install -r FastApiBackend/backend/requirements.txt
4) Configure environment variables
Create a .env file in the backend location used by your app config (example path: FastApiBackend/backend/.env) and add your database/auth settings.

Example (adjust values):

DATABASE_URL=postgresql+psycopg2://user:password@localhost:5432/market_intelligence
SECRET_KEY=change-me
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=60
5) Run migrations (if applicable)
alembic upgrade head
6) Start the API
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
If your entrypoint differs, update command accordingly.

API Docs
After server start:

Swagger UI: http://localhost:8000/docs
ReDoc: http://localhost:8000/redoc
Development Notes
Static analysis uses pyright/basedpyright config.
.gitignore is set up for Python virtualenvs, caches, and common artifacts.
Keep .env out of Git; commit only .env.example (if used).
Suggested Next Improvements
Add tests/ with pytest for core infography routes
Add Dockerfile + docker-compose for one-command local setup
Add CI workflow for lint + type check + tests
Split large router modules into smaller domain files for maintainability
License
This project is currently private/internal. Add a license here if you plan to make it public.

If you want, I can generate a second version tailored for a **public GitHub README** (with badges, API screenshot section, and contributor guide).
