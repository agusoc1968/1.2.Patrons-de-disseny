Inyección  de dependencias

El patrón sigue este comportamiento.

Se añade una nueva tarea y comprobamos que realmente sea nueva (que no exista previamente) y si está completada la borra porque sólo se conservan y se muestran las pendientes.

Esto supone un problema porque podemos dar de alta una nueva tarea que, previamente, haya sido realizada y, por tanto, haya sido borrada.

Podemos consultar directamente la lista existente de las tareas pendientes, pero no la de las ya realizadas, porque ya han sido borradas.

A comprobar si la tarea está realizada, lo comprueba sobre el listado de las tareas pendientes, por lo que busca exactamente los mismos valores y se produce el riesgo de incluir dos tareas similares o idénticas, pero con formulación diferente. Esto supone un riesgo de integridad de la base de la lista de las tareas.

La consulta de la lista de tareas se puede realizar en cualquier momento, porque el patrón está pensado para que sea una ejecución directa, lo que supone la ejecución de un comando que "depure" las tareas ya terminadas.
