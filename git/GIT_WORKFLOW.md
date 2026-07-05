# GIT_WORKFLOW.md

# Git Workflow

## Purpose

This document defines the Git workflow used across the laboratory.

The goal is to maintain a clean, understandable and traceable project history. Git is not only a version control tool; it is also a record of the engineering process behind each project.

A well-maintained Git history helps future contributors understand how the project evolved, why changes were introduced and how different parts of the system were developed.

---

# Core Principles

## 1. The main branch must remain stable

The `main` branch represents the stable state of the project.

Code merged into `main` should be tested, documented and ready to use.

Direct commits to `main` should be avoided except for exceptional cases such as repository initialization or urgent documentation fixes.

---

## 2. Work should happen in branches

Every meaningful change should be developed in a dedicated branch.

Branches keep work isolated and make changes easier to review.

Recommended branch prefixes:

```text
feature/
fix/
docs/
refactor/
test/
chore/
ci/
experiment/
```

Examples:

```text
feature/document-ingestion
feature/semantic-retrieval
docs/add-project-charter
test/add-api-tests
ci/add-github-actions
refactor/retrieval-service
experiment/chunking-strategies
```

---

# Branching Strategy

The default workflow is a simplified trunk-based model:

```text
main
 ↑
 pull request
 ↑
feature/*
```

For most projects, a permanent `develop` branch is not required.

The `main` branch remains stable, while short-lived branches are used for development.

A `develop` branch may be introduced only if the project becomes large enough to require an integration branch.

---

# Commit Guidelines

Commits should be small, focused and meaningful.

Each commit should represent one logical change.

Avoid vague messages such as:

```text
update
changes
fix stuff
final version
```

Use Conventional Commits whenever possible.

---

# Conventional Commits

Commit messages should follow this structure:

```text
type(scope): short description
```

Examples:

```text
feat(api): add document upload endpoint
fix(retrieval): handle empty search results
docs(readme): add installation instructions
test(ingestion): add PDF parser tests
refactor(rag): simplify prompt builder
chore(deps): update development dependencies
ci(github): add test workflow
```

Common commit types:

```text
feat      new functionality
fix       bug fix
docs      documentation changes
test      tests
refactor  internal code improvement
chore     maintenance tasks
ci        continuous integration
perf      performance improvement
style     formatting only
build     build system changes
```

---

# Pull Requests

Every significant change should be integrated through a pull request.

Even when working alone, pull requests provide:

- a review checkpoint;
- a place to explain the motivation of the change;
- a structured history of development;
- an opportunity to connect issues, ADRs and documentation.

A pull request should include:

- summary of changes;
- motivation;
- testing evidence;
- documentation updates;
- related issues or ADRs;
- screenshots or benchmark results when applicable.

---

# Issues

Issues should be used to describe planned work, bugs, improvements and research tasks.

Recommended issue types:

```text
Feature
Bug
Documentation
Research
Experiment
Refactor
Benchmark
Infrastructure
```

An issue should explain:

- context;
- expected outcome;
- acceptance criteria;
- relevant references.

---

# Experiments

Experimental work should be isolated.

Use the prefix:

```text
experiment/
```

Examples:

```text
experiment/qdrant-vs-pgvector
experiment/chunk-size-comparison
experiment/reranking-models
```

Experimental branches may be discarded if the idea is not adopted.

If an experiment influences a long-term decision, an ADR should be created.

---

# Tags and Releases

Stable milestones should be tagged using semantic versioning.

Recommended format:

```text
vMAJOR.MINOR.PATCH
```

Examples:

```text
v0.1.0
v0.2.0
v1.0.0
```

Version meaning:

```text
MAJOR  breaking changes
MINOR  new functionality
PATCH  fixes and small improvements
```

Each release should include:

- changelog;
- relevant documentation;
- tested environment;
- known limitations.

---

# Recommended Workflow

A typical development cycle should follow these steps:

```text
1. Create or select an issue.
2. Create a branch from main.
3. Implement the change.
4. Add or update tests.
5. Update documentation.
6. Commit using Conventional Commits.
7. Open a pull request.
8. Review the change.
9. Merge into main.
10. Delete the branch.
```

Example:

```bash
git checkout main
git pull origin main

git checkout -b feature/document-ingestion

git add .
git commit -m "feat(ingestion): add PDF text extraction service"

git push origin feature/document-ingestion
```

---

# Merge Strategy

Prefer squash merging for small and medium-sized pull requests.

This keeps the `main` history clean while preserving detailed discussion inside the pull request.

For large features with meaningful intermediate commits, regular merge commits may be used.

Rebase may be used to update a branch before merging, but rewritten history should not be forced onto shared branches without coordination.

---

# Protected Branches

Important repositories should protect the `main` branch.

Recommended rules:

- require pull requests before merging;
- require status checks to pass;
- require branch to be up to date;
- prevent force pushes;
- prevent deletion of `main`.

These rules may be relaxed during early initialization, but should be enabled before the first stable release.

---

# Definition of a Good Git History

A good Git history should allow another engineer to understand:

- what changed;
- why it changed;
- when it changed;
- which issue or decision motivated the change;
- whether tests and documentation were updated.

Git history is part of the project documentation.

Poor Git history hides engineering decisions.

Good Git history preserves them.

# GIT_WORKFLOW.md

# Flujo de trabajo con Git

## Propósito

Este documento define el flujo de trabajo con Git utilizado en el laboratorio.

El objetivo es mantener un historial limpio, comprensible y trazable. Git no es únicamente una herramienta de control de versiones; también es un registro del proceso de ingeniería que hay detrás de cada proyecto.

Un historial bien mantenido ayuda a futuros colaboradores a entender cómo evolucionó el proyecto, por qué se introdujeron ciertos cambios y cómo se desarrollaron las distintas partes del sistema.

---

# Principios fundamentales

## 1. La rama main debe mantenerse estable

La rama `main` representa el estado estable del proyecto.

El código integrado en `main` debe estar probado, documentado y listo para ser utilizado.

Deben evitarse los commits directos a `main`, salvo en casos excepcionales como la inicialización del repositorio o correcciones urgentes de documentación.

---

## 2. El trabajo debe realizarse en ramas

Todo cambio significativo debe desarrollarse en una rama dedicada.

Las ramas permiten aislar el trabajo y facilitan la revisión de cambios.

Prefijos recomendados:

```text
feature/
fix/
docs/
refactor/
test/
chore/
ci/
experiment/
```

Ejemplos:

```text
feature/document-ingestion
feature/semantic-retrieval
docs/add-project-charter
test/add-api-tests
ci/add-github-actions
refactor/retrieval-service
experiment/chunking-strategies
```

---

# Estrategia de ramas

El flujo por defecto será una versión simplificada de trunk-based development:

```text
main
 ↑
 pull request
 ↑
feature/*
```

Para la mayoría de proyectos no será necesaria una rama `develop` permanente.

La rama `main` se mantiene estable, mientras que el desarrollo se realiza en ramas de corta duración.

La rama `develop` podrá introducirse únicamente si el proyecto alcanza suficiente complejidad como para necesitar una rama de integración.

---

# Guía de commits

Los commits deben ser pequeños, concretos y significativos.

Cada commit debe representar un único cambio lógico.

Evitar mensajes vagos como:

```text
update
changes
fix stuff
final version
```

Siempre que sea posible, se utilizará la convención Conventional Commits.

---

# Conventional Commits

Los mensajes de commit seguirán esta estructura:

```text
type(scope): short description
```

Ejemplos:

```text
feat(api): add document upload endpoint
fix(retrieval): handle empty search results
docs(readme): add installation instructions
test(ingestion): add PDF parser tests
refactor(rag): simplify prompt builder
chore(deps): update development dependencies
ci(github): add test workflow
```

Tipos habituales:

```text
feat      nueva funcionalidad
fix       corrección de error
docs      cambios en documentación
test      pruebas
refactor  mejora interna del código
chore     tareas de mantenimiento
ci        integración continua
perf      mejora de rendimiento
style     cambios de formato
build     cambios en el sistema de build
```

---

# Pull Requests

Todo cambio significativo deberá integrarse mediante pull request.

Incluso trabajando en solitario, los pull requests aportan:

- un punto formal de revisión;
- un espacio para explicar la motivación del cambio;
- un historial estructurado del desarrollo;
- una oportunidad para vincular issues, ADRs y documentación.

Un pull request deberá incluir:

- resumen de cambios;
- motivación;
- evidencia de pruebas;
- actualizaciones de documentación;
- issues o ADRs relacionados;
- capturas o resultados de benchmarks cuando proceda.

---

# Issues

Las issues se utilizarán para describir trabajo planificado, errores, mejoras y tareas de investigación.

Tipos recomendados:

```text
Feature
Bug
Documentation
Research
Experiment
Refactor
Benchmark
Infrastructure
```

Una issue deberá explicar:

- contexto;
- resultado esperado;
- criterios de aceptación;
- referencias relevantes.

---

# Experimentos

El trabajo experimental debe mantenerse aislado.

Se utilizará el prefijo:

```text
experiment/
```

Ejemplos:

```text
experiment/qdrant-vs-pgvector
experiment/chunk-size-comparison
experiment/reranking-models
```

Las ramas experimentales podrán descartarse si la idea no se adopta.

Si un experimento influye en una decisión a largo plazo, deberá crearse un ADR.

---

# Tags y releases

Los hitos estables deberán etiquetarse mediante versionado semántico.

Formato recomendado:

```text
vMAJOR.MINOR.PATCH
```

Ejemplos:

```text
v0.1.0
v0.2.0
v1.0.0
```

Significado de versión:

```text
MAJOR  cambios incompatibles
MINOR  nueva funcionalidad
PATCH  correcciones y pequeñas mejoras
```

Cada release deberá incluir:

- changelog;
- documentación relevante;
- entorno probado;
- limitaciones conocidas.

---

# Flujo recomendado

Un ciclo típico de desarrollo seguirá estos pasos:

```text
1. Crear o seleccionar una issue.
2. Crear una rama desde main.
3. Implementar el cambio.
4. Añadir o actualizar pruebas.
5. Actualizar documentación.
6. Hacer commit usando Conventional Commits.
7. Abrir un pull request.
8. Revisar el cambio.
9. Integrar en main.
10. Eliminar la rama.
```

Ejemplo:

```bash
git checkout main
git pull origin main

git checkout -b feature/document-ingestion

git add .
git commit -m "feat(ingestion): add PDF text extraction service"

git push origin feature/document-ingestion
```

---

# Estrategia de merge

Se recomienda utilizar squash merge para pull requests pequeños y medianos.

Esto mantiene limpio el historial de `main` y conserva la discusión detallada dentro del pull request.

Para funcionalidades grandes con commits intermedios significativos, podrán utilizarse merge commits normales.

El rebase podrá utilizarse para actualizar una rama antes del merge, pero no deberá forzarse historial reescrito sobre ramas compartidas sin coordinación previa.

---

# Protección de ramas

Los repositorios importantes deberán proteger la rama `main`.

Reglas recomendadas:

- exigir pull request antes de integrar;
- exigir que los checks pasen correctamente;
- exigir que la rama esté actualizada;
- impedir force pushes;
- impedir la eliminación de `main`.

Estas reglas podrán relajarse durante la inicialización del repositorio, pero deberán activarse antes de la primera release estable.

---

# Definición de un buen historial Git

Un buen historial de Git debe permitir que otro ingeniero entienda:

- qué cambió;
- por qué cambió;
- cuándo cambió;
- qué issue o decisión motivó el cambio;
- si las pruebas y la documentación fueron actualizadas.

El historial de Git forma parte de la documentación del proyecto.

Un historial pobre oculta decisiones de ingeniería.

Un buen historial las preserva.
