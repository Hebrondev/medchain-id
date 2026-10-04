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

# 1.10 Criterio para la construcción del tablero Kanban

El backlog inicial deberá trasladarse a un tablero Kanban en GitHub
Projects.

Cada historia deberá convertirse en una tarjeta independiente y
conservar como mínimo:

-   Identificador de la historia.
-   Título.
-   Historia de usuario en formato **Como \[rol\] quiero \[acción\] para
    \[beneficio\]**.
-   Prioridad.
-   Criterios de aceptación.
-   Responsable, cuando sea definido por el equipo.
-   Estado dentro del flujo Kanban.

La estructura recomendada para el tablero es:

``` text
BACKLOG       TODO          IN PROGRESS       DONE
   │            │                │              │
   │            │                │              │
   └────────────┴────────────────┴──────────────┘
```

Las historias P0 y P1 constituyen el conjunto inicial recomendado para
el backlog. Las historias P2 deben permanecer identificadas como trabajo
futuro y no mezclarse con el alcance mínimo del MVP.

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