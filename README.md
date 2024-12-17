# Token Selection Project

This project automates the selection of crypto tokens based on:
1. Liquidity metrics (volume, trade count).
2. On-chain activity.
3. Development activity (GitHub commits).
4. Stability and volatility checks.

## Folder Structure
- `src/`: Core Python scripts.
- `data/`: Exported data files.
- `notebooks/`: Prototyping in Jupyter notebooks.
- `tests/`: Unit tests for the scripts.

## How to Run
1. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # For Mac/Linux
   .\venv\Scripts\activate   # For Windows
