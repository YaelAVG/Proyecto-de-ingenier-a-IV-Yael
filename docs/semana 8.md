# Semana 8: Prototipado y Diseño de Manufactura / Desarrollo de Demos

**Equipo de trabajo / Colaboradores:**

* Yael Alejandro Vázquez González

* Integrantes del Equipo de Proyecto de Ingeniería IV

**Fecha:** Semana 8 - Periodo Académico

**Proyecto:** GPIO Génesis — Videojuego Educativo de Simulación Industrial y Programación en C++

**Plataforma de Distribución:** Steam

## 1. Introducción y Contextualización del Entregable

En esta octava semana del curso, la actividad general correspondiente a **Prototipado y Diseño de Manufactura** se ha adaptado meticulosamente a las dinámicas propias del desarrollo de software y la industria de los videojuegos. Para un producto físico, este hito comprendería la selección de procesos de maquinado, ensamblaje de tarjetas electrónicas (PCB), moldeado por inyección y tolerancias mecánicas. Sin embargo, en **GPIO Génesis**, al ser un bien estrictamente digital comercializado a través de la plataforma Steam, la "manufactura" equivale a la **arquitectura del motor de simulación, la canalización de compilación (Build Pipeline) y el empaquetado del ejecutante (Build)**, mientras que los "prototipos de prueba" se materializan en **Demos jugables e interactivas**.

El propósito central de esta entrega es validar funcionalmente la **Demo v0.1 (Nivel 1: "Arranque de Línea")**, demostrando la convergencia armónica entre el aprendizaje de código real en C++, la respuesta lógica en tiempo real de la línea de ensamblaje de drones y el acompañamiento didáctico de un tutor integrado (Copiloto).

```
   ┌────────────────────────────────────────────────────────────────────────┐
   │                       ARQUITECTURA DIGITAL V0.1                        │
   └────────────────────────────────────────────────────────────────────────┘
                                       │
         ┌─────────────────────────────┴─────────────────────────────┐
         ▼                                                           ▼
┌───────────────────────────┐                             ┌───────────────────┐
│     ENTORNO VIRTUAL       │                             │   IDE & MOTOR     │
├───────────────────────────┤                             ├───────────────────┤
│ • Banda transportadora    │ ◄─── (Señales GPIO D2,D4,D5) ───┤ • Editor C++ Real │
│ • Chasis y Sensores       │                             │ • Parser/Sintaxis │
│ • Luces de estado         │ ───► (Telemetría/Gráfica) ──►│ • Copiloto Tutor  │
└───────────────────────────┘                             └───────────────────┘
```

## 2. Descripción del Prototipo Funcional (Demo v0.1)

El prototipo funcional de esta semana demuestra el *Core Loop* del juego: el jugador asume el puesto de ingeniero de automatización en una planta industrial de drones y debe escribir código C++ sin errores para poner en marcha los actuadores mecánicos y verificar las lecturas de los sensores.

### 2.1 Módulos Integrados en el Prototipo

1. **Interfaz de Navegación y Menú Principal:**

   * Sistema de gestión de perfiles locales (soporte para modo local/offline sin dependencia forzosa de la nube).

   * Menú contextual modular que incluye *Niveles*, *Portafolio de Logros*, *Opciones de Rendimiento* y barra de estado de versión (`v0.1 · demo`).

2. **Simulador Gráfico de Fábrica en 2D (Pixel Art):**

   * Representación física animada de la línea de ensamblaje de drones.

   * Renderizado dinámico de actuadores como la banda transportadora controlada por el pin D5 (`MOTOR_BANDA`) y las estaciones de luz en D2 (`LUZ_ESTACION`).

   * Sensores de presencia de chasis mapeados al pin de entrada D4 (`SENSOR_ESTACION`).

3. **Editor de Código e Entorno C++ Realista:**

   * Editor de texto embebido con resaltado sintáctico e indicación del número de línea.

   * Estructura estándar de programación embebida en microcontroladores basada en las funciones del bloque `setup()` y `loop()`.

   * Soporte directo para palabras reservadas y tipos de datos: `const int`, `pinMode()`, `digitalWrite()`, `OUTPUT`, `INPUT`, `HIGH`, `LOW`.

4. **Telemetría y Osciloscopio Digital en Tiempo Real:**

   * Módulo visual inferior que grafica las ondas cuadradas de nivel lógico (0 V / 5 V equivalentes a `LOW` y `HIGH`) en una ventana temporal de 3 s.

   * Permite al usuario correlacionar visualmente una línea de código C++ con el comportamiento físico del voltaje en el hardware simulado.

5. **Asistente Didáctico "Copiloto":**

   * Avatar y motor de retroalimentación interactiva que analiza la compilación en tiempo real.

   * Proporciona ayuda graduada (hasta 4 niveles de pistas) cuando detecta errores de sintaxis o fallos lógicos en la secuencia de la fábrica.

## 3. Screenshots del Prototipo Desarrollado

### 3.1 Pantalla de Inicio y Estructura del Menú Principal

El menú principal establece la identidad estética retro-industrial del título y la arquitectura de acceso a las sesiones de aprendizaje.

*Figura 1: Pantalla principal de la Demo v0.1 de GPIO Génesis, donde se muestra el panel de control de opciones, estado de la build y confirmación de nivel completado.*

### 3.2 Entorno de Control, Compilación y Telemetría del Juego

El espacio de trabajo unifica el código C++ interactivo con la fábrica en funcionamiento, mostrando el estado de los tres sistemas activos en línea.

*Figura 2: Nivel 1 ("Arranque de Línea"). Visualización paralela del motor de física 2D, el editor con sintaxis `pinMode()` y `digitalWrite()`, la telemetría en tiempo real para D2, D4, D5 y el panel del Copiloto.*

## 4. Pipeline de Manufactura Digital (Software Build Pipeline)

A diferencia de un proceso de manufactura física donde se evalúa el mecanizado CNC o el moldeo de plásticos, la manufactura digital de **GPIO Génesis** sigue una canalización continua de compilación, prueba y despliegue a través del SDK de **Steamworks**.

```
[ Código Fuente C++ / Scripts ] ──► [ Validación de Sintaxis ] ──► [ Transpilador de Código ]
                                                                               │
[ Arte Pixel Art & SFX Audio ]  ──► [ Empaquetador / Build Engine ] ◄──────────┘
                                                 │
                                                 ▼
                              [ Artefacto Ejecutable (.exe/.app) ]
                                                 │
                                                 ▼
                              [ Despliegue Automatizado en Steam ]
```

### 4.1 Tolerancias y Métricas de Calidad del Software

Para garantizar una experiencia fluida y pedagógicamente rigurosa, el software se sujeta a los siguientes estándares de control de calidad:

| Métrica / Tolerancia | Valor Objetivo | Mecanismo de Control | 
| ----- | ----- | ----- | 
| **Tiempo de respuesta de compilación in-game** | Menor a 150 ms | Sub-hilo dedicado para el motor de parsing de C++ | 
| **Frecuencia de cuadros (Frame Rate)** | 60 FPS constantes | Optimización de draw-calls en sprites 2D | 
| **Uso de memoria RAM** | Menor a 450 MB | Gestión eficiente de texturas y limpieza de memoria | 
| **Interrupción de Bucles Infinitos** | Límite en 3 s | Módulo de timeout que previene cuelgues por `while(true)` | 

## 5. Análisis Económico y Estimación de Costos

Basado en las hojas de costo y presupuestos del proyecto (**AlcanceNivelesCostosGPIOGenesis** y **CostosGPIOGenesisSemana7**), se presenta el desglose detallado de la inversión requerida para llevar la Demo v0.1 hasta el producto final de 22 niveles en Steam.

### 5.1 Desglose de Horas Directas de Desarrollo

El esfuerzo de "fabricación" en software se mide principalmente en horas de trabajo especializado (programación, diseño artístico, audio y diseño instruccional).

```
   Distribución de Horas de Desarrollo (MVP vs Proyecto Completo)
   ┌─────────────────────────────────────────────────────────────┐
   │ Programación IDE/Motor  ████████████████ 215h / 481h        │
   │ Arte y Animación 2D     █████████ 98h / 164h                  │
   │ Diseño Instruccional    █████ 48h / 152h                      │
   │ Pruebas y QA            ████ 44h / 140h                      │
   │ Audio y Diseño Sonoro   ██ 18h / 35h                          │
   └─────────────────────────────────────────────────────────────┘
```

* **Horas totales para el MVP (Demo / 5 Niveles):** 423 h

* **Horas totales para el Juego Completo (22 Niveles / 3 Bloques):** 972 h

### 5.2 Estructura de Inversión Financiera

| Categoría de Costo | Versión MVP (5 Niveles) | Versión Completa (22 Niveles) | 
| ----- | ----- | ----- | 
| **Costo Directo de Mano de Obra** | $43,997.00 MXN | $101,113.91 MXN | 
| **Costos Indirectos y Herramientas** | $2,200.00 MXN | $5,055.70 MXN | 
| **Reserva de Contingencia (10%)** | $4,399.70 MXN | $10,111.39 MXN | 
| **TOTAL COSTO DE DESARROLLO** | **$50,596.70 MXN** | **$116,281.00 MXN** | 

### 5.3 Costos Fijos Directos de Salida a Mercado (Out-of-pocket)

Los costos reales de dinero en efectivo necesarios para comercializar el juego de manera profesional en Steam se desglosan a continuación:

* **Steam Direct Fee (Tarifa de publicación por juego):** $100.00 USD (aprox. $1,800.00 MXN)

* **Dominio web y servidor para landing page (12 meses):** $600.00 MXN

* **Certificado de Firma de Código de Software:** $4,500.00 MXN

* **Infraestructura Cloud / Supabase Pro (12 meses):** $2,042.50 MXN

* **Inversión Total Fija Directa:** $8,942.50 MXN

### 5.4 Unit Economics (Economía Unitaria por Juego Vendido)

El modelo de monetización se basa en la venta directa del título en Steam bajo un precio base de lanzamiento:

* **Precio de Venta Sugerido al Público:** $249.00 MXN

1. **Comisión de Plataforma Steam (30%):**  
   Comisión = $249.00 × 0.30 = $74.70 MXN

2. **Ingreso Bruto Promedio por Copia:**  
   Ingreso Bruto = $249.00 - $74.70 = $174.30 MXN

3. **Costo Variable Operativo (Consultas IA Copiloto en la nube):**  
   Costo Variable = aprox. $0.86 MXN por copia (0.5% del ingreso bruto)

4. **Margen Directo de Ganancia por Copia:**  
   Margen Neto = $174.30 - $0.86 = $173.44 MXN (aprox. 69.65% del precio final)

## 6. Plan de Pruebas y Validación Tecnológica

Para validar que la arquitectura de software es robusta y replicable antes del lanzamiento final de la semana 8 en adelante, se ejecuta la siguiente batería de pruebas:

1. **Prueba de Invariabilidad y Tiempo Real:**

   * **Procedimiento:** Mantener la simulación gráfica activa durante 30 minutos continuos mientras el jugador modifica las variables de entrada D4.

   * **Criterio de Aprobación:** Sin desfasamiento en el osciloscopio visual y un consumo estático de CPU menor o igual al 5%.

2. **Prueba de Retroalimentación de Error del Copiloto:**

   * **Procedimiento:** Introducir deliberadamente errores sintácticos (`digitalWrite(MOTOR_BANDA HIGH);` omitiendo la coma) y errores lógicos (asignar entradas como salidas).

   * **Criterio de Aprobación:** El sistema debe capturar el error inmediatamente y mostrar un mensaje contextual en la consola inferior sin detener la ejecución de la app.

3. **Prueba de Generación de Executables Multiplataforma (Build Pipeline Test):**

   * **Procedimiento:** Compilar el proyecto a través del pipeline automatizado para Windows 11 y macOS ARM.

   * **Criterio de Aprobación:** Generación exitosa de los instaladores sin dependencias externas faltantes.
## Reflexión de la Semana 8

Personalmente fue muy emocionante, empezar a ver los primeros resultados del trabajo de 8 semanas, es muy satisfactorio empezar a ver como se marterializa y que el resultado final esta muy cerca.
Pienso que el trabajo de las enteriores semanas ha sido muy productivo aunque no sea visible, facilito mucho el proceso para poder llegar a este paso, confió en el proyecto ya que otorga una propuesta nueva en el mercado y una nueva forma de enseñanza.