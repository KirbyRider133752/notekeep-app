# notekeep-app

Minimal notes REST API built with Flask

Started as a weekend hack, grew on me.

## How to use

```bash
curl -X POST localhost:5000/notes \
  -H 'content-type: application/json' \
  -d '{"title": "first", "body": "hello"}'
```

## Features

- CRUD endpoints for notes
- SQLite storage via sqlite3 stdlib
- pytest coverage for the happy paths
- Request validation and consistent error shape

## Install

```bash
pip install -r requirements.txt
flask --app app run --debug
```

## Project structure

```text
├── .github/
│   └── workflows/
│       └── ci.yml
├── docs/
│   ├── development.md
│   └── faq.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_api.py
├── .gitignore
├── CONTRIBUTING.md
├── LICENSE
├── SECURITY.md
├── app.py
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## License

MIT - see [LICENSE](LICENSE).
