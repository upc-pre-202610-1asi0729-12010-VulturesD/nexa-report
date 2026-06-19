# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

La configuración del ecosistema Nexa se sustenta en cuatro repositorios oficiales de la organización `upc-pre-202610-1asi0729-12010-VulturesD`: `nexa-report`, `nexa-website`, `nexa-webapp` y `nexa-platform`. Cada repositorio mantiene `main` como rama entregable, documentación propia, validaciones automatizadas y una release asociada al corte revisable.

### 5.1.1. Software Development Environment Configuration

| Área | Tecnología/herramienta vigente | Uso verificable |
|---|---|---|
| Gestión | Jira Software | Product Backlog, Sprint Backlog y seguimiento |
| Control de versiones | Git y GitHub | Ramas, commits, PR, tags y releases |
| Documentación | Markdown / Docs-as-Code | Reporte, README, wiki y release notes |
| Diseño | Figma, FigJam, Lucidchart y Mermaid | UX/UI, user flows, C4, UML y base de datos |
| Website | HTML5, CSS3 y JavaScript | Landing Page estática bilingüe |
| WebApp | Angular 21, TypeScript 5.9, Angular Router, HttpClient y Angular Material 21 | SPA por roles e integración REST |
| Platform | Java 21, Spring Boot 3, Spring Security, Spring Data JPA y springdoc-openapi | API REST, JWT, dominio y persistencia |
| Base de datos | PostgreSQL 16 | Persistencia administrada en Render |
| Servicio externo | YouTube Embed | Publicación integrada de About-the-Product y About-the-Team |
| CI/CD | GitHub Actions, GitHub Pages y Render | Lint, build y despliegue |

Enlaces de revisión:

- Website: https://upc-pre-202610-1asi0729-12010-vulturesd.github.io/nexa-website/
- WebApp: https://nexa-webapp-fv2v.onrender.com/login
- Platform API: https://nexa-platform.onrender.com/api/v1
- Health check: https://nexa-platform.onrender.com/actuator/health

### 5.1.2. Source Code Management

| Repositorio | Responsabilidad | Release vigente al inicio de esta auditoría | Rama |
|---|---|---|---|
| `nexa-report` | Informe y evidencia Docs-as-Code | `v4.0.0` | `main` |
| `nexa-website` | Landing Page pública | `v4.0.0` | `main` |
| `nexa-webapp` | Angular Web Application | `v2.0.0` | `main` |
| `nexa-platform` | Spring Boot REST API | `v1.0.0` | `main` |

El flujo aplicado es:

`feature/* → pull request → main → tag/release`

Las correcciones auditadas se publican mediante PR para conservar revisión y merge commit verificables. Los mensajes siguen Conventional Commits:

- `feat(scope): ...`
- `fix(scope): ...`
- `docs(scope): ...`
- `test(scope): ...`
- `chore(release): ...`

Semantic Versioning se aplica de forma independiente porque Website, WebApp, Platform y Report evolucionan a ritmos distintos.

### 5.1.3. Source Code Style Guide & Conventions

**Website**

- HTML semántico, CSS por responsabilidad y JavaScript sin dependencias innecesarias.
- Contenido bilingüe centralizado en `assets/js/i18n.js`.
- Enlaces internos relativos y CTA de acceso dirigidos a la WebApp desplegada.

**WebApp**

- Organización por bounded context.
- Separación `domain`, `application`, `infrastructure` y `presentation`.
- Llamadas HTTP encapsuladas en infrastructure.
- Rutas relativas `api/v1/*` transformadas por el interceptor compartido.
- Angular Router para navegación y guards para autenticación/autorización.

**Platform**

- Paquetes por bounded context.
- Controllers y resources en interfaces.
- Servicios de aplicación para coordinación.
- Entidades y repository ports en domain.
- Adaptadores JPA, seguridad y configuración en infrastructure.
- Java naming conventions y endpoints REST bajo `/api/v1`.

**Report**

- Un archivo Markdown por sección.
- Imágenes bajo `assets/images` con rutas relativas.
- Evidencia identificada por fuente, fecha, repositorio y alcance.
- No se incorporan capturas de implementaciones anteriores como evidencia del producto Open Source.

### 5.1.4. Software Deployment Configuration

| Artefacto | Configuración | Estado verificable |
|---|---|---|
| Website | GitHub Pages desde `main` | Publicado |
| Servicio externo | YouTube mediante `iframe` con reproducción embebida | Integrado en Website |
| WebApp | Render Static Site; `npm ci && npm run build`; publish `dist/nexa-webapp/browser` | Publicado |
| Platform | Render Web Service mediante Docker | Publicado |
| PostgreSQL | Render PostgreSQL 16 | Conectado a Platform |
| Report | Markdown versionado y GitHub Release | Publicado |

Variables principales de Platform:

- `DATABASE_URL`
- `FRONTEND_ORIGIN=https://nexa-webapp-fv2v.onrender.com`
- `SPRING_PROFILES_ACTIVE=postgres,seed`
- `JPA_DDL_AUTO=update`
- `JWT_SECRET`
- `JWT_EXPIRATION_MINUTES=120`

La WebApp compila la URL productiva:

`https://nexa-platform.onrender.com/api/v1`

Render Free puede introducir cold start en Platform. Esta limitación de infraestructura no modifica la arquitectura ni la validez del despliegue, pero debe declararse durante la demostración.
