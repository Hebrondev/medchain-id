# MedChain ID --- Historias de Usuario

**Integrante:** John Fredy Rojas Ceballos\
**GitHub:** `jfrc91`\
**Rol:** Desarrollador

## Historias de usuario complementarias

Las siguientes historias de usuario representan necesidades de escalabilidad, integración y casos críticos (emergencias) para el producto **MedChain ID**, sumando nuevos roles del ecosistema. Se encuentran organizadas de mayor a menor importancia.

### 1. Acceso de Emergencia (Protocolo "Break-Glass")

> **Como médico de urgencias quiero solicitar acceso de emergencia a los registros críticos de un paciente sin su autorización explícita (en caso de que ingrese inconsciente o incapacitado), para poder tomar decisiones vitales de manera inmediata, dejando un registro inmutable en la blockchain que audite este acceso forzado.**

**Prioridad:** Alta

En situaciones de riesgo vital, el paciente no puede otorgar permisos en su aplicación. El sistema debe permitir un acceso excepcional, pero altamente auditado y penalizado si se usa injustificadamente, para garantizar el derecho a la vida sin sacrificar la trazabilidad.

### 2. Gestión de Dependientes y Menores de Edad

> **Como padre, madre o tutor legal quiero vincular y gestionar la identidad médica portable de mis hijos menores de edad o familiares a cargo para poder autorizar o revocar el acceso a sus registros médicos (ej. historial de vacunación, pediatría) desde mi propia cuenta.**

**Prioridad:** Alta

Los menores de edad o personas con discapacidades cognitivas no pueden gestionar sus propias llaves o identidades. El sistema necesita un mecanismo de "delegación de custodia" de la identidad.

### 3. Integración Automatizada (API para Hospitales)

> **Como administrador de TI de una entidad prestadora de salud quiero conectar nuestro sistema interno de historias clínicas (HIS/EMR) con MedChain ID a través de una API estandarizada para que la generación de la referencia verificable (hash) y su vinculación con la identidad del paciente se realice automáticamente en segundo plano cuando el médico guarda la consulta.**

**Prioridad:** Alta

Si las instituciones tienen que registrar los documentos manualmente en MedChain, la adopción fracasará. La integración API silenciosa (Machine-to-Machine) es vital para el éxito del ecosistema.

### 4. Verificación de Entidades (Onboarding de Nodos Confiables)

> **Como administrador de la red MedChain (Consorcio) quiero registrar y certificar criptográficamente a las instituciones de salud legítimas dentro del sistema para que cuando un paciente o médico vea un documento, el sistema pueda garantizar visualmente que fue emitido por un hospital real y verificado, y no por un actor malicioso.**

**Prioridad:** Alta

Para que un documento sea "verificable", la llave pública que lo firma debe pertenecer a una entidad comprobada. Esta historia establece el mecanismo de gobernanza para admitir hospitales en la red.

### 5. Autorización de Acceso Temporal (Time-bound)

> **Como paciente quiero otorgar acceso a un profesional de salud por un tiempo límite predefinido (por ejemplo, 24 o 48 horas) para no tener que preocuparme por recordar entrar a la aplicación para revocar el permiso manualmente después de mi consulta.**

**Prioridad:** Media-Alta

Automatiza la seguridad mediante contratos inteligentes (smart contracts) o lógica de expiración, reduciendo el riesgo de dejar "puertas abiertas" perpetuas a médicos que el paciente no volverá a ver.

### 6. Alertas y Notificaciones Activas

> **Como paciente quiero recibir notificaciones en tiempo real en mi dispositivo cada vez que una institución o médico solicite acceso, visualice mis registros o registre un nuevo documento para tener un conocimiento inmediato de la actividad de mi historial y poder detectar o bloquear intentos de acceso no reconocidos al instante.**

**Prioridad:** Media

Complementa la historia de "Trazabilidad". La trazabilidad es pasiva (el usuario entra a mirar). Las notificaciones son activas, aumentando la sensación de control y seguridad del usuario.

## La más importante y por qué

### Historia #1 --- Acceso de Emergencia (Protocolo "Break-Glass")

> **Como médico de urgencias quiero solicitar acceso de emergencia a los registros críticos de un paciente sin su autorización explícita (en caso de que ingrese inconsciente o incapacitado), para poder tomar decisiones vitales de manera inmediata, dejando un registro inmutable en la blockchain que audite este acceso forzado.**

Considero que esta es la historia complementaria más crítica porque aborda el principal argumento en contra de los sistemas de salud centrados en la privacidad estricta: "¿Qué pasa si el paciente se está muriendo y no puede presionar 'Aceptar' en su celular?".

Resolver tecnológicamente el acceso de emergencia—permitiendo que un médico salve una vida mientras la blockchain registra un evento de auditoría nivel "alerta roja" que será revisado posteriormente—demuestra la madurez del sistema. Combina el derecho a la privacidad con el derecho fundamental a la vida y la atención médica oportuna.

## Resumen de prioridades

| Prioridad | Historia | Rol |
| :--- | :--- | :--- |
| 1 | Acceso de Emergencia (Break-Glass) | Médico de Urgencias |
| 2 | Gestión de Dependientes y Tutores | Padre / Tutor Legal |
| 3 | Integración Automatizada (API HIS/EMR) | Administrador de TI |
| 4 | Verificación de Entidades (Onboarding) | Administrador de Red |
| 5 | Autorización Temporal (Time-bound) | Paciente |
| 6 | Alertas y Notificaciones Activas | Paciente |