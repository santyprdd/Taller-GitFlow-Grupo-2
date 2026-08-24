# Especificación de Requerimientos

## 1. Descripción del sistema

## 2. Integrantes

- Nombre: Santiago Perdomo Peñaranda
- Nombre: Andres David Ríos García
- Nombre: Juan David Penagos Jaramillo
- Nombre: Juan Jose Hurtado Ocampo
- Nombre: Samuel Ruiz Lizarazo

## 3. Requerimientos Funcionales

### RF-01 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


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


### RF-04 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

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

El sistema deberá cancelar correctamente la inscripción del estudiante cuando exista una inscripción previa y la tutoría aún no haya comenzado. Una vez realizada la cancelación, deberá eliminar la inscripción, liberar el cupo correspondiente y mostrar un mensaje de confirmación.

Si alguna de las condiciones establecidas no se cumple, la inscripción no deberá ser cancelada y el sistema deberá mostrar un mensaje indicando el motivo.


## 4. Gestión de Versiones

### Ramas utilizadas

### Proceso de integración

### Conflictos encontrados
