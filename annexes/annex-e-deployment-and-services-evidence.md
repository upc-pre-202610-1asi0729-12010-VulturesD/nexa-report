# Annex E: Deployment and Services Evidence

| Servicio | URL | Resultado esperado |
|---|---|---|
| Landing Page | https://upc-pre-202610-1asi0729-12010-vulturesd.github.io/nexa-website/ | Website público |
| WebApp login | https://nexa-webapp-fv2v.onrender.com/login | Pantalla de acceso |
| Platform health | https://nexa-platform.onrender.com/actuator/health | Estado HTTP saludable |
| Platform users | https://nexa-platform.onrender.com/api/v1/users | Usuarios seed en JSON |

## Render configuration

Platform utiliza PostgreSQL 16, perfiles `postgres,seed`, CORS restringido al origen real de WebApp y health check `/actuator/health`. WebApp utiliza un Static Site con fallback SPA hacia `/index.html` y compila la URL `https://nexa-platform.onrender.com/api/v1`.

## Review limitation

Render Free puede suspender Platform por inactividad. El primer request puede requerir alrededor de dos minutos; las solicitudes posteriores responden con normalidad mientras el servicio permanece activo.

Las capturas antiguas de Render/Swagger asociadas a una implementación anterior no forman parte de la evidencia Open Source.
