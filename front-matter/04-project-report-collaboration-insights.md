# Project Report Collaboration Insights

El trabajo colaborativo de Nexa se organiza en cuatro repositorios oficiales. La evidencia enlazada y las capturas siguientes corresponden a la organización, el NRC y el producto Open Source actuales.

| Repositorio | Propósito | Rama entregable | Release auditada |
|---|---|---|---|
| [nexa-report](https://github.com/upc-pre-202610-1asi0729-12010-VulturesD/nexa-report) | Reporte Docs-as-Code | `main` | `v4.0.2` |
| [nexa-website](https://github.com/upc-pre-202610-1asi0729-12010-VulturesD/nexa-website) | Landing Page | `main` | `v4.0.1` |
| [nexa-webapp](https://github.com/upc-pre-202610-1asi0729-12010-VulturesD/nexa-webapp) | Angular Web Application | `main` | `v2.0.1` |
| [nexa-platform](https://github.com/upc-pre-202610-1asi0729-12010-VulturesD/nexa-platform) | Spring Boot Platform API | `main` | `v1.0.2` |

## Public review environments

| Artefacto | URL |
|---|---|
| Website | https://upc-pre-202610-1asi0729-12010-vulturesd.github.io/nexa-website/ |
| WebApp | https://nexa-webapp-fv2v.onrender.com/login |
| Platform health | https://nexa-platform.onrender.com/actuator/health |
| Platform users | https://nexa-platform.onrender.com/api/v1/users |

## Collaboration model

El equipo utiliza issues, ramas de trabajo, pull requests, Conventional Commits y releases independientes. La trazabilidad se verifica en las vistas públicas de commits, pull requests, Actions y releases de cada repositorio. Las evidencias históricas AV1, TB1 y AV2 permanecen en el registro de versiones; la entrega Open Source se sustenta con el estado actual de `main`.

La analítica pública de `nexa-report`, consultada el 19 de junio de 2026, identifica participación de los cinco integrantes:

| Cuenta GitHub | Commits sin merges mostrados por Insights |
|---|---:|
| `Cmarin2802` | 97 |
| `R0obxdnt-bit` | 94 |
| `DiegoS284` | 90 |
| `JoaquinVerde115` | 88 |
| `GerardRojasMancilla` | 48 |

![GitHub Insights de contribuidores de nexa-report](../assets/images/front-matter/collaboration/nexa-report-contributors-av2.png)

La vista de commits de `main` permite relacionar la participación con cambios concretos de documentación, evidencias, validación, anexos, arquitectura y releases.

![Historial de commits de main en nexa-report](../assets/images/front-matter/collaboration/nexa-report-commits-main-av2.png)

## Quality gates

- Website: parsing HTML, sintaxis JavaScript, enlaces internos y GitHub Pages.
- WebApp: `npm ci`, `npm run build` y auditoría de dependencias productivas.
- Platform: `./mvnw test` y `./mvnw package`.
- Report: Markdown lint, rutas de imágenes, enlaces y consistencia entre capítulos.

No se utilizan capturas de otras organizaciones, cursos o implementaciones como evidencia de colaboración Open Source.
