# Conclusiones

## Conclusiones generales

El proyecto Nexa evolucionó de manera incremental desde AV1 hasta AV2, manteniendo una relación directa entre investigación, diseño, implementación y documentación académica. En AV1 se estableció la base conceptual del producto: el problema de coordinación en la cadena de frío B2B, los segmentos objetivo, el backlog inicial, la Landing Page y la estructura Docs-as-Code del reporte. Esta primera etapa permitió convertir una oportunidad de negocio en una propuesta documentada con trazabilidad.

En TB1, el equipo amplió el alcance hacia la Web Application. El avance se concentró en flujos operativos para coordinación comercial, inventario, pedidos, logística e invoicing, usando artefactos UX/UI, mockups, rutas frontend y soporte controlado de datos simulados. Esta decisión permitió revisar la experiencia de usuario sin sobredeclarar una integración total con servicios backend.

En AV2, Nexa incorporó un primer corte frontend/backend más maduro. La evidencia disponible registra `nexa-website v3.0.0`, `nexa-platform v1.0.0` y `nexa-webapp v2.0.0` como releases de cierre técnico disponibles para revisión. En el caso del reporte, `nexa-report v3.0.0` constituye la versión documental de cierre AV2, con capítulos, evidencias y consistencia de entrega actualizados.

La auditoría Open Source posterior se consolidó dentro del corte `v3.0.0` de `nexa-website` y `nexa-report`, manteniendo `nexa-webapp v2.0.1` y `nexa-platform v1.0.2` como referencias técnicas relacionadas. Este corte alinea las tecnologías declaradas con Angular 21, TypeScript 5.9, Angular Material 21, Java 21, Spring Boot 3 y PostgreSQL 16; recupera la evidencia visual DDD, UML y de base de datos; actualiza las URLs de Render; corrige el metadata público de OpenAPI; y documenta la integración externa de YouTube utilizada por los videos About-the-Product y About-the-Team.

El despliegue académico/controlado también avanzó durante AV2. La Landing Page permanece publicada en GitHub Pages, la Web Application se registra en Render mediante `https://nexa-webapp-fv2v.onrender.com` y la Platform API se registra en Render mediante `https://nexa-platform.onrender.com`. Además, el backend evolucionó su configuración de persistencia hacia PostgreSQL para soportar el despliegue controlado en Render. El reporte incorpora evidencias de Render WebApp, Platform API, PostgreSQL, Swagger/OpenAPI, Jira Sprint 3, releases de `nexa-website`, `nexa-platform` y `nexa-webapp`, navegación/prototyping Sprint 3, wireflow S3, user flow S3 y el Video About-the-Product publicado, sin presentar esta condición como operación productiva definitiva.

Como límite del corte AV2, el informe no declara operación productiva definitiva ni validación estadísticamente concluyente del producto. Las evidencias disponibles incluyen Validation Interviews, evaluación heurística, Video About-the-Product, Video About-the-Team, exposición AV2, coordinación Sprint 3 / AV2 y revisión de evidencias AV2, pero se presentan como soporte académico del cierre documental y no como prueba de adopción real en producción.

## Conclusiones por sprint

### Sprint 1 / AV1

Sprint 1 permitió construir la línea base del proyecto. El equipo definió el problema, los segmentos, la propuesta de valor y los primeros artefactos de investigación, además de organizar el repositorio del informe bajo enfoque Docs-as-Code. La Landing Page sirvió como primera evidencia pública del producto y como punto de entrada para comunicar la propuesta de Nexa.

La principal contribución de AV1 fue establecer coherencia entre discovery, requisitos iniciales, diseño visual y trazabilidad documental. Esta base hizo posible que las entregas posteriores ampliaran el alcance sin perder continuidad académica.

### Sprint 2 / TB1

Sprint 2 consolidó la Web Application como incremento principal de TB1. El trabajo se centró en flujos S1/S2, pantallas representativas, rutas frontend, mockups, evidencia visual y soporte simulado para revisar recorridos operativos. El uso de datos simulados permitió sostener una revisión funcional sin afirmar integración total con servicios internos.

La principal contribución de TB1 fue transformar la propuesta inicial en una experiencia de uso revisable. El equipo logró conectar investigación, UX, backlog y arquitectura, manteniendo límites claros sobre aquello que seguía sujeto a implementación backend.

### Sprint 3 / AV2

Sprint 3 incorporó la primera versión de Web Services y una actualización del corte frontend/backend. `nexa-platform v1.0.0` representa el release de cierre Web Services disponible para revisión AV2, con evidencia de configuración hacia PostgreSQL, Swagger/OpenAPI y despliegue controlado en Render. `nexa-webapp v2.0.0` registra el release de cierre WebApp, con evidencia de GitHub Release, commits, ramas e insights. `nexa-website v3.0.0` actualiza la Landing Page como evidencia disponible de cierre AV2 para revisión.

El resultado del Sprint 3 es una base más integrada entre Web Application, Platform API y documentación, con trazabilidad de Jira, navegación/prototyping, wireflow/user flow S3, Swagger/OpenAPI, releases disponibles, despliegues académicos y videos AV2 publicados y documentados. Esta delimitación conserva rigor académico porque diferencia la evidencia de revisión académica frente a una operación productiva completa.
