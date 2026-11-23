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

<<<<<<< HEAD
Evaluación de modelos
En este proyecto se utilizará el Accuracy (Exactitud) que mide el porcentaje total de predicciones correctas que logra un modelo, siendo útil cuando las categorías están equilibradas pero engañoso si una clase predomina sobre otra. Para resolver ese desbalance existe el F1-score, una métrica que va de 0 a 1 y combina en un solo valor el equilibrio entre no dar falsas alarmas (precisión) y no dejar escapar casos reales (exhaustividad o recall). Por último, el ROC-AUC evalúa la capacidad general del modelo para distinguir y separar una clase de otra a través de distintos umbrales de probabilidad, donde un valor de 0.5 equivale a adivinar al azar y 1.0 representa una separación perfecta. 
=======
Support Vector Machine (SVM) — Máquinas de Vectores de Soporte

El algoritmo Support Vector Machine (SVM) es un método de aprendizaje supervisado utilizado para resolver problemas de clasificación y regresión. En este proyecto se utilizará su variante de regresión, denominada Support Vector Regression (SVR), para predecir la calificación promedio (vote_average) de una película a partir de sus características.

Se utilizará el dataset 
The Movies Dataset
 de Kaggle, que contiene información de aproximadamente 45.000 películas, incluyendo géneros, presupuesto, duración, popularidad, fecha de estreno e información sobre las votaciones. 

SVR busca encontrar una función que permita estimar los valores de la variable objetivo minimizando el error de predicción, utilizando un margen de tolerancia. Mediante diferentes funciones kernel puede modelar relaciones lineales y no lineales entre las características de las películas y sus calificaciones.

En este proyecto, el algoritmo utilizará variables como el presupuesto, la duración, el año de estreno y los géneros cinematográficos para estimar la calificación promedio que podría obtener una película.

Tipo de aprendizaje: Supervisado.
Tipo de problema: Regresión.
Variable objetivo: vote_average (calificación promedio de la película).
Algoritmo: Support Vector Regression (SVR).
>>>>>>> feature/svm

Modelo principal: Random Forest