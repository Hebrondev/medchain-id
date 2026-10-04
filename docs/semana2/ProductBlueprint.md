# Product Blueprint --- MedChain ID

## 1. Priorización de historias

### 1.1 Objetivo

Esta sección consolida y prioriza las historias de usuario propuestas
por los integrantes del equipo para definir el alcance inicial del
producto **MedChain ID**.

La consolidación busca evitar duplicidades entre historias que
representan una misma necesidad funcional y, al mismo tiempo, conservar
aquellas propuestas que aportan capacidades diferenciadas al producto.

La priorización se realiza tomando como referencia el problema definido
en el `ProblemBrief.md`: la fragmentación de información médica entre
diferentes instituciones, plataformas y ubicaciones, especialmente
cuando el paciente necesita acceder, compartir o verificar la
procedencia de sus registros.

> **Estado de esta priorización:** propuesta de consolidación basada en
> las historias disponibles de tres integrantes del equipo: Ana Culma,
> John Fredy Rojas Ceballos y Hernan Daniel Briceño. Las historias que
> presente posteriormente Moises Higuera Acosta deberán evaluarse con
> los mismos criterios antes de considerar una modificación de la
> priorización definitiva.

------------------------------------------------------------------------

### 1.2 Criterios de priorización

Las historias se evaluaron utilizando los siguientes criterios:

1.  **Valor para el problema:** grado en que la historia contribuye
    directamente a reducir la fragmentación de la información médica.
2.  **Dependencia funcional:** necesidad de la funcionalidad para que
    otras capacidades del producto puedan operar.
3.  **Viabilidad del MVP:** posibilidad de implementar y demostrar la
    funcionalidad sin construir desde el inicio un ecosistema sanitario
    completo.
4.  **Impacto para el usuario:** beneficio directo para pacientes,
    profesionales o instituciones.
5.  **Pertinencia tecnológica:** capacidad de la funcionalidad para
    ayudar a demostrar el valor de una capa de confianza, verificación,
    autorización o trazabilidad, sin asumir que blockchain es necesaria
    cuando una alternativa convencional sería suficiente.
6.  **Complejidad y riesgo:** esfuerzo técnico, operativo, de seguridad
    y de gobernanza requerido para implementar la funcionalidad.

La prioridad no representa únicamente la importancia de una necesidad.
También considera el orden lógico en el que las capacidades deberían
incorporarse para construir un producto mínimo coherente.

------------------------------------------------------------------------

## 1.3 Consolidación de historias

Las historias individuales presentaron varias necesidades coincidentes.
Por ello, se consolidaron las propuestas equivalentes en una única
historia funcional, evitando crear tarjetas duplicadas en el backlog.

  -----------------------------------------------------------------------
  ID                      Historia consolidada    Propuestas relacionadas
  ----------------------- ----------------------- -----------------------
  **US-01**               Identidad médica        Hernan + Ana
                          portable                

  **US-02**               Registro y vinculación  Hernan + Ana
                          de documentos médicos   

  **US-03**               Consulta y organización Hernan + Ana
                          de registros médicos    

  **US-04**               Verificación de         Hernan + Ana
                          procedencia y           
                          autenticidad            

  **US-05**               Autorización para       Hernan + Ana
                          compartir información   

  **US-06**               Gestión y revocación de Hernan + Ana
                          permisos                

  **US-07**               Trazabilidad de accesos Ana + Hernan

  **US-08**               Atención médica entre   Hernan
                          instituciones           

  **US-09**               Verificación y          John
                          onboarding de           
                          instituciones           

  **US-10**               Integración con         John
                          sistemas HIS/EMR        
                          mediante API            

  **US-11**               Acceso de emergencia    John
                          --- Break-Glass         

  **US-12**               Autorización de acceso  John
                          temporal                

  **US-13**               Alertas y               John
                          notificaciones activas  

  **US-14**               Gestión de dependientes John
                          y menores               
  -----------------------------------------------------------------------

La consolidación no elimina la autoría de las propuestas originales.
Cada historia consolidada conserva como referencia los integrantes que
propusieron la necesidad funcional correspondiente.

------------------------------------------------------------------------

# 1.4 Priorización P0 --- Núcleo del MVP

Las siguientes historias conforman el núcleo inicial recomendado para
MedChain ID.

  ------------------------------------------------------------------------
                  Orden ID               Historia         Rol principal
                                         consolidada      
  --------------------- ---------------- ---------------- ----------------
                  **1** **US-01**        Identidad médica Paciente
                                         portable         

                  **2** **US-02**        Registro y       Entidad
                                         vinculación de   prestadora
                                         documentos       
                                         médicos          

                  **3** **US-03**        Consulta y       Paciente
                                         organización de  
                                         registros        
                                         médicos          

                  **4** **US-04**        Verificación de  Profesional de
                                         procedencia y    salud
                                         autenticidad     

                  **5** **US-05**        Autorización     Paciente
                                         para compartir   
                                         información      

                  **6** **US-06**        Gestión y        Paciente
                                         revocación de    
                                         permisos         

                  **7** **US-07**        Trazabilidad de  Paciente
                                         accesos          
  ------------------------------------------------------------------------

### Justificación del nivel P0

Estas siete historias forman una cadena funcional coherente:

**Identidad → Registro → Consulta → Verificación → Autorización →
Control de permisos → Trazabilidad**

La **US-01 --- Identidad médica portable** constituye el punto de
partida porque permite establecer la relación entre el paciente y sus
registros, independientemente de la institución que los haya generado.

La **US-02 --- Registro y vinculación de documentos médicos** permite
que las instituciones relacionen los documentos que generan con el
paciente correspondiente, sin sustituir la custodia institucional de la
historia clínica.

La **US-03 --- Consulta y organización de registros médicos** responde
directamente a la necesidad del paciente de localizar información
distribuida entre diferentes entidades.

La **US-04 --- Verificación de procedencia y autenticidad** incorpora la
necesidad de comprobar qué institución emitió un registro y fortalecer
la confianza sobre su procedencia.

La **US-05 --- Autorización para compartir información** permite que el
paciente controle qué información pone a disposición de un profesional o
institución.

La **US-06 --- Gestión y revocación de permisos** complementa la
autorización permitiendo consultar y retirar permisos previamente
concedidos.

Finalmente, la **US-07 --- Trazabilidad de accesos** permite conocer
cuándo y quién ha utilizado información cuyo acceso fue autorizado.

En conjunto, estas historias permiten demostrar el flujo fundamental de
valor de MedChain ID sin convertir el MVP en un sistema completo de
historia clínica.

------------------------------------------------------------------------

# 1.5 Priorización P1 --- Evolución y escalabilidad

Las siguientes historias se consideran de alta importancia, pero se
recomienda incorporarlas después de validar el núcleo del MVP.

  ------------------------------------------------------------------------
                  Orden ID               Historia         Rol principal
                                         consolidada      
  --------------------- ---------------- ---------------- ----------------
                  **8** **US-08**        Atención médica  Profesional de
                                         entre            salud
                                         instituciones    

                  **9** **US-09**        Verificación y   Administrador de
                                         onboarding de    red
                                         instituciones    

                 **10** **US-10**        Integración con  Administrador de
                                         sistemas HIS/EMR TI
                                         mediante API     

                 **11** **US-11**        Acceso de        Médico de
                                         emergencia ---   urgencias
                                         Break-Glass      
  ------------------------------------------------------------------------

### Justificación del nivel P1

La **US-08 --- Atención médica entre instituciones** representa uno de
los escenarios principales de uso de MedChain ID: facilitar la
continuidad de atención cuando el paciente cambia de institución,
ciudad, especialista o contexto de atención.

La **US-09 --- Verificación y onboarding de instituciones** complementa
la verificación de los documentos. No basta con identificar una firma o
una referencia criptográfica; también es necesario establecer un
mecanismo mediante el cual pueda reconocerse que una institución
participante es una entidad legítima y autorizada dentro del ecosistema.

La **US-10 --- Integración con sistemas HIS/EMR mediante API** aborda la
escalabilidad y adopción institucional. Si las entidades tuvieran que
registrar manualmente cada documento en MedChain ID, la solución podría
introducir una carga operativa que dificultaría su adopción.

La **US-11 --- Acceso de emergencia (Break-Glass)** aborda un escenario
clínico crítico en el que el paciente no puede otorgar una autorización
explícita. Aunque tiene alta relevancia funcional, se mantiene fuera del
núcleo inicial debido a su complejidad en materia de seguridad,
gobernanza, auditoría y tratamiento de información clínica sensible.

------------------------------------------------------------------------

# 1.6 Priorización P2 --- Funcionalidades posteriores

Estas historias se consideran evoluciones del producto que pueden
incorporarse después de validar el flujo principal.

  ------------------------------------------------------------------------
                  Orden ID               Historia         Rol principal
                                         consolidada      
  --------------------- ---------------- ---------------- ----------------
                 **12** **US-12**        Autorización de  Paciente
                                         acceso temporal  

                 **13** **US-13**        Alertas y        Paciente
                                         notificaciones   
                                         activas          

                 **14** **US-14**        Gestión de       Padre, madre o
                                         dependientes y   tutor
                                         menores          
  ------------------------------------------------------------------------

### Justificación del nivel P2

La **US-12 --- Autorización de acceso temporal** puede evolucionar sobre
el sistema básico de permisos y revocaciones del MVP, agregando reglas
de expiración automática.

La **US-13 --- Alertas y notificaciones activas** complementa la
trazabilidad de accesos. La trazabilidad permite consultar
posteriormente los eventos, mientras que las notificaciones
proporcionarían una respuesta activa ante nuevas solicitudes, accesos o
registros.

La **US-14 --- Gestión de dependientes y menores** amplía el modelo de
identidad para contemplar relaciones de representación o custodia.
Aunque es relevante, introduce reglas adicionales de identidad,
delegación y autorización que no son indispensables para demostrar
inicialmente el flujo principal de MedChain ID.

------------------------------------------------------------------------

# 1.7 Backlog inicial recomendado

Para el primer backlog del producto se recomienda seleccionar las
historias **P0 y P1**, dejando las historias P2 como funcionalidades
futuras.

### Backlog inicial

1.  **US-01 --- Identidad médica portable**
2.  **US-02 --- Registro y vinculación de documentos médicos**
3.  **US-03 --- Consulta y organización de registros médicos**
4.  **US-04 --- Verificación de procedencia y autenticidad**
5.  **US-05 --- Autorización para compartir información**
6.  **US-06 --- Gestión y revocación de permisos**
7.  **US-07 --- Trazabilidad de accesos**
8.  **US-08 --- Atención médica entre instituciones**
9.  **US-09 --- Verificación y onboarding de instituciones**
10. **US-10 --- Integración con sistemas HIS/EMR mediante API**
11. **US-11 --- Acceso de emergencia --- Break-Glass**

Las historias P2 quedan registradas como posibles evoluciones:

12. **US-12 --- Autorización de acceso temporal**
13. **US-13 --- Alertas y notificaciones activas**
14. **US-14 --- Gestión de dependientes y menores**

------------------------------------------------------------------------

# 1.8 Flujo funcional priorizado

La priorización permite representar el flujo principal del producto de
la siguiente manera:

``` text
┌─────────────────────────────┐
│ US-01                       │
│ Identidad médica portable   │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│ US-02                       │
│ Registro y vinculación      │
│ de documentos               │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│ US-03                       │
│ Consulta y organización     │
│ de registros                │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│ US-04                       │
│ Verificación de procedencia │
│ y autenticidad              │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│ US-05                       │
│ Autorización para compartir │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│ US-06                       │
│ Gestión y revocación        │
│ de permisos                 │
└──────────────┬──────────────┘
               ↓
┌─────────────────────────────┐
│ US-07                       │
│ Trazabilidad de accesos     │
└─────────────────────────────┘

        Evolución P1
               ↓
┌─────────────────────────────────────────┐
│ US-08 · US-09 · US-10 · US-11          │
│ Interinstitucionalidad, gobernanza,     │
│ integración y escenarios críticos       │
└─────────────────────────────────────────┘

        Evolución P2
               ↓
┌─────────────────────────────────────────┐
│ US-12 · US-13 · US-14                  │
│ Permisos temporales, alertas y          │
│ dependientes                            │
└─────────────────────────────────────────┘
```

Este flujo no implica que las funcionalidades deban implementarse
necesariamente de forma estrictamente secuencial. Representa la
dependencia conceptual utilizada para justificar la priorización.

------------------------------------------------------------------------

# 1.9 Consideración sobre blockchain

La priorización no presupone que todas las historias requieran
blockchain.

MedChain ID parte de la hipótesis registrada en el `ProblemBrief.md` de
que una infraestructura distribuida podría aportar valor únicamente en
escenarios donde múltiples organizaciones autónomas necesiten compartir
evidencia verificable sin que una sola entidad deba controlar
unilateralmente ese registro.

Por ello, el MVP debe separar claramente:

-   **Información clínica:** permanece bajo custodia de los sistemas
    responsables y fuera de la blockchain.
-   **Referencias y pruebas verificables:** pueden evaluarse como
    candidatos para una capa de confianza.
-   **Autorizaciones y eventos de auditoría:** pueden evaluarse para
    registro verificable, sujeto a privacidad, seguridad y regulación.
-   **Identidad y gobernanza de entidades:** requieren mecanismos
    adicionales de control y validación.

La blockchain no debe presentarse como mecanismo que determine si un
diagnóstico, tratamiento o resultado médico es clínicamente verdadero.
Su posible función se limita a proporcionar evidencia verificable sobre
eventos, referencias, procedencia o autorizaciones que sean adecuados
para este tipo de infraestructura.

Además, si una base de datos tradicional, firmas digitales, federación
de identidad o una integración convencional resuelven el escenario con
igual confianza, privacidad, interoperabilidad y costo, la utilización
de blockchain deberá reconsiderarse.

------------------------------------------------------------------------

# 1.10 Backlog y tablero Kanban

El backlog inicial de MedChain ID se gestiona mediante un tablero Kanban en GitHub Projects, en lugar de mantenerse como una lista de tareas dentro de un archivo Markdown.

El tablero contiene las historias de usuario priorizadas para el desarrollo inicial del producto y permite realizar seguimiento de su estado durante la ejecución del proyecto.

**Tablero Kanban del proyecto:**

[MedChain ID — Product Backlog](https://github.com/users/Hebrondev/projects/1/views/1)

### Estados del tablero

El flujo de trabajo definido para las historias es:

- **Todo:** historias priorizadas pendientes de iniciar.
- **In Progress:** historias actualmente en desarrollo.
- **Done:** historias cuyos criterios de aceptación han sido cumplidos.

### Historias incluidas en el backlog inicial

El backlog inicial está compuesto por las historias P0 y P1 definidas en esta sección:

| ID | Historia | Prioridad |
|---|---|---|
| US-01 | Identidad médica portable | P0 |
| US-02 | Registro y vinculación de documentos médicos | P0 |
| US-03 | Consulta y organización de registros médicos | P0 |
| US-04 | Verificación de procedencia y autenticidad | P0 |
| US-05 | Autorización para compartir información | P0 |
| US-06 | Gestión y revocación de permisos | P0 |
| US-07 | Trazabilidad de accesos | P0 |
| US-08 | Atención médica entre instituciones | P1 |
| US-09 | Verificación y onboarding de instituciones | P1 |
| US-10 | Integración con sistemas HIS/EMR mediante API | P1 |
| US-11 | Acceso de emergencia — Break-Glass | P1 |

Cada tarjeta del tablero contiene la historia de usuario correspondiente y sus criterios de aceptación, que permiten determinar cuándo una funcionalidad puede considerarse completada.

Las historias P2 —autorización temporal, alertas y notificaciones, y gestión de dependientes— permanecen documentadas como funcionalidades posteriores y no forman parte del backlog inicial del MVP.

------------------------------------------------------------------------

## 1.11 Estado de la decisión

La presente priorización constituye la **propuesta consolidada de
trabajo** a partir de las historias actualmente disponibles.

La decisión definitiva del equipo deberá considerar las historias que
aporte **Moises Higuera Acosta** cuando estén disponibles. Cualquier
nueva historia deberá evaluarse con los mismos criterios definidos en
esta sección y, si corresponde a una necesidad ya representada, deberá
consolidarse en lugar de generar una duplicidad.

La priorización definitiva deberá quedar respaldada por el mecanismo de
decisión acordado por el equipo y posteriormente reflejada en el tablero
GitHub Projects.

------------------------------------------------------------------------

## Referencias internas utilizadas

-   `docs/semana1/ProblemBrief.md`
-   `docs/semana2/HernanDanielBriceno.md`
-   `docs/semana2/AnaElizabethCulma.md`
-   `docs/semana2/JohnFredyRojasCeballos.md`

## 2. Propuesta de valor

MedChain ID propone una identidad médica portable que ayude al paciente
a reunir, consultar y compartir referencias verificables de sus
registros de salud cuando estos provienen de diferentes instituciones,
sistemas o países. La propuesta no busca reemplazar las historias
clínicas existentes ni centralizar la información clínica. Su valor está
en reducir la fricción que aparece cuando una persona debe reconstruir
antecedentes, presentar documentos a un nuevo profesional o demostrar de
dónde proviene un registro.

Para el paciente, el beneficio esperado es mayor control sobre qué
información comparte, con quién y durante cuánto tiempo, acompañado de
evidencia verificable de procedencia. Para profesionales e
instituciones, la propuesta busca facilitar la comprobación del origen
de un documento y reducir verificaciones manuales en escenarios donde no
existe una integración directa entre sistemas.

MedChain ID se diferencia por tratar blockchain como una posible capa de
confianza y no como repositorio de historias clínicas. Los datos
clínicos permanecen bajo custodia de los sistemas responsables y la
solución solo evaluará registrar en una infraestructura compartida las
pruebas mínimas necesarias para verificar referencias, autorizaciones o
eventos. Esta propuesta complementa, en lugar de sustituir, mecanismos
nacionales como IHCE, y deberá demostrar mediante pruebas que aporta
valor en escenarios donde una integración convencional no sea
suficiente.

------------------------------------------------------------------------

## 3. Flujo de usuario

El flujo principal comienza cuando el paciente dispone de una identidad
MedChain ID y vincula a ella referencias de documentos emitidos por
instituciones de salud. La institución conserva el documento clínico en
su sistema o repositorio autorizado y, cuando corresponda, genera una
referencia verificable asociada al documento. El paciente puede
consultar sus registros y seleccionar cuáles desea compartir con un
profesional o institución.

Cuando un profesional recibe una referencia, el sistema verifica la
procedencia declarada, la integridad de la referencia y el estado de la
autorización. Si la autorización es válida, el profesional puede acceder
al documento clínico mediante el mecanismo definido por la institución
responsable, sin que MedChain ID tenga que convertirse en el repositorio
central de la historia clínica. El acceso queda registrado para que el
paciente pueda consultar posteriormente la trazabilidad correspondiente.

En escenarios entre instituciones, el flujo busca permitir que el
receptor obtenga evidencia verificable aun cuando no exista una
integración directa previa. Para escenarios de emergencia,
interoperabilidad avanzada o acceso temporal se utilizarían las
capacidades P1 y P2 definidas en el backlog, después de validar el flujo
básico.

``` mermaid
flowchart TD
    A[Paciente identifica o registra su MedChain ID]
    B[Institución registra referencia del documento]
    C[Documento clínico permanece off-chain]
    D[Paciente consulta sus registros]
    E[Paciente selecciona información y autoriza acceso]
    F[Profesional solicita el registro]
    G[MedChain ID verifica procedencia, integridad y autorización]
    H[Institución entrega el documento autorizado]
    I[Acceso registrado para trazabilidad]

    A --> B
    B --> C
    A --> D
    D --> E
    E --> F
    F --> G
    G --> H
    H --> I
```

------------------------------------------------------------------------

## 4. Alcance del MVP

El MVP de MedChain ID se limitará a demostrar el flujo fundamental de
identidad, registro, consulta, verificación y control de acceso,
evitando construir desde el inicio una plataforma completa de historia
clínica. Dentro del alcance estarán: una identidad médica portable;
registro de referencias a documentos clínicos; consulta y organización
de registros; verificación de procedencia e integridad de referencias;
autorización explícita para compartir información; gestión y revocación
de permisos; y trazabilidad de accesos.

La información clínica completa permanecerá fuera de la blockchain y
bajo custodia de los sistemas responsables. El MVP deberá demostrar al
menos un escenario controlado en el que un registro emitido por una
entidad pueda ser vinculado al paciente, verificado y compartido con un
receptor autorizado.

Quedan fuera del MVP la integración completa con múltiples HIS/EMR, el
acceso de emergencia Break-Glass, los permisos temporales, las
notificaciones activas y la gestión de dependientes. También queda fuera
la sustitución de IHCE o de los sistemas de historia clínica existentes.
Estas capacidades corresponden a evoluciones posteriores del backlog y
requieren validaciones adicionales de interoperabilidad, seguridad,
gobernanza y regulación.

------------------------------------------------------------------------

## 5. Lean Canvas

  -----------------------------------------------------------------------
  Bloque                              Definición
  ----------------------------------- -----------------------------------
  **Problema**                        Información clínica fragmentada
                                      entre instituciones, sistemas y
                                      países; dificultad para localizar,
                                      compartir y verificar registros
                                      fuera de una integración común.

  **Segmentos de usuarios**           Pacientes con atención en múltiples
                                      instituciones o países;
                                      profesionales que reciben pacientes
                                      de otras redes; instituciones
                                      prestadoras y laboratorios.

  **Propuesta de valor única**        Una identidad médica portable que
                                      permita presentar registros con
                                      evidencia verificable de
                                      procedencia y control de acceso,
                                      sin centralizar la historia
                                      clínica.

  **Solución**                        Identidad portable, referencias
                                      verificables de documentos,
                                      autorización y revocación,
                                      trazabilidad e integración
                                      progresiva con sistemas
                                      institucionales.

  **Canales**                         Instituciones piloto,
                                      profesionales, alianzas con actores
                                      de interoperabilidad, comunidades
                                      de innovación Stellar y pilotos
                                      académicos/tecnológicos.

  **Métricas clave**                  Tiempo para localizar un registro;
                                      tiempo para verificar procedencia;
                                      porcentaje de accesos autorizados
                                      correctamente; porcentaje de
                                      referencias verificables; adopción
                                      por instituciones piloto; errores
                                      de asociación o autorización.

  **Ventaja diferencial**             Enfoque en portabilidad y
                                      verificación entre organizaciones
                                      autónomas, con datos clínicos fuera
                                      de blockchain y posibilidad de
                                      coexistir con IHCE.

  **Estructura de costos**            Desarrollo y mantenimiento de
                                      aplicaciones y API; almacenamiento
                                      seguro off-chain; infraestructura y
                                      observabilidad; seguridad;
                                      cumplimiento y pruebas de
                                      interoperabilidad; costos de
                                      operación de la red.

  **Fuentes de ingreso /              Inicialmente pilotos y financiación
  sostenibilidad**                    de innovación; posteriormente
                                      servicios B2B para integración,
                                      verificación o infraestructura de
                                      confianza, sujetos a validación de
                                      mercado y regulación. No se plantea
                                      cobrar al paciente por acceder a su
                                      propia información.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 6. Arquitectura inicial

La arquitectura propuesta separa deliberadamente la información clínica
de la capa de confianza. En la capa de presentación existirían una
aplicación para el paciente y una interfaz para profesionales o
instituciones. Un backend/API actuaría como punto de orquestación,
autenticación, autorización y auditoría, sin convertirse en custodio
único de las historias clínicas.

Los documentos clínicos permanecerían en los sistemas de las
instituciones o en almacenamiento seguro off-chain. MedChain ID
mantendría únicamente los metadatos mínimos necesarios para localizar un
registro y, cuando sea pertinente, una referencia criptográfica que
permita comprobar integridad y procedencia. Un servicio de verificación
calcularía o comprobaría los compromisos criptográficos y validaría el
estado de las autorizaciones.

La capa Stellar se utilizaría únicamente para aquellos eventos que
demuestren una necesidad real de registro compartido: por ejemplo, una
referencia verificable, una atestación de una entidad o un evento de
autorización que deba poder ser comprobado por participantes
independientes. Soroban podría contener la lógica mínima de autorización
y registro de estados verificables, mientras que los datos clínicos
permanecerían fuera de la cadena. La arquitectura deberá aplicar
minimización de datos y evitar incluir PII o contenido clínico
innecesario en el ledger.

``` mermaid
flowchart TB
    P[Paciente]
    M[Profesional / Institución]
    UI[Aplicación / Portal]
    API[Backend / API de MedChain ID]
    AUTH[Identidad, autorización y auditoría]
    VER[Servicio de verificación]
    OFF[Documentos clínicos y datos sensibles<br/>HIS / EMR / almacenamiento seguro]
    ST[Stellar / Soroban<br/>referencias, atestaciones y estados mínimos]

    P --> UI
    M --> UI
    UI --> API
    API --> AUTH
    API --> VER
    API --> OFF
    VER --> OFF
    VER --> ST
    AUTH --> ST
```

**Principio de separación:** la cadena no contiene la historia clínica.
El sistema off-chain conserva el contenido clínico; Stellar se limita a
la evidencia y lógica mínima que realmente requieran un registro
compartido y verificable.

------------------------------------------------------------------------

## 7. Uso de Stellar y justificación

Stellar es pertinente para MedChain ID únicamente en la parte del
problema que requiere una capa compartida de confianza entre
organizaciones que no deben depender de una única base de datos
administrada por una de ellas. El ledger de Stellar mantiene un estado
compartido y persistente, y Soroban permite ejecutar contratos
inteligentes con almacenamiento y reglas de autorización. Esto permite
explorar un registro verificable de referencias, estados de permisos o
atestaciones sin trasladar la historia clínica completa a la red.

Para el MVP, se propone evaluar un contrato Soroban que registre
identificadores no reveladores, compromisos criptográficos y estados
mínimos de autorización. Las firmas y mecanismos de autorización de
Stellar pueden servir para demostrar que una operación fue autorizada
por la cuenta correspondiente, mientras que el contenido clínico
permanece off-chain. Soroban dispone de almacenamiento de datos en
ledger, por lo que el diseño debe limitar estrictamente qué información
se escribe y considerar exposición, retención, costos y gobernanza.

La decisión de usar Stellar deberá validarse contra una alternativa
convencional. Si una base de datos federada, firmas digitales e
interoperabilidad existente ofrecen la misma confianza, privacidad,
gobernanza y costo, blockchain no sería necesaria. En consecuencia,
Stellar es un componente experimental de confianza y no el repositorio
de datos médicos.

### Componentes de Stellar considerados

  -----------------------------------------------------------------------
  Componente              Uso propuesto           Justificación
  ----------------------- ----------------------- -----------------------
  **Stellar Ledger**      Registrar evidencia     Proporciona un estado
                          mínima y verificable    compartido que puede
                                                  ser consultado por
                                                  participantes
                                                  independientes.

  **Soroban**             Implementar reglas de   Permite ejecutar lógica
                          autorización y estados  programable y mantener
                          verificables            datos de contrato en el
                                                  ledger.

  **Cuentas y firmas**    Autorizar operaciones   Permiten asociar
                          de pacientes o          operaciones con una
                          entidades según el      autoridad criptográfica
                          diseño                  verificable.

  **Eventos /             Evidencia de            Permiten observar y
  transacciones**         operaciones relevantes  auditar cambios
                                                  asociados a la lógica
                                                  implementada.
  -----------------------------------------------------------------------

### Límites deliberados

MedChain ID **no almacenará historias clínicas completas, diagnósticos,
resultados, imágenes, documentos PDF ni otros datos clínicos
identificables directamente en Stellar**. La arquitectura deberá
minimizar también metadatos que puedan permitir reidentificación.

La propuesta deberá probar que el uso de Stellar aporta una propiedad
que una alternativa convencional no ofrece con igual nivel de confianza,
privacidad, interoperabilidad y costo. Si esa hipótesis no se confirma,
el proyecto deberá reducir o retirar el componente blockchain.

------------------------------------------------------------------------

## Fuentes complementarias para la sección de Stellar

-   Stellar Development Foundation. **Ledgers --- Stellar Docs:**
    https://developers.stellar.org/docs/learn/fundamentals/stellar-data-structures/ledgers
-   Stellar Development Foundation. **Smart Contracts --- Stellar
    Docs:**
    https://developers.stellar.org/docs/learn/fundamentals/stellar-data-structures/contracts
-   Stellar Development Foundation. **Authorization --- Stellar Docs:**
    https://developers.stellar.org/docs/learn/fundamentals/contract-development/authorization
-   Stellar Development Foundation. **Persisting Data --- Stellar
    Docs:**
    https://developers.stellar.org/docs/learn/fundamentals/contract-development/storage/persisting-data
-   Stellar Development Foundation. **Signatures and Multisig ---
    Stellar Docs:**
    https://developers.stellar.org/docs/learn/fundamentals/transactions/signatures-multisig