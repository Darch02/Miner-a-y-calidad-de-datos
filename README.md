# Proyecto de Minería de Datos: Predicción de Empleabilidad de Estudiantes

Este proyecto tiene como objetivo **predecir si un estudiante será contratado** durante el proceso de reclutamiento en el campus universitario, utilizando técnicas de **Minería de Datos y Machine Learning**.  
El trabajo se divide en tres grandes fases: **Calidad de Datos**, **Minería de Datos** y **Despliegue del Modelo**.

---

## 1. Calidad de Datos

### A. Perfilado de Datos
Se generó un **perfilado de los datos en Python**, donde se evaluaron características estadísticas, tipos de variables, distribución de valores y presencia de datos faltantes.  
El resultado del perfilado fue exportado en formato **HTML** e incluido en este repositorio.

### B. Diagnóstico de Calidad de Datos
A partir del perfilado, se evaluaron las principales **dimensiones de calidad de datos**, entre ellas:

- **Completitud:** Se identificaron valores faltantes y se aplicaron estrategias de imputación.
- **Consistencia:** Se verificaron rangos válidos y coherencia entre variables relacionadas.
- **Exactitud:** Se depuraron registros con errores evidentes.
- **Validez:** Se revisaron los tipos de datos y dominios de valores permitidos.
- **Unicidad:** Se eliminaron posibles duplicados.

### C. Limpieza y Mejora
Los datos fueron tratados mediante:
- Imputación de valores faltantes.
- Codificación de variables categóricas.
- Normalización de variables numéricas.
- Eliminación de inconsistencias detectadas.

---

## 2. Minería de Datos

### A. Objetivo del Modelo
El objetivo del modelo predictivo es **anticipar si un estudiante será colocado en una oferta laboral**, a partir de variables como:
- Rendimiento académico (SSC, HSC, grado, MBA).
- Especialización profesional.
- Experiencia laboral previa.
- Factores personales y de desempeño en pruebas.

Con esto se busca **identificar patrones que influyen en la empleabilidad** y apoyar la toma de decisiones para mejorar la inserción laboral de los estudiantes.

---

### B. Modelos Predictivos Evaluados

Se desarrollaron y evaluaron los siguientes modelos:

| Modelo | Precisión (Accuracy) | Conclusión |
|---------|----------------------|-------------|
| 🌳 Árbol de Decisión | 76.4% | Rendimiento medio, base inicial sólida pero mejorable con tuning. |
| 🌲 Random Forest | 87.64% | Mejor desempeño general, equilibrio entre precisión y recall. |
| 🤝 KNN | 65.17% | Bajo rendimiento, sensible a la distancia entre puntos. |
| 🧠 Red Neuronal | 73.03% | Rendimiento moderado, necesita más iteraciones e hiperajustes. |
| ⚙️ SVM | 85.39% | Muy buen desempeño, comparable al Random Forest. |

**Conclusión general:**  
Los modelos de **Random Forest y SVM** demostraron el mejor desempeño, con altos valores de precisión y F1-score, siendo los más adecuados para este conjunto de datos.

---

### C. Hiperparametrización

Se aplicó **GridSearchCV** para optimizar los hiperparámetros del modelo de **Random Forest**, obteniendo el mejor rendimiento con la siguiente configuración:

```python
RandomForestClassifier(
    bootstrap=True,
    criterion='gini',
    max_depth=None,
    max_features='sqrt',
    max_samples=0.7,
    min_samples_leaf=2,
    min_samples_split=2,
    n_estimators=100,
    random_state=42
)


Por:
Juana Jaramillo y Valentina Soto
