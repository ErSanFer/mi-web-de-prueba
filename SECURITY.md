# Política de Seguridad

## Versiones Soportadas

Este repositorio contiene el juego principal (`juego.html`) y sus variantes (como `DEv65T.html`). Al ser un proyecto web estático, solo se proporcionan actualizaciones de seguridad para las versiones más recientes.

| Componente | Soportado |
| ------- | --------- |
| Juego principal (`juego.html`) | ✅ Sí |
| Variantes (`DEv65T.html`, etc.) | ✅ Sí |
| Versiones antiguas (sin versionar) | ❌ No |

## Reportar una Vulnerabilidad

Si descubres una vulnerabilidad de seguridad en "Duelo de Estrellas" (ya sea en el juego principal o en sus variantes), te agradecemos que nos lo hagas saber de forma responsable. 

**Por favor, NO reportes vulnerabilidades de seguridad abriendo un "Issue" público.**

En su lugar, utiliza una de las siguientes opciones:
1. **Reporte privado de GitHub**: Ve a la pestaña "Security" (Seguridad) de este repositorio y haz clic en "Report a vulnerability" (Reportar una vulnerabilidad).
2. **Correo electrónico**: Envía un correo a `[TU_CORREO_AQUÍ@ejemplo.com]` con el asunto "Vulnerabilidad de Seguridad - Duelo de Estrellas".

### ¿Qué incluir en tu reporte?
Para ayudarnos a entender y solucionar el problema rápidamente, incluye:
* El archivo afectado (ej. `juego.html` o `DEv65T.html`).
* Una descripción clara de la vulnerabilidad.
* Los pasos detallados para reproducirla.
* El impacto potencial (ej. ejecución de scripts, bloqueo del navegador, etc.).
* Si es posible, una prueba de concepto (PoC) o capturas de pantalla.

### ¿Qué puedes esperar?
* Confirmación de recepción de tu reporte en un plazo de **48 a 72 horas**.
* Te mantendremos informado sobre el progreso de la corrección.
* Una vez solucionado, se te dará crédito en las notas de la versión (si así lo deseas).

## Alcance de la Seguridad (Scope)

Dado que este es un juego 100% frontend (lado del cliente) sin backend, las siguientes son las áreas de interés principal para **todos los archivos del repositorio**:
* **Cross-Site Scripting (XSS)**: Inyección de código malicioso a través de la carga de archivos JSON o inputs de texto.
* **Prototype Pollution**: Manipulación maliciosa de objetos JavaScript mediante el sistema de importación de partidas (JSON).
* **Denegación de Servicio (DoS)**: Archivos JSON malformados o gigantes que puedan bloquear el navegador al ser importados, o fallos en la IA (Web Worker) que congelen la interfaz.

## Fuera de Alcance (Out of Scope)

Las siguientes acciones **no** se consideran vulnerabilidades de seguridad en este proyecto:
* **Hacer trampas**: Modificar el código JavaScript a través de la consola del navegador para obtener ventajas, alterar el tablero o desbloquear la IA (aplica tanto a `juego.html` como a las variantes).
* **Modificar archivos locales**: Cambiar el archivo HTML o JSON directamente en tu ordenador.
* **Problemas de rendimiento**: Que la IA tarde mucho en calcular jugadas en dificultades altas.
* **Ataques físicos**: Acceso físico al dispositivo donde se ejecuta el juego.
