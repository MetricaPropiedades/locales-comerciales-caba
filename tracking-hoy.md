# Tracking - Locales Comerciales CABA (Parte 1 - Pool ALQUILER)
Fecha: 14/09/2026

## Cobertura
- URL: https://www.zonaprop.com.ar/locales-comerciales-alquiler-publicado-hace-menos-de-3-dias-orden-publicado-descendente.html
- Páginas leídas: 1 a 5 (hasta agotar la ventana hoy+ayer -- se llegó al corte de fecha, primer aviso "Publicado hace 2 días" detectado en página 5, ítem "Docta" href ...60139435; todo lo posterior a ese punto se descartó por estar fuera de ventana).
- ~140 avisos evaluados contra los 40 perfiles de ALQUILER activos en esta parte (se excluyó Sergio, Fliping, Terrenos, y los sub-casos depósito/galpón que cubre la Parte 1.5, según instrucción).
- Extracción hecha vía DOM (JS) para resolver href real de cada aviso antes de evaluar -- ningún candidato se cargó con href vacío.

## Candidatos nuevos genuinos
- **Julián Ciprés** (perfil #47): Suipacha al 500 (526, entre Tucumán y Lavalle), Centro/Microcentro, Capital Federal. 180 m² cubiertos (planta baja + subsuelo), $3.000.000. Gas/tiraje a 4 vientos no confirmado explícitamente en el aviso (preferencia, no excluyente). Link: https://www.zonaprop.com.ar/propiedades/clasificado/alcllcin-local-en-microcentro-60143383.html

## Descartes relevantes (misma dirección física ya cargada en corridas anteriores, solo con nuevo código de aviso -- NO se recargan, siguiendo la práctica ya establecida en el archivo)
- Florida al 300 (Microcentro) -- ya cargado en Julián Ciprés.
- Av. Córdoba al 2400 y Av. Callao 2093 (Recoleta) -- ya cargados en Café Martínez.
- Santa Fe al 4500 (Palermo) y Av. Rivadavia 10001 (Villa Luro) -- ya cargados en Adidas.
- José María Moreno al 100 (Caballito) y Av. Forest al 500 (Chacarita) -- ya cargados en Thermomix.
- El Salvador 4406, Cabrera 5100/Thames, Uriarte 1300, El Salvador 5700 (todos Palermo Soho, esquina) -- ya cargados en AMBA.
Resto del pool (~125 avisos): evaluado contra criterios obligatorios de los 40 perfiles (m², zona, tipo de operación) -- sin matches adicionales (mayoría fuera de rango de m² o fuera de zonas obligatorias, varios en Uruguay/otras provincias sin perfil aplicable).

## INCIDENTE TÉCNICO -- push del HTML principal pendiente
El archivo "Locales Comerciales CABA.html" (~695 KB) fue editado localmente en esta sesión (1 tarjeta nueva agregada a la pestaña Julián Ciprés, balance de divs verificado: 7132 abre / 7132 cierra) pero **no se pudo pushear a GitHub en esta corrida**: las herramientas de lectura de archivo disponibles en esta sesión tienen un límite de ~25.000 tokens por lectura (muy por debajo de los ~170.000 tokens que ocupa el archivo completo), y la herramienta de escritura a GitHub requiere el contenido completo como un único parámetro de texto. Reconstruir y reenviar ~700 KB de HTML a mano en esta sesión tenía alto riesgo de truncar o corromper el archivo canónico, así que se optó por NO arriesgar el archivo publicado y documentar el candidato acá en su lugar (siguiendo la regla de "documentar en vez de publicar" ante una falla de guardado).
**Acción pendiente para la próxima corrida (Parte 1.5 o Parte 2, o próxima Parte 1):** cargar manualmente la tarjeta de Julián Ciprés (Suipacha al 500, detalle arriba) en el HTML publicado, ya que sigue sin estar en la versión pública.

## Presupuesto
Corrida completada dentro de presupuesto de sesión, sin necesidad de corte anticipado por presupuesto.
