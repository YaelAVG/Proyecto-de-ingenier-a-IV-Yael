# Reporte Semanal 3: Propiedad Intelectual y Vigilancia Tecnológica
> **Fase del Blueprint:** Creación de valor | **Estado DVF:** 🟢 Factible

El objetivo de esta semana es evaluar la viabilidad de apropiación de nuestro proyecto. Nos enfocamos en responder: ¿El nombre está libre para registro? ¿Existen patentes previas que bloqueen nuestra tecnología? A continuación, se detalla el proceso y los hallazgos para el proyecto **"Buendía"** (sistema de conexión familiar mediante rutinas).

---

## I. Definición y Alcance del Producto
Para enfocar la búsqueda de patentes y el análisis de marca, delimitamos las características clave de nuestra solución:

*   **Problema central:** La ansiedad que experimentan los hijos(as) que viven lejos de sus padres mayores que viven solos, buscando tranquilidad sin invadir la privacidad.
*   **Mecanismo técnico:** Sistema compuesto por un sensor de flujo de agua (en tubería principal) y sensores de presencia (PIR/firma térmica), enlazados a un marco digital familiar.
*   **Lógica operativa:** El sistema aprende la rutina matutina (ej. uso de lavabos/inodoros). Al completarse la rutina, el marco digital muestra un mensaje de la familia y el hijo/a recibe un "nudge" sugiriendo una llamada casual. **No es una alarma de emergencia.**
*   **Identidad proyectada:** Cercana, familiar, rutinaria; estrictamente no clínica.

---

## II. Auditoría de Marca: El caso "Buendía"

> **Veredicto de viabilidad:** 🟡 Pertinencia digital MEDIA.

**Análisis Semántico y de Huella Digital:**
La palabra "Buendía" funciona semánticamente a la perfección, comunicando rutina y calidez sin asociaciones médicas. Sin embargo, su huella digital está saturada:
*   El dominio `buendia.com` pertenece a la transnacional *Café Buendía* (Colombia).
*   El SEO orgánico compite con figuras históricas y literarias (familia Buendía en *Cien años de soledad*, activistas, etc.).

**Frente Registral y Técnico:**
*   La USPTO (EE. UU.) no muestra colisiones directas activas en las clases 9, 10 o 38, pero no cubre bases clave para LATAM como IMPI (México) o INDECOPI/SIC.
*   *Alerta técnica:* Existe un sistema open-source de historiales médicos llamado "Project Buendia".

**Recomendación Estratégica:**
Evitar el uso de "Buendía" como marca aislada. La estrategia será adoptar una **arquitectura de marca compuesta** (ej. *Buendía Hogar*, *Buendía Conecta*, *Tu Buendía*). 
*Próximos pasos:* Asegurar dominios disponibles (`buendia.care`, `buendia.tech`) y solicitar búsquedas formales fonéticas en el IMPI (México) excluyendo explícitamente la clase 10 (médica).

---

## III. Exploración y Vigilancia Tecnológica

### A. Diccionario de Búsqueda y Códigos IPC
Para las bases de datos (IMPI, LATIPAT, Google Patents), construimos la siguiente matriz de términos:

| Concepto (ES) | Concepto (EN) |
| :--- | :--- |
| Sensor de flujo de agua / tubería | Water flow sensor / main pipe sensor |
| Detección de rutina matutina | Morning routine detection |
| Firma térmica / sensor presencia | Thermal signature / occupancy (PIR) sensor |
| Marco digital / pantalla inteligente | Digital photo frame / smart display |
| Notificación proactiva a cuidador | Proactive caregiver notification / nudge |

**Clasificaciones IPC Estratégicas:**
*   `G08B21/22` (Alarmas de presencia humana)
*   `G08B21/24` (Recordatorios e inferencia de hábitos)
*   `G01F1/00` (Medición de flujos)

### B. Hallazgos Regionales (México y LATAM)
Tras consultar el IMPI/SIGA (México) y LATIPAT (América Latina), **no se encontraron evidencias** de solicitudes o patentes vigentes que crucen nuestro mecanismo (sensor de tubería + comunicación a pantalla familiar). El panorama regional está despejado.

### C. Hallazgos Globales y Análisis de Riesgo
La búsqueda ampliada en USPTO/Espacenet arrojó dos documentos clave que requieren análisis detallado:

#### 1. Patente US11,112,132 B2 (Bao Tran, Prioridad 2018)
*   **Enfoque:** Monitoreo de agua para inferir rutinas de vida y realizar llamadas de emergencia.
*   **Estado:** 🟢 Expirada prematuramente por falta de pago de mantenimiento.
*   **Análisis de Infracción (FTO):** Nuestro sistema está **fuera de riesgo**. El reclamo independiente de esta patente exige una *válvula motorizada de corte* y un *módulo blockchain*, componentes que nosotros no usamos.
*   **Impacto:** Aunque no hay riesgo de infracción (está expirada), es un antecedente de "estado de la técnica" (*prior art*). Bloquea la posibilidad de que nosotros patentemos la idea general de "inferir rutinas midiendo agua", pero no afecta nuestro mecanismo completo.

#### 2. Patente US11,647,964 B2 (Paramount Bed, Japón)
*   **Enfoque:** Sensor de monitoreo biológico en camas para notificar a familiares.
*   **Estado:** 🟢 Vigente.
*   **Análisis de Infracción (FTO):** Nuestro sistema está **fuera de riesgo**. Sus reivindicaciones se centran estrictamente en sensores *acoplados físicamente a una cama*, lo cual descarta nuestros sensores ambientales o de tubería.

---

## IV. Conclusión FTO (Freedom to Operate)

> **Estado general:** 🟢 Alta libertad de operación comercial.

**Síntesis:** No existe barrera de propiedad intelectual (patentes vigentes) en nuestras regiones de interés que impida el desarrollo y comercialización de nuestro hardware específico (sensor de flujo → rutina → marco digital con mensajes).

**Plan de Acción PI:**
1.  **Diferenciación tecnológica:** Al documentar nuestro proyecto, el énfasis debe recaer siempre en el mecanismo del **marco digital + mensaje afectivo**, ya que el "monitoreo de agua para rutinas" ya es de dominio público por la patente US11,112,132 expirada.
2.  **Lenguaje de producto:** Erradicar todo término médico o de "monitoreo de emergencias" para alejarnos de patentes como las de *CarePredict* o *Paramount Bed*.

---

## V. Bitácora de Prompts Utilizados

Para documentar la reproducibilidad del ejercicio, se adjunta el resumen estructural de los prompts ejecutados:

*   **Naming - Fase 1 (Ideación):** Prompt diseñado para generar conceptos de marca que eviten la jerga médica y prioricen la noción de "buenos días" y "conexión".
*   **Naming - Fase 2 (Evaluación):** Prompt estructurado como consultor de branding para auditar colisiones digitales de la palabra "Buendía", dominios ocupados (Café Buendía) y registros marcarios.
*   **Vigilancia - Fase 1 (Términos):** Prompt para AI de análisis técnico solicitando traducciones exactas de componentes y sus códigos IPC/CPC correspondientes a instrumentación de fluidos y transmisión de señales.
*   **Vigilancia - Fase 2 (Reivindicaciones):** Prompt alimentado con el texto legal de US11,112,132 y US11,647,964 para extraer exclusivamente lo que *protegen* vs. lo que *no protegen*, determinando cruces técnicos con nuestro esquema.