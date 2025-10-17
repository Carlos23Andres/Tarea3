# 🌀 README: Optimización por Enjambre de Partículas (PSO)

Basado en Freitas, D., Lopes, L. G., & Morgado-Dias, F. (2020). Particle Swarm Optimisation: A Historical Review up to the Current Developments. Entropy, 22(3), 362.

## 📖 Introducción

El algoritmo de Optimización por Enjambre de Partículas (PSO) fue introducido en 1995 por el ingeniero eléctrico Russell C. Eberhart y el psicólogo social James Kennedy. Su inspiración provino de la observación del comportamiento colectivo en bandadas de aves buscando comida. Este modelo computacional simula la colaboración social, donde un conjunto de partículas (individuos) trabaja conjuntamente para encontrar soluciones óptimas en un espacio de búsqueda multidimensional.

A diferencia de otros algoritmos evolutivos como los Algoritmos Genéticos (GA), el PSO no utiliza operadores de cruce o mutación. En su lugar, se basa en:

- Memoria individual de cada partícula.

- Intercambio de información social dentro del enjambre.

- Actualización de posiciones y velocidades de forma iterativa.

## 🧬 1. Origen Biológico e Inspiración

El PSO surge del estudio de:

- Comportamientos colectivos naturales (aves, peces, insectos).

- Procesos sociales de cooperación.

- Transmisión de información entre individuos.

🐦 En esencia, cada partícula “aprende” tanto de su propio éxito como del éxito de las demás.

Los investigadores observaron que la cooperación entre individuos simples genera comportamientos colectivos complejos.
De esta observación surgió un modelo matemático que simula cómo un grupo de agentes puede explorar y optimizar un entorno sin un control central.

## ⚙️ 2. Funcionamiento Básico

Cada partícula posee:

- Una posición → posible solución.

- Una velocidad → dirección y magnitud del cambio.

- Una memoria de su mejor posición.

Información del mejor individuo global.

## 🧩 Actualización de las partículas

1. Actualización de velocidad:

![Interfaz Inicial](https://raw.githubusercontent.com/Carlos23Andres/Tarea3/main/Imagenes/Captura%20desde%202025-10-16%2019-20-33.png)

2. Actualización de posición:

![Interfaz Inicial](https://raw.githubusercontent.com/Carlos23Andres/Tarea3/main/Imagenes/Captura%20desde%202025-10-16%2019-21-16.png)

🔁 Este proceso se repite hasta cumplir un criterio de parada (máximo de iteraciones o error mínimo).



## 📈 3. Evolución del PSO y Principales Mejoras

### 🪶 a. Control de Convergencia

- Peso de Inercia (ω) – Introducido por Shi y Eberhart (1998).
Controla la exploración (ω alto) y explotación (ω bajo).

- Factor de Constricción (K) – Clerc (1999).
Garantiza convergencia estable al escalar las velocidades.

- PSO Adaptativo (APSO) – Zhan et al. (2009).
Ajusta dinámicamente los parámetros según el estado evolutivo del enjambre.

### 🌐 b. Estructuras de Vecindad

- gbest (global) → todas las partículas comparten información → convergencia rápida.

- lbest (local) → comunicación solo entre vecinos → más diversidad.

- Vecindarios dinámicos (Suganthan, 1999) → el radio de interacción aumenta con el tiempo.

### 🧪 c. Hibridaciones y Algoritmos Combinados

- PSO + GA (Algoritmos Genéticos) → incorpora selección, cruce y mutación.

- PSO + DE (Evolución Diferencial) → fortalece exploración global.

- PSO + SA (Recocido Simulado) → mejora escape de óptimos locales.

- PSO + ACO / ABC / Cuco → aprovecha estrategias de búsqueda bioinspiradas.


### ⚡ d. Paralelización y Computación Distribuida

- PPSO (Parallel PSO) → usa CPUs o GPUs para evaluar partículas simultáneamente.

- Estrategias síncronas/asíncronas → balancean eficiencia y precisión.

- Implementaciones MapReduce y Load Balancing → optimizan entornos de clúster y nube.

💻 PSO paralelo es esencial para problemas de alta dimensionalidad y big data.


### 🎯 e. Extensiones Especializadas

- MOPSO (Multi-Objective PSO) → maneja múltiples objetivos y genera frentes de Pareto.

- PSO con Restricciones → usa penalizaciones o métodos de preservación de factibilidad.

- PSO Multimodal → identifica múltiples óptimos simultáneamente.

## 🧠 4. Aplicaciones Reales

```text

| Campo                         | Aplicación                                                |
| ----------------------------- | --------------------------------------------------------- |
| 🧮 Redes Neuronales           | Entrenamiento de pesos y estructura.                     |
| 🧬 Bioinformática             | Clasificación y alineamiento genómico.                       |
| ⚡ Ingeniería                 | Diseño de antenas, controladores, estructuras.                    |
| 🛰️ Robótica y Transporte      | Planificación de rutas, control autónomo.                       |
| 💻 Procesamiento de Señales   | Filtrado adaptativo, análisis de ECG, imágenes.                  |
| 🏭 Planificación y Scheduling | Asignación de tareas y recursos en sistemas distribuidos.       |

```

## 🚀 5. Pasos para Implementar PSO (Guía Práctica)

1. Definir la función objetivo → qué se quiere minimizar o maximizar.

2. Inicializar partículas con posiciones y velocidades aleatorias.

3. Evaluar el fitness de cada partícula.

4. Actualizar pbest y gbest según los mejores resultados.

5. Actualizar velocidades y posiciones con las ecuaciones base.

6. Repetir hasta cumplir el criterio de parada.

7. Registrar y visualizar resultados.

🧮 Tip: Ajusta cuidadosamente los parámetros (ω, φ1, φ2) para equilibrar exploración y explotación.


## 📚 6. Conclusiones y Perspectivas Futuras

El PSO sigue evolucionando hacia nuevas fronteras:

- 🤝 Integración con Aprendizaje Profundo – optimización de hiperparámetros y redes neuronales.

- ☁️ Computación en la Nube y Escalamiento Exascale – PSO distribuido masivo.

- 🧩 Explicabilidad (XAI) – PSO aplicado a modelos interpretables.

- 🧠 Autoajuste Inteligente – PSO con aprendizaje autónomo de parámetros.

## 📎 Referencia Principal

Freitas, D., Lopes, L. G., & Morgado-Dias, F. (2020). Particle Swarm Optimisation: A Historical Review up to the Current Developments. Entropy, 22(3), 362.
DOI: 10.3390/e22030362

## 👥 Autor

- *Carlos Andrés Suárez Torres* → [Carlos23Andres](https://github.com/Carlos23Andres)  
