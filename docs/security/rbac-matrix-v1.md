# RBAC Matrix v1 - Sprint 1 Day 2

## Roles iniciales
- OWNER
- ADMIN
- CAJERO
- INVENTARIO
- FACTURACION
- AUDITOR

## Convención
- R = Read
- W = Write
- A = Approve/Admin

## Matriz por módulo

| Rol         | Ventas POS | Inventario | Facturación/CPE | Usuarios/Roles | Reportes |
|-------------|------------|------------|------------------|----------------|----------|
| OWNER       | R/W/A      | R/W/A      | R/W/A            | R/W/A          | R/W      |
| ADMIN       | R/W/A      | R/W/A      | R/W/A            | R/W            | R/W      |
| CAJERO      | R/W        | R          | R                | -              | R        |
| INVENTARIO  | R          | R/W        | -                | -              | R        |
| FACTURACION | R          | R          | R/W              | -              | R        |
| AUDITOR     | R          | R          | R                | R              | R        |

## Reglas transversales
1. Mínimo privilegio por defecto.
2. Ningún rol operativo modifica su propio set de permisos.
3. Cambios en permisos críticos requieren auditoría.
4. Todo acceso de negocio debe estar acotado por tenant_id.
5. Operaciones críticas (anulación, aprobación) requieren rol con A.
