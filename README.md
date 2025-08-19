# Predicción de Churn en TelecomX: Un Enfoque de Machine Learning

## Descripción del Proyecto

Como Analista Junior de Machine Learning en TelecomX, he desarrollado un pipeline completo para predecir la cancelación de clientes (churn) utilizando técnicas avanzadas de análisis de datos y modelado predictivo. Mi objetivo es anticipar el abandono de clientes y proponer estrategias accionables para maximizar la retención y el valor del negocio.

---

## Estructura del Cuaderno

### 🛠️ Preparación de los Datos

En esta sección, me enfoqué en extraer el archivo tratado, eliminar columnas irrelevantes y aplicar técnicas de encoding para transformar las variables categóricas. Verifiqué la proporción de cancelación (churn) y, si fue necesario, balanceé las clases para evitar sesgos en el modelo. Finalmente, normalicé o estandaricé los datos según la necesidad del modelo.

### 🎯 Correlación y Selección de Variables

Realicé un análisis de correlación para identificar las variables más influyentes en el churn. Complementé este análisis con una revisión dirigida, seleccionando aquellas variables que, por su naturaleza o impacto, consideré críticas para el modelado.

### 🤖 Modelado Predictivo

Separé los datos en conjuntos de entrenamiento y prueba, y entrené varios modelos de clasificación. Evalué su desempeño utilizando métricas clave, buscando siempre el equilibrio entre precisión y capacidad de detección de clientes en riesgo.

### 📋 Interpretación y Conclusiones

Analicé la importancia de las variables en los modelos y extraje conclusiones sobre los factores que más inciden en la cancelación. Finalmente, elaboré recomendaciones estratégicas basadas en los hallazgos y el rendimiento del modelo.

---

## 🎯 CONCLUSIONES ESTRATÉGICAS Y RECOMENDACIONES

---

### 🏆 MODELO RECOMENDADO PARA PRODUCCIÓN: Random Forest

Después de comparar varios algoritmos, seleccioné el modelo Random Forest para producción, ya que logró el mejor balance entre precisión y recall.

#### 📊 Rendimiento del modelo:
- **Accuracy:** 77.4% (1635 clientes clasificados correctamente)
- **Precision:** 55.7% (56% de predicciones de churn son correctas)
- **Recall:** 72.7% (Detecta 73% de clientes que realmente abandonan)
- **F1-Score:** 0.631 (Balance óptimo entre precisión y recall)

#### 💼 Impacto en el negocio:
- **Clientes churn detectados correctamente:** 408 de 561
- **Clientes churn no detectados:** 153 (27.3%)
- **Falsas alarmas:** 325 clientes marcados incorrectamente

---

### 🔍 Principales factores que influyen en churn

A partir del análisis de importancia de variables y la comparación entre modelos, identifiqué los siguientes factores críticos:

1. **Tiempo como cliente (tenure):** A mayor antigüedad, menor probabilidad de churn.
2. **Cargo total acumulado:** Clientes con mayor gasto histórico tienden a quedarse.
3. **Contrato mes a mes:** Los clientes sin compromiso contractual son más propensos a abandonar.
4. **Tener dependientes:** Reduce la probabilidad de churn.
5. **Cargo mensual alto:** Aumenta el riesgo de abandono.
6. **Facturación sin papel y pago con cheque electrónico:** Asociados a mayor churn.
7. **Soporte técnico:** La falta de soporte incrementa el riesgo.
8. **Tipo de servicio de internet:** Usuarios de fibra óptica presentan tasas de churn superiores.

---

### 💡 Interpretación de factores clave

- **Contratos mes a mes:** Los clientes sin compromiso son más volátiles.
- **Pagos con cheque electrónico:** Este método, menos conveniente, se asocia a mayor churn.
- **Tenure bajo:** Los clientes nuevos (<12 meses) son más propensos a irse.
- **Servicios adicionales:** La ausencia de servicios como seguridad online incrementa el riesgo.
- **Cargos mensuales altos:** Clientes con tarifas elevadas muestran mayor tendencia al churn.
- **Servicio de fibra óptica:** Presenta mayor tasa de abandono.
- **Edad del cliente:** Los adultos mayores muestran patrones de retención distintos.

---

### 🎯 Estrategias de retención basadas en Machine Learning

#### 🟥 Inmediatas (0-3 meses)
1. Implementar un sistema de scoring predictivo usando el modelo entrenado.
2. Crear alertas automáticas para clientes con alta probabilidad de churn (>70%).
3. Desarrollar campañas específicas para contratos mes a mes.
4. Incentivar la migración a métodos de pago automáticos.
5. Programa de onboarding intensivo para clientes nuevos.

#### 🟨 Mediano plazo (3-12 meses)
1. Ofertas personalizadas según el perfil de riesgo.
2. Optimización de precios para clientes de alto valor en riesgo.
3. Mejorar la experiencia de usuario en servicios de fibra óptica.
4. Upselling proactivo de servicios adicionales.
5. Sistema de retención automatizado con múltiples puntos de contacto.

#### 🟩 Largo plazo (12+ meses)
1. Desarrollar modelos predictivos más avanzados con nuevas variables.
2. Implementar machine learning en tiempo real para detección temprana.
3. Programa de fidelización basado en análisis de comportamiento.
4. Optimización del portafolio de productos según análisis de churn.
5. Segmentación avanzada de clientes para estrategias personalizadas.

---

### 💰 Estimación de Retorno de Inversión (ROI)

- **Tasa de churn actual:** 26.5%
- **Clientes churn detectables:** 408
- **Clientes salvables estimados:** 122 (30% efectividad)
- **Ingresos salvados anuales:** $95,160
- **Costo de implementación:** $100,000
- **Mantenimiento anual:** $50,000
- **ROI primer año:** -36.6%
- **Payback estimado:** 3.3 años

---

### 🚀 Próximos pasos recomendados

1. Validar el modelo con datos más recientes antes de la implementación.
2. Desarrollar un pipeline de datos automatizado para scoring en tiempo real.
3. Capacitar a los equipos de customer success en el uso del modelo.
4. Implementar un sistema de feedback para mejorar continuamente el modelo.
5. Establecer métricas de negocio para medir el impacto de las estrategias de retención.
6. Crear un dashboard ejecutivo con KPIs de churn y efectividad de retención.

---

## 📋 Resumen ejecutivo final

1. Seleccioné Random Forest como modelo óptimo (F1-Score: 63.1%).
2. El modelo detecta el 73% de los clientes que abandonarán.
3. Los principales factores de churn son: contratos mes a mes, método de pago y tenure.
4. El ROI proyectado es de -37% en el primer año, con $95,160 en ingresos salvados.
5. Recomiendo la implementación inmediata para maximizar la retención.
6. El sistema es escalable y mejorará con más datos y feedback.