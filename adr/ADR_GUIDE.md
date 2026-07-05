# ADR_GUIDE.md (English)

# Architecture Decision Record Guide

## Purpose

This document defines how Architecture Decision Records are used across the laboratory.

An Architecture Decision Record, or ADR, is a short document that captures an important technical decision together with its context, alternatives and consequences.

ADRs preserve the reasoning behind the architecture.

---

# Why ADRs Matter

Software architecture is shaped by decisions.

Over time, the reasoning behind those decisions is often forgotten.

ADRs prevent this loss of knowledge by documenting:

- what was decided;
- why it was decided;
- which alternatives were considered;
- what consequences the decision has;
- when the decision was made.

A good ADR makes future maintenance easier.

---

# When to Write an ADR

An ADR should be written whenever a decision has long-term technical impact.

Examples:

- selecting a database;
- choosing a backend framework;
- adopting a machine learning library;
- defining a deployment strategy;
- introducing a message queue;
- choosing a vector database;
- defining the project structure;
- changing authentication strategy;
- selecting a documentation system.

Not every small decision requires an ADR.

ADRs are reserved for decisions that affect architecture, maintainability, scalability, reproducibility or long-term evolution.

---

# ADR Location

ADRs should be stored in:

```text
docs/adr/
```

Recommended naming convention:

```text
0001-use-fastapi.md
0002-use-qdrant.md
0003-use-mkdocs-material.md
```

The number is sequential and should never be reused.

---

# ADR Status

Each ADR must include one status.

Recommended statuses:

```text
Proposed
Accepted
Deprecated
Superseded
Rejected
```

## Proposed

The decision is being discussed.

## Accepted

The decision has been adopted.

## Deprecated

The decision is no longer recommended but may still exist in the system.

## Superseded

The decision has been replaced by a newer ADR.

## Rejected

The decision was considered but not adopted.

---

# ADR Structure

Each ADR should follow this structure:

```text
# ADR-0001: Title

Date: YYYY-MM-DD

Status: Accepted

## Context

## Decision

## Alternatives Considered

## Consequences

## Related Documents
```

---

# Context

The context explains the problem or situation that required a decision.

It should include:

- project constraints;
- technical requirements;
- relevant background;
- existing limitations;
- trade-offs.

The context should be factual and concise.

---

# Decision

The decision section explains what has been chosen.

It should be direct and unambiguous.

Example:

```text
We will use FastAPI as the backend framework for the initial API layer.
```

---

# Alternatives Considered

This section lists realistic alternatives.

Each alternative should include a short explanation of why it was not selected.

Example:

```text
Flask was considered because of its simplicity, but FastAPI was preferred because of built-in type validation and automatic OpenAPI documentation.
```

---

# Consequences

The consequences section describes the impact of the decision.

It should include both positive and negative consequences.

Example:

```text
This decision improves API documentation and validation, but introduces a dependency on the FastAPI ecosystem.
```

---

# Related Documents

This section links to related documents when relevant:

- project charter;
- architecture overview;
- benchmark reports;
- research notes;
- previous ADRs;
- superseding ADRs.

---

# ADR Principles

## 1. Record reasoning, not just outcomes

An ADR should explain why a decision was made.

---

## 2. Keep ADRs short

An ADR should be long enough to preserve context, but short enough to be read quickly.

---

## 3. Do not rewrite history

Accepted ADRs should not be modified to hide past reasoning.

If a decision changes, write a new ADR and mark the previous one as superseded.

---

## 4. Document trade-offs

Every meaningful technical decision has trade-offs.

A decision that only lists benefits is incomplete.

---

## 5. Prefer clarity over formality

ADRs should be useful, not bureaucratic.

The goal is to help future engineers understand the system.

---

# ADR Review

Before accepting an ADR, verify that:

- the decision is clearly stated;
- the context is understandable;
- alternatives are realistic;
- consequences include trade-offs;
- related documents are linked when useful.

---

# Example ADR

```text
# ADR-0001: Use FastAPI for the Backend API

Date: 2026-07-06

Status: Accepted

## Context

The project requires a backend API for document ingestion, retrieval and question answering.

The API should support request validation, automatic documentation and integration with Python-based machine learning components.

## Decision

We will use FastAPI as the backend framework.

## Alternatives Considered

Flask was considered because of its simplicity and maturity.

Django REST Framework was considered because of its complete ecosystem.

FastAPI was selected because it provides type-driven validation, automatic OpenAPI documentation and strong compatibility with modern Python development.

## Consequences

FastAPI improves developer experience and API documentation.

The project becomes dependent on the FastAPI and Starlette ecosystem.

The team must follow asynchronous programming practices when appropriate.

## Related Documents

- ARCHITECTURE.md
- PROJECT_CHARTER.md
```

# ADR_GUIDE.md (Español)

# Guía de Registros de Decisiones Arquitectónicas

## Propósito

Este documento define cómo se utilizan los Registros de Decisiones Arquitectónicas dentro del laboratorio.

Un Registro de Decisión Arquitectónica, o ADR, es un documento breve que recoge una decisión técnica importante junto con su contexto, alternativas y consecuencias.

Los ADR preservan el razonamiento que hay detrás de la arquitectura.

---

# Por qué importan los ADR

La arquitectura de software se construye a partir de decisiones.

Con el tiempo, el razonamiento detrás de esas decisiones suele olvidarse.

Los ADR evitan esa pérdida de conocimiento documentando:

- qué se decidió;
- por qué se decidió;
- qué alternativas se consideraron;
- qué consecuencias tiene la decisión;
- cuándo se tomó la decisión.

Un buen ADR facilita el mantenimiento futuro.

---

# Cuándo escribir un ADR

Debe escribirse un ADR cuando una decisión tenga impacto técnico a largo plazo.

Ejemplos:

- seleccionar una base de datos;
- elegir un framework backend;
- adoptar una librería de machine learning;
- definir una estrategia de despliegue;
- introducir una cola de mensajes;
- elegir una base de datos vectorial;
- definir la estructura del proyecto;
- cambiar la estrategia de autenticación;
- seleccionar un sistema de documentación.

No toda decisión pequeña requiere un ADR.

Los ADR se reservan para decisiones que afectan a la arquitectura, mantenibilidad, escalabilidad, reproducibilidad o evolución a largo plazo.

---

# Ubicación de los ADR

Los ADR deberán almacenarse en:

```text
docs/adr/
```

Convención de nombres recomendada:

```text
0001-use-fastapi.md
0002-use-qdrant.md
0003-use-mkdocs-material.md
```

El número es secuencial y nunca debe reutilizarse.

---

# Estado de un ADR

Cada ADR debe incluir un estado.

Estados recomendados:

```text
Proposed
Accepted
Deprecated
Superseded
Rejected
```

## Proposed

La decisión está siendo discutida.

## Accepted

La decisión ha sido adoptada.

## Deprecated

La decisión ya no se recomienda, aunque todavía puede existir en el sistema.

## Superseded

La decisión ha sido sustituida por un ADR posterior.

## Rejected

La decisión fue considerada, pero no adoptada.

---

# Estructura de un ADR

Cada ADR seguirá esta estructura:

```text
# ADR-0001: Title

Date: YYYY-MM-DD

Status: Accepted

## Context

## Decision

## Alternatives Considered

## Consequences

## Related Documents
```

---

# Contexto

La sección de contexto explica el problema o situación que requiere una decisión.

Debe incluir:

- restricciones del proyecto;
- requisitos técnicos;
- información relevante;
- limitaciones existentes;
- compromisos técnicos.

El contexto debe ser factual y conciso.

---

# Decisión

La sección de decisión explica qué se ha elegido.

Debe ser directa y no ambigua.

Ejemplo:

```text
We will use FastAPI as the backend framework for the initial API layer.
```

---

# Alternativas consideradas

Esta sección enumera alternativas realistas.

Cada alternativa debe incluir una breve explicación de por qué no fue seleccionada.

Ejemplo:

```text
Flask was considered because of its simplicity, but FastAPI was preferred because of built-in type validation and automatic OpenAPI documentation.
```

---

# Consecuencias

La sección de consecuencias describe el impacto de la decisión.

Debe incluir consecuencias positivas y negativas.

Ejemplo:

```text
This decision improves API documentation and validation, but introduces a dependency on the FastAPI ecosystem.
```

---

# Documentos relacionados

Esta sección enlaza documentos relacionados cuando sea relevante:

- project charter;
- arquitectura general;
- informes de benchmark;
- notas de investigación;
- ADR anteriores;
- ADR que sustituyen al actual.

---

# Principios de los ADR

## 1. Registrar el razonamiento, no solo el resultado

Un ADR debe explicar por qué se tomó una decisión.

---

## 2. Mantener los ADR breves

Un ADR debe ser suficientemente completo para preservar el contexto, pero lo bastante breve para poder leerse rápidamente.

---

## 3. No reescribir la historia

Los ADR aceptados no deben modificarse para ocultar razonamientos pasados.

Si una decisión cambia, se escribe un nuevo ADR y el anterior se marca como sustituido.

---

## 4. Documentar los compromisos

Toda decisión técnica relevante implica compromisos.

Un ADR que solo enumera ventajas está incompleto.

---

## 5. Priorizar claridad sobre formalidad

Los ADR deben ser útiles, no burocráticos.

El objetivo es ayudar a futuros ingenieros a comprender el sistema.

---

# Revisión de ADR

Antes de aceptar un ADR, debe verificarse que:

- la decisión está claramente formulada;
- el contexto es comprensible;
- las alternativas son realistas;
- las consecuencias incluyen compromisos;
- los documentos relacionados están enlazados cuando aporten valor.

---

# Ejemplo de ADR

```text
# ADR-0001: Use FastAPI for the Backend API

Date: 2026-07-06

Status: Accepted

## Context

The project requires a backend API for document ingestion, retrieval and question answering.

The API should support request validation, automatic documentation and integration with Python-based machine learning components.

## Decision

We will use FastAPI as the backend framework.

## Alternatives Considered

Flask was considered because of its simplicity and maturity.

Django REST Framework was considered because of its complete ecosystem.

FastAPI was selected because it provides type-driven validation, automatic OpenAPI documentation and strong compatibility with modern Python development.

## Consequences

FastAPI improves developer experience and API documentation.

The project becomes dependent on the FastAPI and Starlette ecosystem.

The team must follow asynchronous programming practices when appropriate.

## Related Documents

- ARCHITECTURE.md
- PROJECT_CHARTER.md
```
