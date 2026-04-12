# AI-Driven Anomaly Detection for CI/CD Pipeline Security

This project keeps the existing anomaly detection implementation unchanged and
adds a CI/CD execution layer so the pipeline can run automatically in a DevOps
workflow.

## Project Structure

Use the following structure for clean CI/CD integration:

- `Nandana.ipynb`: Primary executable notebook containing the anomaly detection
  pipeline
- `dataset1/`, `dataset2/`, `dataset3/`, `dataset4/`: input datasets
- `outputs/`: generated plots, CSV comparison, and report artifacts
- `requirements.txt`: Python dependencies used by the pipeline
- `.github/workflows/ci-cd.yml`: GitHub Actions workflow for automation

## CI/CD Automation Flow

The workflow in `.github/workflows/ci-cd.yml` runs on every push and pull
request.

It performs the following steps:

1. Check out the repository
2. Set up Python 3.11
3. Install dependencies from `requirements.txt`
4. Run the anomaly detection pipeline by executing the Jupyter notebook
   (`Nandana.ipynb`) using automated notebook execution
5. Upload generated outputs as artifacts (`png`, `csv`, `docx`)

## Why This Simulates CI/CD Pipeline Monitoring

In a real DevSecOps environment, CI/CD jobs continuously emit build, test, and
deployment telemetry. Automating this ML pipeline in GitHub Actions simulates
that operational model by running anomaly analysis on each code change and
preserving artifacts for review, trend tracking, and incident triage.

## Datasets are not included due to size limitations. 
They can be downloaded from:
1. Log data for Anomaly Detection: https://www.kaggle.com/datasets/krishd123/log-data-for-anomaly-detection
2. UNSW-NB15 Dataset: https://research.unsw.edu.au/projects/unsw-nb15-dataset
3. Intrusion Detection Evaluation Dataset: https://www.unb.ca/cic/datasets/ids-2017.html
4. CI/CD Pipeline failures Dataset: https://www.kaggle.com/datasets/mirzayasirabdullah07/cicd-pipeline-failure-logs-dataset-for-aiops