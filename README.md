# Campo App (monorepo)

Monorepo inicial para una aplicación **React (frontend)** + **Spring Boot (backend)** con **MariaDB** y despliegue en **QNAP (Container Station)**.

> **Arquitectura objetivo QNAP**: Este repo está preparado para publicar imágenes Docker multi-arquitectura, incluyendo **linux/arm/v7** para QNAP TS-431P3 (ARM Cortex-A15).

## Estructura
```
frontend/    # React + Vite (se generará en el paso 2)
backend/     # Spring Boot 3 (se generará en el paso 2)
infra/       # docker-compose, traefik, scripts de despliegue
docs/        # documentación funcional/técnica
.github/     # workflows de CI/CD
```

## Flujo de ramas
- **main**: Producción
- **develop**: Integración
- **feature/***: Trabajo de características

## Próximos pasos
1. Configurar CI en `.github/workflows/ci.yml` (se completa en pasos siguientes).
2. Generar los proyectos en `frontend/` y `backend/`.
3. Probar entorno local con `infra/docker-compose.dev.yml`.
4. Publicar imágenes multi-arch en GHCR y desplegar en QNAP.
