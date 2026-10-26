# claudetest

Originally a scratch repository; it now carries two things.

- **`site/`** — a static personal site, plain HTML and CSS, served by GitHub Pages.
- **`monitor/`** — the **Monitor de Crédito LatAm**: a self-updating monthly
  monitor of the Latin American credit cycle, built from central bank data.
  See [`monitor/README.md`](monitor/README.md) for how it runs and what it needs.

Quick start for the monitor:

    python3 monitor/fetch.py && python3 monitor/build.py

Standard library only — no install step.
