📊 Predicción de Cancelación de Clientes - Interconnect

Este proyecto busca predecir la tasa de cancelación de clientes de la empresa de telecomunicaciones Interconnect.
El objetivo es identificar con anticipación a los usuarios que podrían dejar el servicio, para ofrecerles códigos promocionales o planes especiales, mejorando así la retención.

🏢 Contexto del Negocio

Interconnect ofrece principalmente dos tipos de servicios:

Telefonía fija → opción de múltiples líneas.

Internet → mediante DSL o fibra óptica.

Servicios adicionales:

Protección de dispositivos (antivirus).

Seguridad en línea (bloqueo de sitios maliciosos).

Soporte técnico.

Backup en la nube.

Streaming de TV y películas.

Clientes pueden elegir entre pago mensual o contrato de 1-2 años, con varios métodos de pago y facturación electrónica.

📂 Datos Utilizados

Archivos enlazados por la columna customerID:

contract.csv → Información de contratos.

personal.csv → Datos personales.

internet.csv → Servicios de Internet.

phone.csv → Servicios de telefonía.

📅 Los datos son válidos a partir del 1 de febrero de 2020.

⚙️ Librerías Principales

Procesamiento y análisis: numpy, pandas, re, datetime.

Visualización: seaborn, matplotlib.

Preprocesamiento y escalado: StandardScaler, MinMaxScaler, LabelEncoder, OneHotEncoder, SimpleImputer.

Balanceo de clases: SMOTE, RandomOverSampler.

Modelado:

Modelos clásicos: LogisticRegression, DecisionTreeClassifier, RandomForestClassifier.

Modelos avanzados: XGBoost, LightGBM, CatBoost, SVC, GradientBoostingClassifier, AdaBoostClassifier.

Selección de características: BorutaPy.

Evaluación: roc_auc_score, precision_score, recall_score, f1_score, confusion_matrix, classification_report.

📈 Resultados de Modelos
Modelo	Accuracy	Precision	Recall	F1-Score	AUC-ROC
Regresión Logística	0.79	0.73	0.66	0.69	0.81
Árbol de Decisión	0.77	0.70	0.65	0.67	0.78
Random Forest	0.81	0.75	0.70	0.72	0.83
XGBoost	0.82	0.76	0.72	0.74	0.83
LightGBM	0.82	0.77	0.72	0.74	0.83
CatBoost	0.83	0.78	0.73	0.75	0.83
Gradient Boosting	0.82	0.77	0.71	0.74	0.82
AdaBoost	0.83	0.78	0.74	0.76	0.84

📌 Conclusión: Aunque varios modelos tienen resultados competitivos, AdaBoost mostró el mejor balance, alcanzando un AUC-ROC ≈ 0.84.

🔍 Conclusiones del Análisis

Factores clave en la cancelación:

Cargos mensuales elevados → influyen directamente en la decisión de cancelar.

Servicio de Internet por fibra óptica → posible relación con la calidad del servicio.

Recomendaciones:

Ofrecer planes diferenciados a clientes con cargos altos.

Dar atención especial a clientes con fibra óptica para evitar cancelaciones.

✅ Impacto Esperado

Con este modelo, Interconnect podrá:

Detectar clientes con mayor riesgo de cancelar.

Implementar campañas de retención personalizadas.

Optimizar la experiencia del cliente.

Reducir la tasa de cancelación y aumentar la estabilidad financiera.