# SETUP_FLOW.md

Este documento define el flujo estandarizado de inicialización de proyectos, desde el scaffold inicial hasta el despliegue y la iteración por ramas.

---

## 🚀 Flujo de Configuración (Paso a Paso)

### Fase 1: Estructura y Backend
1.  **Instalar Next.js Latest:**
    * Ejecutar: `pnpm create next-app@latest`
    * Configuración: App Router, TypeScript, ESLint, Tailwind CSS.
2.  **Instalar Convex:**
    * Ejecutar: `pnpm add convex`
    * Inicializar con `npx convex dev` para vincular el dashboard.
3.  **Agregar Wrapper de Convex:**
    * Crear `ConvexClientProvider.tsx` y envolver el `layout.tsx` principal.
4.  **Configurar Auth de Convex:**
    * Implementar el método de autenticación (Clerk o Auth.js integrado) según la documentación oficial de Convex.

### Fase 2: UI y Especificaciones
5.  **Instalar Shadcn/UI (Custom Colors):**
    * Ejecutar: `npx shadcn-ui@latest init`
    * Configurar variables CSS personalizadas para mantener la identidad visual del proyecto desde el inicio.
6.  **Definir Requerimientos Funcionales:**
    * Crear el archivo `FUNCTIONAL_REQUIREMENTS.md` específico para el proyecto actual.

### Fase 3: Generación e Inteligencia Artificial
7.  **Generación con OPUS:**
    * Proveer a Claude OPUS los archivos `FUNCTIONAL_REQUIREMENTS.md` y `NON_FUNCTIONAL_REQUIREMENTS.md`.
    * Solicitar la generación de esquemas de base de datos, Server Functions y componentes base siguiendo ambos documentos.

### Fase 4: Despliegue y Control de Calidad
8.  **Configuración de Deployment:**
    * Vincular el repositorio a **Vercel**.
    * Configurar las variables de entorno (`CONVEX_DEPLOYMENT_KEY`, `NEXT_PUBLIC_CONVEX_URL`, etc.) en los dashboards de Vercel y Convex.
9.  **Validación de Flujo:**
    * Realizar pruebas E2E básicas para confirmar que la lectura/escritura en Convex y la autenticación funcionan en producción.

### Fase 5: Ciclo de Desarrollo
10. **Iteración por Branches:**
    * Una vez validado el plan inicial, crear ramas independientes por funcionalidad (ej. `feat/auth`, `feat/dashboard`) para mejorar el sistema por partes.

---

> **Nota:** Nunca saltar el paso 7; la alineación entre los requerimientos no funcionales (rendimiento/seguridad) y el código generado por IA es crítica para evitar deuda técnica temprana.