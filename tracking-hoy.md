# Tracking diario -- Corrida unificada (Parte 1 + 1.5 + 2, ejecutada en una sola sesión)

## Jueves 24 de septiembre de 2026 (corrida desatendida vía Claude Code, git+node) -- CORRIDA DE RECUPERACIÓN

Recuperación: la última "Corrida diaria" publicada fue el 22/09 (no hubo corrida el 23/09). Ventana ampliada según sección 2b:
`publicado-hace-menos-de-3-dias` + `--max-days 2` (cubre 22/09 tarde, 23/09 y 24/09). Todos los pools con `--max-pages 9`.

### Pools (RESUMEN de zp-extract.js)
Divisiones: el nacional de alquiler (`loc-nac`, 969 avisos) queda como control y se cubre con las divisiones por zona.
`loc-capital-federal` (468) y `vloc-capital-federal` (485) superaban 9 páginas incluso por zona: se cubrieron con 3 órdenes distintos
(publicado descendente + precio ascendente + precio descendente, 9 páginas cada uno) = 438 y 450 avisos únicos dentro de la ventana.
`locales-*-buenos-aires-interior` no existe en ZonaProp (HTTP 301 persistente): se descartó ese pool.
- `d2-barrio-norte` páginas=2 avisos_vistos=35 devueltos=30 corte="última página"
- `d2-belgrano` páginas=4 avisos_vistos=95 devueltos=76 corte="corte de fecha en pág 4"
- `d2-nunez` páginas=3 avisos_vistos=61 devueltos=52 corte="corte de fecha en pág 3"
- `d2-palermo` páginas=8 avisos_vistos=233 devueltos=190 corte="corte de fecha en pág 8"
- `d2-recoleta` páginas=3 avisos_vistos=75 devueltos=63 corte="última página"
- `d2-saavedra` páginas=1 avisos_vistos=27 devueltos=20 corte="última página"
- `d2-villa-crespo` páginas=2 avisos_vistos=58 devueltos=44 corte="última página"
- `d2-villa-urquiza` páginas=2 avisos_vistos=60 devueltos=45 corte="última página"
- `d3-almagro` páginas=2 avisos_vistos=60 devueltos=44 corte="última página"
- `d3-barrio-norte` páginas=2 avisos_vistos=39 devueltos=32 corte="última página"
- `d3-belgrano` páginas=4 avisos_vistos=98 devueltos=83 corte="corte de fecha en pág 4"
- `d3-boedo` páginas=1 avisos_vistos=21 devueltos=11 corte="última página"
- `d3-caballito` páginas=3 avisos_vistos=81 devueltos=61 corte="última página"
- `d3-nunez` páginas=2 avisos_vistos=50 devueltos=43 corte="última página"
- `d3-palermo` páginas=7 avisos_vistos=190 devueltos=154 corte="corte de fecha en pág 7"
- `d3-recoleta` páginas=3 avisos_vistos=90 devueltos=73 corte="última página"
- `d3-saavedra` páginas=1 avisos_vistos=16 devueltos=10 corte="última página"
- `d3-villa-crespo` páginas=2 avisos_vistos=38 devueltos=31 corte="última página"
- `d3-villa-urquiza` páginas=2 avisos_vistos=56 devueltos=47 corte="última página"
- `d4-almagro` páginas=2 avisos_vistos=31 devueltos=26 corte="corte de fecha en pág 2"
- `d4-boedo` páginas=1 avisos_vistos=4 devueltos=3 corte="última página"
- `d4-palermo` páginas=6 avisos_vistos=160 devueltos=141 corte="corte de fecha en pág 6"
- `dep-alq` páginas=7 avisos_vistos=190 devueltos=167 corte="corte de fecha en pág 7"
- `loc-capital-federal-precio-ascendente` páginas=9 avisos_vistos=270 devueltos=246 corte="max-pages"
- `loc-capital-federal-precio-descendente` páginas=9 avisos_vistos=270 devueltos=259 corte="max-pages"
- `loc-capital-federal` páginas=9 avisos_vistos=270 devueltos=270 corte="max-pages"
- `loc-cordoba` páginas=3 avisos_vistos=68 devueltos=57 corte="corte de fecha en pág 3"
- `loc-costa-atlantica` páginas=2 avisos_vistos=45 devueltos=33 corte="última página"
- `loc-entre-rios` páginas=1 avisos_vistos=1 devueltos=1 corte="última página"
- `loc-gba-norte` páginas=4 avisos_vistos=93 devueltos=65 corte="corte de fecha en pág 4"
- `loc-gba-oeste` páginas=3 avisos_vistos=65 devueltos=52 corte="corte de fecha en pág 3"
- `loc-gba-sur` páginas=4 avisos_vistos=107 devueltos=84 corte="corte de fecha en pág 4"
- `loc-mendoza` páginas=1 avisos_vistos=14 devueltos=12 corte="última página"
- `loc-nac` páginas=9 avisos_vistos=270 devueltos=270 corte="HTTP 403 en pág 10 tras reintentos"
- `loc-neuquen` páginas=1 avisos_vistos=9 devueltos=7 corte="última página"
- `loc-salta` páginas=1 avisos_vistos=7 devueltos=2 corte="última página"
- `loc-santa-fe` páginas=2 avisos_vistos=56 devueltos=44 corte="última página"
- `loc-tucuman` páginas=1 avisos_vistos=8 devueltos=7 corte="última página"
- `terr-alq-caba` páginas=1 avisos_vistos=8 devueltos=8 corte="última página"
- `terr-caba` páginas=9 avisos_vistos=250 devueltos=223 corte="corte de fecha en pág 9"
- `terr-malv` páginas=1 avisos_vistos=10 devueltos=9 corte="última página"
- `vloc-capital-federal-precio-ascendente` páginas=9 avisos_vistos=270 devueltos=242 corte="max-pages"
- `vloc-capital-federal-precio-descendente` páginas=9 avisos_vistos=270 devueltos=259 corte="max-pages"
- `vloc-capital-federal` páginas=9 avisos_vistos=270 devueltos=267 corte="max-pages"
- `vloc-cordoba` páginas=2 avisos_vistos=43 devueltos=32 corte="última página"
- `vloc-costa-atlantica` páginas=2 avisos_vistos=46 devueltos=36 corte="última página"
- `vloc-gba-norte` páginas=3 avisos_vistos=88 devueltos=78 corte="última página"
- `vloc-gba-oeste` páginas=2 avisos_vistos=32 devueltos=26 corte="corte de fecha en pág 2"
- `vloc-gba-sur` páginas=3 avisos_vistos=68 devueltos=43 corte="corte de fecha en pág 3"
- `vloc-mendoza` páginas=1 avisos_vistos=18 devueltos=13 corte="última página"
- `vloc-neuquen` páginas=1 avisos_vistos=11 devueltos=10 corte="última página"
- `vloc-santa-fe` páginas=3 avisos_vistos=64 devueltos=46 corte="corte de fecha en pág 3"
- Galpones en alquiler: sin categoría propia (cubierto por `dep-alq`).

### MATCH (match-perfiles.js)
MATCH avisos=3206 perfiles=60 candidatos_a_revisar=1352 en 45 pestañas (geo-check.js: 3206 avisos, sin_coordenadas=9, OK_DISTANCIA=3131 · DESCARTAR=6743 · TRAMO=43 · DENTRO=70 · BORDE=46 · CERCA=170).

### Revisión fina y candidatos cargados hoy (327 tarjetas en 40 pestañas)
Metodología: en pestañas con criterio OBLIGATORIO de texto (esquina real, planta baja con los m² pedidos en PB, balcón, sin amenities, lavadero, cochera, "a reciclar", terreno real, calle/ciudad puntual) se exigió la mención explícita en el aviso; ante ambigüedad se descartó. Se deduplicaron avisos republicados bajo distinta etiqueta de barrio (misma dirección+precio+m²) y los que ya estaban cargados en la pestaña con otro ID. En pestañas sin obligatorios de alto volumen se cargó una selección de 20 priorizando esquina/avenida/PB/fecha, igual que en corridas anteriores.

caba-amba 26 · interior 4 · marcanueva-sabores 2 · laura-flores 13 · rilstore 1 · freddo 7 · chapaypintura 6 · bostani 20 · changomas 20 · havanna 1 · rappi 20 · petshop-naturallife 2 · bigpons 5 · hunterville 1 · sergio 5 · caballitosur 2 · valeria 20 · nikki 1 · cafemartinez 5 · tostado 6 · thermomix 4 · tostado-fastcasual 18 · tostado-flagship 20 · guitarrita 15 · smartfit 8 · chery 1 · multibazar 20 · simplicity 13 · julian-cipres 1 · adidas 20 · icbc 2 · terrenos 2 · pedidosya2026 5 · osde-sanmartin-barracas 1 · osde-ambulancias 8 · fliping 5 · farmatodo 1 · puppis-caba 12 · arcos-mostaza-locales 1 · arcos-mostaza-terrenos 3

### Descartes relevantes en la revisión fina
- AMBA +800m², Carrefour y Adidas Factory: 0 nuevos. Los que mencionaban PB no llegan a los m² pedidos EN planta baja (Paraná 100, Maipú 500, H. Yrigoyen 1400: PB 683 m², Perón 1500, Sarmiento 2900 hotel; Carrefour: El Salvador 5600/5700 con solo 100 m² en PB, Esmeralda 100 con 92 m² en PB).
- Farmatodo (1) y Arcos Dorados/Mostaza Locales (1): solo B. Mitre 3100 esq. Jean Jaures (400 m² en PB) cumple esquina + m² en PB; descartados Cabrera 5100 (PB 130), Oro 2700 (PB 202), El Salvador (PB 100), Ibáñez 7400 y Sarmiento 2900 (sin m² de PB claros).
- AMBA: descartados Florida 816 ("a pocos metros de la esquina", no es esquina) y Erezcano 1200 Adrogué ("cinco esquinas" es la zona); 41 ya estaban cargados con otro ID.
- Laura Flores: 10 sin balcón explícito, 5 con amenities, y 2 con cochera incluida (Av. La Plata 647 y Av. La Plata e/ EE.UU. e Independencia; el perfil pide sin cochera). Castro Barros 900 va con nota de cochera opcional aparte.
- Interior: descartados 4 que solo decían "flujo/movimiento peatonal" (no están sobre una peatonal).
- Café Martínez: descartados 4 de Caballito que no están en zona Parque Rivadavia (Rivadavia 6000 y 7100, Díaz Vélez 5300, J. M. Moreno 0).
- Farmacias Simplicity: descartados 8 de Mar del Plata fuera de Rivadavia/Santa Fe/Alem y 2 de Mendoza fuera de San Martín/Godoy Cruz/Las Heras.
- Pedidos Ya 2026: descartados Córdoba fuera de calle 25 de Mayo (2), Funes (no es Rosario centro), MdP Champagnat y Alte. Brown (no es zona sur), showroom Güemes sin m² y Neuquén 700 Mendoza sin m².
- Sergio: 7 sin cochera/guardacoche. Cristina: 2 sin lavadero. Fliping: 6 que no dicen que hay que reciclar. OSDE San Martín y Barracas: 16 sin PB explícita. Julián Ciprés: 9 sin PB explícita.
- Chango Mas: descartado Av. Santa Fe 1700 ($300.000 y 13.702 m², datos inconsistentes).
- Ril Store Mates: 1 (Av. Cabildo 2000, 60 m² en PB, cabecera de galería con frente 4 m).
- Open Pharma y Padel PRO: los candidatos ya estaban cargados.

PENDIENTES.md: revisado, no tenía nada pendiente de aplicar.
