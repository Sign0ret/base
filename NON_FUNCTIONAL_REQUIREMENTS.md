# Requerimientos No Funcionales (NFR)

Este documento define los criterios de operación, rendimiento, seguridad y usabilidad del sistema.

## 1. Rendimiento (Performance)
* **NFR-01: Tiempo de Respuesta:** Las peticiones de lectura deben responder en menos de 200ms bajo condiciones normales.
* **NFR-02: Concurrencia:** El sistema debe soportar hasta 1,000 usuarios activos simultáneos sin degradación del servicio.

## 2. Seguridad
* **NFR-03: Cifrado de Datos:** Todos los datos en tránsito deben estar protegidos mediante TLS 1.3, y las contraseñas deben almacenarse usando el algoritmo Argon2 o BCrypt.
* **NFR-04: Control de Acceso:** Se debe implementar un modelo de Control de Acceso Basado en Roles (RBAC).

## 3. Disponibilidad y Mantenibilidad
* **NFR-05: Disponibilidad (Uptime):** El sistema debe garantizar una disponibilidad del 99.9% (SLA).
* **NFR-06: Documentación:** Toda la API debe estar documentada bajo el estándar OpenAPI (Swagger).

## 4. Usabilidad
* **NFR-07: Compatibilidad:** La interfaz debe ser responsive y compatible con las últimas dos versiones de Chrome, Safari y Firefox.