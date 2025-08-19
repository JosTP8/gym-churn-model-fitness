# 🏋️‍♂️ Predicción de Cancelación y Clustering — Model Fitness

## 📌 Descripción
Proyecto de analítica para una cadena de gimnasios. Se construyen modelos para **predecir churn** (cancelación de membresía) y se segmentan clientes con **K-Means** para diseñar estrategias de retención.

## 🎯 Objetivos
- Predecir probabilidad de churn el próximo mes.
- Identificar factores de riesgo de cancelación.
- Generar **perfiles de clientes** (clústeres) y su tasa de churn.
- Proponer acciones de retención.

## 📂 Dataset
Datos simulados de TripleTen. Archivo: `gym_churn_us.csv` (no incluido por tamaño/licencia).  
Consulta `data/README.md` para obtenerlo.

**Variables clave:** edad, cercanía al gimnasio, contrato (meses), meses restantes, clases grupales, frecuencia histórica y actual, gastos adicionales, etc.  
**Target:** `Churn` (1 = se fue, 0 = permanece).

## 🔍 Metodología
1. **EDA:** descriptivos, histogramas, correlación.
2. **Modelado:** Regresión Logística y **Random Forest** (mejor recall).
3. **Clustering:** dendrograma (Ward) + **K-Means (k=5)**; tasas de churn por grupo.
4. **Recomendaciones** de negocio por clúster.

## 📈 Resultados (resumen)
- Contratos cortos + baja frecuencia ⇒ **alto riesgo** de churn.  
- Participar en **clases grupales** y contratos de 6–12 meses ⇒ **mayor lealtad**.  
- Random Forest superó a Regresión Logística en *recall*.

## ⚙️ Reproducibilidad
```bash
pip install -r requirements.txt
jupyter notebook notebook.ipynb

🧰 Tech Stack

Python (pandas, numpy, matplotlib, seaborn, scikit-learn, scipy), Jupyter.

🗂️ Estructura
gym-churn-model-fitness/
├── notebook.ipynb
├── vertopal.com_notebook.pdf
├── requirements.txt
├── README.md
├── data/
│   └── README.md
└── imgs/  (gráficas/resultados)

👤 Autor

Josué Téllez
