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

#### Resultado esperado


## 4. Gestión de Versiones

### Ramas utilizadas

### Proceso de integración

### Conflictos encontrados
