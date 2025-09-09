# Contributing to PyPlotJuggling

## Development Setup

1. Clone the repository
2. Create a virtual environment: `python -m venv .venv`
3. Activate it: `source .venv/bin/activate` (Linux/Mac) or `.venv\Scripts\activate` (Windows)
4. Install in development mode: `pip install -e ".[dev]"`

## Running Tests

```bash
python -m pytest tests/ -v
```

## Code Style

Please ensure your code follows Python best practices. The CI will run basic linting checks.

## Making a Release

1. Update the version in `pyproject.toml` and `PyPlotJuggling/__init__.py`
2. Update the changelog
3. Create a git tag: `git tag v0.1.1`
4. Push the tag: `git push origin v0.1.1`
5. Create a GitHub release from the tag

The GitHub Actions workflow will automatically publish to PyPI when you create a release.

## Testing Changes

- Push to `main` branch will run tests and publish to Test PyPI
- Pull requests will run the full test suite
- Releases will publish to production PyPI
