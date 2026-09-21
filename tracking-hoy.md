# Tracking diario -- Corrida unificada (Parte 1 + 1.5 + 2)

## Lunes 21 de septiembre de 2026 (corrida desatendida vía Claude Code, git+node)

**CORRIDA DE RECUPERACIÓN:** la última corrida publicada fue la del 19/09; faltó el día 20/09. Ventana ampliada: publicado-hace-menos-de-3-dias + --max-days 2.

### Pools (RESUMEN de zp-extract.js)
- `d2-almagro`: RESUMEN páginas=2 avisos_vistos=36 devueltos=23 corte="corte de fecha en pág 2"
- `d2-barrio-norte`: RESUMEN páginas=1 avisos_vistos=10 devueltos=5 corte="última página"
- `d2-belgrano`: RESUMEN páginas=2 avisos_vistos=50 devueltos=20 corte="corte de fecha en pág 2"
- `d2-boedo`: RESUMEN páginas=1 avisos_vistos=15 devueltos=8 corte="última página"
- `d2-caballito`: RESUMEN páginas=3 avisos_vistos=63 devueltos=34 corte="corte de fecha en pág 3"
- `d2-nunez`: RESUMEN páginas=2 avisos_vistos=34 devueltos=17 corte="corte de fecha en pág 2"
- `d2-palermo`: RESUMEN páginas=4 avisos_vistos=120 devueltos=75 corte="corte de fecha en pág 4"
- `d2-recoleta`: RESUMEN páginas=2 avisos_vistos=39 devueltos=15 corte="corte de fecha en pág 2"
- `d2-saavedra`: RESUMEN páginas=1 avisos_vistos=14 devueltos=8 corte="última página"
- `d2-villa-crespo`: RESUMEN páginas=2 avisos_vistos=34 devueltos=20 corte="corte de fecha en pág 2"
- `d2-villa-urquiza`: RESUMEN páginas=2 avisos_vistos=34 devueltos=23 corte="corte de fecha en pág 2"
- `d3-almagro`: RESUMEN páginas=2 avisos_vistos=43 devueltos=29 corte="corte de fecha en pág 2"
- `d3-barrio-norte`: RESUMEN páginas=1 avisos_vistos=11 devueltos=6 corte="última página"
- `d3-belgrano`: RESUMEN páginas=2 avisos_vistos=60 devueltos=23 corte="corte de fecha en pág 2"
- `d3-boedo`: RESUMEN páginas=1 avisos_vistos=16 devueltos=14 corte="última página"
- `d3-caballito`: RESUMEN páginas=2 avisos_vistos=52 devueltos=33 corte="última página"
- `d3-nunez`: RESUMEN páginas=2 avisos_vistos=32 devueltos=12 corte="corte de fecha en pág 2"
- `d3-palermo`: RESUMEN páginas=3 avisos_vistos=90 devueltos=45 corte="corte de fecha en pág 3"
- `d3-recoleta`: RESUMEN páginas=2 avisos_vistos=48 devueltos=32 corte="última página"
- `d3-saavedra`: RESUMEN páginas=1 avisos_vistos=10 devueltos=7 corte="última página"
- `d3-villa-crespo`: RESUMEN páginas=1 avisos_vistos=20 devueltos=13 corte="última página"
- `d3-villa-urquiza`: RESUMEN páginas=1 avisos_vistos=25 devueltos=13 corte="última página"
- `d4-almagro`: RESUMEN páginas=1 avisos_vistos=14 devueltos=9 corte="última página"
- `d4-boedo`: RESUMEN páginas=1 avisos_vistos=2 devueltos=2 corte="última página"
- `d4-palermo`: RESUMEN páginas=3 avisos_vistos=90 devueltos=38 corte="corte de fecha en pág 3"
- `dep-alq`: RESUMEN páginas=3 avisos_vistos=90 devueltos=36 corte="corte de fecha en pág 3"
- `deptos-2`: RESUMEN páginas=9 avisos_vistos=270 devueltos=264 corte="HTTP 403 en pág 10 tras reintentos"
- `deptos-3`: RESUMEN páginas=9 avisos_vistos=270 devueltos=265 corte="HTTP 403 en pág 10 tras reintentos"
- `deptos-4`: RESUMEN páginas=9 avisos_vistos=270 devueltos=264 corte="HTTP 403 en pág 10 tras reintentos"
- `galp-alq`: RESUMEN páginas=0 avisos_vistos=0 devueltos=0 corte="HTTP 301 en pág 1 tras reintentos"
- `loc-buenos-aires-costa-atlantica`: RESUMEN páginas=1 avisos_vistos=23 devueltos=18 corte="última página"
- `loc-capital-federal`: RESUMEN páginas=6 avisos_vistos=177 devueltos=132 corte="corte de fecha en pág 6"
- `loc-cordoba`: RESUMEN páginas=1 avisos_vistos=28 devueltos=19 corte="última página"
- `loc-gba-norte`: RESUMEN páginas=3 avisos_vistos=66 devueltos=35 corte="corte de fecha en pág 3"
- `loc-gba-oeste`: RESUMEN páginas=2 avisos_vistos=39 devueltos=25 corte="corte de fecha en pág 2"
- `loc-gba-sur`: RESUMEN páginas=3 avisos_vistos=62 devueltos=41 corte="corte de fecha en pág 3"
- `loc-mendoza`: RESUMEN páginas=1 avisos_vistos=11 devueltos=5 corte="última página"
- `loc-nac`: RESUMEN páginas=9 avisos_vistos=270 devueltos=270 corte="HTTP 403 en pág 10 tras reintentos"
- `loc-neuquen`: RESUMEN páginas=1 avisos_vistos=10 devueltos=4 corte="última página"
- `loc-santa-fe`: RESUMEN páginas=2 avisos_vistos=31 devueltos=17 corte="corte de fecha en pág 2"
- `terr-caba`: RESUMEN páginas=4 avisos_vistos=120 devueltos=66 corte="corte de fecha en pág 4"
- `terr-malv`: RESUMEN páginas=1 avisos_vistos=30 devueltos=0 corte="corte de fecha en pág 1"
- `venta-loc`: RESUMEN páginas=9 avisos_vistos=270 devueltos=269 corte="HTTP 403 en pág 10 tras reintentos"
- `vloc-buenos-aires-costa-atlantica`: RESUMEN páginas=1 avisos_vistos=15 devueltos=8 corte="última página"
- `vloc-capital-federal`: RESUMEN páginas=5 avisos_vistos=139 devueltos=93 corte="corte de fecha en pág 5"
- `vloc-cordoba`: RESUMEN páginas=2 avisos_vistos=34 devueltos=17 corte="corte de fecha en pág 2"
- `vloc-gba-norte`: RESUMEN páginas=2 avisos_vistos=42 devueltos=25 corte="corte de fecha en pág 2"
- `vloc-gba-oeste`: RESUMEN páginas=2 avisos_vistos=40 devueltos=27 corte="corte de fecha en pág 2"
- `vloc-gba-sur`: RESUMEN páginas=2 avisos_vistos=47 devueltos=31 corte="última página"
- `vloc-mendoza`: RESUMEN páginas=1 avisos_vistos=8 devueltos=6 corte="última página"
- `vloc-neuquen`: RESUMEN páginas=1 avisos_vistos=6 devueltos=3 corte="última página"
- `vloc-santa-fe`: RESUMEN páginas=2 avisos_vistos=49 devueltos=37 corte="última página"
- Pools grandes que superaron 9 páginas (nacional de locales en alquiler, venta de locales, deptos 2/3/4 amb de CABA) se descartaron/complementaron con divisiones por zona y por barrio (todas cortaron por fecha o última página, sin 403). El pool nacional de alquiler (270 avisos, 403 en pág 10) queda cubierto por sus zonas (CABA, GBA norte/sur/oeste, Córdoba, Santa Fe, Costa Atlántica, Mendoza, Neuquén); provincias sin división propia (Tucumán, Salta, etc.) solo cubiertas por las primeras 9 páginas. Galpones-alquiler: URL devuelve 301 (sin categoría propia). Padel PRO: 30 avisos vistos, 0 en ventana.

### MATCH
MATCH avisos=1201 perfiles=55 candidatos_a_revisar=547 en 41 pestañas (267 avisos únicos revisados a mano).

### Candidatos cargados hoy (251 tarjetas)
caba-amba 27 · interior 3 · amba-800 1 · laura-flores 7 · rilstore 2 · freddo 2 · chapaypintura 5 · bostani 27 · carrefour 6 · changomas 12 · havanna 1 · rappi 1 · bigpons 1 · hunterville 1 · osde-nunez 1 · osde-nordelta-belgrano 1 · sergio 2 · caballitosur 2 · cetrogar 1 · havaiana 2 · cafemartinez 2 · tostado 3 · thermomix 2 · tostado-fastcasual 15 · tostado-flagship 15 · guitarrita 12 · smartfit 5 · chery 1 · multibazar 14 · simplicity 1 · julian-cipres 5 · adidas 17 · icbc 1 · terrenos 1 · pedidosya2026 1 · osde-sanmartin-barracas 7 · osde-ambulancias 4 · valeria 31 · fliping 9

### Descartes en la revisión fina (criterio conservador)
- Laura Flores: sin balcón confirmado o con cochera/amenities: 60193680, 60193992, 60194566, 60200308, 60205767 (cochera/amenities); 60196960, 60197094, 60198122, 60198480, 60199203, 60200269, 60203955 (balcón no confirmado en el aviso).
- Sergio: 60193764 y 60194432 sin cochera confirmada. Cristina: 60195754, 60200503, 60202235, 60202282 sin cochera confirmada; 60195476 Caballito Norte.
- AMBA +800: sin planta baja >=800 m² confirmada (Virrey Liniers PB 331 m², Florida/Pueyrredón/Corrientes con planta baja menor).
- Fliping: descartados los "refaccionado a nuevo"/sin dato claro de reforma. Romina: excluidas 60198637 y 60202745 (mencionan cochera), 60199170 (precio inconsistente), 60198951 (apto profesional).
- Adidas, Tostado Flagship/Fast casual, MultiBazar, Bostani y Chango Mas: selección de los mejores por ubicación/arteria; el resto de los candidatos del filtro duro no se cargó.
