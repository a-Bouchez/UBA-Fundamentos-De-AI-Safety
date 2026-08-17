# Fundamentos de AI Safety

Repositorio con el material y los trabajos prácticos de la materia **Fundamentos de AI Safety**, dictada por **Sergio Alejandro Abriola**.

## Sobre la materia

Este curso teórico explora los principales desafíos para garantizar el desarrollo seguro y alineado de sistemas de IA avanzados, con foco en sistemas generales. Si bien el estudio de estos temas tiene una larga trayectoria, los avances recientes en sistemas de IA cada vez más capaces volvieron a estos tópicos sumamente relevantes.

El programa arranca con conceptos básicos de IA y machine learning, aborda cuestiones filosóficas sobre la noción de AGI (artificial general intelligence) y recorre problemas clásicos del área como la formación de metas, la distinción entre metas instrumentales y terminales, la tesis de ortogonalidad y la convergencia instrumental. Se analizan además las implicancias de la IA avanzada, incluyendo cómo estos sistemas pueden desarrollar objetivos o valores que no coinciden con las intenciones originales de quienes los diseñaron, así como casos de estudio concretos que ilustran comportamientos inesperados y las formas en que distintas estrategias de mitigación pueden fallar frente a sistemas con suficiente poder de optimización.

A lo largo del curso también se profundiza en el problema de la alineación de objetivos, el alineamiento engañoso, el control de capacidades, el AI containment, los oráculos, la especificación de objetivos, los optimizadores base y mesa-optimizadores, los modelos de recompensa, la (mal)generalización de metas, las técnicas de supervisión escalables y la interpretabilidad. Finalmente, se discute el rol de la gobernanza y la regulación, analizando —desde una perspectiva de teoría de juegos y simulación bajo incertidumbre— cómo distintas políticas pueden favorecer o evitar equilibrios subóptimos y dinámicas del tipo "race to the bottom".

### Temario

- Introducción al machine learning: redes neuronales, descenso del gradiente, aprendizaje por refuerzo.
- LLMs: RLHF, predicciones condicionadas, simuladores.
- Conceptos básicos de AGI: sistemas específicos vs. sistemas generales, características de alto nivel.
- Especificación de metas y *specification gaming*: Ley de Goodhart, tesis de ortogonalidad, aprendizaje de preferencias humanas, optimizadores base y mesa-optimizadores, objetivos terminales e instrumentales, convergencia instrumental, alineamiento engañoso.
- Corregibilidad y el problema del apagado.
- Control de capacidades: *containment*, oráculos, profecías autocumplidas, oráculos contrafácticos.
- Supervisión escalable: amplificación iterada, técnicas adversariales.
- Interpretabilidad: mecanicista y conceptual, detección de mentiras.
- Gobernanza, regulación, dinámicas dañinas y escenarios posibles.

## Organización del repositorio

```
.
├── Clases/       # Material teórico de cada clase (slides/PDFs)
└── TPs/          # Trabajos prácticos de la materia
    ├── tp1/          # Informe sobre un área de aplicación de la IA
    └── tp-final/     # Análisis crítico de un paper de AI safety
```

- **`Clases/`**: contiene el material correspondiente a cada clase del curso (presentaciones y apuntes), siguiendo el orden del temario detallado arriba.
- **`TPs/`**: contiene los trabajos prácticos entregados durante la cursada. Cada TP tiene su propia carpeta con un README que explica de qué trata, su enfoque y sus conclusiones principales.

Cada subcarpeta de `TPs/` incluye su propio README con el detalle del trabajo correspondiente.
