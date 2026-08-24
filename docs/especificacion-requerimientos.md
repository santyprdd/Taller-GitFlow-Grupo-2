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

#### Resultado esperado

El sistema deberá validar las condiciones necesarias para que un estudiante pueda inscribirse en una tutoría. Si el estudiante se encuentra activo, la tutoría existe, hay cupos disponibles y no existe una inscripción previa, la validación deberá ser exitosa y se permitirá continuar con el proceso de inscripción. Si alguna condición no se cumple, el sistema deberá rechazar la inscripción y mostrar al estudiante un mensaje indicando claramente el motivo del rechazo.


## 4. Gestión de Versiones

### Ramas utilizadas

### Proceso de integración

### Conflictos encontrados
