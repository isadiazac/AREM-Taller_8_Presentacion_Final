# 📄 Resumen Ejecutivo del Proyecto Arquitectónico

## 🏢 Nombre del Cliente

Falek Latina S.A.S.

## 🎯 Objetivo General del Proyecto

El proyecto tuvo como propósito analizar la arquitectura empresarial y tecnológica de Falek Latina S.A.S. para identificar limitaciones que afectan su operación y crecimiento estratégico. Se evaluaron los procesos críticos, la infraestructura, la gestión de datos, la seguridad y el cumplimiento normativo de la organización, con el fin de proponer soluciones que permitan mejorar la integración tecnológica, reducir riesgos operacionales y habilitar la expansión internacional de la empresa hacia Miami.

## 🧱 Vistas Arquitectónicas Cubiertas

| Vista                   | Alcance de la Solución                                                                                                  |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| Procesos de Negocio     | Análisis del proceso de gestión de cotizaciones y flujo operativo entre sedes.                                          |
| Información / Datos     | Identificación de silos de información y ausencia de una fuente única de verdad para clientes, precios e inventario.    |
| Aplicaciones / Sistemas | Evaluación de integración entre Excel, Helisa y Google Suite; propuesta de CRM SaaS integrado vía API REST.             |
| Infraestructura         | Diagnóstico del servidor local como Punto Único de Falla (SPOF) y propuesta de migración a Google Cloud Platform.       |
| Seguridad               | Análisis STRIDE del proceso de cotizaciones e identificación de amenazas activas; propuesta de MFA, RBAC y cifrado TLS. |
| Cumplimiento Normativo  | Evaluación de cumplimiento de Ley 1581 (Habeas Data) e identificación de brechas frente a ISO 27001.                    |

## 🧩 Hallazgos Clave

* ❗ Se identificó que el proceso de cotizaciones depende de archivos Excel desconectados del inventario y del sistema contable, generando errores manuales y falta de trazabilidad.
* 🔄 La arquitectura actual presenta ausencia total de integración entre Excel, Helisa y Google Suite, provocando duplicidad de información y silos de datos.
* 📌 Existe un Punto Único de Falla (SPOF) en el servidor local ubicado en Bogotá, lo que pone en riesgo la operación de las tres sedes de la empresa.
* 🔐 El análisis STRIDE identificó amenazas relacionadas con autenticación débil, ausencia de cifrado y falta de auditoría de accesos.
* ⚖️ Se evidenció incumplimiento parcial de la Ley 1581 de protección de datos personales, con riesgo de sanciones regulatorias.
* 🌎 La arquitectura tecnológica actual dificulta técnicamente la expansión internacional proyectada hacia Miami.

## 🚀 Recomendaciones Principales

* Implementar un CRM SaaS integrado con Helisa mediante API REST para centralizar clientes y automatizar cotizaciones.
* Migrar la infraestructura local hacia Google Cloud Platform para eliminar el SPOF y habilitar acceso remoto seguro.
* Implementar autenticación multifactor (MFA), control de acceso basado en roles (RBAC) y cifrado TLS para fortalecer la seguridad.
* Adecuar la organización a la Ley 1581 mediante políticas de privacidad, canales ARCO y responsables de tratamiento de datos.
* Definir políticas de seguridad de la información y establecer prácticas formales de gobierno TI y gestión de cambios.

## 💡 Reflexión Final

Este proyecto permitió aplicar de manera práctica los conceptos de arquitectura empresarial en un contexto organizacional real, abordando problemáticas relacionadas con procesos, infraestructura, seguridad y cumplimiento normativo. El ejercicio fortaleció las capacidades del equipo en análisis arquitectónico, identificación de riesgos, modelado empresarial y formulación de soluciones tecnológicas alineadas con los objetivos estratégicos del negocio.

---

*Este resumen ejecutivo forma parte de la entrega final del curso AREM - Arquitectura Empresarial - Universidad de La Sabana.*
