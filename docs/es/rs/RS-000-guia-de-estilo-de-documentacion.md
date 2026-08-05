---
id: RS-000

slug: guia-de-estilo-de-documentacion

title: Guía de Estilo de Documentación

version: 1.0.0

status: Draft

classification: Normative

language: es

owner: RetroSynth Project

maintainer: Horacio Filippi

authors:
  - Horacio Filippi

reviewers: []

approved_by: null

created: 2026-08-04
updated: 2026-08-04

license: CC BY-SA 4.0

category: Documentation

tags:
  - documentacion
  - estandares
  - procesos

related:
  - RS-001
---

# 🎹 RetroSynth Project

# 📚 RS-000 — Guía de Estilo de Documentación

> **Where Retro Computing Meets Modern Synthesis.**

---

| Campo | Valor |
|-------|-------|
| **ID del Documento** | RS-000 |
| **Versión** | 1.0.0 |
| **Estado** | Draft |
| **Clasificación** | Normative |
| **Idioma** | Español |
| **Licencia** | CC BY-SA 4.0 |

---

# 1. Introducción

La documentación es un artefacto fundamental de ingeniería dentro de RetroSynth Project.

Define la arquitectura del proyecto, preserva las decisiones de diseño, comunica el conocimiento técnico y facilita la colaboración a largo plazo entre los colaboradores.

La documentación se considera parte del producto y está sujeta a los mismos estándares de ingeniería que el código fuente.

Todo documento almacenado en el repositorio del proyecto DEBERÁ cumplir las reglas definidas en esta especificación, salvo que exista una excepción expresamente documentada.

---

# 2. Propósito

El propósito de este documento es definir un estándar unificado para toda la documentación de RetroSynth Project.

Este estándar garantiza que la documentación sea:

- Consistente
- Precisa
- Mantenible
- Versionada
- Fácil de revisar
- Fácil de consultar
- Escalable

El objetivo es asegurar que la documentación siga siendo útil durante todo el ciclo de vida del proyecto.

---

# 3. Alcance

Esta especificación aplica a todos los documentos contenidos en el repositorio de RetroSynth Project, incluyendo, entre otros:

- Especificaciones de arquitectura
- Especificaciones de hardware
- Especificaciones de software
- Documentación para usuarios
- Documentación para desarrolladores
- Documentación de procesos
- Documentación de gobernanza
- Architecture Decision Records (ADR)
- Plantillas
- Documentación del sitio web

Salvo indicación expresa en contrario, todos los documentos DEBERÁN cumplir esta especificación.

---

# 4. Lenguaje de Conformidad

Las palabras clave **MUST**, **MUST NOT**, **REQUIRED**, **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **RECOMMENDED**, **MAY** y **OPTIONAL** deberán interpretarse de acuerdo con RFC 2119.

Cuando estas palabras aparezcan en un documento clasificado como **Normative**, indicarán el nivel de obligatoriedad definido por dicha especificación.

---

# 5. Principios de la Documentación

Los siguientes principios definen la cultura documental de RetroSynth Project.

## 5.1 La Documentación es Parte del Producto

La documentación DEBERÁ considerarse un entregable del producto.

Una funcionalidad no se considerará terminada hasta que su documentación correspondiente haya sido actualizada.

---

## 5.2 Documentación Antes de la Implementación

Siempre que sea práctico, las decisiones de arquitectura, las interfaces, los diseños de hardware y las funcionalidades importantes DEBERÍAN documentarse antes de comenzar su implementación.

La documentación constituye el principal artefacto de diseño del proyecto.

---

## 5.3 Fuente Única de Verdad

Cada concepto DEBERÁ tener un único documento de referencia.

La duplicación de información NO DEBERÁ producirse de manera innecesaria.

Los documentos DEBERÍAN hacer referencia a otras especificaciones en lugar de repetir contenido existente.

---

## 5.4 Documentación como Código

La documentación DEBERÁ tratarse con el mismo nivel de calidad que el código fuente.

Todo documento DEBERÁ:

- almacenarse en Git;
- mantener un historial completo de revisiones;
- ser revisado antes de su aprobación;
- seguir Semantic Versioning;
- evolucionar junto con el proyecto.

---

## 5.5 El Texto como Formato Principal

Siempre que sea posible, los recursos documentales DEBERÁN utilizar formatos basados en texto.

Los formatos preferidos son:

- Markdown
- Mermaid
- SVG
- PlantUML
- Draw.io
- YAML
- JSON

Los formatos binarios DEBERÍAN utilizarse únicamente cuando no exista una alternativa práctica basada en texto.

---

## 5.6 El Inglés como Idioma Canónico

El inglés SERÁ el idioma canónico de la documentación de RetroSynth Project.

El español SE MANTENDRÁ como una localización oficial.

En caso de discrepancias entre ambas versiones, la versión en inglés prevalecerá hasta que ambas vuelvan a estar sincronizadas.

---

## 5.7 Referencias Estables

Los documentos DEBERÁN hacer referencia a otros documentos del proyecto mediante su identificador permanente.

Ejemplo:

```
RS-004
```

en lugar de:

```
architecture.md
```

Esto garantiza referencias estables incluso si cambian los nombres de los archivos o la estructura del repositorio.

---

## 5.8 Documentación Modular

La documentación DEBERÍA mantenerse modular.

Los temas extensos DEBERÍAN dividirse en múltiples documentos especializados en lugar de crear especificaciones excesivamente grandes.

Cada documento DEBERÍA abordar un único tema principal.

---

## 5.9 Documentación Permanente

La documentación DEBERÁ reflejar con precisión el estado actual del proyecto.

La información obsoleta DEBERÁ actualizarse, marcarse como obsoleta o archivarse.

La documentación DEBERÁ evolucionar junto con el hardware y el software.

---

## 5.10 La Arquitectura Primero

Siempre que sea práctico, las decisiones de ingeniería DEBERÍAN documentarse antes de comenzar la implementación.

El diseño precede a la implementación.

La implementación DEBERÁ seguir las especificaciones aprobadas cuando estas existan.

---

# 6. Clasificación de la Documentación

RetroSynth Project define dos clasificaciones para la documentación.

| Clasificación | Descripción |
|---------------|-------------|
| **Normative** | Define reglas, requisitos, estándares o especificaciones obligatorias del proyecto. Su cumplimiento es requerido. |
| **Informative** | Proporciona orientación, explicaciones, ejemplos o tutoriales. Su cumplimiento no es obligatorio. |

Los documentos **Normative** establecen los estándares oficiales del proyecto.

Los documentos **Informative** facilitan la comprensión y aplicación de dichos estándares.