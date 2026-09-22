# Tracking diario -- Corrida unificada (Parte 1 + 1.5 + 2, ejecutada en una sola sesión)

## Martes 22 de septiembre de 2026 (corrida desatendida vía Claude Code, git+node)

Ventana normal: última "Corrida diaria" publicada fue ayer 21/09 -> `publicado-hace-menos-de-2-dias` + `--max-days 1`.
Clientes nuevos ya presentes en perfiles.json (commit `dcae195` de esta mañana): Farmatodo, Puppis CABA, Smart Fit, Arcos Dorados y Mostaza · Locales, Arcos Dorados y Mostaza · Terrenos.

### Pools (RESUMEN de zp-extract.js) -- 45 pools, todos con `--max-days 1`, ninguno necesitó dividirse más
- `loc-nac` (nacional, control): páginas=9 avisos_vistos=270 devueltos=270 corte="HTTP 403 en pág 10 tras reintentos" (cubierto por las divisiones por zona de abajo)
- `loc-capital-federal`: páginas=6 avisos_vistos=180 devueltos=180 corte="última página"
- `loc-gba-norte`: páginas=2 avisos_vistos=44 devueltos=44 corte="última página"
- `loc-gba-sur`: páginas=2 avisos_vistos=48 devueltos=48 corte="última página"
- `loc-gba-oeste`: páginas=1 avisos_vistos=28 devueltos=28 corte="última página"
- `loc-cordoba`: páginas=1 avisos_vistos=24 devueltos=24 corte="última página"
- `loc-santa-fe`: páginas=1 avisos_vistos=22 devueltos=22 corte="última página"
- `loc-costa-atlantica`: páginas=1 avisos_vistos=16 devueltos=16 corte="última página"
- `loc-mendoza`: páginas=1 avisos_vistos=6 devueltos=6 corte="última página"
- `loc-neuquen`: páginas=1 avisos_vistos=4 devueltos=4 corte="última página"
- `vloc-capital-federal`: páginas=6 avisos_vistos=174 devueltos=173 corte="última página"
- `vloc-gba-norte`: páginas=1 avisos_vistos=17 devueltos=17 corte="última página"
- `vloc-gba-sur`: páginas=2 avisos_vistos=36 devueltos=36 corte="última página"
- `vloc-gba-oeste`: páginas=1 avisos_vistos=12 devueltos=12 corte="última página"
- `vloc-cordoba`: páginas=1 avisos_vistos=15 devueltos=15 corte="última página"
- `vloc-santa-fe`: páginas=1 avisos_vistos=26 devueltos=25 corte="última página"
- `vloc-costa-atlantica`: páginas=1 avisos_vistos=14 devueltos=14 corte="última página"
- `vloc-mendoza`: páginas=1 avisos_vistos=9 devueltos=9 corte="última página"
- `vloc-neuquen`: páginas=1 avisos_vistos=2 devueltos=2 corte="última página"
- `dep-alq` (depósitos en alquiler, nacional): páginas=3 avisos_vistos=80 devueltos=80 corte="última página"
- `terr-caba` (terrenos venta CABA): páginas=3 avisos_vistos=85 devueltos=85 corte="última página"
- `terr-malv` (terrenos venta Malvinas Argentinas, Padel PRO): páginas=1 avisos_vistos=7 devueltos=7 corte="última página"
- `terr-alq-caba` (terrenos alquiler CABA, nuevo por Arcos Dorados): páginas=1 avisos_vistos=5 devueltos=5 corte="última página"
- Departamentos venta 2 ambientes (Fliping/Romina): `d2-saavedra` 1/12(11) · `d2-nunez` 1/18 · `d2-belgrano` 2/37 · `d2-villa-crespo` 1/23 · `d2-villa-urquiza` 1/21(20) · `d2-palermo` 4/94 · `d2-recoleta` 1/23 · `d2-barrio-norte` 1/8 (páginas/avisos_vistos, todos "última página")
- Departamentos venta 3 ambientes (Fliping/Sergio/Cristina/Laura Flores): `d3-saavedra` 1/7 · `d3-nunez` 1/20 · `d3-belgrano` 1/29 · `d3-villa-crespo` 1/10 · `d3-villa-urquiza` 1/11(10) · `d3-palermo` 3/83 · `d3-recoleta` 1/30 · `d3-barrio-norte` 1/10 · `d3-caballito` 2/31 · `d3-almagro` 1/23 · `d3-boedo` 1/13 (todos "última página")
- Departamentos venta 4 ambientes (Sergio/Laura Flores): `d4-palermo` 3/77 · `d4-almagro` 1/11 · `d4-boedo` 1/2 (todos "última página")
- Galpones en alquiler: categoría separada no existe (redirige/301), no se corrió pool aparte -- cubierto por `dep-alq`.
- Ningún pool superó las 9 páginas salvo el nacional de control (`loc-nac`), que ya estaba cubierto por sus divisiones por zona.

### MATCH (match-perfiles.js)
MATCH avisos=1441 perfiles=60 candidatos_a_revisar=602 en 43 pestañas (geo-check.js: 1441 avisos, sin_coordenadas=2, OK_DISTANCIA=1410 · DESCARTAR=2858 · BORDE=21 · TRAMO=14 · CERCA=77 · DENTRO=33).

### Revisión fina y candidatos cargados hoy (301 tarjetas)
Metodología: para cada pestaña con criterio OBLIGATORIO de texto (planta baja, esquina real, balcón, sin amenities, cochera/guardacoche, terreno real, "a reciclar" vs "reciclado", ciudad/calle puntual) se exigió la mención explícita en la descripción del aviso -- ante ambigüedad de un obligatorio, se descartó (regla del cliente). Se deduplicaron avisos idénticos republicados bajo distinta etiqueta de barrio (mismo domicilio+precio+m²). En pestañas de alto volumen y criterio de preferencia (no obligatorio) -- Adidas, Bostani, Chango Mas, MultiBazar -- se curó una selección de hasta 20 por candidato, priorizando esquina/avenida, igual que en corridas anteriores.

caba-amba 30 · interior 5 · amba-800 8 · marcanueva-sabores 3 · laura-flores 3 · freddo 2 · chapaypintura 7 · bostani 20 · carrefour 13 · changomas 20 · havanna 1 · rappi 6 · bigpons 2 · hunterville 3 · osde-nordelta-belgrano 2 · osde-flores 3 · openpharma 1 · sergio 6 · valeria(Romina) 20 · cetrogar 1 · cafemartinez 2 · tostado 6 · thermomix 6 · tostado-fastcasual 5 · tostado-flagship 12 · guitarrita 10 · smartfit 15 · multibazar 20 · simplicity 11 · padelpro 1 · adidas 20 · adidas-factory 2 · icbc 1 · terrenos 1 · pedidosya2026 7 · osde-sanmartin-barracas 2 · osde-ambulancias 1 · fliping 3 · farmatodo 9 · puppis-caba 3 · arcos-mostaza-locales 3 · arcos-mostaza-terrenos 5

### Descartes relevantes en la revisión fina
- Laura Flores: 5 de 8 candidatos del filtro duro descartados por no mencionar balcón explícitamente o mencionar amenities (full amenities, piscina/gym/sum) -- solo 3 cumplen ambos obligatorios (balcón + sin amenities).
- AMBA +800m²: 34 de 42 descartados por no confirmar "planta baja" explícita en el aviso (muchos solo informan m² totales sin aclarar si están en PB o repartidos en varias plantas) -- ante ambigüedad de un obligatorio, se excluye.
- Carrefour: 5 de 18 descartados (plantas múltiples explícitas, no compatible con planta baja obligatoria).
- OSDE San Martín y Barracas: 9 de 11 descartados por no confirmar planta baja explícita.
- Adidas Factory: 22 de 24 descartados por no confirmar planta baja explícita (perfil exige 1.000 m² en PB).
- Farmatodo: 18 de 27 descartados por no confirmar esquina real + planta baja juntas.
- Arcos Dorados y Mostaza · Locales: 4 de 7 descartados por no confirmar esquina + planta baja juntas.
- Fliping: descartados los que dicen "reciclado"/"refaccionado a nuevo"/"impecable estado" (ya reformados, lo opuesto a lo buscado); solo 3 confirman explícitamente que falta reciclar/refaccionar.
- Sergio: 3 de 9 descartados por no mencionar cochera/guardacoche en la descripción.
- OSDE Ambulancias: 4 de 5 descartados (no confirman 8 cocheras para el caso "local"; los "depósito/galpón" sin ese dato no se exigieron cocheras).
- Café Martínez: 1 de 5 en Caballito descartado por no mencionar Parque Rivadavia.
- Cristina (tab-caballitosur): 0 candidatos nuevos hoy (el pool de deptos de Caballito 3 amb no trajo ningún caso con cochera+lavadero+balcón+antigüedad≤25 años+USD≤235.000 confirmados en la ventana hoy+ayer).
- Ril Store Mates: 0 candidatos nuevos hoy (sin avisos de 30-60 m² PB sobre los tramos de Cabildo/Santa Fe pedidos en la ventana hoy+ayer).
- Pestañas de alto volumen y preferencia (Adidas, Bostani, Chango Mas, MultiBazar): se cargó una selección curada de 20 (de 91, 36, 43 y 38 candidatos válidos respectivamente) priorizando esquina/avenida; el resto del filtro duro no se cargó, igual que en corridas anteriores.

PENDIENTES.md: revisado, no tenía nada pendiente de aplicar (última nota 19/09).
