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

## 📜 Licencia
Este proyecto está bajo la **Licencia MIT**, lo que permite su uso, modificación y distribución con atribución adecuada.

---
