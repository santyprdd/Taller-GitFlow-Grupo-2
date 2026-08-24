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

#### Resultado esperado


## 4. Gestión de Versiones

### Ramas utilizadas

### Proceso de integración

### Conflictos encontrados
