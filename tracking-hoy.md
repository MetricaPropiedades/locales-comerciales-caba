# Tracking diario -- Corrida unificada (Parte 1 + 1.5 + 2)

## Viernes 18 de septiembre de 2026 (corrida desatendida vía Claude Code, git+node, ver `legacy-tareas/ADAPTACION-CLAUDE-CODE.md`)

### PARTE 1 -- Alquiler nacional de locales comerciales
- Nacional: `páginas=9 avisos_vistos=270 devueltos=243 corte="HTTP 403 en pág 10 tras reintentos"` -> se dividió por zona:
  - capital-federal: `páginas=4 avisos_vistos=104 devueltos=80 corte="última página"`
  - gba-norte: `páginas=2 avisos_vistos=38 devueltos=36` · gba-sur: `páginas=2 avisos_vistos=50 devueltos=40` · gba-oeste: `páginas=1 avisos_vistos=27 devueltos=24`
  - cordoba: `páginas=1 avisos_vistos=20 devueltos=20` · santa-fe: `páginas=1 avisos_vistos=21 devueltos=17` · costa-atlantica: `páginas=1 avisos_vistos=14 devueltos=12` (todas "última página")
- Provincias chicas no desagregadas (Mendoza, Neuquén, etc.) solo cubiertas por lo que entra en las primeras 9 páginas del nacional.

### PARTE 1.5 -- Depósitos
- `depositos-alquiler-...2-dias`: `páginas=3 avisos_vistos=87 devueltos=86 corte="última página"`. Galpones: sin categoría propia (mezclados en depósitos). Sin candidatos: Agustín Ali, Cetrogar, Bazar Freddy; Rappi/Chapa/Pedidos Ya sí (ver abajo).

### PARTE 2 -- Venta y perfiles residenciales
- Venta locales nacional: `páginas=9 avisos_vistos=257 devueltos=245 corte="última página"` (cobertura completa).
- Deptos 8 barrios 2 amb (Fliping/Romina): `páginas=8 vistos=238 devueltos=228` · 3 amb (Fliping/Sergio): `páginas=9 vistos=245 devueltos=240`
- Caballito 3 amb: `páginas=2 vistos=43` · Palermo 4 amb (Sergio): `páginas=3 vistos=83` · Almagro 3 amb: `páginas=2 vistos=33` · Almagro 4 amb: `páginas=1 vistos=18` (Laura Flores)
- Terrenos CABA: `páginas=4 vistos=99` · Padel PRO (Malvinas Argentinas): `páginas=1 vistos=5` (todas "última página")

### Candidatos cargados hoy (160 tarjetas en 30 pestañas)
Romina 30 · Fliping 14 · Bostani 13 · Changomas 10 · Adidas 10 · Multibazar/City Moda 8 · AMBA 5 · Interior 7 · Chapa y Pintura 6 · Simplicity 6 · Rappi 5 · Tostado Flagship 5 · Laura Flores 5 · AMBA +800 4 · Guitarrita 4 · Café Martínez 3 · Pedidos Ya 2026 3 · Carrefour 2 · Havanna 2 · Big Pons 2 · Hunterville 2 · OSDE Nordelta/Belgrano 2 · Tostado Café Club 2 · Smartfit 2 · Julián Ciprés 2 · Marca Nueva Sabores 2 · Thermomix 1 · ICBC 1 · Tostado Fast Casual 1 · Sergio 1.
Sin candidatos hoy: Freddo, Pet Shop, OSDE Núñez/Flores/Olivos/Lanús/San Martín-Barracas/Ambulancias (ningún aviso con 8 cocheras), Open Pharma, Cetrogar, Puppis, Nikki, Havaiana, KFC, Chery, Adidas Factory, Agustín Ali, Bazar Freddy, Hazrat, Sabores Express, Hamburguesas Extremas, Caballito Sur, Terrenos (ninguno <= USD 250k; el de "USD 1" es dato erróneo), Padel PRO (ninguno de 2.000-10.000 m²).

### Criterios aplicados / descartes dudosos
- AMBA +800, Adidas, Smartfit, Multibazar: solo locales comerciales (los depósitos solo se evaluaron para los 5 perfiles que los aceptan + Cetrogar/Ambulancias). Zárate excluido de AMBA.
- Av. Santa Fe 1900 (900 m²) es un mismo aviso publicado en 3 barrios (60181034/60180701/60180700): se cargó solo 60181034.
- Carrefour: descartados por cercanía a sucursal de la lista (Santa Fe 1600, Esmeralda 500, Gurruchaga 900, Guardia Vieja 4000, Miró 100); cargados Ramírez de Velasco 1500 y Las Cañitas -> confirmar a mano. Havanna: sin archivo de referencia, confirmar a mano.
- KFC: Fleming 1292 (San Isidro) descartado, no está sobre Centenario/Belgrano/Cosme Beccar.
- Caballito Sur: Hortiguera 500 (60182329) descartado, la cochera es "optativa".
- Tostado Fast Casual/Flagship: solo con palabra clave de ubicación. Laura Flores: polígono Almagro aproximado por calles (Rivadavia/Mitre/Yrigoyen/Belgrano 3500-4500, Medrano/La Plata 0-1000); expensas bajas solo informativo.
- Interior: descartados Santa Fe 1200 Rosario (a metros de la esquina) y locales sin esquina/peatonal. Bostani: descartados Villa Allende, San Rafael, Plottier, MdP USD 320.000 (precio dudoso).
- Retención de 15 días: sigue pendiente (requiere script de parseo de fechas).
