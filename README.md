# ENDGAME 2.0 Beta

## Incluido
- PWA con caché offline (requiere HTTPS o localhost).
- Biblioteca vacía, creación de bancos e importación JSON/CSV con vista previa.
- Modo estudio con corrección inmediata.
- Simulacros con temporizador, respuestas guardadas, revisión y corrección final.
- Historial local y estadísticas básicas.
- Copia JSON completa, restauración aditiva y exportación CSV.
- Tema oscuro/claro, alto contraste y tamaño de texto.

## Limitaciones conocidas
Esta es una Beta inicial. No incluye cuentas, nube, sincronización entre dispositivos, colaboración, push, cifrado de copias, Ranked adaptativo completo, listas/favoritos/notas, auditoría avanzada ni resolución detallada de duplicados. La recuperación de exámenes debe probarse antes de considerarse fiable. No ha sido verificada en dispositivos físicos.

## Ejecutar en ordenador
Desde esta carpeta ejecuta `python -m http.server 8000` y abre `http://localhost:8000`. PWA/service worker requiere HTTPS o localhost; no abras el HTML como archivo local.

## Instalar en iPhone/iPad
Publica los archivos en un hosting HTTPS estático. Abre la URL en Safari y usa Compartir → Añadir a pantalla de inicio.

## Formato JSON básico
Una matriz de preguntas, cada una con `prompt`, `options` y `correctAnswer`. `options` puede ser una matriz de objetos `{ "id": "A", "text": "..." }`; se aceptan también algunos nombres de campo alternativos. Se pueden incluir `module`, `subtopic` y `explanation`.
