# Clangen Docs
This repository contains the documentation for Clangen.

## Contributing

Thank you for your interest in contributing to Clangen's documentation! To make a change in the documentation, you just have to change the corresponding `.md` file in the `/docs` folder. You can also create a new file in the folder and it will automatically create a new page in the documentation.

## Build Instructions

> [!IMPORTANT]
> If you just want to contribute documentation, you don't **have** to do this. Building the documentation just creates a local copy of the documentation website on your computer, which can be useful for previewing your changes, but isn't necessarily required.

### Using pure Python

1. Install dependencies:
   ```
   pip install .
   ```
2. Build and serve documentation:
   ```
   python3 -m mkdocs serve
   ```
   Running this command will build the documentation and start a local server on your computer. While the server is running, you can access the documentation at http://localhost:8000. The site will update whenever the files in `/docs` are changed.

### Using uv

1. Install [uv](https://docs.astral.sh/uv/getting-started/installation/).
2. Install dependencies:
   ```
   uv venv
   uv pip install .
   ```
3. Build and serve documentation:
   ```
   uv run mkdocs serve
   ```
   Running this command will build the documentation and start a local server on your computer. While the server is running, you can access the documentation at http://localhost:8000. The site will update whenever the files in `/docs` are changed.

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
4. You can access the documentation at http://localhost:8000. Unlike with uv and Python, this site will *not* update when the files in `/docs` are changed. To update the site, you have to close the server, then rebuild the image and run the server again.
