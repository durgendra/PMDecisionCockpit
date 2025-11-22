# LLM Council

Local multi-model comparison app that routes a prompt to several LLMs, has them review one another, and then composes a final answer.

## About

The project is a polished demo for side-by-side model comparison. It pairs a FastAPI backend with a React frontend and uses OpenRouter as the transport layer to talk to multiple model providers. The app is intentionally experimental, but the core idea is technically solid and portfolio-friendly.

## Key Features

- Multi-model prompt fanout
- Cross-review and ranking workflow
- Final "chairman" response assembly
- React chat-style frontend
- JSON-based conversation storage

## Architecture

- `backend/` holds the FastAPI application and OpenRouter integration
- `frontend/` contains the Vite + React UI
- `main.py` and `start.sh` provide top-level convenience entry points

## Tech Stack

- Python 3.10+
- FastAPI
- Uvicorn
- React 19
- Vite
- OpenRouter API

## Prerequisites

- Python 3.10 or newer
- Node.js

## Installation

```bash
uv sync
cd frontend
npm install
```

## Configuration

- `OPENROUTER_API_KEY`

## How to Run

```bash
./start.sh
```

Or run the pieces manually:

```bash
uv run python -m backend.main
cd frontend
npm run dev
```

## Example Usage

- Submit a question
- Review the individual model answers
- Inspect the final council response

## Project Structure

- `backend/` - API, model orchestration, and storage
- `frontend/` - browser UI
- `data/conversations/` - conversation storage
- `header.jpg` - banner asset

## Current Status

Experimental but coherent. The README and code both frame it as a hack-style demo rather than a maintained product.

## Limitations

- No repo-level license
- The project depends on an external OpenRouter key
- Intended as a lightweight local demo

## License

No explicit license file was found at the repository root.
