# Airflow
## 📘 Description

Projet inspiré du Lab 2 de Ramin Mohammadi, réalisé uniquement avec Apache Airflow.
L’objectif : automatiser un pipeline de régression logistique sur des données publicitaires.

⚙️ Structure
airflow_home/
├── dags/
│   ├── data/advertising.csv
│   ├── src/model_development.py
│   └── main.py
├── templates/ (emails)
└── requirements.txt

## 🚀 Installation
python3 -m venv airflow_env
source airflow_env/bin/activate
pip install -r requirements.txt
export AIRFLOW_HOME=~/airflow
airflow db migrate
airflow webserver --port 8080
airflow scheduler


Interface : http://localhost:8080

## 🧠 Pipeline

load_data – Charger les données

preprocess_data – Prétraiter

train_model – Entraîner la régression logistique

evaluate_model – Évaluer le modèle

Notifications par e-mail (succès / échec)