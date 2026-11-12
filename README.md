# VPN Threat Detection Using Machine Learning

## Overview

VPN Threat Detection is a final-year B.Tech Computer Engineering project focused on analyzing VPN traffic and identifying potentially malicious network activity using machine learning and traffic metadata.

The project explores whether encrypted network traffic can be analyzed using observable characteristics without decrypting its payload.

## Objectives

- Analyze VPN and non-VPN traffic using network metadata.
- Identify potentially malicious traffic using machine learning.
- Explore traffic classification across different VPN protocols.
- Investigate behavioral differences between benign and malicious encrypted traffic.
- Support VPN security analysis through traffic classification and evidence-based reporting.

## Project Architecture

The project follows a modular approach:

- **Data Processing:** Extract and transform network traffic datasets into structured features.
- **Exploratory Data Analysis:** Analyze traffic distributions, feature relationships, duplicates, and data quality.
- **Machine Learning:** Train classifiers for VPN traffic classification and malicious traffic identification.
- **Inference:** Generate predictions and probability scores for traffic records.
- **Security Analysis:** Integrate ML findings with VPN configuration, IPsec/IKE analysis, and supporting evidence.
- **Reporting:** Present detection results and relevant security observations.

## Datasets

### 1. Encrypted VPN Dataset

Used to study VPN and non-VPN traffic across multiple applications and VPN protocols.

Includes:

- OpenVPN
- WireGuard
- L2TP
- L2TP/IPsec
- PPTP
- SSTP
- Non-VPN traffic

### 2. Malware TLS Traffic Dataset

Used to develop a machine learning classifier for benign and malicious TLS traffic.

The dataset contains network traffic metadata, TLS-related features, malware labels, and contextual information.

> Note: The malware TLS dataset is not exclusively VPN traffic. Its predictions should not be interpreted as direct proof of malicious activity inside a VPN tunnel.

## Machine Learning Components

### VPN Traffic Classification

Classifies network traffic as VPN or non-VPN using observable traffic characteristics.

### Malware Traffic Classification

A Random Forest-based classification pipeline trained on TLS traffic metadata to distinguish:

- Benign traffic
- Malicious traffic

The classifier generates predicted labels and class probabilities for traffic records.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook
- Joblib
- Git
- GitHub

## Repository Structure

```text
VPN_Threat_Detection/
├── notebooks/
│   └── 01_data_processing.ipynb
├── .gitignore
└── README.md
```

Additional notebooks, model artifacts, source code, and documentation will be added as development progresses.

## Limitations

- Classification performance depends on dataset quality and representativeness.
- Malware TLS classification does not independently establish whether a VPN tunnel contains malicious activity.
- Generalization to unseen VPN protocols and real-world traffic requires additional validation.
- ML predictions are indicators for further investigation, not definitive security verdicts.

## Project Information

**Project Type:** Final-Year Engineering Project  
**Degree:** B.Tech Computer Engineering  
**Domain:** Artificial Intelligence & Machine Learning

## Project Status

Currently under development.

---

**Status:** Under Development
