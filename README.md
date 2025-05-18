# 📁 Data Versioning and CI/CD with DVC

This project demonstrates a minimal setup for **data versioning using DVC** and **CI/CD using GitHub Actions**, focused on the real-world scenario of managing datasets stored in the cloud (e.g., AWS S3 or GCP Cloud Storage).

---

## 🧩 Scenario

This project addresses a common real-world need in data engineering and MLOps:

- ✅ **Version and track datasets** used in data pipelines using DVC.
- ☁️ **Simulate remote data access** from cloud storage providers like AWS S3 or GCP Cloud Storage.
- 🛡️ **Validate dataset accessibility and structure** before running pipelines — helping to:
  - Avoid unnecessary data pushes or downloads
  - Prevent pipeline failures due to missing or malformed files
  - Reduce cloud compute and storage costs

---

## ✅ Current Logic

The script `test_pipeline.py` performs a dry run:

- Attempts to access a CSV file (e.g., `data/sample.csv`).
- Prints the number of rows and columns to verify structure.
- This script is run automatically in CI/CD.

---

## 🔧 To-Do

1. ✅ **Check if file exists** before trying to read it.
2. 🟨 Use **partial read** (e.g., `nrows=10`) or **wildcard/glob** to test schema/layout.
3. 🟨 **Learn and Setup DVC** (e.g., S3, SSH, or mapped drive).
4. 🟨 Optionally add **data schema validation** (e.g., using `pandera` or `great_expectations`).

---

## 📚 Libraries Used

- [**DVC**](https://dvc.org/) – For data versioning, remote data storage, and pipeline tracking
- [**pandas**](https://pandas.pydata.org/) – For reading and validating structured data (CSV, etc.)

---

