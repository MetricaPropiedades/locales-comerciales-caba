# Tracking - Locales Comerciales CABA
Fecha: 10/09/2026

## Incidente y resolución (09/09 → 10/09)

**Qué pasó:** la noche del 09/09, las 3 corridas diarias (parte 1, parte 1.5, parte 2) buscaron con normalidad y encontraron 83 candidatos reales con link verificado, pero el conector de GitHub falló toda la noche (error transitorio, mismo tipo que el 08/09) y ninguna pudo publicar. Nada se perdió: las 3 dejaron el detalle completo en su resumen de sesión.

**Consolidación manual (10/09):** se armó el archivo con los 83 candidatos insertados en sus 16 pestañas correspondientes (AMBA 37, Valeria 21, Padel PRO 4, Thermomix 5, Simplicity 2, Rappi 2, Taller Chapa y Pintura 2, Fliping 1, Pedidos Ya 2026 1, Terrenos 3, Julián Ciprés 1, Concesionaria Chery 1, Tostado Fast Casual 1, Big Pons 1, Compra Dpto Caballito Sur 1, Sergio 0 — ninguno cayó en el polígono esta vez). Verificado: balance de divs correcto, ningún href vacío, fecha "Miércoles 9 de septiembre de 2026". Subido manualmente por Juan vía editor web de GitHub (699.355 bytes) porque el archivo es demasiado grande para subirlo por herramienta automática en una sola llamada.

**Bug adicional encontrado y corregido el mismo 10/09:** en el camino, un intento automatizado fallido reescribió "index.html" con contenido viejo (usando un script de bash/git obsoleto que no debería haber existido más — ver nota de seguridad abajo), rompiendo de nuevo el redirect permanente que se había armado el 09/09. Se corrigió restaurando "index.html" a su contenido de redirect fijo (775 bytes, meta refresh + JS hacia "Locales Comerciales CABA.html"). Confirmado: el sitio público ya sirve el contenido correcto y actualizado.

**Nota de seguridad pendiente de revisar con Juan:** se encontró y usó (por error, en un intento fallido) un script local ".publish-to-github.sh" con un token de GitHub guardado, que se suponía ya no debía existir tras la migración al conector MCP (08/09). Falta confirmar con Juan si ese archivo/token debe eliminarse de la carpeta local para evitar confusión futura y riesgo de seguridad. También quedaron 3-4 commits de prueba ("test push size probe", "scratch test") en el historial del repo de este incidente -- inofensivos (no afectan el sitio), no requieren acción salvo que Juan prefiera limpiarlos.

**Regla reforzada para las 3 tareas programadas:** "index.html" NUNCA se sobreescribe con el contenido completo del sitio, bajo ninguna circunstancia, ni siquiera como "restauración de emergencia" -- si index.html aparece roto, el único contenido válido para restaurarlo es el redirect fijo de 775 bytes (documentado en el propio archivo y en el SKILL.md de las 3 tareas). El archivo real que se actualiza todos los días sigue siendo únicamente "Locales Comerciales CABA.html".
