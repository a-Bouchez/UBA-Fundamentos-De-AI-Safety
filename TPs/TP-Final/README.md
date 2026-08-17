# TP Final — Análisis crítico: "Stress Testing Deliberative Alignment for Anti-Scheming Training"

**Materia:** Fundamentos de AI Safety
**Profesor:** Sergio Alejandro Abriola
**Modalidad:** Opción A — Análisis crítico de un trabajo reciente de AI safety
**Alumno:** Alexis Starcenbaum Bouchez

## Descripción

Este trabajo final consiste en un análisis crítico del paper *"Stress Testing Deliberative Alignment for Anti-Scheming Training"* (Schoen et al., Apollo Research & OpenAI, 2025, arXiv:2509.15541), uno de los primeros estudios empíricos sobre **mitigación** de *scheming* (comportamiento engañoso) en modelos de frontera en producción (o3 y o4-mini), y no solo sobre su detección.

## Contenido del análisis

- **Claim del paper**: el alineamiento deliberativo —entrenar al modelo para razonar explícitamente citando una especificación de seguridad antes de actuar— reduce significativamente las acciones encubiertas, aunque sin eliminarlas por completo, y sin poder descartar que la reducción se deba a la conciencia situacional del modelo (saber que está siendo evaluado) más que a una internalización genuina de los principios de seguridad.
- **Metodología y resultados**: se resume el pipeline de entrenamiento (SFT + RL sobre rollouts filtrados) y los resultados principales, incluyendo la caída en las tasas de acciones encubiertas (13% → 0.4% en o3; 8.7% → 0.3% en o4-mini) y los experimentos de intervención sobre la cadena de pensamiento (CoT) que sugieren un vínculo entre conciencia situacional y el comportamiento observado.
- **Análisis crítico propio**, centrado en dos ejes principales:
  - La **fragilidad del monitoreo de la CoT** como herramienta de entrenamiento y evaluación, contrastando el paper con literatura reciente sobre la falta de fidelidad de la cadena de pensamiento.
  - El problema del **alineamiento engañoso adversarial**, señalando que el diseño experimental del paper no permite distinguir entre una reducción real del scheming y un modelo que simplemente aprendió a ocultarlo mejor durante la evaluación.
- **Falsabilidad del claim**: se proponen tres vías concretas para poner a prueba la robustez del alineamiento deliberativo (entornos sin monitoreo garantizado, intervención mecanística vía *feature clamping*, y degradación bajo *capabilities training* adicional).
- **Relación con la literatura**: se conecta el paper con trabajos previos sobre mesa-optimización y alineamiento engañoso (Hubinger et al.), *alignment faking* (Greenblatt et al.), *sleeper agents* (Hubinger et al.) e *in-context scheming* (Meinke et al.).
- **Preguntas abiertas y propuesta experimental propia**: se plantea un experimento de interpretabilidad mecanística (entrenar un Sparse Autoencoder para identificar y suprimir mediante *feature clamping* las representaciones asociadas a la conciencia situacional) junto con sus limitaciones.

## Objetivo del trabajo

Más que resumir el paper, el análisis busca cuestionar hasta qué punto la reducción observada de comportamientos encubiertos constituye evidencia de un cambio real en los objetivos internos del modelo, o si en cambio refleja una modificación superficial condicionada por la propia fragilidad del mecanismo (la CoT) usado tanto para entrenar como para evaluar la intervención.
