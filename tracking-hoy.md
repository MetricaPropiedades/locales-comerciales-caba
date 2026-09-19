# Tracking diario -- Corrida unificada (Parte 1 + 1.5 + 2)

## Sábado 19 de septiembre de 2026 (corrida desatendida vía Claude Code, git+node)

### PARTE 1 -- Alquiler nacional de locales comerciales
- Nacional: `páginas=7 avisos_vistos=204 devueltos=175 corte="última página"` (cobertura completa, sin 403). Zonas de control (todas "última página"): capital-federal `p=3 vistos=61 dev=46` · gba-norte `p=2 vistos=33 dev=29` · gba-sur `p=1 vistos=26 dev=23` · gba-oeste `p=1 vistos=20 dev=19` · cordoba `p=1 vistos=12 dev=11` · santa-fe `p=1 vistos=15 dev=15` · costa-atlantica `p=1 vistos=10 dev=9`.

### PARTE 1.5 -- Depósitos
- `depositos-alquiler-...2-dias`: `páginas=3 avisos_vistos=68 devueltos=65 corte="última página"`. Galpones sin categoría propia.
- Cargados: Chapa y Pintura (Benavídez 370 m²), Pedidos Ya 2026 (Barracas Vieytes 1575, 900 m² tot.). Sin candidatos: Rappi, Bazar Freddy, Agustín Ali, Cetrogar, Ambulancias (depósito >=300 m² en Núñez/Palermo/V. Crespo/Belgrano: ninguno).

### PARTE 2 -- Venta y perfiles residenciales
- Venta locales nacional: `páginas=6 vistos=166 devueltos=156 "última página"`.
- Deptos 8 barrios 2 amb: `p=7 vistos=187 dev=163` · 3 amb: `p=6 vistos=176 dev=169` · Caballito 3 amb `p=1 v=23` · Palermo 4 amb `p=2 v=58` · Almagro 3 amb `p=1 v=18` · 4 amb `p=1 v=7` · Terrenos CABA `p=3 v=61` · Padel PRO (Malvinas Argentinas): `p=1 v=30`, 0 avisos en ventana de 2 días.

### Candidatos cargados hoy (98 tarjetas en 25 pestañas)
Bostani 13 · Romina 11 · Adidas 9 · Laura Flores 8 · Changomas 7 · Simplicity 7 · Tostado Flagship 7 · Multibazar 6 · Fliping 5 · Tostado Fast Casual 4 · AMBA 3 · Interior 3 · Carrefour 2 · Chery 2 · Freddo 1 · Havanna 1 · Tostado Café Club 1 · Café Martínez 1 · Big Pons 1 · Havaiana 1 · OSDE Ambulancias 1 · Chapa y Pintura 1 · Pedidos Ya 2026 1 · AMBA +800 1 · Terrenos 1.
Sin candidatos: Thermomix, Guitarrita, Pet Shop, Hunterville, OSDE Núñez/Flores/Olivos/Nordelta-Belgrano/Lanús/San Martín-Barracas, Open Pharma, Cetrogar, Puppis, Nikki, KFC, Adidas Factory, Smartfit, ICBC, Ciprés, Rappi, Bazar Freddy, Agustín Ali, Hazrat, Marca Nueva Sabores, Sabores Express, Hamburguesas Extremas, Sergio (ninguna dirección dentro del polígono), Caballito Sur (ninguno cumple lavadero+balcón+cochera+antigüedad<=25+<=USD 235k), Padel PRO.

### Criterios aplicados / descartes dudosos
- Tipo de cambio usado: 1 USD = $1.500. Filtro de m² sobre superficie cubierta; avisos sin m² cubiertos no se cargaron salvo aclaración.
- La Plata Av. 7 y 35 (60191448): cargado en Interior (La Plata no es AMBA estricto) y en Simplicity. Confirmar a mano.
- Carrefour: Cuenca 627 (Flores) y Sáenz Peña 200 (Congreso) cargados; confirmar a mano distancia a sucursales. Descartado Melincue 4600 (Hipermercado Villa Devoto, Varela 4750, muy cerca). Havanna: sin archivo de referencia, confirmar a mano.
- Hamburguesas Extremas: Cazón 1251 (Tigre) descartado, fuera del rango 1300-1600.
- Guatemala 500 (341 m²) es el mismo aviso en 4 barrios (60189566/60189536/60189531/60189522): se cargó solo 60189536.
- AMBA +800: descartados Castelar (m² cubiertos 1332 vs total 132, dato erróneo), Lanús Oeste 1100 m² y San Telmo Bolivar 400 (PB no confirmada).
- Fleming 1292 (San Isidro): descartado de KFC (no está sobre Centenario/Belgrano/Cosme Beccar), cargado solo en Adidas.
- Laura Flores: zona aproximada por barrio Almagro (no se verificó cada dirección contra el polígono); expensas <= $300.000 como corte práctico.
- Romina: descartados Guatemala 5840 (60186448, USD 150.000 justo, revisar) y Maure 1800 (precio "$ 1").
