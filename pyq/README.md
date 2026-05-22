# MPPSC GS1 PYQ Analyzer

A deterministic, re-runnable analysis pipeline that ingests every available
MPPSC State Service Preliminary General Studies Paper-I (GS Paper-I) from exam
cycle 2014 onward, classifies every question across eight academic dimensions,
runs 25 analytical modules, and emits a single comprehensive Markdown report
with a Hinglish executive summary aimed at the MPPSC 2027 Prelims.

CSAT (Paper-II) papers are out of scope.

## Requirements

- Python **3.11+**
- Runtime dependencies: `pdfplumber`, `scipy`, `pyyaml`
- Dev dependencies: `pytest`, `pytest-xdist`, `hypothesis`, `coverage`

Install both runtime and dev dependencies with:

```bash
pip install -e ".[dev]"
```

## Single Entry-Point Command

The analyzer exposes exactly one command. There are no other CLI verbs and no
hidden flags. This is the command documented in design "Re-runnability
Strategy" and is the only supported way to run the pipeline:

```bash
python -m mppsc_pyq_analyzer.run \
    --input-dir . \
    --output-dir .kiro/specs/mppsc-gs1-pyq-analyzer/output
```

- `--input-dir` is the directory the **Ingestor** scans for source paper files
  (HTML and PDF). The default expectation is the project root, where the
  current corpus of GS Paper-I HTML and PDF files lives.
- `--output-dir` is where the **Report Generator** writes the final
  artifacts (`report.md`, any backup `report.<UTC_TIMESTAMP>.md`, the
  classifications cache, and `run_log.txt`). The default location used in the
  command above mirrors design "Re-runnability Strategy" and satisfies
  Requirement 16.1 (output artifact location).

## Re-runnability

When new MPPSC GS Paper-I source files become available (for example the 2026
or 2027 papers):

1. Drop the new HTML or PDF file into the same input directory used above.
2. Re-run the command. No code changes are required.
3. If a previous `report.md` exists in the output directory, the Report
   Generator renames it to `report.<UTC_TIMESTAMP>.md` (with a numeric
   suffix on collision) before writing the new report.
4. When the actual 2027 paper is added to the corpus, the Auditor automatically
   scores every prediction in the most recent prior report against the
   actual outcome and emits an Audit section in the new report.

If a new file's filename does not match the year-extraction regex, the run
aborts cleanly with a precise instruction to add the filename to the
filename-to-year mapping table — no backup, no overwrite.

## Determinism

The pipeline is byte-deterministic except for the run timestamp recorded in
the Methodology section (Requirement 21.2). Two runs on the same machine with
the same corpus and unchanged configuration produce a `report.md` that differs
only in that timestamp. Determinism is preserved by:

- Sorting every list, table, and category enumeration with a documented key.
- Rounding all reported numbers at emission time.
- Using a layered, regex-driven rule engine for classification with no
  randomized inference.
- Writing `report.md` atomically with `\n` line endings.

## Layout

```
mppsc_pyq_analyzer/
├── __init__.py
├── ingestion/
├── classification/
├── analysis/
├── prediction/
├── reporting/
└── util/
tests/
└── conftest.py
```

## Testing

The test suite uses `pytest` with `hypothesis` for property-based tests.
The shared `tests/conftest.py` configures a Hypothesis profile with
`max_examples=200` and `deadline=None`. Run the suite with:

```bash
pytest
```

Run with parallel workers via `pytest-xdist`:

```bash
pytest -n auto
```

Run with coverage:

```bash
coverage run -m pytest
coverage report
```

## Spec

The full requirements, design, and task plan live under
`.kiro/specs/mppsc-gs1-pyq-analyzer/`.
