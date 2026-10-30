# Feature Spec: Confirmación Automatizada de Citas y Recuperación de Espacios

## 1. Definición del Problema
El consultorio de la Dra. Laura pierde un 30% de sus ingresos debido a pacientes que no asisten a sus citas. La asistente pierde hasta 2 horas diarias enviando mensajes manuales por WhatsApp uno a uno sin un registro estructurado de respuesta.

## 2. Diseño de la Solución
Un módulo automatizado de recordatorios que envía un mensaje dinámico por WhatsApp 24 horas antes de la cita con opciones de confirmación en un solo clic (Confirmar / Reagendar). Si el paciente reagenda o cancela, la agenda en Google Calendar se libera automáticamente y la asistente recibe un aviso en el dashboard.

## 3. Criterios de Aceptación Verificables
- [ ] **CA-1 (Envío Automático):** Todo paciente con cita agendada en Google Calendar para el día siguiente debe figurar en el tablero con un estado "Recordatorio Enviado" y un mensaje formateado listo para despacho.
- [ ] **CA-2 (Procesamiento de Respuesta):** Si el paciente responde "1" o "Confirmar", el estado de la cita en el tablero cambia automáticamente a "Confirmada" (color verde).
- [ ] **CA-3 (Reagendamiento y Liberación):** Si el paciente responde "2" o "Reagendar", el sistema sugiere 3 slots libres de Google Calendar y cambia el estado a "Espacio Liberado / Pendiente Reagendar" (color naranja).
- [ ] **CA-4 (Medición de Impacto):** El dashboard muestra un contador en tiempo real de "% de Inasistencia Estimado" que disminuye a medida que las citas pasan al estado "Confirmada".
