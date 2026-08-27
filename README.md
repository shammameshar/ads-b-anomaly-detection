# ADS-B Anomaly Detection

Aviation cybersecurity and Big Data analytics system for detecting anomalies and GPS spoofing in ADS-B aircraft surveillance data.

## Overview

This project uses 2,669,349 aircraft telemetry records from the OpenSky Network to build a scalable, distributed machine learning pipeline for detecting suspicious ADS-B signals — a critical safety layer for modern aviation surveillance systems. The pipeline follows the OSEMN framework (Obtain, Scrub, Explore, Model, iNterpret) and is built with PySpark for distributed processing.

## Key Features

- **Distributed pipeline**: PySpark-based ingestion, cleaning, feature engineering, and partitioning across 2.6M+ telemetry records
- **Aviation-specific feature engineering**: spatial displacement, altitude change, and other domain-informed signals
- **Model comparison**: Logistic Regression baseline vs. a distributed Multi-Layer Perceptron (MLP) — the MLP achieved **95.19% validation accuracy**
- **Scalability benchmarking**: performance tested at 20%, 50%, and 100% of the dataset
- **Explainable AI**: SHAP-aligned feature importance for model transparency
- **Interactive demo**: a three-tab Gradio interface for real-time signal validation, anomaly visualization, and system performance monitoring

## Project Structure


## Data Source

Telemetry data sourced from the [OpenSky Network](https://opensky-network.org/). The raw dataset (`flightlist.csv`, ~524MB) is not included in this repository due to size; it can be obtained directly from OpenSky Network.

## Requirements

- PySpark
- Python (pandas, numpy, matplotlib, scikit-learn)
- SHAP
- Gradio

## Author

Shamma Mohammad Almheiri

## License

This project is released under the MIT License.