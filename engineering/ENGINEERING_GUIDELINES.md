# Engineering Guidelines

## Purpose

This document defines the engineering practices adopted throughout the laboratory.

Its objective is to establish a consistent development methodology that promotes maintainability, reproducibility, technical excellence and continuous learning.

Every repository developed within the laboratory should follow these guidelines unless a justified architectural decision states otherwise.

---

# Engineering Philosophy

Engineering is a decision-making process.

Writing code is only one stage within a much larger lifecycle.

A successful project is not measured by the amount of code produced, but by the quality of its design, its documentation, its reproducibility and its ability to evolve over time.

---

# Development Lifecycle

Every project follows the same lifecycle.

```
Idea
    ↓
Research
    ↓
Requirements
    ↓
Architecture
    ↓
Architecture Decision Records (ADRs)
    ↓
Implementation
    ↓
Testing
    ↓
Benchmarking & Evaluation
    ↓
Documentation
    ↓
Review
    ↓
Release
```

Each phase is mandatory.

Skipping a phase requires explicit justification.

---

# Phase 1 — Research

Every project begins by understanding the problem.

Research should answer questions such as:

- What problem are we solving?
- Why is it relevant?
- What solutions already exist?
- Which scientific papers, books or technical references are available?
- What are the current limitations?

Research should be documented whenever it influences future engineering decisions.

---

# Phase 2 — Requirements

Before implementation, projects define:

## Functional Requirements

What the system must do.

Examples:

- Ingest PDF documents.
- Retrieve semantically relevant passages.
- Generate cited responses.

## Non-Functional Requirements

How the system should behave.

Examples:

- Scalability
- Performance
- Security
- Reproducibility
- Maintainability
- Observability

---

# Phase 3 — Architecture

Every project should define its architecture before implementation.

Architectural documentation should include:

- high-level system overview;
- component diagram;
- data flow;
- deployment architecture;
- external dependencies;
- design rationale.

Architecture evolves throughout the project but should never be undocumented.

---

# Phase 4 — Architecture Decision Records

Important technical decisions must be recorded.

Examples include:

- choosing a database;
- selecting an ML framework;
- adopting a communication protocol;
- defining deployment strategies.

Each ADR should explain:

- context;
- decision;
- alternatives considered;
- consequences.

---

# Phase 5 — Implementation

Implementation should follow these principles:

- small, focused modules;
- single responsibility;
- explicit interfaces;
- readable code;
- meaningful naming;
- minimal coupling;
- high cohesion.

The objective is not only functional software, but understandable software.

---

# Phase 6 — Testing

Testing is part of development.

Projects should include tests appropriate to their scope, including:

- unit tests;
- integration tests;
- API tests;
- regression tests;
- data validation tests;
- end-to-end tests when applicable.

New functionality should not reduce existing test coverage.

---

# Phase 7 — Benchmarking and Evaluation

Performance should be measured rather than assumed.

Depending on the project, benchmarking may include:

- execution time;
- memory usage;
- scalability;
- latency;
- throughput;
- accuracy;
- precision;
- recall;
- F1-score;
- cost analysis.

Benchmark methodology should be documented to ensure reproducibility.

---

# Phase 8 — Documentation

Documentation evolves together with the project.

Every repository should provide documentation for:

- users;
- contributors;
- maintainers;
- researchers.

Documentation should explain not only how the system works, but also why it was designed that way.

---

# Phase 9 — Review

Before merging any feature, verify:

- requirements satisfied;
- tests passing;
- documentation updated;
- benchmarks executed (when applicable);
- ADRs written (if required);
- code reviewed;
- style guidelines respected.

No feature is complete until it satisfies these conditions.

---

# Phase 10 — Release

A release represents a stable milestone.

Every release should include:

- version number;
- changelog;
- documentation updates;
- reproducible environment;
- validated benchmarks (when applicable).

Releases should be meaningful, not arbitrary.

---

# Definition of Done

A task is considered complete only if:

- implementation is finished;
- tests pass successfully;
- documentation has been updated;
- architectural implications have been documented;
- quality requirements have been satisfied;
- reproducibility has been verified.

"Working" is not equivalent to "finished."

---

# Continuous Improvement

Engineering standards are expected to evolve.

Every completed project should contribute improvements to this playbook.

The laboratory itself is a living system.

Its engineering practices should improve together with the people who apply them.

# Guía de Ingeniería

## Propósito

Este documento define las prácticas de ingeniería adoptadas por el laboratorio.

Su objetivo es establecer una metodología de desarrollo consistente que favorezca la mantenibilidad, la reproducibilidad, la excelencia técnica y el aprendizaje continuo.

Todos los repositorios desarrollados dentro del laboratorio deberán seguir estas directrices salvo que exista una decisión arquitectónica debidamente justificada.

---

# Filosofía de Ingeniería

La ingeniería es un proceso de toma de decisiones.

Escribir código constituye únicamente una etapa dentro de un ciclo de vida mucho más amplio.

El éxito de un proyecto no se mide por la cantidad de código desarrollado, sino por la calidad de su diseño, su documentación, su reproducibilidad y su capacidad para evolucionar con el tiempo.

---

# Ciclo de Desarrollo

Todos los proyectos seguirán el mismo ciclo de vida.

```
Idea
    ↓
Investigación
    ↓
Requisitos
    ↓
Arquitectura
    ↓
Registros de Decisiones Arquitectónicas (ADR)
    ↓
Implementación
    ↓
Pruebas
    ↓
Benchmarks y Evaluación
    ↓
Documentación
    ↓
Revisión
    ↓
Release
```

Cada fase es obligatoria.

Omitir una fase requerirá una justificación explícita.

---

# Fase 1 — Investigación

Todo proyecto comienza comprendiendo el problema.

La investigación debe responder, entre otras, a las siguientes preguntas:

- ¿Qué problema queremos resolver?
- ¿Por qué es relevante?
- ¿Qué soluciones existen actualmente?
- ¿Qué artículos científicos, libros o referencias técnicas son relevantes?
- ¿Cuáles son las limitaciones del estado del arte?

Toda investigación que influya en decisiones posteriores deberá quedar documentada.

---

# Fase 2 — Requisitos

Antes de comenzar la implementación se definirán:

## Requisitos Funcionales

Describen qué debe hacer el sistema.

Ejemplos:

- Ingerir documentos PDF.
- Recuperar fragmentos relevantes.
- Generar respuestas con citas.

## Requisitos No Funcionales

Describen cómo debe comportarse el sistema.

Ejemplos:

- Escalabilidad.
- Rendimiento.
- Seguridad.
- Reproducibilidad.
- Mantenibilidad.
- Observabilidad.

---

# Fase 3 — Arquitectura

Todo proyecto deberá definir su arquitectura antes de comenzar la implementación.

La documentación arquitectónica incluirá, como mínimo:

- visión general del sistema;
- diagrama de componentes;
- flujo de datos;
- arquitectura de despliegue;
- dependencias externas;
- justificación del diseño.

La arquitectura puede evolucionar, pero nunca debe dejar de estar documentada.

---

# Fase 4 — Registros de Decisiones Arquitectónicas (ADR)

Las decisiones técnicas con impacto a largo plazo deberán registrarse mediante ADR.

Entre ellas:

- selección de bases de datos;
- elección de frameworks;
- estrategias de despliegue;
- protocolos de comunicación;
- decisiones estructurales.

Cada ADR deberá explicar:

- contexto;
- decisión;
- alternativas consideradas;
- consecuencias.

---

# Fase 5 — Implementación

La implementación seguirá los siguientes principios:

- módulos pequeños y cohesionados;
- responsabilidad única;
- interfaces explícitas;
- código legible;
- nombres significativos;
- bajo acoplamiento;
- alta cohesión.

El objetivo no es únicamente construir software funcional, sino software comprensible.

---

# Fase 6 — Pruebas

Las pruebas forman parte del desarrollo.

Cada proyecto incorporará las que correspondan a su alcance:

- pruebas unitarias;
- pruebas de integración;
- pruebas de API;
- pruebas de regresión;
- validación de datos;
- pruebas extremo a extremo cuando proceda.

La incorporación de nuevas funcionalidades nunca deberá reducir la cobertura existente.

---

# Fase 7 — Benchmarks y Evaluación

El rendimiento debe medirse, nunca suponerse.

Dependiendo del proyecto podrán evaluarse:

- tiempo de ejecución;
- consumo de memoria;
- escalabilidad;
- latencia;
- throughput;
- precisión;
- recall;
- F1-score;
- coste computacional.

La metodología empleada deberá documentarse para garantizar la reproducibilidad.

---

# Fase 8 — Documentación

La documentación evoluciona junto con el proyecto.

Todo repositorio proporcionará documentación dirigida a:

- usuarios;
- colaboradores;
- mantenedores;
- investigadores.

La documentación debe explicar no solo cómo funciona el sistema, sino también por qué fue diseñado de esa manera.

---

# Fase 9 — Revisión

Antes de integrar cualquier funcionalidad deberá verificarse que:

- los requisitos se han cumplido;
- todas las pruebas superan correctamente;
- la documentación está actualizada;
- los benchmarks se han ejecutado cuando corresponda;
- los ADR se han redactado cuando sean necesarios;
- el código ha sido revisado;
- se respetan los estándares del laboratorio.

Una funcionalidad no se considera terminada hasta cumplir todos estos criterios.

---

# Fase 10 — Release

Una release representa un hito estable del proyecto.

Toda release deberá incluir:

- número de versión;
- registro de cambios;
- documentación actualizada;
- entorno reproducible;
- benchmarks validados cuando corresponda.

Las versiones deben representar avances significativos y verificables.

---

# Definición de Terminado

Una tarea únicamente se considerará finalizada cuando:

- la implementación esté completa;
- todas las pruebas hayan sido superadas;
- la documentación se haya actualizado;
- las implicaciones arquitectónicas hayan sido registradas;
- los requisitos de calidad se hayan satisfecho;
- la reproducibilidad haya sido verificada.

"Funciona" no significa "está terminado".

---

# Mejora Continua

Los estándares de ingeniería evolucionan junto con el laboratorio.

Cada proyecto deberá contribuir a mejorar este playbook mediante nuevas prácticas, plantillas o lecciones aprendidas.

El laboratorio es un sistema vivo.

Su metodología debe mejorar continuamente.
