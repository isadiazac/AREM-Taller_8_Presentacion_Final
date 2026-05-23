# Resumen Ejecutivo – Proyecto Aplicado de Arquitectura Empresarial
## Falek Latina S.A.S.

**Equipo:** Isabela Díaz Acosta · Samuel Esteban López Huertas · Sebastián Sánchez Sandoval  
**Materia:** Arquitectura Empresarial · Universidad de La Sabana · 2026

---

## El cliente

Falek Latina S.A.S. es una empresa colombiana con más de 40 años de experiencia en el suministro y comercialización de insumos industriales y maquinaria para el sector metalúrgico. Opera con 12 empleados y aproximadamente 100 clientes activos, con sede principal en Bogotá y operaciones en Cota y Barranquilla. Su CEO, Alejandra Galindo, tiene como objetivo estratégico declarado la expansión a Miami para gestionar distribución desde China y EE.UU.

## El problema central

La arquitectura tecnológica actual de Falek Latina frena en lugar de habilitar sus objetivos estratégicos. El proceso más crítico de la empresa —la gestión de cotizaciones, corazón de la atención al cliente— corre sobre archivos Excel desconectados del inventario real y del sistema contable. No existe integración entre los tres sistemas que usa la empresa (Excel, Helisa y Google Suite), lo que genera silos de información, errores manuales, doble digitación y ausencia total de trazabilidad.

## Hallazgos principales

A lo largo del proyecto se identificaron **20 riesgos** distribuidos en 7 dominios de arquitectura:

- **Infraestructura:** Un servidor local en Bogotá actúa como Punto Único de Falla (SPOF). Si cae, las tres sedes pierden operatividad simultáneamente. No existe disaster recovery ni política de backups verificada.
- **Aplicaciones:** Excel opera como sistema transaccional, concentrando riesgos de errores, pérdida de datos y vulnerabilidades de seguridad identificadas en el análisis STRIDE.
- **Datos:** No existe fuente única de verdad para clientes, precios ni inventario. Los datos están dispersos en correos, hojas de cálculo y el ERP contable sin integración.
- **Seguridad:** Sin autenticación multifactor, sin cifrado de datos en tránsito, sin logs de auditoría y sin plan de respuesta a incidentes. El análisis STRIDE identificó 6 amenazas activas en el proceso de cotizaciones.
- **Normativo:** 4 criterios No cumple en Ley 1581 (Habeas Data), con riesgo de sanciones SIC de hasta 2.000 SMMLV. Sin certificación ni controles ISO 27001.
- **Negocio:** La arquitectura actual hace técnicamente imposible la expansión a Miami sin una transformación completa.

## La propuesta TO-BE

Se proponen 5 iniciativas priorizadas que transforman la arquitectura de Falek Latina en una ventaja competitiva:

1. **CRM SaaS integrado con Helisa** (Prioridad Alta): adoptar HubSpot o Zoho CRM para centralizar clientes, automatizar cotizaciones e integrar con Helisa vía API REST. Elimina Excel como sistema operacional.
2. **Migración a Google Cloud Platform** (Prioridad Alta): eliminar el SPOF migrando el servidor local a GCP. Habilita acceso remoto desde Miami y las sedes regionales.
3. **Seguridad: MFA + RBAC + TLS** (Prioridad Alta): implementar autenticación multifactor, control de accesos por rol y cifrado. Mitiga las 6 amenazas STRIDE identificadas.
4. **Adecuación normativa Ley 1581** (Prioridad Alta): publicar política de privacidad, habilitar canal ARCO y designar responsable de datos. Plazo: 30 días.
5. **Política de SI y gobierno TI** (Prioridad Media): documentar arquitectura, aprobar política de seguridad y establecer gestión de cambios.

## Hoja de ruta

| Plazo | Iniciativa |
|---|---|
| 30 días | Adecuación Ley 1581 + MFA |
| 60 días | CRM SaaS + integración Helisa |
| 90 días | Migración servidor → GCP |
| 6 meses | Política de SI + gobierno TI completo |

## Impacto esperado

La implementación de estas iniciativas permitirá a Falek Latina reducir el tiempo de generación de cotizaciones, eliminar el riesgo de pérdida total de operación por fallo de infraestructura, cumplir con la normativa colombiana de protección de datos, y habilitar técnicamente la expansión a Miami que es el objetivo estratégico de mayor impacto para el crecimiento de la empresa.

---

_Universidad de La Sabana · Arquitectura Empresarial · 2026_
