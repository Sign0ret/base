# Requerimientos No Funcionales (NFR)

Este documento define los criterios de operación, rendimiento, seguridad y usabilidad del sistema.

## 1. Rendimiento (Performance)
* **NFR-01: Tiempo de Respuesta:** Las peticiones de lectura deben responder en menos de 200ms bajo condiciones normales.
* **NFR-02: Concurrencia:** El sistema debe soportar hasta 1,000 usuarios activos simultáneos sin degradación del servicio.

## 2. Seguridad
* **NFR-03: Cifrado de Datos y Autenticación:** Todos los datos en tránsito deben estar protegidos mediante TLS 1.3, y la gestión de identidad y autenticación debe realizarse exclusivamente mediante **Convex Auth**.
* **NFR-04: Control de Acceso:** Se debe implementar un modelo de Control de Acceso Basado en Roles (RBAC).

## 3. Disponibilidad y Mantenibilidad
* **NFR-05: Disponibilidad (Uptime):** El sistema debe garantizar una disponibilidad del 99.9% (SLA).
* **NFR-06: Documentación:** Toda la API o funciones expuestas deben estar documentadas apropiadamente.

## 4. Usabilidad
* **NFR-07: Compatibilidad:** La interfaz debe ser responsive y compatible con las últimas dos versiones de Chrome, Safari y Firefox.

## 5. Arquitectura y Stack Tecnológico
* **NFR-08: Framework de Aplicación:** La aplicación debe estar construida utilizando **Next.js**.
* **NFR-09: Base de Datos:** La persistencia de datos (DB) debe implementarse de forma obligatoria usando **Convex**.
* **NFR-10: Almacenamiento de Archivos (Storage):** Todo el manejo de archivos estáticos y subidas de usuarios debe gestionarse a través de **Convex Storage**.
* **NFR-11: Despliegue e Infraestructura:** El despliegue de la aplicación (Deployment) debe realizarse en **Vercel**.
