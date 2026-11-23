# Telco Customer Churn — práctica de Git

**Nota sobre datos:** `data/telco_demo.csv` es un dataset **sintético**, con columnas inspiradas en Telco Customer Churn. No es una copia de Kaggle ni contiene datos de clientes reales. Se incluye para que la práctica funcione sin descargar nada. Para las prácticas posteriores se puede sustituir por el dataset real de Kaggle, revisando nombres y esquema.

## Requisitos
- Windows con Python 3.10+ y Git instalados.
- Visual Studio Code con terminal integrada (PowerShell).

## Ejecutar
```powershell
py -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m src.train --model forest
.\.venv\Scripts\python.exe -m src.train --model logistic
.\.venv\Scripts\python.exe -m src.train --model svm
```

Si `py` no existe, sustituirlo por `python`. La ejecución mediante `.venv\Scripts\python.exe` evita cambiar la política de ejecución de PowerShell.

## Git
Seguir `GUIA_GIT.md`. Este ZIP no contiene `.git`, para que cada alumno inicialice su propio repositorio.

Este proyecto utiliza Regresión Logística, Random Forest y SVM. 

Evaluación de modelos
En este proyecto se utilizará el Accuracy (Exactitud) que mide el porcentaje total de predicciones correctas que logra un modelo, siendo útil cuando las categorías están equilibradas pero engañoso si una clase predomina sobre otra. Para resolver ese desbalance existe el F1-score, una métrica que va de 0 a 1 y combina en un solo valor el equilibrio entre no dar falsas alarmas (precisión) y no dejar escapar casos reales (exhaustividad o recall). Por último, el ROC-AUC evalúa la capacidad general del modelo para distinguir y separar una clase de otra a través de distintos umbrales de probabilidad, donde un valor de 0.5 equivale a adivinar al azar y 1.0 representa una separación perfecta. 