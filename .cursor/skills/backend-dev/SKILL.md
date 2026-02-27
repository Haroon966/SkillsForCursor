---
name: backend-dev
description: Django backend development. Use when the user works on or asks about Django views, URLs, models, Django REST Framework (DRF), serializers, authentication/authorization (Django auth, JWT, session), middleware, Django settings, management commands, Celery or background tasks, deployment (WSGI, env), or backend testing in Django.
---

# Backend Dev (Django)

Apply when implementing or reviewing **Django** backend code: views, APIs (DRF), auth, settings, middleware, commands, or deployment.

## When to Use This Skill

- Django views, URLs, request/response handling
- Django REST Framework (DRF): APIs, serializers, ViewSets
- Authentication and authorization (Django auth, JWT, session)
- Middleware, Django settings, environment config
- Management commands, Celery or background tasks
- Deployment (WSGI, env vars, production config)
- Backend testing in Django

## Principles

- **Structure**: Fat models / thin views where it makes sense; put business logic in models or services, not in view bodies.
- **Errors**: Return clear HTTP status codes and consistent error payloads; use DRF exceptions and validation.
- **Security**: Validate and sanitize input; use CSRF protection; never put secrets in code—use env vars for SECRET_KEY, DB URLs, API keys.
- **Built-ins first**: Use Django’s auth, permissions, signals, and DRF features before writing custom code.

## Patterns

- **URLs**: Use namespacing and clear names; keep urlpatterns organized (include by app or feature).
- **Views**: Prefer class-based views (DRF ViewSets, Django generic views) when they fit; function-based when simpler.
- **DRF**: ViewSets + serializers for CRUD; use permissions classes; throttle and filter as needed.
- **Settings**: Split base / local / production; read from env (e.g. django-environ or os.environ).
- **Migrations**: Don’t write migrations by hand for schema changes; use `makemigrations`. For schema design and migration strategy, see [database-dev](.cursor/skills/database-dev/SKILL.md).

## Conventions

- Follow project structure: apps, `settings.py`, `urls.py`, consistent naming.
- Use Django and DRF idioms (e.g. get_queryset, get_serializer_class, permission_classes).
- Document API endpoints (docstrings, OpenAPI, or a linked API doc).

For schema design and migrations, see [database-dev](.cursor/skills/database-dev/SKILL.md).
