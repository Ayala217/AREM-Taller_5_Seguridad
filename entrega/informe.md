#  Informe Técnico del Taller

##  Nombre del Taller
_Taller 5 - Seguridad_

##  Integrantes del equipo
- Arciniegas Guerrero Camilo
- Ayala Silva Juan Sebastián
- Campo Conde Juan Diego

##  Descripción general del trabajo
Describa brevemente el objetivo del taller y cómo se desarrolló la actividad.

##  Proceso de desarrollo
Explique cómo realizaron el trabajo: qué decisiones tomaron, qué herramientas utilizaron, qué aspectos modelaron primero y cómo lo fueron ajustando.

##  Análisis del modelo propuesto
Incluya un análisis sobre:
- Cómo se estructura el modelo entregado
- Cómo representa las necesidades del cliente
- Qué supuestos se tomaron

##  Investigación complementaria

### Tema investigado:

### Buenas prácticas de seguridad en diversos sectores

#### **1. Sector de la Salud**

La seguridad en el ámbito de la atención sanitaria ha de poder garantizar los tres principios de Confidencialidad, Integridad y Disponibilidad en un entorno de gran presión.

**Segmentación de Red para IoMT (Internet de las Cosas Médicas):** la segmentación de los dispositivos médicos en VLANs independientes ha de aplicarse, ya que sólo así evitarán que un compromiso de la red administrativa o de invitados pueda extenderse a equipos críticos de soporte vital.

**Cifrado Homomórfico y en Reposo:** los estándares AES-256 se han de aplicar a las bases de datos de las Historias Clínicas. El uso de cifrado homomórfico es una práctica avanzada que permite la ejecución de análisis estadísticos de datos clínicos sin la necesidad de descifrarlos para preservar la privacidad ante la investigación del paciente.

**Arquitectura Zero Trust:** Adopción de un modelo "nunca confiar, siempre verificar". Cualquier intento de acceso a los datos clínicos ha de ser autenticado, autorizado y validado de forma contínua, independientemente de su procedencia.[1]

#### **2. Sector Educación**
La dificultad principal consiste en trabajar con un número de usuarios muy elevado y variable y la integridad de los procesos de validación de los menores.

**Control de Identidad y Acceso:** Empleo de la centralización del acceso a portales de notas y bibliotecas mediante aplicaciones especializadas de seguridad. La centralización permite, por ejemplo, revocar automáticamente los permisos al finalizar la temporada del ciclo escolar o cuando hay una desvinculación del sistema.

**Protección contra DDoS y WAF:** Configuración de las WAF (_Web Application Firewall_) y las redes de entrega de contenido con un objetivo, mitigar los ataques de DDoS en momentos tales como las inscripciones y las evaluaciones finales, para asegurar el funcionamiento de la plataforma.

**Prevención de Pérdidas de Datos:** Monitorear la situación del estado de la aplicación de exámenes antes que se hagan efectivos y proteger la información sensible de los alumnos también de acuerdo con la normativa internacional.

#### **3. Sector de Software** 
La seguridad en el área de Software es un punto vital para cualquier sistema o infraestructura, pues se deben tener en cuenta la posibilidad de sufrir ciberataques, cuellos de botella, mala implementación...etc.

**Secret Management:** Prohibición de las credenciales en el código fuente. Se deben propiciar las vaults de secretos para inyectar keys de API y contraseñas de base de datos de forma dinámica en runtime.[2]

**Vulnerability Scanning en pipeline:** Integración de herramientas de análisis estático y dinámico en el flujo de CI/CD para detectar los fallos de seguridad.

**Escaneo de Infraestructura como Código:** En entornos de nube, se deben analizar automáticamente archivos de configuración para detectar configuraciones inseguras, como buckets de almacenamiento públicos, grupos de seguridad demasiado permisivos o falta de cifrado en bases de datos.[3]

### Resumen:

La investigación realizada enfatiza la necesidad de realizar controles de seguridad específicos en función del ámbito sectorial, teniendo como principio de su adecuada realización la tríada de la confidencialidad, la integridad y la disponibilidad.
En sectores importantes, típicamente la salud y la educación, las buenas prácticas sobre buenas prácticas están relacionadas con aislar automáticamente los dispositivos médicos con VLANs, 
el uso de cifrados de alta seguridad y la gestión centralizada de las identidades 
relacionadas con datos sensibles y la continuidad del servicio frente a un ataque de denegación de servicio.

En el sector  de software, la investigación hace se enfoca en la necesidad de que haya una cultura DevSecOps que integre las prácticas de seguridad en el ciclo de vida del producto; el uso de prácticas como la gestión de secretos a través de bóvedas dinámicas, 
realizar escaneos de vulnerabilidades en pipelines de CI/CD, el análisis de la infraestructua como código...etc., son prácticas imprescindibles para mitigar riesgos antes de alcanzar el entorno de producción. Estas estrategias aseguran que las aplicaciones
sean resilientes ante ciberataques y ante los errores de configuración más comunes que ocurren en la nube.

Esta investigación se relaciona con el contexto del taller debido a que el marco STRIDE también busca implementar mitigaciones a partir de los riesgos identificados. Las mitigaciones se suelen relacionar directamente con las buenas prácticas de seguridad, pues ambas buscan evitar riesgos que pueden dañar la integridad de un sistema y por ende, de una empresa. 


## Referencias
[1] National Institute of Standards and Technology (NIST), "Security and Privacy Controls for Information Systems and Organizations," NIST Special Publication 800-53, Rev. 5, Sep. 2020. [En línea]. Disponible: https://doi.org/10.6028/NIST.SP.800-53r5

[2] OWASP Foundation, "OWASP Top 10:2021 - The Definitive Guide to Web Application Security Risks," 2021. [En línea]. Disponible: https://owasp.org/www-project-top-ten/

[3] Cloud Native Computing Foundation (CNCF), "Cloud Native Security Whitepaper v2," CNCF Security Technical Advisory Group, Mayo 2022. [En línea]. Disponible: https://github.com/cncf/tag-security/


_Este documento hace parte de la entrega del taller 5 del curso AREM (Arquitectura Empresarial) - Universidad de La Sabana._
