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

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


### RF-03 - [Nombre del requerimiento]

#### Resumen

#### Entradas

| Entrada | Tipo de dato | Descripción |
|---|---|---|

#### Reglas o condiciones

#### Salidas

| Salida | Tipo de dato | Descripción |
|---|---|---|

#### Resultado esperado


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
