# intelius_extraction

This project extracts contact information from Intelius.

## Setup

1. Clone the repository:
   - `git clone https://github.com/n00b-bot-rgb/intelius-extraction.git`
2. Enter the project folder:
   - `cd intelius-extraction`
3. Install Python dependencies:
   - `pip install -r requirements.txt`
4. Create `intelius/creds.py` with your credentials:
   - `username = "..."`
   - `password = "..."`
5. Add your `input.csv` file to `repository root`.

## Run

- Execute: `python -m intelius.run`

## Pipeline and workflow integration

A GitHub Actions workflow is included at `.github/workflows/pipeline.yml` and runs on `push` and `pull_request` events.

It runs a baseline integration check by:
- Installing system and Python dependencies
- Compiling the `intelius` package (`python -m compileall intelius`)
- Running `pytest` when tests are collected by pytest discovery
