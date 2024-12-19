# Clangen Docs
This repository contains the documentation for Clangen.

## Contributing

Thank you for your interest in contributing to Clangen's documentation! To make a change in the documentation, you just have to change the corresponding `.md` file in the `/docs` folder. You can also create a new file in the folder and it will automatically create a new page in the documentation.

## Build Instructions

### Using pure Python

1. Install dependencies:
   ```
   pip install .
   ```
2. Build documentation:
   ```
   python3 -m mkdocs build
   ```
3. The documentation will be in the `site` directory.
   * Alternatively, you can run `python3 -m http.server -d site 8000` in order to access the documentation at http://localhost:8000.

### Using uv

1. Install [uv](https://docs.astral.sh/uv/getting-started/installation/).
2. Install dependencies:
   ```
   uv venv
   uv pip install .
   ```
3. Build documentation:
   ```
   uv run mkdocs build
   ```
4. The documentation will be in the `site` directory.
   * Alternatively, you can run `uv run python3 -m http.server -d site 8000` in order to access the documentation at http://localhost:8000.

### Using Docker

1. Install [Docker](https://www.docker.com).
2. Build image:
   ```
   docker buildx build . -t clangen-docs
   ```
3. Run server:
   ```
   docker run -p 8000:80 clangen-docs
   ```
4. You can access the documentation at http://localhost:8000.
