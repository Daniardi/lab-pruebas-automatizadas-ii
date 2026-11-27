# Respuesta inicial de IA — analisis de riesgos

Generada por Codex en esta sesion a partir del bloque Prompt de prompts/01_analisis_riesgos.md y los requisitos del repositorio. Es una propuesta, no un listado de bugs confirmados. La probabilidad es una estimacion cualitativa sin medicion de frecuencia. No se asumen compras, proveedores, lotes ni modulos externos al MVP.

|ID|Riesgo|Impacto|Probabilidad estimada|Modulo|Idea de prueba|Consecuencia|
|---|---|---|---|---|---|---|
|R01|Salidas mayores al disponible|Alto|Alta|Movimientos|OUT 10 con stock 3; nunca permitir negativo|Entrega ficticia y falta de insumos en laboratorio|
|R02|Valor de inventario incorrecto|Alto|Media|Dashboard|Recalcular Σ stock × precio en COP y comparar|Decisiones presupuestales y auditoria equivocadas|
|R03|Operador altera el catalogo|Alto|Media|Roles|Separar controles UI de rechazo del servidor|Cambios no autorizados de precios y productos|
|R04|SKU repetido|Alto|Media|Productos|Crear dos productos con el mismo SKU|Conteos y entregas atribuidos al articulo equivocado|
|R05|CSV incompleto|Alto|Media|Exportacion|Comparar cantidad e identidad de filas con catalogo|Conciliacion y soportes de auditoria incompletos|
|R06|ADJUST suma en vez de fijar el conteo|Alto|Media|Movimientos|Stock 10; conteo 4; esperado final 4|Diferencias fisicas se amplifican al conciliar|
|R07|Precio o stock inicial negativo|Alto|Media|Productos|Precio -100 COP y stock -1|Inventario y valor monetario inconsistentes|
|R08|Texto ejecuta scripts|Alto|Media|UI|Carga local inocua en nombre y observar ejecucion|Alteracion de la sesion del usuario|
|R09|Eliminacion rompe trazabilidad|Alto|Media|Integridad|Eliminar producto con movimientos y revisar referencias|Dificultad para reconstruir entregas|
|R10|Busqueda depende de mayusculas|Medio|Alta|Productos|Mouse, mouse y MOUSE deben devolver lo mismo|Creacion de duplicados por no hallar el producto|
|R11|Alertas omiten el limite exacto|Medio|Media|Alertas|Stock igual al minimo debe alertar|Reposicion tardia|
|R12|Vistas muestran estados distintos|Medio|Media|Integridad|Movimiento y revisar Productos, Alertas y Dashboard|Operador actua con informacion desactualizada|

Top 5 inicial sugerido: R01, R02, R03, R04, R05. La prioridad responde al posible dano en entregas, dinero y control de cambios. Estas estimaciones deben refinarse con la importancia del conteo fisico y evidencia real.
