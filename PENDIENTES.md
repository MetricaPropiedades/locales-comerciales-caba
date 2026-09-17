# PENDIENTES para aplicar en "Locales Comerciales CABA.html" apenas ande el sandbox

Última actualización: 17/09/2026. Este archivo vive en GitHub (no depende del sandbox roto), así que sobrevive aunque cambie de sesión. No hace falta que Juan repita nada de esto — apenas el sandbox de bash funcione, se aplica todo de una.

## 0) FIX APLICADO (17/09): cobertura de Parte 1 del 16/09 fue de solo 10% por una causa distinta al sandbox

Se corrigió el SKILL.md de `locales-comerciales-caba-diario`: antes intentaba traer/reconstruir el HTML de 700KB AL PRINCIPIO de la sesión, y al fallar el sandbox gastaba casi todo el presupuesto en reintentos, dejando muy poco para buscar. Ahora el orden es: buscar TODO primero (no depende del sandbox), y recién al final intentar tocar el HTML. Esto no vuelve a pasar de nuevo.

## 1) Ediciones de texto pendientes — APLICADAS el 17/09 (Parte 1, corrida de fin de semana)

Las 3 ediciones de texto (nota de brokers en Rappi, "8 cocheras" en OSDE Ambulancias, City Bell + Av. 8/12 en Simplicity) y el rename Valeria→Romina se aplicaron hoy directo sobre "Locales Comerciales CABA.html" con Edit + verificación de balance de divs. Ya no están pendientes.

## 2) Pestañas nuevas pendientes (3) — sin crear todavía

Nota (17/09): no se crearon esta corrida por ser cirugía estructural más grande (botón + tab-panel + bloque filters) sobre un HTML de 700KB+, mientras esta misma corrida ya estaba cargando ~180 tarjetas nuevas en 27 pestañas existentes — se prefirió no combinar ambos riesgos en una sola sesión desatendida. Quedan listas para crear en una corrida dedicada.

1. **Nueva pestaña — Hazrat Namasté India (Restaurante)**:
   - Local comercial en alquiler
   - 120 a 200 m² en planta baja
   - Zona: Calle Defensa (CABA), entre altura 800 y 1200
3. **Nueva pestaña — Laura Flores**:
   - Departamento en venta, 3 o 4 ambientes, sin cochera, con balcón, sin amenities
   - Nota: expensas bajas
   - Zona: Almagro — polígono entre Av. Rivadavia (3500-4500), Av. Medrano (0-1000), Av. La Plata (0-1000) y Av. Independencia (asumido 3500-4500 por ser paralela a Rivadavia, sin confirmar con Laura), + calles paralelas, aprox. 2-3 cuadras alrededor del perímetro. Prioridad: cerca de Rivadavia, Medrano y La Plata.
4. **Nueva pestaña — Hamburguesas Extremas** — LISTA COMPLETA, CONFIRMADA POR JUAN, LISTA PARA CARGAR:
   - Local comercial en alquiler, 100 a 150 m²
   - Mismo criterio que Sabores Express: sobre la calle de la PRIMERA columna, NO es polígono, son cuadras sobre esa calle cruzando/tocando la calle de la SEGUNDA columna. Juan aclaró (16/09): en general son 4 cuadras, pero varía según la esquina — usar el rango de altura exacto de la tabla de abajo en cada caso.
   - Guardar esta lista completa en la pestaña (visible) y en el SKILL.md de la tarea de búsqueda, para que la skill compare cada aviso contra estas calles+alturas y sume el candidato si coincide.
   - **Alturas confirmadas por Juan el 16/09 (9 esquinas):**

   | Calle (buscar local sobre esta) | Altura | Localidad |
   |---|---|---|
   | Alvear | 0-200 | Martínez |
   | Yrigoyen | 0-200 | Martínez |
   | Av. Cazón | 1300-1600 | Tigre |
   | Yrigoyen | 1700-2100 | José C. Paz |
   | Av. Constitución | 0-200 | Savio |
   | Av. Alvear | 2700-3100 | Benavídez |
   | Av. Villanueva | 1400-1700 | Maschwitz |
   | Av. Ing. Agustín Roca | 0-300 | Campana |
   | Av. Ing. Eduardo Madero | 1200-1600 | Del Viso |

## 3) Sabores Express — SON DOS PESTAÑAS DISTINTAS, no confundir

### 3.1) "Marca Nueva Sabores Express" — lista para cargar tal cual
- Local comercial en alquiler, 160 a 250 m² (preferencia: 160 m² en PB)
- Zonas: Saavedra, Núñez, Belgrano, Caballito

### 3.2) "Sabores Express" — perfil de esquinas con altura, 35-60 m² (típico 45 m²) — LISTA COMPLETA, CONFIRMADA POR JUAN, LISTA PARA CARGAR
Local comercial en alquiler. Es sobre la calle de la PRIMERA columna (no polígono), en rango de 3 cuadras (300 números) que toquen/crucen con la calle de la SEGUNDA columna. Excluidas 2 filas marcadas "Firmado" en la foto de Juan; incluida la fila "Campana - Negociando". Total: 14 esquinas (confirmado por Juan el 16/09, no falta ninguna).

| Calle (buscar local sobre esta) | Altura | Localidad |
|---|---|---|
| Av. Maipú | 1300-1700 | Florida |
| Av. San Martín | 2100-2500 | Florida |
| Roca | 500-900 | Vicente López |
| Mitre | 3600-4000 | San Martín |
| Alvear | 2600-2900 | Villa Ballester |
| Altube | 1700-2100 | José C. Paz |
| Av. Perón | 2900-3400 | Victoria |
| Eva Perón | 500-900 | Derqui |
| Rivadavia | 500-900 | Pilar |
| Vélez Sarsfield | 4500-5000 | Munro |
| Independencia | 2700-3000 | Carapachay |
| Juan B. Justo | 0-200 | Beccar |
| Ayacucho | 0-100 | Beccar |
| Laprida | 4000-4400 | Villa Martelli |

## 4) Retención de contenido — purga pendiente

- Política definitiva: **15 días de retención** (se descartaron 7 y 30 días).
- Hay contenido viejo sin purgar desde el 24 de julio en adelante. Cuando ande el sandbox: borrar todas las day-sections de todas las pestañas con fecha anterior a 15 días desde hoy.

## 5) Candidatos sin cargar al HTML — TODOS APLICADOS el 17/09 (corrida unificada Claude Code, insert-cards.js con dedup por ID)

(Sergio y Terrenos dieron 0 candidatos reales el 16/09, revisado a fondo.)

## 6) Otros pendientes viejos (de la lista de tareas, sin urgencia confirmada)
- Armar archivo de referencia Havanna (sucursales CABA/AMBA).
- Definir avenidas+alturas concretas para OSDE San Martín y Barracas.
- Re-chequear cobertura completa de páginas 1-13 del 15/09 contra los 48 perfiles (las tareas parche solo compararon contra un subconjunto).

---
Cuando se aplique cualquiera de estos puntos, borrarlo de este archivo (o tacharlo) para que no se vuelva a aplicar dos veces.
