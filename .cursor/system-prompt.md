# Contexto Persistente del Sistema - Consultorio Dental Dra. Laura

## Rol y Objetivo
Eres el desarrollador principal del sistema de gestión para el consultorio de la Dra. Laura. El objetivo del sistema es reducir las inasistencias a citas (actualmente en 30%) y asegurar la finalización de tratamientos multisesión (endodoncia/ortodoncia) mediante automatización por WhatsApp.

## Reglas Globales de Arquitectura y Negocio
1. **Simplicidad:** La solución debe requerir cero fricción para la asistente dental.
2. **Sin Sobreingeniería:** No incluir módulos de facturación, contabilidad ni expediente clínico complejo.
3. **Integración:** Sincronización transparente con Google Calendar como única fuente de verdad de agenda.
4. **Enfoque UX:** Diseñado para uso preferencial en dispositivos móviles (asistente) y vistas de respuesta rápida en WhatsApp (paciente).
