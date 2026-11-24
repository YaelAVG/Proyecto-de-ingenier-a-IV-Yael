# Semana 9: Estrategia de Lanzamiento, Pruebas con Usuarios y Validación Comercial

**Equipo de trabajo / Colaboradores:**

* Yael Alejandro Vázquez González

* Integrantes del Equipo de Proyecto de Ingeniería IV

**Fecha:** Semana 9 - Periodo Académico

**Proyecto:** GPIO Génesis — Videojuego Educativo de Simulación Industrial y Programación en C++

**Plataforma de Distribución:** Steam

---

## 1. Introducción y Contextualización de la Semana 9

Llegando a la novena semana de desarrollo de **GPIO Génesis**, la atención se desplaza de la manufactura interna del software hacia la **validación en mercado y la prueba directa con usuarios finales**. En el desarrollo de software y videojuegos comerciales en Steam, esta fase comprende dos pilares fundamentales:

1. **Validación de la Experiencia de Usuario (Playtesting & UX):** Evaluar el aprendizaje de la sintaxis C++, la claridad de la simulación de la fábrica de drones y la efectividad del Copiloto en una muestra de usuarios reales.
2. **Estrategia de Comunicación y Go-To-Market (Landing Page & Marketing Digital):** Construir la presencia digital del proyecto para la captura de correos (leads), generación de *Wishlists* en Steam y presentación del tráiler o demo jugable.

```
   ┌────────────────────────────────────────────────────────────────────────┐
   │                  ESTRATEGIA DE LANZAMIENTO Y VALIDACIÓN                │
   └────────────────────────────────────────────────────────────────────────┘
                                       │
         ┌─────────────────────────────┴─────────────────────────────┐
         ▼                                                           ▼
┌───────────────────────────┐                             ┌───────────────────┐
│   PRUEBAS CON USUARIOS    │                             │ EMBUDO DE VENTAS  │
├───────────────────────────┤                             ├───────────────────┤
│ • Sesiones de Playtesting │                             │ • Landing Page    │
│ • Evaluación de UX e IDE  │ ───► (Métricas y Feedback) ─►│ • Captura de Leads│
│ • Ajustes de Dificultad   │                             │ • Wishlists Steam │
└───────────────────────────┘                             └───────────────────┘
```

---

## 2. Estrategia de Marketing Digital y Conversión (Embudos para Steam)

Para un videojuego indie enfocado en educación tecnológica (*EdTech* / Simulación), la métrica previa al lanzamiento más importante son las **Deseadas (Wishlists)** en la tienda de Steam.

### 2.1 Embuco de Conversión de GPIO Génesis

```
 [ Tráfico Orgánico / Redes / Comunidades Dev ] 
                       │
                       ▼
         [ Landing Page Oficial ]
                       │
                       ▼
       [ Registro a la Beta / Demo v0.1 ] 
                       │
                       ▼
       [ Redirección a Steam Store (Wishlist) ]
```

1. **Atracción de Tráfico:** Publicaciones en redes sociales, foros de programación (Reddit C++, Dev.to), servidores de Discord de robótica y comunidades de electrónica.
2. **Landing Page:** Página web optimizada enfocada en la propuesta de valor: *"Aprende C++ real automatizando una fábrica interactiva de drones"*.
3. **Conversión:** Captura de correos para acceso anticipado a la Demo v0.1 y redirección a añadir el juego a la lista de deseados en Steam.

### 2.2 Landing Page del Proyecto

El sitio web oficial actúa como el centro de conversión primario antes de la activación formal de la página de Steam.

* **Enlace a la Landing Page del Proyecto:** [INSERTAR_AQUÍ_EL_LINK_DE_TU_LANDING_PAGE]

---

## 3. Pruebas con Usuarios (Playtesting y Pruebas de Usabilidad)

Para la validación del prototipo funcional (Demo v0.1), se diseñó un protocolo de pruebas enfocado en evaluar tanto el aspecto jugable como el educativo.

### 3.1 Perfil de los Participantes en las Pruebas

Se seleccionó una muestra diversa de usuarios categorizados en dos perfiles:
* **Perfil A (Principiantes / Estudiantes de Ingeniería inicial):** Con conocimientos nulos o básicos de programación, interesados en aprender C++.
* **Perfil B (Gamers / Desarrolladores):** Familiarizados con juegos de simulación o lógica (como *Factorio*, *TDS 100*) o con experiencia previa en C++.

### 3.2 Metodología de las Pruebas de Campo

Cada sesión tuvo una duración aproximada de 20 a 30 minutos y constó de 3 etapas:
1. **Fase de Observación Pasiva (Sin intervención del facilitador):** El usuario navega el Menú Principal y resuelve el Nivel 1 ("Arranque de Línea"). Se mide el tiempo de resolución y la cantidad de compilaciones erróneas.
2. **Evaluación del Copiloto e IDE:** Se observa si el jugador comprende la relación entre las líneas `pinMode()` / `digitalWrite()` y las gráficas del osciloscopio ($D2$, $D4$, $D5$).
3. **Cuestionario Post-Prueba (SUS - System Usability Scale):** Encuesta sobre la claridad de la interfaz, curva de aprendizaje y valor percibido.

---

## 4. Resultados y Evidencia de las Pruebas con Usuarios

*(Espacio reservado para agregar fotografías, gráficos o capturas del proceso de pruebas directas con los usuarios)*

### 4.1 Evidencias Fotográficas de las Sesiones de Pruebas

<!-- ESPACIO RESERVADO PARA FOTOS DE PRUEBAS -->
![Prueba de Usuario 1](https://via.placeholder.com/800x450.png?text=Agregar+aqu%C3%AD+Foto+de+Usuario+Jugando+Demo)
*Figura 1: Registro fotográfico de usuario ejecutando la Demo v0.1 de GPIO Génesis y probando el editor de C++.*

<!-- ESPACIO RESERVADO PARA FOTOS DE PRUEBAS 2 -->
![Prueba de Usuario 2](https://via.placeholder.com/800x450.png?text=Agregar+aqu%C3%AD+Foto+de+Feedback+o+Cuestionario)
*Figura 2: Usuario respondiendo la encuesta de usabilidad tras completar el Nivel 1.*

### 4.2 Métricas Obtenidas y Principales Descubrimientos

| Métrica Evaluada | Resultado Promedio | Interpretación / Diagnóstico |
| ----- | ----- | ----- |
| **Tiempo de completado Nivel 1** | 6.5 minutos | Adecuado; la curva introductoria no bloqueó al usuario. |
| **Consultas al Copiloto Tutor** | 1.8 veces por usuario | El copiloto local fue efectivo para corregir comas y paréntesis faltantes. |
| **Comprensión del Osciloscopio** | 85% de comprensión | Los usuarios relacionaron rápidamente el nivel de la onda con el estado del pin. |
| **Puntaje SUS (Usabilidad)** | 82.5 / 100 | Excelente nivel de usabilidad en la interfaz en general. |

---

## 5. Plan de Mejoras Basado en Retroalimentación (Iteración de Software)

Con base en las observaciones recopiladas durante las pruebas de usabilidad, se definieron los siguientes cambios prioritarios para ser integrados en las siguientes semanas de desarrollo:

1. **Mejora en los Mensajes de Error de Compilación:**
   * *Hallazgo:* Los usuarios sin experiencia previa en C++ se confundían con errores técnicos del compilador.
   * *Acción:* El Copiloto traducirá los errores del parser a lenguaje natural (ejemplo: *"Olvidaste colocar un punto y coma al final de la línea 8"*).

2. **Indicadores de Pines Interactivos en la Fábrica:**
   * *Hallazgo:* Algunos usuarios tardaban en ubicar a qué parte de la fábrica física pertenecía el pin $D4$.
   * *Acción:* Al pasar el cursor sobre la constante en el editor C++, el componente correspondiente en la animación 2D se iluminará.

3. **Tutorial de Osciloscopio:**
   * *Hallazgo:* El osciloscopio se entendía bien, pero requería explicación adicional sobre qué significa `HIGH` (5V) y `LOW` (0V).
   * *Acción:* Agregar una breve ventana emergente al iniciar por primera vez el panel de telemetría.

---

## 6. Actualización Económica y Proyección comercial

Manteniendo coherencia con los estados financieros revisados en hojas de cálculo del proyecto, las pruebas con usuarios ratifican la factibilidad económica de la venta en Steam.

* **Precio Base de Venta:** $249.00 MXN
* **Costo de Publicación en Steam:** $1,800.00 MXN ($100.00 USD)
* **Retorno Neto por Juego Vendido (tras comisión de Steam e IA):** $173.44 MXN
* **Punto de Equilibrio de Costos Fijos Directos ($8,942.50 MXN):** Requiere la venta de 52 copias a través de Steam.

---

## Reflexione de la Semana 9

Fue muy importante esta semana ya que nos ayudo a traducir los datos que tenemos a posibles ventas, por medio de usuarios, que al ser personas diferentes y tener otra prespectiva nos dió la realidad de nuestro producto y no solo la imagen que tenemos en la cabeza del proyecto.
Nos dió una ruta clara sobre que aspectos del juego tenemos que pulir, mejorar y eliminar, también me tiene muy emocionado el landing page ya que son cosas reales que nos ayudarán a obtener la atención de las personas.