¿Por qué es mala práctica usar SELECT * en producción? Mencioná al menos dos razones concretas (rendimiento, mantenibilidad, seguridad).

Un motivo podria ser el tráfico innecesario: Si una tabla tiene 40 columnas o campos de texto largo, transferir todo a través de la red consume mucha memoria (RAM) y ancho de banda.
Se podría exponer accidentalmente datos sensibles (como contraseñas, documentos de identidad o sueldos) si la tabla contiene columnas privadas que no deberían mostrarse en ese reporte.

¿Por qué son importantes los alias para un stakeholder no técnico? Explicá con un ejemplo concreto cómo un alias transforma total_amount en algo que cualquier persona del área de finanzas puede interpretar directamente.

Los Alias te permiten renombrar temporalmente estas columnas en el resultado de tu consulta para que sean amigables para el usuario final, en este caso renombraríamos asi: Select total_amount AS monto_total FROM (tabla sales).

Son importantes porque aportan claridad, sirve por si luego se exporta a Power BI o Excel, deja todo listo para armar una presentación y se utiliza para dar nombre a resultados de calculos.
