# batchask

Run a JSONL of prompts through an LLM, results to JSONL

## How to use

```bash
python batch.py prompts.jsonl -o answers.jsonl --workers 4
```

## Getting started

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
```

## Highlights

- Idempotent: skips ids already present in the output
- JSONL in, JSONL out: stream-safe for huge inputs
- Concurrent workers with a rate ceiling
- Retries failed items with backoff, logs them aside

## Project structure

```text
├── .github/
│   └── dependabot.yml
├── docs/
│   ├── configuration.md
│   ├── development.md
│   ├── faq.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── .editorconfig
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── batch.py
├── prompts.sample.jsonl
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
