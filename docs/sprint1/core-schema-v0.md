# Core Schema v0 - Sprint 1 Day 1

## Tablas iniciales
- tenants
- users
- products
- lots
- sales

## Reglas base
- Todas las tablas de negocio con tenant_id
- PK autoincremental o UUID (definir estándar)
- FK explícitas para integridad referencial
- Montos en DECIMAL(15,2) persistido
- Fechas en UTC

## Índices sugeridos
- tenants: (id), (status)
- users: (tenant_id, email) UNIQUE
- products: (tenant_id, sku) UNIQUE
- lots: (tenant_id, product_id), (expires_at)
- sales: (tenant_id, created_at), (status)
