# Tracking diario -- Parte 1 (alquiler, pool nacional de locales comerciales)

## Miércoles 17 de septiembre de 2026 (corrida de fin de semana, desatendida, vía Claude Code / adaptación local con git+node)

### Pool cubierto
- URL: `https://www.zonaprop.com.ar/locales-comerciales-alquiler-publicado-hace-menos-de-2-dias-orden-publicado-descendente.html` (`--max-days 1`, excluye avisos ya cargados en el HTML).
- RESUMEN del script (`zp-extract.js`): `páginas=9 avisos_vistos=243 devueltos=243 ya_cargados_excluidos=sí corte="última página"`. Un solo HTTP 522 transitorio en la página 2, resuelto con el reintento automático del script. No hizo falta dividir por zona (no se llegó al límite de 9 páginas con bloqueo 403).
- Cobertura: 100% del pool de alquiler nacional dentro de la ventana "hoy + ayer".

### Método de evaluación
Los 243 avisos se filtraron con un script Node contra los ~40 perfiles de alquiler que cubre esta Parte 1 (zona, m² cubiertos, tope de precio cuando aplica, y verificación de esquina/planta baja/palabra clave vía regex sobre título+dirección+descripción completa). Se corrigieron manualmente colisiones de nombre de zona con otra provincia/ciudad homónima (San Martín→Mendoza, San Justo/Avellaneda→Santa Fe, Bella Vista→Corrientes, Neuquén capital vs. San Martín de los Andes, Santa Fe capital vs. Rosario/Rafaela) exigiendo coincidencia exacta de componente de ciudad+provincia en vez de substring. Los 99 avisos únicos sobrevivientes se revisaron uno por uno (dirección, m², precio, esquina/PB/palabras clave, cocheras) antes de cargar.

### Candidatos nuevos cargados hoy (221 tarjetas en 28 pestañas)
- AMBA: 10 · Interior del País: 1 · AMBA +800m²: 5 (se excluyó 1 aviso con m² mal parseado por el sitio, ver nota) · Freddo: 3 · Taller Chapa y Pintura: 4 · Bostani Coffee: 23 · Carrefour: 6 · Havanna: 9 · Rappi (local): 1 · Big Pons: 1+3 (pendientes del 15/09) · Hunterville: 2+1 (íd.) · Osde Núñez: 1+1 (íd.) · Café Martínez: 1 · Tostado Café Club: 1 · Pizzería La Guitarrita: 13 · Thermomix: 2 · Concesionaria Chery: 1 · MultiBazar/City Moda: 13 · Smartfit/On Fit Gym: 1 · Farmacias Simplicity: 5 · Adidas: 39 · Pedidos Ya 2026 (local): 1 · Adidas Factory: 5 · Tostado Fast Casual: 13 · Tostado Flagship: 27 · Chango Mas: 24 · Julián Ciprés: 2 · OSDE Ambulancias (local): 2.
- Perfiles con volumen alto (Adidas, Chango Mas, Tostado Flagship, Bostani, Pizzería La Guitarrita, MultiBazar, Tostado Fast Casual) tienen zonas obligatorias muy amplias (CABA/AMBA completo) y poco filtro adicional, por lo que un pool nacional grande produce naturalmente muchos candidatos — no es un error del filtro.
- Sin novedades hoy: Puppis, Nikki, Havaiana, KFC, Osde Flores, Open Pharma, Cetrogar, Bazar Freddy, Fundación ICBC, OSDE Lanús Oeste, OSDE San Martín y Barracas, Tostado Casual to go (pausado, no se buscó).

### Descartes obligatorios relevantes (no se cargaron)
- **Carrefour**: se excluyeron 6 avisos que sí cumplían m²/precio pero cuya dirección está a ~4-5 cuadras o menos de una sucursal Carrefour existente (según `referencias/carrefour-sucursales-caba.txt`) o con precio/PB ambiguos: Hipólito Yrigoyen 500 y Florida 300 (Microcentro, USD 15.000 supera el tope), Costa Rica 5100 y El Salvador s/n (PB no confirmado), Av. Cabildo 1932 (≈5 cuadras de la sucursal Cabildo 2441), Av. del Libertador 6802 (precio no informado).
- **OSDE Ambulancias (sub-caso local)**: de 19 avisos que cumplían zona + mínimo 200 m², solo 2 confirmaban explícitamente el mínimo de 8 cocheras (obligatorio); los otros 17 no lo mencionaban y se excluyeron por ambigüedad de un criterio obligatorio (regla del proyecto: ante duda en un obligatorio, no cargar).
- Un aviso en Microcentro (id 60169942) traía un m² total mal parseado por el sitio (18.200 en vez de 182 reales, según la propia descripción) — se excluyó de "AMBA +800m²" y "Adidas Factory" (no llega al mínimo real) pero se mantuvo en Tostado Flagship y Chango Mas (182 m² sí califica ahí).

### PENDIENTES.md aplicado hoy
- 3 ediciones de texto (nota de brokers en Rappi + 15 zonas actualizadas, "8 cocheras" + split local/depósito en OSDE Ambulancias, City Bell + Av. 8/12 en Farmacias Simplicity) y el rename de pestaña Valeria → Romina, aplicados directo sobre el HTML con Edit (balance de divs verificado: 8882/8882 antes y después).
- 5 candidatos sueltos del 15/09 (Big Pons x3, Hunterville, Osde Núñez) cargados con `insert-cards.js`.
- 2 candidatos del 16/09 (Freddo, Thermomix) resultaron ser los mismos ID de aviso que ya trajo el pool de hoy — no se duplicaron.
- Se dejaron pendientes (sin evaluar con rigor suficiente esta corrida) los 3 perfiles nuevos sin pestaña propia (Hazrat Namasté India, Laura Flores, Hamburguesas Extremas) y las 2 pestañas de Sabores Express: requieren lógica de calle+altura exacta por esquina que el filtro grueso de hoy no puede verificar de forma confiable (solo hace coincidencia de nombre de calle, no de rango de altura), así que no se cargó nada especulativo ahí. Quedan para una corrida dedicada a crear esas pestañas.
- Bug encontrado y corregido en `insert-cards.js`: no detectaba la pestaña activa por defecto (`class="tab-panel active"` en vez de `class="tab-panel"`), lo que hacía fallar silenciosamente la carga en la pestaña AMBA. Corregido para tolerar clases extra en el div.

### Publicación
Un solo commit + push al final de la corrida (ver hash en el resumen de la sesión).
