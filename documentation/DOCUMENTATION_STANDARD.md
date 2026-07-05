# DOCUMENTATION_STANDARD.md (English)

# Documentation Standard

## Purpose

This document defines the documentation standards adopted throughout the laboratory.

Documentation is considered a first-class engineering artifact. It evolves together with the software and plays a fundamental role in maintainability, reproducibility, collaboration and knowledge transfer.

Every project developed within the laboratory should comply with this standard unless explicitly justified otherwise.

---

# Documentation Philosophy

Documentation is not written after development.

Documentation is part of development.

Every architectural decision, experiment, benchmark and implementation should be documented while the project evolves.

Good documentation explains:

- what the system does;
- why it exists;
- how it works;
- why specific decisions were made.

---

# Objectives

Project documentation should:

- enable reproducibility;
- facilitate onboarding;
- preserve engineering knowledge;
- support maintenance;
- justify technical decisions;
- document experiments;
- serve as educational material.

Documentation is intended for both present and future contributors.

---

# Documentation Principles

Every document should be:

## Accurate

Documentation must reflect the current state of the project.

Outdated documentation should be updated or removed.

---

## Clear

Write concise, precise and unambiguous explanations.

Avoid unnecessary jargon.

---

## Complete

Document enough information for another engineer to understand and continue the project without external guidance.

---

## Consistent

Naming, formatting, terminology and structure should remain consistent across all repositories.

---

## Reproducible

Whenever experiments or benchmarks are described, sufficient information should be provided to reproduce them.

---

# Documentation Levels

Each project contains multiple layers of documentation.

## Level 1 — Repository Documentation

Mandatory.

Includes:

- README
- LICENSE
- CHANGELOG
- CONTRIBUTING (when applicable)

Purpose:

Provide a quick understanding of the project.

---

## Level 2 — Engineering Documentation

Documents intended for developers.

Examples:

- Project Charter
- Architecture Overview
- ADRs
- Development Guide
- Deployment Guide
- API Reference

Purpose:

Explain how the system is designed and maintained.

---

## Level 3 — Scientific Documentation

Required whenever the project includes algorithms, models or experiments.

Examples:

- research notes;
- benchmark reports;
- mathematical derivations;
- experiment logs;
- model evaluation.

Purpose:

Explain the scientific reasoning behind the project.

---

## Level 4 — User Documentation

Intended for end users.

Examples:

- installation guide;
- user guide;
- CLI reference;
- API usage examples;
- tutorials.

Purpose:

Enable users to operate the software efficiently.

---

# Standard Project Documentation

Every project should include, when applicable:

```text
README.md
PROJECT_CHARTER.md
ARCHITECTURE.md
CHANGELOG.md
CONTRIBUTING.md
API_REFERENCE.md
INSTALLATION.md
DEVELOPMENT.md
DEPLOYMENT.md
BENCHMARK_REPORT.md
ENGINEERING_JOURNAL.md
```

Machine Learning projects should additionally include:

```text
MODEL_CARD.md
DATASET_CARD.md
EXPERIMENT_REPORT.md
```

---

# README Structure

Every README should include:

- Project description
- Motivation
- Features
- Technology stack
- Architecture overview
- Installation
- Usage
- Documentation links
- Roadmap
- License

The README should provide an overview without duplicating detailed documentation.

---

# Documentation Directory

Projects should organize documentation as follows:

```text
docs/

├── architecture/
├── api/
├── development/
├── deployment/
├── research/
├── benchmark/
├── reports/
├── adr/
├── assets/
└── images/
```

The structure may evolve according to project complexity.

---

# Diagrams

Whenever appropriate, documentation should include diagrams such as:

- C4 diagrams;
- component diagrams;
- sequence diagrams;
- deployment diagrams;
- data flow diagrams;
- UML diagrams.

Diagrams should communicate architecture, not decorate documentation.

---

# Mathematical Content

Projects involving mathematical models should explain:

- theoretical background;
- notation;
- assumptions;
- derivations (when relevant);
- references.

Equations should complement engineering explanations rather than replace them.

---

# Versioning

Documentation should evolve together with the project.

Major architectural changes require documentation updates before release.

Documentation should never lag significantly behind implementation.

---

# Documentation Review

Before every release, verify that:

- documentation matches the implementation;
- architecture diagrams are current;
- installation instructions work;
- API examples remain valid;
- benchmarks correspond to the latest version.

Documentation review is part of the release process.

---

# Definition of Complete Documentation

Documentation is considered complete when another engineer can:

- understand the project;
- install it;
- run it;
- reproduce the experiments;
- understand the architecture;
- extend the implementation;
- contribute confidently.

If external explanations are still required, documentation is incomplete.

# DOCUMENTATION_STANDARD.md (Español)

# Estándar de Documentación

## Propósito

Este documento define los estándares de documentación adoptados por el laboratorio.

La documentación se considera un artefacto de ingeniería de primera categoría. Evoluciona junto con el software y desempeña un papel fundamental en la mantenibilidad, la reproducibilidad, la colaboración y la transferencia de conocimiento.

Todo proyecto desarrollado dentro del laboratorio deberá cumplir este estándar, salvo que exista una justificación explícita para actuar de otra manera.

---

# Filosofía de la documentación

La documentación no se escribe después del desarrollo.

La documentación forma parte del desarrollo.

Toda decisión arquitectónica, experimento, benchmark e implementación debe documentarse a medida que el proyecto evoluciona.

Una buena documentación explica:

- qué hace el sistema;
- por qué existe;
- cómo funciona;
- por qué se tomaron determinadas decisiones.

---

# Objetivos

La documentación debe:

- garantizar la reproducibilidad;
- facilitar la incorporación de nuevos colaboradores;
- preservar el conocimiento de ingeniería;
- facilitar el mantenimiento;
- justificar las decisiones técnicas;
- documentar los experimentos;
- servir como material de aprendizaje.

Está dirigida tanto a los colaboradores actuales como a los futuros.

---

# Principios de documentación

Toda documentación debe ser:

## Precisa

Debe reflejar fielmente el estado actual del proyecto.

La documentación obsoleta deberá actualizarse o eliminarse.

---

## Clara

Las explicaciones deben ser concisas, precisas y sin ambigüedades.

Se evitará la jerga innecesaria.

---

## Completa

Debe contener la información suficiente para que otro ingeniero pueda comprender y continuar el proyecto sin depender del autor original.

---

## Consistente

La estructura, terminología, formato y nomenclatura deberán mantenerse coherentes entre todos los repositorios.

---

## Reproducible

Siempre que se documenten experimentos o benchmarks deberá proporcionarse información suficiente para reproducirlos.

---

# Niveles de documentación

Cada proyecto dispondrá de varios niveles de documentación.

## Nivel 1 — Documentación del repositorio

Obligatoria.

Incluye:

- README
- LICENSE
- CHANGELOG
- CONTRIBUTING (cuando proceda)

Objetivo:

Ofrecer una visión general rápida del proyecto.

---

## Nivel 2 — Documentación de ingeniería

Dirigida a desarrolladores e ingenieros.

Ejemplos:

- Project Charter
- Arquitectura
- ADR
- Guía de desarrollo
- Guía de despliegue
- Referencia de la API

Objetivo:

Explicar cómo está diseñado y mantenido el sistema.

---

## Nivel 3 — Documentación científica

Obligatoria cuando el proyecto incluya algoritmos, modelos o experimentos.

Ejemplos:

- notas de investigación;
- informes de benchmarks;
- derivaciones matemáticas;
- registros de experimentos;
- evaluación de modelos.

Objetivo:

Explicar el razonamiento científico detrás del proyecto.

---

## Nivel 4 — Documentación de usuario

Dirigida a usuarios finales.

Ejemplos:

- guía de instalación;
- guía de usuario;
- referencia de la CLI;
- ejemplos de uso de la API;
- tutoriales.

Objetivo:

Permitir utilizar el software de forma eficiente.

---

# Documentación estándar de un proyecto

Todo proyecto deberá incluir, cuando corresponda:

```text
README.md
PROJECT_CHARTER.md
ARCHITECTURE.md
CHANGELOG.md
CONTRIBUTING.md
API_REFERENCE.md
INSTALLATION.md
DEVELOPMENT.md
DEPLOYMENT.md
BENCHMARK_REPORT.md
ENGINEERING_JOURNAL.md
```

Los proyectos de Machine Learning incorporarán además:

```text
MODEL_CARD.md
DATASET_CARD.md
EXPERIMENT_REPORT.md
```

---

# Estructura del README

Todo README deberá incluir:

- descripción del proyecto;
- motivación;
- funcionalidades;
- stack tecnológico;
- visión general de la arquitectura;
- instalación;
- uso;
- enlaces a la documentación;
- roadmap;
- licencia.

El README ofrece una visión general y no debe sustituir a la documentación especializada.

---

# Organización de la documentación

La documentación deberá organizarse preferentemente de la siguiente manera:

```text
docs/

├── architecture/
├── api/
├── development/
├── deployment/
├── research/
├── benchmark/
├── reports/
├── adr/
├── assets/
└── images/
```

La estructura podrá ampliarse según la complejidad del proyecto.

---

# Diagramas

Siempre que resulte útil, la documentación incorporará diagramas como:

- diagramas C4;
- diagramas de componentes;
- diagramas de secuencia;
- diagramas de despliegue;
- diagramas de flujo de datos;
- diagramas UML.

Los diagramas deben ayudar a comprender la arquitectura, no ser elementos decorativos.

---

# Contenido matemático

Los proyectos con base matemática deberán documentar:

- fundamentos teóricos;
- notación empleada;
- hipótesis asumidas;
- derivaciones relevantes;
- referencias bibliográficas.

Las expresiones matemáticas deben complementar las explicaciones de ingeniería, no sustituirlas.

---

# Versionado

La documentación evoluciona junto con el proyecto.

Toda modificación arquitectónica importante deberá ir acompañada de la actualización correspondiente antes de realizar una nueva release.

La documentación nunca debe quedar significativamente desactualizada respecto al código.

---

# Revisión de la documentación

Antes de cada release deberá verificarse que:

- la documentación refleja la implementación actual;
- los diagramas están actualizados;
- la instalación funciona correctamente;
- los ejemplos de la API siguen siendo válidos;
- los benchmarks corresponden a la versión más reciente.

La revisión de la documentación forma parte del proceso de publicación.

---

# Definición de documentación completa

La documentación se considerará completa cuando otro ingeniero sea capaz de:

- comprender el proyecto;
- instalarlo;
- ejecutarlo;
- reproducir los experimentos;
- entender la arquitectura;
- ampliar la implementación;
- contribuir con confianza.

Si todavía es necesaria una explicación externa para utilizar o mantener el proyecto, la documentación aún no está completa.
