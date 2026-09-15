# Tracking - Locales Comerciales CABA (Parte 1.5 - Pool DEPÓSITOS/GALPONES)
Fecha: 15/09/2026

## Cobertura
- Pool Depósitos: https://www.zonaprop.com.ar/depositos-alquiler-publicado-hace-menos-de-3-dias-orden-publicado-descendente.html — FUNCIONÓ correctamente, título confirmado "72 Depósitos más recientes publicado hace menos de 3 dias en alquiler en Argentina".
- Páginas leídas: 1, 2 y 3. Se frenó en los avisos "Publicado hace 2 días" de la página 2 (últimos incluidos en la evaluación); página 3 arrancaba directo en "Publicado hace 3 días", por lo que quedó fuera de ventana y no se seguyó leyendo.
- Total evaluados dentro de ventana (hoy + ayer + hace 2 días): ~45 avisos, contra los 5 perfiles de esta tarea (Taller Chapa y Pintura, Rappi, Bazar Freddy, Agustín Ali, Pedidos Ya 2026) + bonus Cetrogar.
- Pool Galpones: probado https://www.zonaprop.com.ar/galpones-alquiler-publicado-hace-menos-de-3-dias-orden-publicado-descendente.html y también https://www.zonaprop.com.ar/galpones-alquiler.html — AMBAS URLs dan Error 404. Confirmado: ZonaProp NO tiene una categoría/URL separada para "Galpones"; los galpones aparecen mezclados dentro del pool de Depósitos (muchos avisos del pool de Depósitos se autodescriben como "galpón"). No se perdió tiempo adicional en esto.

## Candidatos nuevos encontrados
Ninguno. Se revisaron todos los avisos dentro de la ventana de fecha contra los 5 perfiles + bonus:
- **Taller Chapa y Pintura** (Vicente López, Martínez, San Isidro, Tigre, San Fernando, Benavídez; 150-400 m²): los únicos avisos en zonas correctas (Ombu 1200, Florida, Vicente López — 500 m²; Roberto Laplace 3100, Don Torcuato, Tigre — 450 m²) superan el rango de m² permitido.
- **Rappi** (zonas actualizadas 10/09: Adrogué, Villa Ballester, San Justo/La Matanza, Caseros, Villa Madero, San Fernando, Colegiales, Floresta, Barrio Norte, Almagro, Chacarita, Once, Avellaneda, Quilmes, Ituzaingó; 300-600 m²): ningún aviso dentro de la ventana cae en esas zonas con el m² requerido (los de Floresta e Ituzaingó vistos eran de 100-160 m², muy por debajo del rango).
- **Bazar Freddy** (Bella Vista/San Miguel, Chascomús; 900-2.000 m²): sin avisos en esas zonas dentro de la ventana.
- **Agustín Ali** (San Isidro, Villa Adelina; 200-400 m² obligatorio): el único aviso en Villa Adelina (Domingo de Acassuso 6600) ofrece desde 500 m² hasta 10.000 m², por debajo del piso mínimo no hay opción — no cumple el tope de 400 m².
- **Pedidos Ya 2026** (900-1.500 m² totales; múltiples zonas): ningún aviso dentro de la ventana cae en las zonas de la lista con ese rango de m².
- **Bonus Cetrogar** (Quilmes, Pacheco; 400-1.000 m²): el único aviso en Quilmes visto (USD 36.000, 6.000 m², Calle 144, Berazategui — no es Quilmes en sí) está fuera de rango de m² y de zona exacta.

## Método de búsqueda — qué funcionó y qué no
- URL de Depósitos con filtro de fecha: funcionó sin problemas, título y etiquetas de fecha visibles y correctos.
- URL de Galpones (con o sin filtro de fecha): 404 en ambos casos — no existe esa categoría separada en ZonaProp, confirmado nuevamente.

## Presupuesto
Corrida completada dentro de presupuesto, sin necesidad de corte anticipado. No hubo candidatos para cargar, por lo que no se tocó "Locales Comerciales CABA.html" ni se hizo push de ese archivo en esta corrida (solo se actualiza este tracking).
