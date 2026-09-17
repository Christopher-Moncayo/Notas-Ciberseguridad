# 🛡️ 01. Fundamentos de Ciberseguridad

> ¡Hola! En este primer curso me enfoqué en construir los cimientos: entender qué hace realmente un analista de seguridad en su día a día (lejos del mito de hacker de la nasa jaja), cómo se estructuran las defensas con la tríada CIA[cite: 1] y cuáles son los vectores de ataque más comunes como el phishing y el malware.  
> 
> Aquí pues escribí y ordene mis apuntes en limpio, organizando los marcos teóricos y las herramientas clave para tener siempre a mano una referencia rápida y clara de lo aprendido.

---

## 📌 Tabla de Contenidos
1. [Definición de Ciberseguridad y Postura Defensiva](#1-definición-de-ciberseguridad-y-postura-defensiva)
2. [El Rol del Analista de Ciberseguridad Jr / L1](#2-el-rol-del-analista-de-ciberseguridad-jr--l1)
3. [La Tríada CIA (CID)](#3-la-tríada-cia-cid)
4. [Panorama de Amenazas, Vulnerabilidades y Ataques](#4-panorama-de-amenazas-vulnerabilidades-y-ataques)
5. [Marcos Normativos, Dominios CISSP y Ética](#5-marcos-normativos-dominios-cissp-y-ética)
6. [Caja de Herramientas del Analista](#6-caja-de-herramientas-del-analista)

---

## 1. Definición de Ciberseguridad y Postura Defensiva

* **Ciberseguridad:** Es la práctica de garantizar la confidencialidad, integridad y disponibilidad de la información protegiendo redes, dispositivos, personas y datos frente a accesos no autorizados o explotación delictiva.
* **Postura de Seguridad:** Es la capacidad colectiva de una organización para gestionar sus defensas de activos críticos, proteger datos sensibles y reaccionar de forma ágil ante incidentes o cambios en el entorno.
* **Activos Críticos y Protección de Datos:**
  * **PII (*Personally Identifiable Information*):** Cualquier dato que permite inferir la identidad de un individuo (nombres, números telefónicos, direcciones).
  * **SPII (*Sensitive PII*):** Información que exige controles más estrictos debido al alto impacto de su compromiso (números de identificación gubernamental, tarjetas de crédito, datos bancarios).

---

## 2. El Rol del Analista de Ciberseguridad Jr / L1

El analista de seguridad de nivel de entrada centra su labor en el aspecto operacional del Centro de Operaciones de Seguridad (SOC):
* **Monitoreo y Triaje:** Supervisión continua del tráfico de red interna y evaluación de eventos alertados por las herramientas de detección.
* **Respuesta Inicial ante Incidentes:** Aplicación de políticas y procedimientos establecidos (playbooks) al dispararse una alerta de malware o actividad anómala.
* **Auditorías Periódicas:** Revisión de registros de acceso, autenticaciones y verificación del cumplimiento de normativas internas.
* **Diferencia Operativa vs. Ingeniería:** Mientras que el analista de seguridad junior se concentra en las operaciones diarias, el triaje y la investigación de alertas, el ingeniero de seguridad diseña los sistemas, configura las arquitecturas y crea las reglas de detección.

---

## 3. La Tríada CIA (CID)

Modelo fundamental de ciberseguridad utilizado para la evaluación de riesgos y diseño de políticas defensivas:

* **Confidencialidad (*Confidentiality*):** Garantiza que únicamente los usuarios y sistemas debidamente autorizados puedan acceder a los datos. 
  * *Mecanismos:* Cifrado en tránsito/reposo, listas de control de acceso y aplicación del principio de mínimo privilegio (*Least Privilege*).
* **Integridad (*Integrity*):** Garantiza que la información se mantenga auténtica, exacta y libre de modificaciones no autorizadas o maliciosas.
  * *Mecanismos:* Funciones hash criptográficas, firmas digitales y control de versiones.
* **Disponibilidad (*Availability*):** Asegura que los sistemas, redes y datos permanezcan accesibles para las partes autorizadas en el momento que lo requieran.
  * *Mecanismos:* Redundancia de infraestructura, balanceo de carga, planes de respaldo (backups) y mitigación de ataques DoS/DDoS.

---

## 4. Panorama de Amenazas, Vulnerabilidades y Ataques

### A. Tipos de Amenazas
* **Amenazas Internas (*Insider Threats*):** Empleados, exempleados o proveedores de confianza que, de forma intencionada o accidental, abusan de sus privilegios comprometiendo los sistemas.
* **Amenazas Persistentes Avanzadas (APT):** Grupos de ciberactores organizados que mantienen acceso no detectado a redes específicas durante períodos prolongados.

### B. Vectores de Malware Comunes
* **Virus:** Código malicioso que requiere la interacción de un usuario para propagarse (ejecutar un archivo o abrir un adjunto).
* **Gusanos (*Worms*):** Software malicioso con capacidad de autorreplicarse y propagarse de forma autónoma a través de protocolos y servicios de red vulnerables.
* **Ransomware:** Cifrado extorsivo de activos y archivos de la organización con solicitud de un rescate financiero para restaurar el acceso.
* **Spyware / InfoStealers:** Programas encubiertos diseñados para registrar datos, credenciales, pulsaciones de teclado y archivos personales sin consentimiento.

### C. Ingeniería Social y Phishing
Manipulación psicológica que explota el factor humano para obtener credenciales, transferencias o acceso físico:
* **Spear Phishing:** Ataque de ingeniería social por correo electrónico dirigido a un usuario o equipo específico tras una recolección previa de información.
* **Whaling:** Ataques de alta prioridad dirigidos contra directivos y personal con alto poder de decisión (*C-Level*).
* **BEC (*Business Email Compromise*):** Suplantación o secuestro de cuentas corporativas para desviar fondos mediante transferencias fraudulentas.
* **Smishing / Vishing:** Variantes ejecutadas por mensajes de texto (SMS) o canales de voz/teléfono.
* **Disparadores Psicológicos (Cialdini):** *Autoridad, Urgencia, Intimidación, Escasez, Consenso/Prueba Social y Confianza*.

---

## 5. Marcos Normativos, Dominios CISSP y Ética

### Los 8 Dominios del CISSP
Estructura estándar de la industria que agrupa las responsabilidades del profesional de seguridad:
1. **Seguridad y Gestión de Riesgos:** Gobernanza, cumplimiento normativo y continuidad del negocio.
2. **Seguridad de Activos:** Ciclo de vida, clasificación y destrucción segura de datos físicos y lógicos.
3. **Arquitectura e Ingeniería de Seguridad:** Principios de diseño seguro, modelos de amenazas y defensa en profundidad.
4. **Seguridad de las Comunicaciones y Redes:** Protocolos, segmentación de redes y protección perimetral.
5. **Gestión de Identidad y Acceso (IAM):** Autenticación, autorización y menor privilegio.
6. **Evaluación y Pruebas de Seguridad:** Pruebas de penetración, análisis de vulnerabilidades y auditorías.
7. **Operaciones de Seguridad:** Monitoreo SIEM, triaje de alertas y respuesta ante incidentes.
8. **Seguridad en el Desarrollo de Software (AppSec):** Ciclo de desarrollo seguro (SSDLC) y mitigación de fallos en código.

### Marcos de Trabajo (Frameworks)
* **NIST CSF (versión 2.0):** Estructura defensiva organizada en 6 funciones: *Govern (Gobernar), Identify (Identificar), Protect (Proteger), Detect (Detectar), Respond (Responder) y Recover (Recuperar)*.
* **ISO/IEC 27001:** Estándar internacional para implementar y operar un Sistema de Gestión de Seguridad de la Información (SGSI).

### Ética y Legalidad en la Defensa
* En la mayoría de legislaciones internacionales (como la CFAA en EE.UU.), el **contraataque (*hack-back*) es ilegal** para el sector privado y se clasifica como vigilantismo. 
* Las funciones del analista defensivo se limitan a la contención perimetral, la investigación forense, el aislamiento de amenazas y la notificación a las autoridades pertinentes.

---

## 6. Caja de Herramientas del Analista

* **Herramientas SIEM (*Security Information and Event Management*):** Soluciones como Splunk, Google Chronicle o Wazuh que centralizan e indexan registros de eventos (logs) para detectar patrones y anomalías.
* **Sistemas de Detección de Intrusiones (IDS):** Motores como Suricata o Snort que inspeccionan paquetes en busca de firmas y comportamientos anómalos.
* **Playbooks de Respuesta:** Guías procedimentales estandarizadas que definen el paso a paso operacional a seguir ante cada tipología de alerta.
* **Lenguajes Clave:**
  * **Bash / Linux CLI:** Navegación por sistemas de archivos, filtrado de texto y lectura de registros del sistema (`/var/log`).
  * **SQL:** Consultas a bases de datos relacionales para auditar tablas y verificar modificaciones de datos.
  * **Python:** Automatización de tareas rutinarias de triaje, consultas a APIs de inteligencia de amenazas e inspección de logs.
