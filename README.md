# recommendation service (demo)

Minimal stand-in recommendation service for AIOps code-fix evaluation
scenarios. Stdlib-only Python; `python recommendation_server.py` starts an
HTTP server on :8080 plus a background load thread.

## Endpoints

- `GET /recommend` — top-5 recommendations (catalog match, excluding the input ids)
- `GET /metrics` — Prometheus text exposition
- `GET /healthz` — liveness

## Build / test
```bash
pip install -r requirements.txt
python -m py_compile $(git ls-files '*.py')
pytest -q
```
