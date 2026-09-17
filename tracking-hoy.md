# Tracking diario -- Corrida unificada (Parte 1 + 1.5 + 2)

## Jueves 17 de septiembre de 2026 (corrida desatendida vía Claude Code, adaptación local con git+node, ver `legacy-tareas/ADAPTACION-CLAUDE-CODE.md`)

### PARTE 1 -- Alquiler nacional de locales comerciales
Pool base: `locales-comerciales-alquiler-publicado-hace-menos-de-2-dias-orden-publicado-descendente.html` (`--max-days 1`).
- RESUMEN nacional: `páginas=9 avisos_vistos=270 devueltos=203 corte="HTTP 403 en pág 10 tras reintentos"` (total real del pool: 307 avisos; ZonaProp bloquea páginas 10+ fuera de navegador).
- Para cubrir el resto se dividió por zona (según indica el script):
  - capital-federal: `páginas=4 avisos_vistos=108 devueltos=54 corte="última página"`
  - gba-norte: `páginas=2 avisos_vistos=39 devueltos=30 corte="última página"`
  - gba-sur: `páginas=2 avisos_vistos=39 devueltos=35 corte="última página"`
  - gba-oeste: `páginas=1 avisos_vistos=19 devueltos=17 corte="última página"`
  - cordoba: `páginas=1 avisos_vistos=24 devueltos=23 corte="última página"`
  - santa-fe: `páginas=1 avisos_vistos=19 devueltos=18 corte="última página"`
  - buenos-aires-costa-atlantica: `páginas=1 avisos_vistos=23 devueltos=18 corte="última página"`
- Cobertura por zonas: ~271 de 307 avisos vistos (~88%); el resto (~36) corresponde a provincias chicas no desagregadas (Mendoza, Entre Ríos, etc., cada una con pocos avisos). No se dividió más por presupuesto de tiempo.
- Todos los pools (nacional + zonas) se dedupearon por ID de aviso antes de filtrar.

### PARTE 1.5 -- Depósitos y galpones
- Depósitos: `https://www.zonaprop.com.ar/depositos-alquiler-publicado-hace-menos-de-2-dias-orden-publicado-descendente.html` → `páginas=2 avisos_vistos=54 devueltos=54 corte="última página"`.
- Galpones: confirmado (de nuevo) que la categoría separada NO existe -- la URL devuelve 404 y redirige a `handleUrlNotRecognize`. Los galpones están mezclados dentro del pool de Depósitos, como ya estaba documentado.

### PARTE 2 -- Venta de locales, Fliping, Sergio, Caballito Sur, Romina/Valeria, Terrenos, Padel PRO
- Venta locales comerciales (nacional): `locales-comerciales-venta-publicado-hace-menos-de-2-dias-orden-publicado-descendente.html` → `páginas=8 avisos_vistos=220 devueltos=218 corte="última página"` (no llegó al límite de 9 páginas, cobertura 100%).
- Departamentos venta, 8 barrios (Saavedra, Núñez, Belgrano, Villa Crespo, Villa Urquiza, Palermo, Recoleta, Barrio Norte), 2 ambientes (Fliping + Romina/Valeria): `páginas=7 avisos_vistos=205 devueltos=200 corte="última página"`.
- Mismos 8 barrios, 3 ambientes (Fliping + Sergio): `páginas=7 avisos_vistos=205 devueltos=199 corte="última página"`.
- Caballito, 3 ambientes (Caballito Sur): `páginas=2 avisos_vistos=39 devueltos=39 corte="última página"`.
- Palermo, 4 ambientes (Sergio): `páginas=2 avisos_vistos=44 devueltos=43 corte="última página"`.
- Terrenos, mismos 8 barrios (Terrenos): `páginas=1 avisos_vistos=15 devueltos=15 corte="última página"`.
- Terrenos Malvinas Argentinas (Padel PRO): `páginas=1 avisos_vistos=5 devueltos=5 corte="última página"` (con filtro de fecha agregado; la URL fija original del perfil no trae orden por fecha y daba 0 en la ventana hoy+ayer).

### Método de evaluación
Todos los pools (locales alquiler+venta deduplicados = 442 avisos únicos, depósitos = 54, deptos 2amb = 200, deptos 3amb = 199, Palermo 4amb = 43, Caballito 3amb = 39, terrenos = 15, Padel PRO = 5) se filtraron con un script Node contra los 48 perfiles de la Parte 1 + los perfiles de depósito/galpón de la Parte 1.5 + Fliping/Sergio/Caballito Sur/Romina/Terrenos/Padel PRO de la Parte 2, usando zona (con corrección de colisión de nombre de provincia: San Martín→Mendoza, San Justo/Avellaneda→Santa Fe, Bella Vista→Corrientes, Microcentro→Chaco, y exclusión de La Plata/Brandsen/Costa Atlántica del criterio estricto "AMBA"), m² cubiertos/totales, presupuesto (equivalencia USD/ARS ~$1.550), esquina/planta baja/palabras clave por regex sobre título+dirección+descripción completa, altura sobre calle para los perfiles de calles puntuales o polígono (Open Pharma, Sergio, Pet Shop Jardín Botánico), cocheras, ambientes y antigüedad para los perfiles residenciales. Los sobrevivientes se revisaron a mano (dirección, m², precio, esquina/PB/palabras clave) antes de cargar.

### Candidatos nuevos cargados hoy (162 tarjetas en 28 pestañas)
De la búsqueda de hoy (141): Adidas 10 · Bostani Coffee 14 · Romina 22 · Fliping 15 · AMBA +800m² 11 · Farmacias Simplicity 11 · AMBA 8 · Interior del País 5 · Tostado Fast Casual 5 · Chango Mas 5 · Havanna 4 · Pedidos Ya 2026 3 · Tostado Café Club 3 · Tostado Flagship 3 · Taller Chapa y Pintura 3 · Compra Dpto Caballito Sur 3 · Thermomix 2 · Cetrogar 2 · Pizzería La Guitarrita 2 · Smartfit/On Fit Gym 2 · OSDE Ambulancias 2 · Concesionaria Chery 1 · Freddo 1 · Carrefour 1 · MultiBazar/City Moda 1 · Rappi 1 · Agustín Ali 1.
De PENDIENTES.md (backlog 15-16/09, aplicado hoy, 21 nuevas tras dedup): Romina 14 · Fliping 3 · Compra Dpto Caballito Sur 1 · Rappi 1 · AMBA 1 · Padel PRO 1. (El resto del backlog ya había sido encontrado también por la búsqueda de hoy -- deduplicado automáticamente por `insert-cards.js`.)
Sin novedades hoy: KFC, Osde Núñez, Osde Nordelta/Belgrano, Osde Flores, Open Pharma, Osde Olivos, Puppis, Nikki, Havaiana, Café Martínez, Big Pons, Hunterville, Pet Shop-Natural Life, Fundación ICBC, OSDE Lanús Oeste, Bazar Freddy, OSDE San Martín/Barracas, Adidas Factory, Julián Ciprés, Sergio, Terrenos (0 candidatos reales tras revisión completa).

### Descartes / notas de verificación manual pendiente
- **Carrefour** (1 candidato, Av. Eslovenia 1987/Las Cañitas): no hay sucursal Carrefour listada en Las Cañitas ni sobre Scalabrini Ortiz/Cabildo a menos de 4 cuadras según `referencias/carrefour-sucursales-caba.txt` -- cargado, pero recomendable confirmar a mano.
- **Havanna** (4 candidatos): no existe archivo de referencia de sucursales Havanna en el repo (pendiente #6 de PENDIENTES.md) -- se cargaron igual, sin poder verificar automáticamente la regla de "mínimo 8 cuadras de otra sucursal".
- **KFC y OSDE Lanús Oeste**: 0 candidatos hoy que superen el filtro automático de calle+altura/polígono.
- **OSDE Ambulancias**: los 2 candidatos cargados son del sub-caso depósito/galpón (300m²+, cocheras sin confirmar, preferencia no excluyente) -- no se encontró ningún local comercial con las 8 cocheras obligatorias confirmadas en el texto.
- Se corrigió durante el filtro un falso positivo sistemático: la keyword "peatonal" venía matcheando frases como "tránsito vehicular y peatonal" (no calles peatonales reales) para el criterio "esquina obligatoria salvo peatonales" de Interior del País -- se ajustó a exigir la frase "calle/paseo/zona peatonal".
- Se excluyó 1 candidato de Terrenos con precio "USD 1" (dato mal parseado del sitio, no confiable).

### PENDIENTES.md aplicado hoy
- Sección 5 completa (38 candidatos sueltos con link real de días previos, 15-16/09): aplicados con `insert-cards.js` sobre el HTML de hoy; 17 ya habían sido encontrados de nuevo por la búsqueda de hoy y se dedupearon automáticamente por ID, 21 eran genuinamente nuevos y se cargaron. Sección borrada del archivo.
- Quedan pendientes (sin tocar esta corrida, decisión conservadora -- requieren cirugía estructural de HTML: botón de menú + tab-panel + bloque filters nuevos, no combinable con una corrida de búsqueda desatendida): 3 pestañas nuevas (Hazrat Namasté India, Laura Flores, Hamburguesas Extremas) y las 2 sub-pestañas de Sabores Express (Marca Nueva + calles/alturas). Ver `docs/cambios-clientes-17-09.md` para el detalle completo ya confirmado por Juan.
- Retención de 15 días (purga de contenido viejo desde 24/07): sigue pendiente, requiere script dedicado de parseo de fechas en español -- no se hizo esta corrida por alcance/tiempo.

### Publicación
Un solo commit + push al final de la corrida (adaptación local con git, ver `legacy-tareas/ADAPTACION-CLAUDE-CODE.md`). Hash del commit en el resumen final de la sesión.
