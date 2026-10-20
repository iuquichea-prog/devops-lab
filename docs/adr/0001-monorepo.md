# ADR 0001: Usar un monorepo

- **Estado:** Aceptado
- **Fecha:** 2026-10-19

## Contexto

El laboratorio incluye un frontend web, un CMS y la infraestructura que los
despliega. Mantenerlos en repositorios separados obligaría a coordinar
versiones, PRs y pipelines entre varios repos para cambios que suelen ir juntos.

## Decisión

Usaremos un único repositorio (monorepo) con esta estructura:

- `apps/web`: aplicación web
- `apps/cms`: CMS
- `infra`: infraestructura como código (Terraform)
- `docs/adr`: registros de decisiones de arquitectura

## Consecuencias

- **Positivas:** un solo lugar para revisar cambios, PRs atómicos que tocan
  app e infraestructura a la vez, y configuración compartida (gitignore,
  plantillas, CI).
- **Negativas:** el CI debe filtrar por rutas para no construir todo en cada
  cambio, y los permisos son por repositorio, no por carpeta.
