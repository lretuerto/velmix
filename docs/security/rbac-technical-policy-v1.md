# RBAC Technical Policy v1

## Objetivo
Establecer base técnica para control de acceso por rol y permiso.

## Lineamientos
- Definir permisos atómicos por acción: read, create, update, approve, admin.
- Resolver autorización en backend, nunca solo en frontend.
- Loggear acciones críticas con actor, rol, tenant_id y timestamp UTC.
- Prohibir acciones sin contexto de tenant en módulos multiempresa.

## Próximos pasos
- Traducir matriz a seeders/migrations.
- Agregar pruebas de aislamiento por rol y tenant.
