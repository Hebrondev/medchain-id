# MedChain ID

**Problem statement:** Los pacientes tienen su información médica fragmentada entre diferentes instituciones, plataformas y ubicaciones, lo que dificulta acceder a ella, compartirla y verificar su origen cuando la necesitan.

## Decisión del problema

### Problema elegido

Los pacientes tienen su información médica fragmentada entre diferentes instituciones, plataformas y ubicaciones, lo que dificulta acceder a ella, compartirla y verificar su origen cuando la necesitan. La propuesta fue presentada por **Hernan Daniel Briceño**, integrante del equipo interdisciplinar.

### Por qué elegimos este

El equipo eligió MedChain ID porque aborda una dificultad reconocible para las personas y permite explorar una aplicación de confianza digital en un flujo con múltiples prestadores, sistemas y jurisdicciones. La fragmentación puede hacerse visible cuando una persona cambia de IPS, ciudad o país y necesita reconstruir antecedentes, resultados o tratamientos producidos en atenciones anteriores. La propuesta también permite investigar trazabilidad y verificación sin plantear que los datos clínicos sensibles deban publicarse en una cadena.

La selección no presupone que Colombia carezca de interoperabilidad. La Ley 2015 de 2020 creó el marco de la Historia Clínica Electrónica Interoperable (IHCE), y el Ministerio reportó que para el 6 de junio de 2026 ya operaban 744 prestadores y 2.456 sedes, mientras 1.087 IPS y 3.606 sedes adelantaban pruebas de incorporación. Esto muestra tanto una infraestructura nacional en operación como un despliegue que continúa ampliándose. El equipo ve una oportunidad para estudiar necesidades complementarias, en particular portabilidad transfronteriza y verificación de procedencia por terceros, y deberá demostrar que no duplica funciones existentes. [Ley 2015 de 2020](https://www.minsalud.gov.co/Normatividad_Nuevo/Ley%202015%202020.pdf) · [avance IHCE, 6 de junio de 2026](https://www.minsalud.gov.co/Comunicaciones/noticias/2026/Paginas/millones-de-registros-se-intercambian-gracias-a-IHCE.aspx)

### Propuestas descartadas

Las alternativas se discutieron en equipo y se compararon por diferenciación, complejidad, pertinencia tecnológica, regulación y potencial de desarrollo. Se descartaron por consenso, excepto Revenue Sharing, que quedó por debajo en la puntuación y votación interna.

| Propuesta | Quién la propuso | Motivo de descarte |
|---|---|---|
| Entradas con depósito anti-reventa o reventa controlada | John Fredy Rojas (`jfrc91`) | Se parecía a casos de uso frecuentes del ecosistema blockchain y ofrecía menor diferenciación. |
| “Dead Man’s Switch” financiero | Moises Higuera Acosta (`morthuis`) | El alcance inicial parecía simple y ofrecía menos posibilidades de desarrollo e innovación. |
| Remesas inteligentes para Latinoamérica - RemitChain | Hernan Daniel Briceño (`hebrondev`) | Aunque atiende un problema real, el sector ya cuenta con numerosas propuestas blockchain similares. |
| Facturación empresarial verificable - TrustInvoice | Hernan Daniel Briceño (`hebrondev`) | Se acercaba a soluciones financieras existentes y podía enfrentar barreras de integración y adopción, especialmente en pequeñas y medianas empresas. |
| Crowdfunding con dinero condicionado | Moises Higuera Acosta (`morthuis`) | Había soluciones similares y preocupaban los retos regulatorios de captación de recursos del público en Colombia. |
| Revenue sharing para pequeños negocios | Ana Culma (`anaculma`) | No se descartó por consenso: recibió una valoración menor que MedChain ID en la puntuación y votación comparativa. |

### Cómo tomamos la decisión

El equipo debatió las propuestas y buscó consenso sobre su diferenciación, complejidad, pertinencia de blockchain y viabilidad de desarrollo. Cuando no hubo una decisión unánime, se complementó el debate con una votación interna. Cinco propuestas se descartaron por común acuerdo; Revenue Sharing se evaluó mediante puntuación y votación y no fue seleccionada. MedChain ID obtuvo la decisión favorable como propuesta a desarrollar. Esta descripción corresponde al proceso registrado por el equipo en la fase de ideación.

## Problem Brief

### Equipo y roles

| Integrante | Usuario de GitHub | Rol asumido |
|---|---|---|
| Ana Culma | `anaculma` | Desarrolladora y gestora |
| Moises Higuera Acosta | `morthuis` | Desarrollador, orquestador y responsable de entregas |
| John Fredy Rojas | `jfrc91` | Desarrollador y gestor |
| Hernan Daniel Briceño | `hebrondev` | Desarrollador, orquestador y responsable de entregas |

**Responsables de las entregas:** Ana Culma, Moises Higuera Acosta, John Fredy Rojas y Hernan Daniel Briceño.  
**Canales de coordinación interna:** Discord y WhatsApp.

### Problema y evidencia

En Colombia, una persona puede tener datos, documentos y resultados clínicos generados en distintos prestadores y sistemas; cuando cambia de institución, ciudad o país, puede necesitar localizarlos, compartirlos y confirmar su procedencia para dar continuidad a su atención. La necesidad puede surgir en cada nueva atención con un profesional que no dispone del contexto previo, ante una remisión, una urgencia o el traslado del paciente. La evidencia disponible para este brief es documental: no contamos todavía con entrevistas o mediciones propias que permitan cuantificar cuánto tiempo o dinero pierde cada paciente.

La fragmentación no significa que no exista una respuesta nacional. La Ley 2015 de 2020 estableció la IHCE, ordenó el intercambio de datos clínicos relevantes y preservó la custodia en los prestadores; también reconoce el derecho del paciente a recibir su historia clínica electrónicamente de forma gratuita, completa y rápida. El 6 de junio de 2026, el Ministerio informó que 744 prestadores con 2.456 sedes ya intercambiaban información, con 1.087 IPS y 3.606 sedes en pruebas de incorporación. Estas cifras evidencian actividad y expansión, pero no miden por sí mismas la experiencia individual ni la portabilidad internacional. [Ley 2015 de 2020, arts. 1, 3, 5 y 9](https://www.minsalud.gov.co/Normatividad_Nuevo/Ley%202015%202020.pdf) · [Ministerio de Salud, 6 de junio de 2026](https://www.minsalud.gov.co/Comunicaciones/noticias/2026/Paginas/millones-de-registros-se-intercambian-gracias-a-IHCE.aspx)

### Usuario y actores

El usuario principal es el paciente que recibe atención en más de una institución y necesita reunir o poner a disposición información relevante de manera oportuna, segura y comprensible. Hoy puede recurrir a los canales de cada prestador, pedir copias electrónicas, conservar archivos recibidos o indicar a un profesional dónde se encuentran sus antecedentes. La ley reconoce el suministro electrónico, gratuito, completo y rápido de la historia clínica; por eso el problema que se investiga no es la inexistencia de ese derecho, sino la carga práctica de localizar, organizar, compartir y verificar registros cuando intervienen sistemas distintos, especialmente fuera del alcance de una red nacional. El costo concreto en horas, trámites o gastos debe medirse con pacientes y prestadores; no se presenta aquí como un dato cuantificado.

Los profesionales de salud necesitan información pertinente y confiable para apoyar decisiones clínicas y continuidad del cuidado. Hospitales, clínicas, laboratorios, IPS y profesionales independientes generan registros y responden por su manejo según las reglas aplicables. Los proveedores de software soportan los sistemas de historia clínica; el Ministerio de Salud define y administra el modelo IHCE, y MinTIC participa en la plataforma tecnológica conforme a la Ley 2015. Las secretarías territoriales y entidades de salud acompañan la implementación. Paciente, prestador de origen y profesional receptor participan en el intercambio, sujeto a reserva, finalidad legítima, seguridad y autorizaciones que correspondan; IHCE ya facilita intercambio nacional entre prestadores.

### Flujo actual de valor

El flujo principal mueve información clínica, no dinero. La historia clínica debe ser registrada, custodiada y compartida bajo obligaciones legales; en Colombia la Ley 2015 dispone su interoperabilidad y mantiene la custodia en los prestadores.

1. **Atención:** el paciente consulta en una IPS, hospital, clínica, laboratorio o con un profesional. El prestador identifica al paciente y presta el servicio.
2. **Registro:** el profesional documenta hallazgos, diagnósticos, procedimientos, medicamentos y resultados en el sistema del prestador. La historia clínica es reservada y su contenido debe manejarse con seguridad.
3. **Custodia:** el prestador conserva el registro y responde por su guarda. Otros actores pueden tener responsabilidades según su participación y el tratamiento de datos.
4. **Solicitud o consulta posterior:** el paciente puede pedir su historia clínica por medios electrónicos. Un profesional que atiende después puede requerir antecedentes pertinentes y debe acceder según las reglas de tratamiento, reserva y autorización aplicables.
5. **Intercambio nacional:** los prestadores incorporados pueden intercambiar datos clínicos mediante IHCE y los Resúmenes Digitales de Atención (RDA), siguiendo los estándares y procedimientos definidos por el Ministerio. El Ministerio reportó operación desde abril de 2026 y una incorporación progresiva de sedes.
6. **Atención receptora:** el nuevo profesional interpreta la información disponible y la integra a su valoración. Si el origen está fuera del circuito conectado o del país, el paciente puede tener que aportar archivos o solicitar documentos por separado; esta brecha requiere validación con usuarios.

Los intermediarios actuales son el prestador que custodia el registro, sus sistemas y proveedores tecnológicos, los canales institucionales de entrega y, para intercambio nacional, la plataforma IHCE. [Ley 2015 de 2020](https://www.minsalud.gov.co/Normatividad_Nuevo/Ley%202015%202020.pdf) · [IHCE y RDA](https://www.minsalud.gov.co/ihce/rda/Paginas/inicio.aspx)

### Fricciones identificadas

Las fricciones siguientes son hipótesis derivadas del flujo y de la fase de ideación, no resultados de entrevistas. Deben comprobarse con pacientes, profesionales y prestadores antes de priorizar una solución.

1. **Localizar registros (pasos 3 y 4):** la información está en los sistemas de los prestadores que la generaron. Si el paciente no sabe qué institución conserva cada resultado o no puede entrar a un canal digital, debe reconstruir dónde pedirlo. Esto afecta al paciente y puede retrasar la preparación de una consulta.
2. **Reunir formatos y antecedentes (pasos 4 y 5):** documentos, imágenes y resultados pueden llegar por portales, archivos o solicitudes separadas. El paciente invierte esfuerzo en organizarlos y el profesional receptor en revisar qué es pertinente. IHCE reduce barreras de intercambio nacional entre participantes, por lo que no se debe atribuir esta fricción a todos los casos ni ignorar el avance de adopción.
3. **Verificar procedencia fuera de una integración compartida (pasos 4 y 6):** cuando un registro se presenta como archivo aislado, el receptor puede necesitar confirmar quién lo emitió, cuándo y si corresponde al paciente. El impacto potencial recae en ambos, pero la magnitud de esta situación requiere evidencia.
4. **Cruzar fronteras o redes no conectadas (paso 6):** la interoperabilidad nacional no demuestra por sí sola que exista un mecanismo equivalente entre países o sistemas ajenos a IHCE. La persona puede depender de documentos que lleve consigo y de procesos manuales; se validará en escenarios concretos de movilidad.

No se asignan ahorros ni tiempos porque las fuentes consultadas no los cuantifican para estos casos. La validación deberá registrar frecuencia, duración, número de trámites y errores o duplicaciones asociados.

### Oportunidad e hipótesis

La oportunidad priorizada es facilitar que el paciente reúna y presente registros clínicos emitidos por distintas entidades y ubicaciones con evidencia verificable de origen, empezando por escenarios en los que no hay integración directa entre el prestador de origen y el receptor, como movilidad entre países. Se prioriza porque responde a la fragmentación identificada y podría complementar IHCE, cuya misión ya es intercambiar información clínica dentro del marco nacional. El proyecto debe integrarse o coexistir con los mecanismos oficiales cuando corresponda, no reemplazarlos ni duplicarlos.

**Hipótesis inicial:** si el paciente puede vincular a su identidad referencias verificables a documentos clínicos emitidos por instituciones, y compartir acceso mediante una autorización explícita y revocable cuando jurídicamente proceda, el profesional receptor podría comprobar la procedencia y consultar el documento con menos verificaciones manuales. En una arquitectura por explorar, los datos clínicos permanecerían fuera de una cadena; solo se considerarían pruebas criptográficas, referencias no reveladoras y eventos mínimos de autorización o auditoría, sujetos a evaluación de privacidad y regulación. La propuesta no implica que el registro distribuido autentique la verdad clínica ni que sustituya la firma o responsabilidad del profesional y del prestador. Para validar valor, se comparará el tiempo de recuperación y verificación con el proceso actual y con las capacidades de IHCE. La principal incógnita es si los prestadores y receptores aceptarían esa evidencia y si aporta algo que una integración convencional no pueda resolver.

### Criterio de pertinencia

IHCE ya es la vía nacional definida para intercambiar datos clínicos entre prestadores colombianos. Por tanto, la necesidad general de compartir información no justifica por sí sola una cadena de bloques: una base de datos tradicional o mejores integraciones podrían resolver el caso con menos complejidad. La pertinencia potencial aparece solo si se confirma un escenario concreto en el que varias organizaciones autónomas, sin un operador común aceptado o sin relación bilateral de confianza, necesitan validar una constancia común de emisión, integridad o autorización, y ninguna de ellas debe controlar unilateralmente ese historial compartido.

Esto se relaciona con los criterios de la Sesión 1 de múltiples partes que requieren compartir un registro y de conservar evidencia de cambios o verificaciones. Una red distribuida podría ofrecer reglas comunes y registros resistentes a alteración para referencias y eventos limitados, mientras que los documentos seguirían bajo custodia de las entidades responsables. No debe asumirse que esto elimina intermediarios: la operación clínica y la custodia continuarían en prestadores, y una autoridad o consorcio todavía tendría que gobernar la red. Si un servicio federado, firmas digitales e interoperabilidad convencional satisfacen el caso con igual confianza, privacidad y costo, blockchain no sería pertinente. La comparación técnica debe incluir esa alternativa y respetar IHCE y sus estándares. [Ley 2015 de 2020](https://www.minsalud.gov.co/Normatividad_Nuevo/Ley%202015%202020.pdf) · [marco IHCE](https://www.minsalud.gov.co/ihce/Paginas/default.aspx)

### Supuestos y riesgos

La hipótesis depende de tres supuestos por validar:

1. Existe un grupo de pacientes que, al cambiar de país o de red desconectada, no puede resolver de forma suficientemente simple la obtención y verificación de documentos mediante los canales actuales o las integraciones existentes.
2. Al menos algunos prestadores podrían emitir documentos o constancias verificables y los profesionales receptores estarían dispuestos a consultarlos, siempre que el proceso no interfiera con la atención ni con IHCE.
3. La arquitectura puede proteger datos sensibles, identidad y metadatos, y ofrecer control de acceso comprensible sin almacenar información clínica personal en una cadena pública. El diseño también tendría que respetar la reserva de la historia clínica, las reglas de protección de datos, la custodia institucional y las autorizaciones aplicables.

La propuesta perdería pertinencia si entrevistas y pruebas muestran que IHCE u otras soluciones interoperables cubren el caso de uso priorizado, si documentos firmados e integraciones convencionales verifican origen con menor costo, o si no hay aceptación de prestadores y receptores. También puede invalidarse por riesgos de reidentificación a través de metadatos, pérdida de credenciales, errores de asociación de identidad, exposición de claves, imposibilidad práctica de corregir o retirar referencias, problemas de gobernanza transfronteriza o costos de cumplimiento. Una prueba de concepto no demostraría cumplimiento legal ni validez clínica: antes de operar en salud habría que evaluar privacidad, seguridad, interoperabilidad y obligaciones regulatorias con los actores competentes.

## Fuentes

- Congreso de Colombia. **Ley 2015 de 2020**, por medio de la cual se crea la Historia Clínica Electrónica Interoperable. [Texto oficial](https://www.minsalud.gov.co/Normatividad_Nuevo/Ley%202015%202020.pdf).
- Ministerio de Salud y Protección Social. **Más de 7,7 millones de registros clínicos ya se intercambian de manera segura a través de la interoperabilidad de la historia clínica electrónica en Colombia**, 6 de junio de 2026. [Noticia oficial](https://www.minsalud.gov.co/Comunicaciones/noticias/2026/Paginas/millones-de-registros-se-intercambian-gracias-a-IHCE.aspx).
- Ministerio de Salud y Protección Social. **Resumen Digital de Atención (RDA)**. [Descripción y alcance](https://www.minsalud.gov.co/ihce/rda/Paginas/inicio.aspx).
- Ministerio de Salud y Protección Social. **Interoperabilidad de la Historia Clínica Electrónica (IHCE)**. [Estrategia oficial](https://www.minsalud.gov.co/ihce/Paginas/default.aspx).
