# 📁 Data Versioning and CI/CD with DVC

This project demonstrates a minimal setup for **data versioning using DVC** and **CI/CD using GitHub Actions**, focused on the real-world scenario of managing datasets stored in the cloud (e.g., AWS S3 or GCP Cloud Storage).

---

## 🧩 Scenario

You want to:

- Version and track datasets used in data pipelines.
- Simulate remote data access (e.g., from AWS or GCP buckets).
- Validate that the dataset is accessible and well-formed before running your pipeline.

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

