# toolkit-rag-quality: codebase map

Read alongside `AGENTS.md`, `README.md` and `pyproject.toml`. This map describes
source locations, not an independent capability or readiness assessment.

| Path | Responsibility |
|---|---|
| `src/toolkit_rag_quality/cli.py`, `__main__.py` | `toolkit-rag` entry point and CLI dispatch |
| `retrieval.py`, `formats.py` | Retrieval metrics and qrels/run import and export |
| `compare.py`, `stats.py` | Regression budgets and paired significance calculations |
| `overlap.py`, `leakage.py` | Corpus overlap and eval containment checks |
| `adapters.py` | Optional retriever integrations, imported lazily |
| `report.py`, `envelope.py`, `io.py` | Report envelopes, validation and file I/O |
| `src/toolkit_rag_quality/control_plane/` | Control-plane integration code |
| `tests/`, `tests/fixtures/` | Behavioral checks, reference values and CLI fixtures |
| `schemas/`, `docs/report-envelope.md` | Shared report format contract |
| `action.yml`, `.github/workflows/` | Composite action and CI checks |

The module paths without a directory prefix above are relative to
`src/toolkit_rag_quality/`. Commands and execution locations are in `AGENTS.md`.
