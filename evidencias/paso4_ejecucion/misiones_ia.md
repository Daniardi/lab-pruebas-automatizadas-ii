# Respuesta IA — tres misiones de 25 minutos

Generada en esta sesion a partir de prompts/03_exploracion_guiada.md.

A. Integridad de stock (elegida): atacar OUT superior/igual/cero/negativo, ADJUST menor y cero, repeticion de conteos y frontera stock=minimo. Falla si cambia stock en contra de RF-04 o se pierde coherencia con Alertas. No dispersarse a estilos visuales.

B. Credibilidad de dashboard y CSV: recalcular COP, contar SKU y verificar comas/comillas y articulos sin stock. Falla si se pierde un registro o cambia el valor monetario. No asumir que tener el mismo numero de filas garantiza contenido correcto.

C. Permisos y texto: comparar operador/admin y contextos de renderizado de un payload local inocuo. Separar controles UI de autorizacion API. Un comentario de codigo no demuestra XSS.

Notas de sesion: hora, idea, dato, observacion, evidencia, requisito, bug candidato y siguiente experimento. La sesion A se ejecuta con navegador real y se registra en exploracion/sesion.json; el metodo es asistido por agente e incluye analisis entre experimentos, no se afirma operacion manual humana continua.
