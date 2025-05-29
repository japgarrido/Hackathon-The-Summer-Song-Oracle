# 🎵 Summer Hit Predictor

**Oracle AI Hackathon 2025**
En este proyecto, desarrollado para la Hackathon de Oracle 2025, nos centramos en la predicción de la popularidad de canciones para identificar la próxima **canción del verano**. Utilizamos un conjunto de datos con características musicales que incluyen atributos acústicos, rítmicos y categóricos, junto con información del género y modo musical.

El enfoque principal del proyecto es doble: por un lado, lograr una predicción precisa del nivel de popularidad de cada canción, y por otro, ofrecer interpretabilidad sobre qué características son determinantes en esa popularidad.

---

## 🔍 Descripción del problema

Las canciones del verano suelen compartir ciertas características: ritmos bailables, energía alta, géneros populares, etc.  
Este proyecto tiene como objetivo:

- **Predecir el nivel de popularidad** de una canción usando datos musicales.
- **Identificar qué atributos influyen más** en esa popularidad.
- Asegurar interpretabilidad en los modelos utilizados.

---

## 🧠 Stack tecnológico

El proyecto fue desarrollado en **Python** (versión 3.11) utilizando herramientas modernas de ciencia de datos:

| Tecnología           | Uso principal                                      |
|----------------------|----------------------------------------------------|
| `pandas`, `numpy`    | Manipulación y análisis de datos                   |
| `matplotlib`, `seaborn` | Visualización exploratoria e interpretativa       |
| `scikit-learn`       | Modelado, preprocesado, selección y validación     |
| `umap-learn`         | Reducción de dimensionalidad no lineal             |
| `GaussianMixture` (sklearn) | Identificación de subpoblaciones             |
| `PCA` (sklearn)      | Reducción lineal de dimensionalidad                |
| `shap`               | Interpretación avanzada de modelos mediante valores SHAP |

---

## ⚙️ Enfoque del proyecto

### 1. Preprocesamiento guiado por EDA
- Tratamiento de outliers (Isolation Forest).
- Codificación de variables categóricas (`explicit`, `key`, `mode`, `time_signature`, `track_genre`).
- Ajuste de un modelo **Gaussian Mixture Model (GMM)** sobre la variable objetivo.

### 2. Enriquecimiento semántico
- Incorporación de jerarquías de género musical (basadas en conocimiento experto).

### 3. Reducción de dimensionalidad
- Aplicación de **PCA** para conservar el 95% de la varianza explicada.
- Alternativamente, se visualiza con **UMAP** para exploración estructural.

---

## 🧪 Modelos evaluados

Se probaron y compararon múltiples modelos para balancear precisión e interpretabilidad:

- **Modelos lineales**:
  - `LinearRegression`
  - `Lasso`
  - `Ridge`
  - `ElasticNet` (con ajuste de regularización)

- **Modelos no lineales**:
  - `DecisionTreeRegressor` (modelo explicativo)

### Validación:
- **Cross Validation** con 5 folds
- **RandomizedSearchCV** para optimización de hiperparámetros

### Interpretabilidad avanzada:
- Uso de **SHAP values** para explicar el impacto de cada característica en las predicciones, proporcionando una visión granular y global sobre la importancia de las variables en los modelos.

---

## 🏆 Resultados



---

## 👥 Equipo

Desarrollado por el equipo **NoVirusPincha**:
- [Jose Ángel Pérez Garrido](https://github.com/japgarrido)
- [Miguel José Da Silva Araujo](https://github.com/Enmiguelado)
- [Jose Luis Ruanova Lea](https://github.com/lruanova)

Oracle AI Hackathon 2025 🚀