# Especificación de Requerimientos

## 1. Descripción del sistema

## 2. Integrantes

- Nombre: Santiago Perdomo Peñaranda
- Nombre: Andres David Ríos García
- Nombre: Juan David Penagos Jaramillo
- Nombre: Juan Jose Hurtado Ocampo
- Nombre: Samuel Ruiz Lizarazo

## 3. Requerimientos Funcionales

### RF-01 - Registrar tutorías académicas

#### Resumen
El sistema deberá permitir a los profesores registrar tutorías indicando su código de profesor, tema, fecha, hora de inicio y cantidad máxima de estudiantes. La fecha no podrá ser anterior a la actual y la cantidad de estudiantes deberá estar entre 1 y 10. Al registrarse correctamente, el sistema deberá asignar un identificador único y confirmar la creación.

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
| Código de profesor | String | Código que identifica al profesor que registra la tutoría. |
| Tema de la tutoría | String | Tema académico que se abordará durante la tutoría. |
| Fecha | Date | Fecha en la que se realizará la tutoría. |
| Hora de inicio | Time | Hora en la que comenzará la tutoría. |
| Cantidad máxima de estudiantes | Integer | Cantidad máxima de estudiantes que podrán participar en la tutoría. |

#### Reglas o condiciones

1. El código de profesor debe corresponder a un profesor registrado en la Universidad.
2. La fecha de la tutoría no puede ser anterior a la fecha actual.
3. La cantidad máxima de estudiantes debe estar entre 1 y 10.
4. Todos los datos requeridos deben ser ingresados.
5. El sistema debe asignar un identificador único a la tutoría.
6. Si alguna de las condiciones no se cumple, la tutoría no debe ser registrada.

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
| Identificador de la tutoría | String/Integer | Identificador único asignado a la tutoría por el sistema. |
| Mensaje de confirmación | String | Mensaje que informa al profesor que la tutoría fue creada correctamente. |
| Mensaje de error | String | Mensaje que informa el motivo por el cual no fue posible registrar la tutoría. |

#### Resultado esperado

El sistema registra correctamente la tutoría cuando todos los datos cumplen las condiciones establecidas, asigna un identificador único y muestra un mensaje de confirmación al profesor. Si alguna condición no se cumple, la tutoría no se registra y el sistema informa el motivo del error.


### RF-02 - [Nombre del requerimiento]

#### Resumen

El sistema deberá permitir a los estudiantes consultar las tutorías disponibles indicando una fecha y, opcionalmente, una asignatura o tema. 
El sistema deberá mostrar el identificador, tema, profesor responsable, fecha, hora y cantidad de cupos disponibles. si no existen resultados,
deberá informar al estudiante.

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
| Fecha | LocalDate | Fecha en la que el estudiante desea consultar las tutorías disponibles |
| Asignatura | String | Asignatura que el estudiante desea consultar |
| Tema | String | Tema específico que desea consultar |

#### Reglas o condiciones
La fecha es un dato obligatorio para consultar la tutoría
La asignatura y el tema son opcionales 
El sistema debe mostrar únicamente las tutorías que cumplan los criterios
Si se especifica uno de los criterios opcionales, los resultados deben coincidir 
Si no existen tutorías disponibles, el sistema deberá notificar al estudiante

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
| Identificador | Int | Identificador único de la tutoría |
| Tema | String | Tema a tratar en la tutoría |
| Profesor responsable | String | Profesor al que le corresponde la tutoría |
| Fecha | LocalDate | Hora de la tutoría |
| Hora | Time | hora de la tutoría |
| Cupos disponibles | Int | Cantidad de cupos disponibles |
| Mensaje | String | Mensaje si no existen tutorías |

#### Resultado esperado
El sistema muestra al estudiante las tutorías disponibles que coincidan con la fecha y, 
si fueron especificadas , con la asignatura o tema, mostrando su identificador, tema, profesor responsable, fecha, hora y cantidad de cupos disponibles.
Si no se encuentran tutorías, se informa al estudiante que no existen resultados.


### RF-03 - [Inscribir estudiantes en tutorías]

#### Resumen
El sistema deberá permitir a los estudiantes solicitar su inscripción a una tutoría mediante su código estudiantil y el identificador de la tutoría. La inscripción solo podrá realizarse si el estudiante está activo, la tutoría existe, tiene cupos disponibles y el estudiante no está previamente inscrito. Al completar la inscripción, el sistema deberá actualizar los cupos y mostrar una confirmación.

#### Entradas

| Entrada | Tipo de dato | Descripción |
| Código estudiantil | String o entero | Identificador único del estudiante que está solicitando la inscripción |
| Identificador de la tutoría | String o entero | Código único asignado por el sistema a la tutoría específica en la que el estudiante desea participar |

#### Reglas o condiciones
1. Estado del estudiante: El estudiante debe encontrarse activo en la Universidad.
2. Existencia de la tutoría: El identificador proporcionado debe corresponder a una tutoría que exista en el sistema.
3. Disponibilidad de cupos: La tutoría debe tener al menos un (1) cupo disponible en el momento de la solicitud.
4. Restricción de duplicidad: El estudiante no puede encontrarse previamente inscrito en la misma tutoría.

#### Salidas

| Salida | Tipo de dato | Descripción |
| Mensaje del sistema | String | Mensaje de confirmación indicando que la inscripción fue exitosa, o un mensaje de error explicando cuál de las condiciones no se cumplió |

#### Resultado esperado
El sistema registra de manera persistente la inscripción del estudiante en la tutoría solicitada. Adicionalmente, el sistema actualiza (reduce en 1) la cantidad de cupos que todavía se encuentran disponibles para esa tutoría.


### RF-04 - [Validar y rechazar inscripciones no validas]

#### Resumen El sistema debe validas las condiciones necesarias para realizar una inscripcion y, cuando alguna no se cumpla, debera impedir la inscripcion e informar al estudiante el motivo del rechazo.

#### Entradas: Codigo estudiantil y identificador de la tutoria

| Entrada | Tipo de dato | Descripción |
|---|---|---|
| Codigo estudiantil | String | Identificador del estudiante que solicita la inscripcion. |
| Identificador de la tutoria | String/Integer | Identificador unico de la tutoria en la que el estudiante desea inscribirse. |

#### Reglas o condiciones

1. El estudiante debe encontrarse activo en la Universidad.
2. La tutoría indicada debe existir en el sistema.
3. La tutoría debe tener al menos un cupo disponible.
4. El estudiante no debe estar previamente inscrito en la tutoría.
5. Si alguna de las condiciones anteriores no se cumple, la inscripción no deberá realizarse.
6. El sistema deberá informar al estudiante el motivo por el cual la inscripción fue rechazada.
7. Si todas las condiciones se cumplen, la validación será exitosa y podrá realizarse la inscripción.

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
| Resultado de la validacion | Boolean | Indica si el estudiante cumple las condiciones necesarias para realizar la inscripcion. |
| Mensaje de resultado | String | Informa al estudiante si la inscripcion puede realizarse o el motivo por el cual fue rechazada. |

### RF-05 - Cancelar inscripción en una tutoría

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|
| Código de estudiante | String | Identificador único del estudiante que desea cancelar su participación en la tutoría. |
| Identificador de la tutoría | String/Integer | Identificador único de la tutoría en la cual el estudiante se encuentra inscrito. |

#### Reglas o condiciones

1. El estudiante debe tener una inscripción previa en la tutoría indicada.
2. La tutoría debe existir en el sistema.
3. La tutoría no debe haber comenzado al momento de solicitar la cancelación.
4. Si se cumplen todas las condiciones, el sistema deberá eliminar la inscripción del estudiante.
5. Al realizar la cancelación, el sistema deberá liberar nuevamente el cupo correspondiente.
6. Si alguna de las condiciones no se cumple, la cancelación no deberá realizarse y el sistema deberá informar el motivo.

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|
| Estado de la cancelación | Boolean | Indica si la cancelación de la inscripción fue realizada exitosamente. |
| Cupos disponibles actualizados | Integer | Cantidad de cupos disponibles en la tutoría después de realizar la cancelación. |
| Mensaje de confirmación | String | Mensaje que informa al estudiante que la cancelación fue realizada correctamente. |
| Mensaje de error | String | Mensaje que informa al estudiante el motivo por el cual no fue posible realizar la cancelación. |

#### Resultado esperado

El sistema deberá validar las condiciones necesarias para que un estudiante pueda inscribirse en una tutoría. Si el estudiante se encuentra activo, la tutoría existe, hay cupos disponibles y no existe una inscripción previa, la validación deberá ser exitosa y se permitirá continuar con el proceso de inscripción. Si alguna condición no se cumple, el sistema deberá rechazar la inscripción y mostrar al estudiante un mensaje indicando claramente el motivo del rechazo.


## 4. Gestión de Versiones

### Ramas utilizadas

Para el desarrollo del proyecto se utilizaron diferentes ramas en Git con el objetivo de organizar el trabajo de cada integrante y evitar modificaciones directas sobre la rama principal.

- `main`: Rama principal del proyecto, utilizada para almacenar las versiones estables y funcionales del sistema.
- `develop`: Rama utilizada para integrar y probar los cambios realizados por los integrantes antes de incorporarlos a la rama principal.
- `feature/registro-tutorias`: Rama destinada al desarrollo del RF-01, correspondiente al registro de tutorías académicas.
- `feature/consulta-tutorias`: Rama destinada al desarrollo del RF-02, correspondiente a la consulta de tutorías disponibles.
- `feature/inscripcion-tutorias`: Rama destinada al desarrollo de los RF-03 y RF-04, relacionados con la inscripción y validación de estudiantes.
- `feature/cancelacion-inscripcion`: Rama destinada al desarrollo del RF-05, correspondiente a la cancelación de inscripciones.

### Proceso de integración

El desarrollo se realizó utilizando Git como sistema de control de versiones. Cada integrante trabajó en una rama independiente de acuerdo con el requerimiento asignado.

El proceso de integración fue el siguiente:

1. Se creó una rama específica para cada funcionalidad.
2. Cada integrante realizó sus modificaciones y las registró mediante commits.
3. Los cambios fueron enviados al repositorio remoto mediante `push`.
4. Una vez finalizado un requerimiento, se integraron los cambios en la rama `develop`.
5. Se realizaron pruebas para comprobar que las nuevas funcionalidades funcionaran correctamente y no afectaran las funcionalidades existentes.
6. Después de verificar el funcionamiento del sistema, los cambios fueron integrados a la rama `main`.

### Conflictos encontrados

Durante el desarrollo se presentaron conflictos al integrar algunos cambios realizados de manera simultánea sobre archivos relacionados con las funcionalidades de tutorías.

Los conflictos fueron solucionados revisando las modificaciones realizadas por cada integrante y seleccionando o combinando los cambios necesarios. Posteriormente, se realizaron pruebas para verificar que la solución del conflicto no afectara el funcionamiento de los requerimientos implementados.

Una vez solucionados los conflictos y verificadas las funcionalidades, los cambios fueron integrados nuevamente a la rama correspondiente.
