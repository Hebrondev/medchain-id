# MedChain ID --- Historias de Usuario

**Integrante:** Hernan Daniel Briceño\
**GitHub:** `hebrondev`\
**Rol:** Desarrollador, Orquestador y Responsable de Entregas

## Mis historias de usuario

Las siguientes historias de usuario representan necesidades principales
del producto **MedChain ID**, considerando diferentes roles dentro del
ecosistema de atención en salud. Se encuentran organizadas de mayor a
menor importancia para el desarrollo inicial del producto.

### 1. Identidad médica portable

> **Como paciente quiero contar con una identidad médica portable para
> asociar y consultar mis registros de salud independientemente de la
> institución donde fueron generados.**

**Prioridad:** Muy alta

Esta es la historia central de MedChain ID, ya que permite establecer
una identidad que pueda acompañar al paciente entre diferentes
instituciones y contextos de atención.

### 2. Consulta de registros médicos

> **Como paciente quiero consultar mis registros médicos asociados a mi
> identidad para acceder fácilmente a mi información de salud cuando la
> necesite.**

**Prioridad:** Muy alta

Esta historia aborda directamente la dificultad de acceder a información
médica que puede encontrarse distribuida entre diferentes instituciones,
plataformas o documentos.

### 3. Verificación de autenticidad

> **Como profesional de salud quiero verificar que un registro médico
> fue emitido por una institución autorizada para confiar en la
> autenticidad de la información recibida.**

**Prioridad:** Alta

Esta funcionalidad permite verificar la procedencia de los registros
médicos y fortalecer la confianza en la información utilizada durante la
atención.

### 4. Compartir información de manera controlada

> **Como paciente quiero autorizar a un profesional o institución a
> consultar determinados registros médicos para compartir únicamente la
> información necesaria para mi atención.**

**Prioridad:** Alta

Esta historia incorpora el control del paciente sobre el acceso a su
información, evitando que compartir información implique necesariamente
entregar todo su historial médico.

### 5. Revocar autorización

> **Como paciente quiero revocar una autorización previamente concedida
> para recuperar el control sobre quién puede consultar mis registros
> médicos.**

**Prioridad:** Alta

La gestión de permisos debe contemplar no solamente la autorización,
sino también la posibilidad de revocar accesos previamente concedidos.

### 6. Registrar un documento médico verificable

> **Como institución de salud quiero registrar la existencia y
> procedencia de un documento médico para que posteriormente pueda
> verificarse que fue emitido por nuestra institución.**

**Prioridad:** Media/Alta

Esta historia incorpora a las instituciones de salud como actores del
ecosistema, permitiendo asociar la procedencia de los registros con la
entidad que los generó.

### 7. Atención entre instituciones

> **Como profesional de salud quiero consultar registros médicos
> previamente autorizados por el paciente para disponer de información
> relevante cuando atiendo a una persona proveniente de otra
> institución.**

**Prioridad:** Media

Esta historia representa uno de los escenarios principales de uso de
MedChain ID: facilitar la continuidad de la atención cuando un paciente
cambia de institución, ciudad, especialista o contexto de atención.

## La más importante y por qué

### Historia #1 --- Identidad médica portable

> **Como paciente quiero contar con una identidad médica portable para
> asociar y consultar mis registros de salud independientemente de la
> institución donde fueron generados.**

Esta es la historia más importante porque constituye el núcleo funcional
de **MedChain ID**. El problema identificado no consiste únicamente en
almacenar documentos médicos, sino en la dificultad que tiene el
paciente para mantener una relación portable con información que
actualmente se encuentra distribuida entre diferentes instituciones.

A partir de esta identidad se pueden construir las demás funcionalidades
del producto: asociación de registros, consulta, verificación de
procedencia, autorización de acceso y revocación de permisos.

Además, esta historia mantiene el enfoque definido para MedChain ID: no
crear un nuevo repositorio centralizado de historias clínicas, sino
facilitar una capa que permita al paciente relacionarse con registros
que pueden permanecer almacenados fuera de la blockchain.

## Resumen de prioridades

  Prioridad   Historia                                     Rol
  ----------- -------------------------------------------- ----------------------
  1           Identidad médica portable                    Paciente
  2           Consulta de registros médicos                Paciente
  3           Verificación de autenticidad                 Profesional de salud
  4           Compartir información de manera controlada   Paciente
  5           Revocar autorización                         Paciente
  6           Registrar un documento médico verificable    Institución de salud
  7           Atención entre instituciones                 Profesional de salud
