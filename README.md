# F1 Driver Risk and Predictive Maintenance Testbed

Notebook-based Formula 1 research project for telemetry feature engineering, driver-risk scoring, anomaly detection, and lightweight deployment packaging. The repository stays notebook-first so the modeling, export, and service-generation steps remain visible in sequence.

## Repository Contents

- `f1driverbehavior&anomalydetection.ipynb`: end-to-end workflow from session data loading through ONNX export and service scaffolding
- `requirements.txt`: dependency list for the local Anaconda data-science workflow

## Notebook Coverage

The notebook includes:

- FastF1-based session ingestion and caching
- feature engineering for driver telemetry and race context
- sequence-model training and evaluation
- anomaly scoring with ROC-AUC reporting
- ONNX export for a lightweight inference artifact
- `FastAPI`, Prometheus, and Docker scaffolding generated from notebook cells

## Environment

This refresh is based on the local Anaconda `datascience312` workflow (Python 3.12):

```bash
conda activate datascience312
pip install -r requirements.txt
```

## Notes

- The deployment files are created from `%%bash` cells inside the notebook when those cells are run.
- FastF1 will build a local cache directory as part of normal notebook execution.
- The goal of this refresh is presentation and portability, not a structural rewrite of the original notebook project.
