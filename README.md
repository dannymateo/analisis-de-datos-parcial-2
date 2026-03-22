# Proyecto — Análisis de Datos (Evaluación 2)

**Instituto Tecnológico Metropolitano** · Departamento de Sistemas · Ingeniería de Sistemas  
**Curso:** Análisis de Datos · **Docente:** Daniel Alexis Nieto Mora · **Semestre:** 2025-2


Este repositorio documenta el **segundo evento evaluativo**: exploración de bases de datos, **análisis exploratorio (EDA)** y **preprocesamiento con reducción de dimensionalidad**, según el enunciado oficial del curso.

---

## Objetivo del proyecto

Aplicar lo visto en las primeras semanas del curso en un proyecto práctico que incluya:

1. Explorar **al menos tres bases de datos** de **al menos dos tipos** distintos (p. ej. tabular, imágenes, audio, texto).
2. **Justificar** la elección de la base final (completitud, relevancia, documentación, manejabilidad).
3. Realizar un **EDA** completo sobre la base seleccionada.
4. Aplicar **preprocesamiento** (codificación, escalado) y **reducción de dimensionalidad** (p. ej. PCA).

**Entregables del curso:** repositorio en GitHub con notebooks organizados, este README y **commits** que permitan identificar la participación de cada integrante; **video explicativo** (máx. 8 minutos) con el proceso, criterios de selección, fragmentos relevantes del código, dificultades, hallazgos y conclusiones.

---

## Fases del trabajo

| Fase | Contenido (según enunciado) | Dónde está en el repo |
|------|-----------------------------|-------------------------|
| **1. Exploración de bases** | Fuente y tipo de datos, registros/atributos/tamaño, documentación, aplicaciones posibles; criterios de selección | Carpeta [`data/`](data/): revisión por dataset en `Revision.txt` |
| **2. EDA** | Valores faltantes, outliers (gráficos + IQR/z-score), distribuciones, análisis uni- y multivariado, correlaciones / tablas cruzadas, hipótesis, visualizaciones, ≥5 insights | Notebook principal [`Covid_19.ipynb`](Covid_19.ipynb) (secciones de EDA) |
| **3. Preprocesamiento** | Codificación de categóricas, escalado de numéricas, PCA (u otro método) y visualización | [`Covid_19.ipynb`](Covid_19.ipynb) (sección de preprocesamiento) |

---

## Bases de datos consideradas

| Dataset | Tipo | Notas |
|---------|------|--------|
| **COVID-19 Colombia** (datos.gov.co) | Tabular | Base **seleccionada** para el análisis principal; datos abiertos oficiales. |
| **Titanic** (Kaggle) | Tabular | Exploración documentada en `data/titanic/`. |
| **Fashion MNIST** (Kaggle) | Imágenes | Exploración documentada en `data/Fashion/`. |

La documentación por fuente (características, tamaño, aplicaciones) está en:

- [`data/COVID/Revision.txt`](data/COVID/Revision.txt)
- [`data/titanic/revisión.txt`](data/titanic/revisión.txt)
- [`data/Fashion/Revision.txt`](data/Fashion/Revision.txt)

---

## Estructura del repositorio

```
├── README.md
├── Covid_19.ipynb            # Notebook: carga, EDA, preprocesamiento, 
├── Entrega_Evaluacion2.pdf   # Enunciado en PDF
└── data/
    ├── COVID/Revision.txt
    ├── Fashion/Revision.txt
    └── titanic/revisión.txt
```

---

## Requisitos y ejecución

- **Python 3.10+** (recomendado)

Dependencias típicas del proyecto (ajusta si tu entorno usa versiones fijas):

```bash
pip install pandas numpy seaborn matplotlib scikit-learn jupyter
```

**Ejecutar el análisis:**

```bash
jupyter notebook Covid_19.ipynb
```

> El notebook consume datos desde la **API** de datos abiertos de Colombia (`datos.gov.co`). Se requiere **conexión a internet** al ejecutar las celdas de carga. Si la API aplica límite de filas, los resultados corresponden a la muestra descargada.

---

## Integrantes

1. Danny Mateo Hernández Sánchez
2. Stefany Builes Lopera
3. Leidy Daihana Mora Trujillo
4. Alejandra Alvarez Serna
