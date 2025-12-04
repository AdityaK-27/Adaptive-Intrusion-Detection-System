# Dynamic Intrusion Detection System (IDS) using Machine Learning & Evolutionary Game Theory

## Overview
This repository implements an adaptive Intrusion Detection System (IDS) that combines:

- Machine learning (Random Forest classifier) for intrusion detection
- Evolutionary Game Theory (EGT) for dynamic strategy adaptation
- Real-time multi-channel alerts (Email and Telegram)

The IDS alternates between aggressive and passive detection modes based on observed network behavior, aiming to improve detection accuracy while controlling false positives.

---

## Key Features

**Machine learning-based intrusion detection**

- Random Forest classifier for binary classification of network traffic (benign vs. attack).
- Data preprocessing, feature extraction, and model evaluation (classification report and confusion matrix).

**Evolutionary Game Theory (EGT) integration**

- Payoff matrices and replicator dynamics model attacker–defender interactions.
- Dynamic threshold and strategy updates to optimize defender payoffs.

**Real-time alerting**

- Email alerts using Python's `smtplib`.
- Telegram notifications via the Telegram Bot API.
- Configurable alert thresholds and templates.

**Simulation and monitoring**

- Tracks strategy evolution over time and adaptive responses to attack frequency.

---

## Tech Stack

- Languages: Python
- Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn, requests
- Automation: smtplib, Telegram Bot API
- Concepts: ML classification, anomaly detection, EGT, replicator dynamics

---

## Project Structure

```
├── IDS_EGT.ipynb               # Main Jupyter notebook with experiments and visualizations
├── small_intrusion_dataset.csv     # Sample dataset (first 50 rows used for demo)
├── requirements.txt            # Python dependencies
├── alert_email_template.txt    # Email alert template
├── alert_telegram_sample.json  # Telegram alert example
└── README.md                   # Project documentation
```

---

## How it works

1. **Data preprocessing**: Load network traffic, perform cleaning and feature engineering, and prepare the labels.

2. **Model training**: Train a Random Forest classifier and evaluate performance using precision, recall, and F1-score.

3. **EGT-based adaptation**: Define payoff matrices, compute replicator dynamics, and update defender strategy weights over time. The defender switches between aggressive and passive modes according to strategy weights and observed outcomes.

4. **Alerting and automation**: Trigger email and Telegram alerts when model predictions exceed configured thresholds.

---

## Usage

Clone the repository:

```bash
git clone https://github.com/AdityaK-27/Adaptive-Intrusion-Detection-System.git
cd Adaptive-Intrusion-Detection-System
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Open the notebook:

```bash
jupyter notebook IDS_EGT.ipynb
```

Run the script (optional):

```bash
python ids_egt.py
```

---

## Sample outputs

- Classification report (precision, recall, F1-score)
- Confusion matrix
- Strategy evolution chart showing defender adaptation
- Logs of triggered alerts

---

## Notes and considerations

- The included dataset is a small sample intended for demonstration and education. Do not use this repository with real or sensitive data without appropriate anonymization and compliance checks.
- Replace placeholder configuration values (email credentials, Telegram bot token, chat IDs) with secure environment variables before running in any environment.

---

## License

This project is provided for educational and research purposes. Use under the terms of the MIT License.

---

## Author

Aditya Kankarwal

For questions or collaboration, please open an issue or contact via the GitHub profile.

