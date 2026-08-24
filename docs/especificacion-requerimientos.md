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

#### Resultado esperado


## 4. Gestión de Versiones

### Ramas utilizadas

### Proceso de integración

### Conflictos encontrados
