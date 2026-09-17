# ⚙️ 02. Gestión de Riesgos y Seguridad Técnica

> 💡 **Bitácora personal del módulo:**  
> ¡Hola! En este segundo curso pasé de los conceptos generales a cómo se organiza la seguridad en una empresa real. Me enfoqué en entender la diferencia entre amenazas, riesgos y vulnerabilidades, cómo se auditan los sistemas y cómo los equipos de seguridad utilizan herramientas como los SIEM y los playbooks para no improvisar ante un ataque.  
> 
> Documenté aquí los marcos de trabajo más importantes (NIST, ISO 27001) y la lógica operativa de las alertas para tener clara la estructura que protege a una organización.

---

## 📌 Tabla de Contenidos
1. [Marcos de Referencia y Gobernanza](#1-marcos-de-referencia-y-gobernanza)
2. [Gestión de Riesgos, Amenazas y Vulnerabilidades](#2-gestión-de-riesgos-amenazas-y-vulnerabilidades)
3. [Clasificación de Controles de Seguridad](#3-clasificación-de-controles-de-seguridad)
4. [Auditorías de Seguridad Internas](#4-auditorías-de-seguridad-internas)
5. [Tecnología SIEM y Monitoreo de Registros](#5-tecnología-siem-y-monitoreo-de-registros)
6. [Playbooks de Respuesta a Incidentes (IR)](#6-playbooks-de-respuesta-a-incidentes-ir)

---

## 1. Marcos de Referencia y Gobernanza

Los marcos (*frameworks*) establecen directrices estandarizadas para mitigar riesgos, alinear la seguridad con los objetivos del negocio y cumplir con regulaciones legales.

* **NIST Cybersecurity Framework (CSF v2.0):** Marco voluntario de referencia estructurado en 6 funciones operativas esenciales:
  1. **Govern (Gobernar):** Establecer prioridades, políticas y supervisión de la gestión de riesgos de ciberseguridad.
  2. **Identify (Identificar):** Comprender los activos críticos, proveedores y riesgos del entorno.
  3. **Protect (Proteger):** Aplicar salvaguardas (control de acceso, formación, cifrado) para contener impactos.
  4. **Detect (Detectar):** Identificar anomalías y eventos de seguridad mediante monitoreo continuo.
  5. **Respond (Responder):** Ejecutar acciones de contención, análisis y mitigación ante incidentes confirmados.
  6. **Recover (Recuperar):** Restaurar sistemas, operaciones y capacidades afectadas por brechas.
* **ISO/IEC 27001:** Estándar internacional auditable que define los requisitos para diseñar, implementar y mantener un Sistema de Gestión de Seguridad de la Información (SGSI).
* **Cyber Threat Framework (CTF):** Marco desarrollado para proveer un lenguaje técnico común al describir y comunicar la actividad de los adversarios.

---

## 2. Gestión de Riesgos, Amenazas y Vulnerabilidades

### Definiciones Operativas
* **Activo (Asset):** Recurso físico o digital con valor para la organización (datos PII/SPII, servidores, código fuente).
* **Amenaza (Threat):** Circunstancia o evento con potencial de causar daño a los recursos.
* **Vulnerabilidad (Vulnerability):** Debilidad o fallo en un sistema, proceso o configuración que puede ser explotado por una amenaza (ej. fallos conocidos como ProxyLogon, Log4Shell o ZeroLogon).
* **Riesgo (Risk):** La probabilidad de que una amenaza explote una vulnerabilidad multiplicada por el impacto del incidente.

$$\text{Riesgo} = \text{Probabilidad de Amenaza} \times \text{Impacto}$$

### Estrategias de Tratamiento del Riesgo
* **Mitigación:** Aplicar salvaguardas y controles técnicos para reducir la probabilidad o el impacto.
* **Transferencia:** Trasladar la carga financiera del riesgo a un tercero (contratación de ciberseguros).
* **Aceptación:** Asumir el impacto del riesgo residual cuando el costo del control supera el valor del activo.
* **Evitación:** Eliminar completamente la exposición al riesgo cesando la actividad vulnerable.

---

## 3. Clasificación de Controles de Seguridad

Los controles son las medidas defensivas aplicadas para reducir riesgos específicos:

* **Controles Técnicos:** Implementados mediante hardware o software.
  * Firewalls perimetrales y de host.
  * Sistemas de autenticación multifactor (MFA).
  * Motores IDS/IPS (Suricata) y agentes EDR en endpoints.
* **Controles Administrativos (o de Gestión):** Procesos y directrices humanas.
  * Políticas corporativas de uso aceptable.
  * Separación de funciones (Separation of Duties - SoD).
  * Principio de privilegio mínimo (Least Privilege).
* **Controles Físicos:** Barreras tangibles que limitan el acceso directo a instalaciones y equipos.
  * Cerraduras biométricas o lectores de credenciales RFID.
  * Circuitos cerrados de televisión (CCTV) y sensores de intrusión.
  * Guardias de seguridad física y control perimetral.

---

## 4. Auditorías de Seguridad Internas

Una auditoría de seguridad evalúa de forma independiente si las operaciones de TI cumplen con las políticas internas y las normativas externas (GDPR, PCI-DSS, HIPAA).

### Fases de una Auditoría Interna:
1. **Definición del Alcance y Objetivos:** Delimitar qué activos, redes, procesos y personal serán inspeccionados.
2. **Evaluación de Riesgos:** Determinar las amenazas críticas que pesan sobre el alcance definido.
3. **Evaluación de Controles:** Clasificar y validar si los controles existentes funcionan adecuadamente o tienen fallos de configuración.
4. **Verificación de Cumplimiento:** Medir la adherencia a estándares obligatorios de la industria.
5. **Reporte y Remediación:** Documentar los hallazgos y proponer medidas correctivas para reducir la exposición.

---

## 5. Tecnología SIEM y Monitoreo de Registros

Las herramientas SIEM (*Security Information and Event Management*) centralizan, correlacionan y almacenan datos de registro (*logs*) de múltiples fuentes (servidores, firewalls, endpoints) para ofrecer visibilidad en tiempo real.

### Paneles Operativos Clave
* **Panel de Revisión de Incidentes:** Ofrece una cronología detallada de las alertas disparadas para que el analista investigue eventos correlacionados.
* **Panel de Análisis de Riesgo:** Muestra el nivel de amenaza asociado a objetos específicos (usuarios que inician sesión en horarios anómalos o IPs externas con tráfico excesivo).
* **Panel de Postura / Resumen:** Visión global del estado de defensas y métricas operativas en las últimas 24 horas.

### Soluciones del Mercado
* **Google Chronicle:** SIEM analítico nativo de la nube centrado en búsquedas a escala masiva y cruce directo con indicadores de compromiso (IoCs).
* **Splunk Enterprise / Cloud:** Plataforma de análisis de datos de máquina que permite búsquedas avanzadas y tableros personalizados para SOC.
* **Wazuh (Código Abierto):** EDR y SIEM integral para recolección de eventos de sistema, integridad de archivos (FIM) y cumplimiento normativo.
* **SOAR (Security Orchestration, Automation and Response):** Plataformas que automatizan respuestas repetitivas (aislamiento automático de un host o bloqueo de un usuario) para permitir que los analistas se concentren en incidentes complejos.

---

## 6. Playbooks de Respuesta a Incidentes (IR)

Un **Playbook** (o runbook) es un manual procedimental paso a paso que estandariza la forma en que los analistas deben contener y resolver incidentes específicos.

### Fases Operativas de un Incidente (NIST SP 800-61):
1. **Preparación:** Establecimiento de herramientas, políticas, listas de contactos y simulacros.
2. **Detección y Análisis:** Monitoreo continuo de alertas SIEM, validación del evento y descarte de falsos positivos.
3. **Contención:** 
   * *A corto plazo:* Aislar el equipo de la red local para evitar propagación o movimiento lateral.
   * *A largo plazo:* Aplicar parches temporales y bloquear dominios maliciosos en el firewall.
4. **Erradicación y Recuperación:** Eliminar el malware o artefactos persistentes del sistema y restaurar los servicios afectados desde copias de seguridad confiables.
5. **Actividad Post-Incidente:** Redacción del informe final, análisis de causa raíz y actualización de las reglas de monitoreo para prevenir incidentes similares.
