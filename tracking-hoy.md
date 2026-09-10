# Tracking - Locales Comerciales CABA

**Fecha de esta actualización:** Jueves 10 de septiembre de 2026

## ✅ INCIDENTE RESUELTO — publicación del 09/09 completada

El incidente reportado el 09/09 (index.html sobrescrito con "PLACEHOLDER" al intentar pushear vía `create_or_update_file` con el contenido completo del sitio en una sola llamada) quedó resuelto hoy.

**Causa real del problema anterior:** no era un límite real de la herramienta de GitHub sino el método usado — se intentó pasar el archivo completo (~640.000 caracteres) como texto literal en una sola llamada de `create_or_update_file`, lo cual es propenso a fallar/truncarse en sesiones de este tamaño. El repo ya contaba con un mecanismo correcto para esto: el script `.publish-to-github.sh`, que clona el repo, copia los archivos actualizados desde la carpeta local y hace `git push` normal con credencial guardada (`.gh-publish-token`). Este es el método que usan las corridas programadas diarias, y por eso nunca tuvieron el problema.

**Corrección aplicada hoy:**
1. Se ejecutó `.publish-to-github.sh` apuntando a la carpeta local "CLAUDE Metrica", que ya tenía el archivo consolidado con los candidatos pendientes.
2. Commit resultante: `0d2b001` (rama `main`), mensaje "Actualizacion diaria 10/09/2026".
3. Se verificó el sitio publicado (https://metricapropiedades.github.io/locales-comerciales-caba/) — `index.html` ya no muestra el placeholder roto, redirige correctamente y `Locales Comerciales CABA.html` sirve el contenido completo (confirmado sin la palabra "PLACEHOLDER" en el HTML servido).
4. `Locales Comerciales CABA.html` ya estaba sincronizado con el contenido local (mismo tamaño que el remoto antes del push, sin diferencias) — el archivo nunca se corrompió, tal como se había registrado el 09/09.

**Pendiente / a confirmar en la próxima corrida:**
- Verificar manualmente en el sitio publicado que los candidatos de la corrida del 09/09 (Pedidos Ya 2026 y Agustín Ali, detallados en el tracking anterior) estén efectivamente visibles en sus pestañas correspondientes.
- Usar siempre `.publish-to-github.sh` (o el flujo git normal) para publicar el archivo grande — no `create_or_update_file` con el contenido completo en una sola llamada.
