# Sistema Inteligente de Gestao de Rotas

Plataforma web com API REST, dashboard administrativo, banco de dados, autenticacao JWT e relatorios para gestao de rotas logisticas.

## Stack

- Python 3.13
- FastAPI
- SQLAlchemy
- MySQL em Docker
- Bootstrap, Chart.js e Plotly
- JWT, Passlib/Bcrypt
- ReportLab e OpenPyXL

## Como executar com Docker

```bash
docker compose up --build
```

Acesse:

- API: http://localhost:8000
- Swagger/OpenAPI: http://localhost:8000/docs
- Dashboard: http://localhost:8000/app/dashboard

Usuario inicial criado automaticamente:

- Email: `admin@rotas.com.br`
- Senha: `admin123`

## Como executar localmente

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
copy .env.example .env
uvicorn backend.app.main:app --reload
```

Por padrao, o `.env.example` usa SQLite para facilitar desenvolvimento local. Para MySQL, altere `DATABASE_URL`.

## Principais endpoints

- `POST /auth/login`
- `POST /usuarios`
- `GET /usuarios`
- `POST /motoristas`
- `GET /motoristas`
- `POST /veiculos`
- `GET /veiculos`
- `POST /clientes`
- `GET /clientes`
- `POST /entregas`
- `GET /entregas`
- `POST /rotas`
- `GET /rotas`
- `GET /dashboard`
- `GET /relatorios?formato=pdf`
- `GET /relatorios?formato=excel`

## Estrutura

```text
backend/
  app/
    core/
    models/
    routes/
    schemas/
    services/
    repository/
    middleware/
    dashboard/
    reports/
    utils/
    tests/
frontend/
  templates/
  static/
    css/
    js/
```
