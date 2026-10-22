# NSE Market Data Downloader

A Python-based tool to fetch, validate, and store market data in CSV format. Supports configurable data sources, duplicate handling, error logging, and automated retries.

**Note:** Live NSE integration is not configured yet. The current demo uses synthetic data and does not represent actual market prices.

## Features
- Configurable data sources for four datasets
- CSV export with source trading dates
- Data validation and duplicate detection
- Retry handling for network errors and rate limits
- Logging and dataset-level error handling
- Unit tests with mocked responses and fixtures

## Setup

```bash
git clone <repository-url>
cd <project-folder>

python -m venv .venv
```

Activate the environment and install dependencies:

```bash
# Windows
.venv\Scripts\activate


pip install -r requirements.txt
```

## Usage

Run the demo:

```bash
python main.py --demo
```

Run a specific dataset:

```bash
python main.py --demo --dataset top-gainers-losers
```

Run tests:

```bash
python -m pytest -q
```

## Output

Generated CSV files are stored in `output/demo/` for demo runs and `output/live/` for live runs.

## Live Data

Configure a permitted HTTPS JSON data source in `config/datasets.json` and verify its schema before running with `--authorized-access`. The authorization flag does not grant access to NSE data.

## Tech Stack

Python · Requests · CSV · Pytest · Docker
