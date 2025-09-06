# Project Improvement Tasks

This file outlines a set of tasks to improve the intelligent trading bot project.

## 1. Code Refactoring and Configuration Improvements

-   **Move `futures` flag to config:** In `scripts/download_binance.py`, the `futures` flag is hardcoded. It should be moved to the configuration file to allow for downloading futures data without changing the code.
-   **Make download start date configurable:** In `scripts/download_binance.py`, the start date for historical data download is hardcoded. This should be a parameter in the configuration file.
-   **Refactor `download_binance.py`:** The script could be made more modular, for example by extracting the logic for handling existing files into a separate function.

## 2. Documentation

-   **Update `docs/scripts.md`:** This file is marked as outdated. It should be updated to reflect the current state of the scripts, including the `labels` script and other changes mentioned in `README.md`.
-   **Create a "Getting Started" guide:** A guide for new developers on how to set up the environment, configure the pipeline, and run the scripts would be very helpful. This could be a new markdown file or a section in the `README.md`.

## 3. New Features

-   **Add a new data source:** Implement a downloader for a new exchange, for example, KuCoin or Bybit. This would involve creating a new script similar to `scripts/download_binance.py`.
-   **Optimize feature generation:** The `README.md` mentions that feature generation can be slow. Investigate the `scripts/features.py` script and the feature generators in `common/` to identify performance bottlenecks and optimize them.

## 4. Testing

-   **Add unit tests:** The `tests/` directory contains only a few tests. Adding more unit tests for the data processing pipeline and the service would improve the project's robustness.
