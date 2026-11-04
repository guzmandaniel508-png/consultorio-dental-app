# Feature Spec: Seguimiento de tratamientos de varias sesiones

## 1. Problema
Los pacientes con endodoncia u ortodoncia dejan de venir cuando el dolor desaparece. Nadie les da seguimiento, el tratamiento queda incompleto y la Dra. Laura pierde ingresos y resultados clínicos.

## 2. Usuarios
- **Marcela (asistente):** usuaria diaria. Necesita saber a quién escribir, sin revisar la agenda a mano.
- **Dra. Laura:** consulta cuántos tratamientos se terminan.

## 3. Solución
Cada tratamiento tiene un número de sesiones. Si un paciente con tratamiento incompleto pasa 7 días sin una cita agendada, aparece en la lista "Pacientes por recuperar" con un mensaje de WhatsApp ya redactado.

## 4. Alcance
**Incluye:** lista de pacientes por recuperar, progreso por sesiones, mensaje prellenado, marcar "Ya agendó".
**No incluye:** facturación, expediente clínico, envío automático sin intervención de Marcela.

## 5. Criterios de aceptación
- [ ] **CA-1:** Dado un tratamiento de 3 sesiones con 1 completada, cuando pasan 7 días sin cita agendada, entonces el paciente aparece en "Pacientes por recuperar".
- [ ] **CA-2:** Dado un paciente en la lista, cuando Marcela pulsa "Enviar por WhatsApp", entonces se abre WhatsApp con un mensaje que incluye su nombre, el tratamiento y la siguiente sesión.
- [ ] **CA-3:** Dado un paciente en la lista, cuando Marcela pulsa "Ya agendó", entonces sale de la lista en menos de 1 segundo y el contador se actualiza.
- [ ] **CA-4:** Los pacientes con 14 días o más sin volver se muestran en rojo y primero en la lista.
- [ ] **CA-5:** Marcela completa el flujo (abrir, enviar mensaje, marcar agendado) en 3 clics o menos por paciente.
- [ ] **CA-6:** Si no hay pacientes por recuperar, la pantalla lo dice y explica cuándo aparecerá alguien.

## 6. Métricas de éxito
| Métrica | Línea base | Meta a 3 meses | Cómo se mide |
|---|---|---|---|
| Tratamientos terminados | 50% | 75% | Tratamientos con todas las sesiones / tratamientos iniciados |
| Pacientes recuperados | 0 | 60% de los contactados agenda en 7 días | "Ya agendó" / mensajes enviados |
| Tiempo en mensajes | 2 h/día | 20 min/día | Registro semanal de Marcela |
| Inasistencia general | 30% | 15% | Citas no atendidas / citas agendadas |

## 7. Riesgos
- El paciente se molesta por mensajes repetidos: máximo 2 mensajes por paciente cada 14 días.
- Datos desactualizados en Google Calendar: Marcela confirma con "Ya agendó".
