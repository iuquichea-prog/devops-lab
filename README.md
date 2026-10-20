# devops-lab

Laboratorio de prácticas DevOps: aplicación web, CMS e infraestructura como
código en un solo repositorio.

## Estructura

```
apps/
  web/   # aplicación web
  cms/   # CMS
infra/   # infraestructura (Terraform)
docs/
  adr/   # decisiones de arquitectura
```

## Flujo de trabajo

1. Crea una rama desde `main` (`feat/...`, `fix/...`, `chore/...`).
2. Usa mensajes de commit con [Conventional Commits](https://www.conventionalcommits.org/es/).
3. Abre un PR; la plantilla se carga automáticamente.
4. `main` está protegida: no se hace push directo.

## Decisiones

- [ADR 0001: Usar un monorepo](docs/adr/0001-monorepo.md)
