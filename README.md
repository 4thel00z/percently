<div align="center">
  <h1>percently</h1>
  <p><strong>Fast percentile calculator written in Rust — shipped as a Python package.</strong></p>

  <p>
    <a href="https://github.com/4thel00z/percently/actions/workflows/CI.yml">
      <img alt="CI" src="https://github.com/4thel00z/percently/actions/workflows/CI.yml/badge.svg" />
    </a>
    <a href="https://pypi.org/project/percently/">
      <img alt="PyPI" src="https://img.shields.io/pypi/v/percently" />
    </a>
    <a href="https://pypi.org/project/percently/">
      <img alt="Python versions" src="https://img.shields.io/pypi/pyversions/percently" />
    </a>
    <a href="LICENSE">
      <img alt="License" src="https://img.shields.io/github/license/4thel00z/percently" />
    </a>
    <img alt="Rust" src="https://img.shields.io/badge/Rust-2021-000000?logo=rust" />
    <img alt="maturin" src="https://img.shields.io/badge/built%20with-maturin-2A2A2A" />
  </p>
</div>

## Motivation

When you’re processing load test timings (or any latency distribution), you typically want buckets like p50/p95/p99 quickly. `percently` provides a small, fast Rust implementation exposed to Python.

## Features

- **Fast**: Rust core
- **Simple API**: one call to compute a percentile
- **Python-friendly**: works with regular lists/iterables of floats

## Installation

Using `uv`:

```bash
uv add percently
```

Using `pip`:

```bash
pip install percently
```

## 🧮 Usage

```python
import percently

data = [10.5, 22.0, 18.7, 19.2, 30.1, 25.3]

# Calculate the 95th percentile (f64)
p95 = percently.percentile(data, 95)
print(f"95th percentile: {p95:.2f}")
```

## Development

Build/install locally (editable) with `maturin`:

```bash
uv sync
uv run maturin develop
```

## License

MIT — see `LICENSE`.
