# Property Management System — Laravel

Sistema web de gestión de propiedades y reservaciones desarrollado como
proyecto freelance en 2020. Arquitectura Laravel modular con separación
estricta de responsabilidades.

## Estructura del proyecto

    app/
    ├── Helpers/          # Funciones auxiliares por contexto
    │   ├── ContactsHelper.php
    │   ├── ImagesHelper.php
    │   ├── LanguageHelper.php
    │   ├── PMHelper.php
    │   ├── PMTransactionHelper.php
    │   ├── RatesHelper.php
    │   ├── RoleHelper.php
    │   ├── UserHelper.php
    │   └── WorkgroupHelper.php
    ├── Http/             # Controllers y Middleware
    ├── Models/           # Modelos Eloquent
    ├── Notifications/    # Notificaciones por correo (Laravel Mail)
    ├── Providers/        # Service Providers
    ├── Repositories/     # Capa de acceso a datos
    ├── Traits/           # Traits reutilizables (AppModel)
    └── Validations/      # Reglas de validación

## Características

- Gestión completa de reservaciones — booking, balance, pagos y transacciones organizados por entidad
- Sistema de notificaciones por correo — alertas automáticas a usuarios ante eventos del sistema usando Laravel Notifications
- Control de acceso por roles — `RoleHelper` con permisos diferenciados por tipo de usuario y grupo de trabajo
- Helpers segmentados por contexto — contactos, imágenes, idioma, tarifas, transacciones, usuarios y grupos de trabajo
- Repositorios como capa de acceso a datos — separación entre lógica de negocio y consultas a base de datos
- Traits reutilizables — `AppModel` como base extendible para modelos
- Validaciones centralizadas — reglas independientes del controller
- Diseño de base de datos normalizado con MySQL

## Entidades principales

| Entidad | Descripción |
|---|---|
| `BookingDetails` | Información central de cada reservación |
| `DetailsBalance` | Control de saldos por reservación |
| `DetailsContact` | Datos de contacto asociados |
| `DetailsPayment` | Registro de pagos |
| `DetailsTransaction` | Historial de transacciones |

## Explorar código

- [Helpers](app/Helpers/) — funciones auxiliares segmentadas por contexto
- [Repositories](app/Repositories/) — capa de acceso a datos
- [Notifications](app/Notifications/) — sistema de notificaciones por correo
- [Models](app/Models/) — modelos Eloquent
- [Validations](app/Validations/) — reglas de validación centralizadas
- [Traits](app/Traits/) — traits reutilizables

## Stack técnico

- **Backend:** PHP, Laravel
- **Frontend:** Bootstrap, Blade Templates
- **Base de datos:** MySQL
- **Notificaciones:** Laravel Notifications + Laravel Mail
- **Control de versiones:** Git

## Contexto

Proyecto freelance desarrollado en 2020 como solución de gestión interna
para administración de propiedades y reservaciones. Arquitectura pensada
para escalar y mantener sin fricción — separación de Helpers,
Repositories y Validations desde el inicio del proyecto.
