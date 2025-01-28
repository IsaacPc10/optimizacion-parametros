Aquí tienes el contenido actualizado para el `README.md`, explicando que el trabajo está enfocado en la **optimización de hiperparámetros** y aclarando que los datos no serán subidos al repositorio:

---

# 🔧 Optimización de Hiperparámetros para la Clasificación de Cáncer de Mama 🎗️

Este repositorio contiene el desarrollo de un modelo de **aprendizaje automático supervisado** para la **clasificación de cáncer de mama** (benigno o maligno), enfocándose en la **optimización de hiperparámetros** mediante diferentes estrategias.

## 📌 Objetivo del Proyecto
El propósito es aplicar técnicas de **optimización de hiperparámetros** para mejorar el rendimiento de un modelo de clasificación utilizando el dataset de **Breast Cancer Wisconsin (Diagnostic)**. Se evalúan diferentes combinaciones de parámetros para encontrar el mejor ajuste del modelo.

## 📂 Contenido del Repositorio
- **`10-Optimizacion-Hiperparametros-IsaacPorras.ipynb`** → Cuaderno de Jupyter con la implementación del modelo y la optimización de hiperparámetros.
- **`modelo_optimizado.pkl`** → Modelo final entrenado con los mejores hiperparámetros encontrados.
- **`LICENSE`** → Licencia MIT para el uso del código.
- **`README.md`** → Explicación del proyecto y su contenido.

## 🏗️ Desarrollo del Proyecto
El flujo de trabajo incluye las siguientes etapas:

### 1️⃣ Preprocesamiento de Datos
- Eliminación de columnas irrelevantes.
- División en conjuntos de **entrenamiento y prueba**.
- **Escalado** de las variables para normalizar los datos.

### 2️⃣ Selección del Modelo y Hiperparámetros
- Se selecciona un **modelo base** de clasificación supervisada.
- Se analizan los principales hiperparámetros y su impacto en el rendimiento.

### 3️⃣ Optimización de Hiperparámetros
Se implementan dos estrategias para encontrar la mejor configuración del modelo:
1. **GridSearchCV** → Explora combinaciones exhaustivas de hiperparámetros en una cuadrícula predefinida.
2. **RandomSearchCV** → Explora una selección aleatoria de combinaciones, permitiendo encontrar soluciones más rápido.

Cada técnica de optimización se ejecuta con:
- **Al menos 3 valores por hiperparámetro en GridSearch.**
- **Al menos 5 valores por hiperparámetro en RandomSearch.**
- **5 validaciones cruzadas** para evaluar la estabilidad del modelo.
- **25 iteraciones en RandomSearchCV.**

### 4️⃣ Entrenamiento del Mejor Modelo
- Se reentrena el modelo con los **parámetros óptimos** encontrados.
- Se evalúa su desempeño con métricas como **accuracy, precision, recall y matriz de confusión**.
- Se guarda el modelo final en `modelo_optimizado.pkl`.

  Voy a revisar los resultados en el archivo que subiste y redactaré un apartado de **Resultados** para el `README.md`. Dame un momento.

Aquí tienes la sección de **Resultados** para agregar al `README.md`, basada en los resultados obtenidos en tu notebook:

---

## 📊 Resultados de la Optimización

Después de aplicar **GridSearchCV** y **RandomSearchCV**, se determinaron los mejores hiperparámetros para el modelo de clasificación de cáncer de mama.

### 🔍 Mejores Hiperparámetros Encontrados:
1. **GridSearchCV**:
   - `criterion`: **entropy**
   - `max_depth`: **None**
   - `n_estimators`: **10**
   - **Mejor Score:** `0.956`

2. **RandomSearchCV**:
   - `n_estimators`: **50**
   - `max_depth`: **5**
   - `criterion`: **entropy**
   - **Mejor Score:** `0.958`

### 🏆 Desempeño del Modelo Final
Tras reentrenar el modelo con los mejores parámetros, se obtuvo un rendimiento óptimo:

- **Precisión del modelo:** `96%`
- **Matriz de confusión:**
  ```
  [[70  1]
   [ 3 40]]
  ```
- **Reporte de Clasificación:**
  ```
                precision    recall  f1-score   support

        Benigno (B)     0.96      0.99      0.97        71
        Maligno (M)     0.98      0.93      0.95        43

        Accuracy                           0.96       114
        Macro avg       0.97      0.96      0.96       114
        Weighted avg    0.97      0.96      0.96       114
  ```

El modelo optimizado logra una alta precisión y un buen balance entre **recall** y **f1-score**, demostrando una capacidad efectiva para distinguir entre tumores benignos y malignos.

---


## 📜 Licencia
Este proyecto está bajo la **Licencia MIT**, lo que permite su uso, modificación y distribución con atribución adecuada.

---
