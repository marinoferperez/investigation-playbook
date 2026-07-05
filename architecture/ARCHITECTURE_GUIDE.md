# ARCHITECTURE_GUIDE.md (English)

# Architecture Guide

## Purpose

This document defines how software architecture should be designed, documented and reviewed across the laboratory.

Architecture describes the structure of a system, the responsibilities of its components, the relationships between them and the technical decisions that allow the system to satisfy its requirements.

Good architecture makes software easier to understand, maintain, test, extend and deploy.

---

# Architecture Philosophy

Architecture is not decoration.

Architecture is a tool for reasoning.

A good architecture document should help engineers answer:

- what the system does;
- how the system is structured;
- how data flows through the system;
- where responsibilities are located;
- what external dependencies exist;
- what trade-offs shaped the design;
- how the system can evolve.

Architecture should be documented before implementation and updated as the system changes.

---

# Core Principles

## 1. Start from requirements

Architecture should be derived from functional and non-functional requirements.

Technology choices should follow the needs of the system, not personal preference or popularity.

---

## 2. Separate responsibilities

Each component should have a clear responsibility.

A component should be easy to describe in one or two sentences.

If a component has too many responsibilities, it should be split.

---

## 3. Minimize coupling

Components should depend on each other as little as possible.

Low coupling makes systems easier to test, replace and extend.

---

## 4. Maximize cohesion

Related behavior should live together.

High cohesion makes modules easier to understand and maintain.

---

## 5. Make boundaries explicit

Architecture should define clear boundaries between:

- API layer;
- domain logic;
- data access;
- external services;
- infrastructure;
- machine learning components;
- evaluation pipelines.

Explicit boundaries reduce accidental complexity.

---

## 6. Design for change

Systems evolve.

Architecture should allow future changes without requiring unnecessary rewrites.

---

# Required Architecture Documents

Each non-trivial project should include:

```text
docs/architecture/
├── overview.md
├── components.md
├── data-flow.md
├── deployment.md
└── decisions.md
```

For smaller projects, these sections may be combined into a single `ARCHITECTURE.md`.

---

# Architecture Overview

The architecture overview should explain the system at a high level.

It should include:

- purpose of the system;
- main components;
- external dependencies;
- main workflows;
- deployment context.

This document should be understandable without reading the source code.

---

# Component Architecture

The component architecture should describe each major component.

For each component, document:

- responsibility;
- inputs;
- outputs;
- dependencies;
- failure modes;
- testing strategy.

Example components in an RAG system:

```text
Document Ingestion Service
Text Extraction Service
Chunking Service
Embedding Service
Vector Store
Retriever
Reranker
Generation Service
Evaluation Service
API Layer
```

---

# Data Flow

The data flow documentation should explain how data moves through the system.

It should describe:

- input data;
- transformations;
- storage;
- retrieval;
- outputs;
- metadata;
- error handling.

For data-intensive projects, this section is mandatory.

---

# Deployment Architecture

The deployment architecture should explain how the system runs.

It should document:

- services;
- containers;
- databases;
- environment variables;
- external APIs;
- networking;
- persistent storage;
- monitoring when applicable.

Deployment documentation should be reproducible.

---

# Diagram Standards

Diagrams should communicate structure or behavior.

Recommended diagram types:

- C4 context diagram;
- C4 container diagram;
- component diagram;
- sequence diagram;
- deployment diagram;
- data flow diagram.

Every diagram should have:

- title;
- purpose;
- legend when needed;
- date or version;
- short explanation.

A diagram without explanation is incomplete.

---

# Architecture Decision Records

Architecture documents should explain the current design.

ADRs should explain why important decisions were made.

Both are required.

Architecture documentation answers:

```text
What is the system structure?
```

ADRs answer:

```text
Why was it designed this way?
```

---

# Architecture Review

Architecture should be reviewed before major implementation phases.

A review should verify:

- requirements are addressed;
- responsibilities are clear;
- dependencies are justified;
- failure modes are considered;
- data flow is understood;
- deployment is reproducible;
- ADRs exist for major decisions.

---

# Evolution

Architecture is expected to evolve.

When the system changes, architecture documentation must be updated.

If a major architectural decision changes, a new ADR should be written.

Outdated architecture documentation is dangerous because it creates false confidence.

---

# Definition of Good Architecture

A good architecture should make the system:

- easier to understand;
- easier to test;
- easier to deploy;
- easier to extend;
- easier to debug;
- easier to document.

Architecture is successful when it reduces cognitive load for future engineers.

# ARCHITECTURE_GUIDE.md (Español)

# Guía de Arquitectura

## Propósito

Este documento define cómo debe diseñarse, documentarse y revisarse la arquitectura de software dentro del laboratorio.

La arquitectura describe la estructura de un sistema, las responsabilidades de sus componentes, las relaciones entre ellos y las decisiones técnicas que permiten satisfacer los requisitos del proyecto.

Una buena arquitectura facilita comprender, mantener, probar, ampliar y desplegar el software.

---

# Filosofía de arquitectura

La arquitectura no es decoración.

La arquitectura es una herramienta para razonar.

Un buen documento de arquitectura debe ayudar a responder:

- qué hace el sistema;
- cómo está estructurado;
- cómo fluye la información;
- dónde se ubican las responsabilidades;
- qué dependencias externas existen;
- qué compromisos técnicos dieron forma al diseño;
- cómo puede evolucionar el sistema.

La arquitectura debe documentarse antes de la implementación y actualizarse cuando el sistema cambie.

---

# Principios fundamentales

## 1. Partir de los requisitos

La arquitectura debe derivarse de los requisitos funcionales y no funcionales.

Las decisiones tecnológicas deben responder a las necesidades del sistema, no a preferencias personales o popularidad.

---

## 2. Separar responsabilidades

Cada componente debe tener una responsabilidad clara.

Un componente debería poder describirse en una o dos frases.

Si un componente acumula demasiadas responsabilidades, deberá dividirse.

---

## 3. Minimizar el acoplamiento

Los componentes deben depender unos de otros lo menos posible.

Un bajo acoplamiento facilita probar, sustituir y ampliar el sistema.

---

## 4. Maximizar la cohesión

El comportamiento relacionado debe vivir junto.

Una alta cohesión facilita comprender y mantener los módulos.

---

## 5. Hacer explícitos los límites

La arquitectura debe definir límites claros entre:

- capa de API;
- lógica de dominio;
- acceso a datos;
- servicios externos;
- infraestructura;
- componentes de machine learning;
- pipelines de evaluación.

Los límites explícitos reducen la complejidad accidental.

---

## 6. Diseñar para el cambio

Los sistemas evolucionan.

La arquitectura debe permitir cambios futuros sin exigir reescrituras innecesarias.

---

# Documentos de arquitectura requeridos

Todo proyecto no trivial deberá incluir:

```text
docs/architecture/
├── overview.md
├── components.md
├── data-flow.md
├── deployment.md
└── decisions.md
```

En proyectos pequeños, estas secciones podrán agruparse en un único `ARCHITECTURE.md`.

---

# Visión general de arquitectura

La visión general debe explicar el sistema a alto nivel.

Debe incluir:

- propósito del sistema;
- componentes principales;
- dependencias externas;
- flujos principales;
- contexto de despliegue.

Este documento debe ser comprensible sin necesidad de leer el código fuente.

---

# Arquitectura de componentes

La arquitectura de componentes debe describir cada componente principal.

Para cada componente se documentará:

- responsabilidad;
- entradas;
- salidas;
- dependencias;
- modos de fallo;
- estrategia de pruebas.

Ejemplos de componentes en un sistema RAG:

```text
Document Ingestion Service
Text Extraction Service
Chunking Service
Embedding Service
Vector Store
Retriever
Reranker
Generation Service
Evaluation Service
API Layer
```

---

# Flujo de datos

La documentación de flujo de datos debe explicar cómo se mueve la información dentro del sistema.

Debe describir:

- datos de entrada;
- transformaciones;
- almacenamiento;
- recuperación;
- salidas;
- metadatos;
- gestión de errores.

En proyectos intensivos en datos, esta sección es obligatoria.

---

# Arquitectura de despliegue

La arquitectura de despliegue debe explicar cómo se ejecuta el sistema.

Debe documentar:

- servicios;
- contenedores;
- bases de datos;
- variables de entorno;
- APIs externas;
- red;
- almacenamiento persistente;
- monitorización cuando proceda.

La documentación de despliegue debe ser reproducible.

---

# Estándares para diagramas

Los diagramas deben comunicar estructura o comportamiento.

Tipos recomendados:

- diagrama de contexto C4;
- diagrama de contenedores C4;
- diagrama de componentes;
- diagrama de secuencia;
- diagrama de despliegue;
- diagrama de flujo de datos.

Todo diagrama deberá tener:

- título;
- propósito;
- leyenda cuando sea necesaria;
- fecha o versión;
- explicación breve.

Un diagrama sin explicación está incompleto.

---

# Registros de Decisiones Arquitectónicas

Los documentos de arquitectura explican el diseño actual.

Los ADR explican por qué se tomaron decisiones importantes.

Ambos son necesarios.

La documentación de arquitectura responde:

```text
¿Cómo está estructurado el sistema?
```

Los ADR responden:

```text
¿Por qué fue diseñado de esta manera?
```

---

# Revisión de arquitectura

La arquitectura deberá revisarse antes de las fases importantes de implementación.

Una revisión debe verificar que:

- los requisitos están cubiertos;
- las responsabilidades son claras;
- las dependencias están justificadas;
- se han considerado los modos de fallo;
- el flujo de datos se comprende;
- el despliegue es reproducible;
- existen ADR para las decisiones principales.

---

# Evolución

La arquitectura está destinada a evolucionar.

Cuando el sistema cambie, la documentación arquitectónica deberá actualizarse.

Si cambia una decisión arquitectónica importante, deberá escribirse un nuevo ADR.

La documentación arquitectónica desactualizada es peligrosa porque genera una falsa sensación de seguridad.

---

# Definición de buena arquitectura

Una buena arquitectura debe hacer que el sistema sea:

- más fácil de entender;
- más fácil de probar;
- más fácil de desplegar;
- más fácil de ampliar;
- más fácil de depurar;
- más fácil de documentar.

La arquitectura tiene éxito cuando reduce la carga cognitiva de los futuros ingenieros.
