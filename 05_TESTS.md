# TESTS — Registro de validación (v2.0)

**Última actualización: 2026-11-23 (versión 2.0 candidata).** Este archivo distingue lo EJECUTADO de lo PENDIENTE. Nada se marca como superado si no se completó. Debajo (sección «HISTORIAL») se conservan íntegros los registros de las versiones 1.0 a 1.1.1.

## 1. Veredicto honesto de esta ronda
- **¿Utilizable por un alumno como versión de PRUEBA?** Sí, con aviso de que es candidata y de que no se ha probado en otras IA.
- **¿Validada para publicarla como recurso FINAL?** **No.** Faltan las pruebas en sesiones nuevas de ChatGPT, Gemini, Perplexity y Claude (ver §6). Las pruebas A-G se ejecutaron solo en el entorno local de Claude (navegador integrado), por el mismo modelo que escribió el prompt: no son ciegas ni independientes.

## 2. Resultado de cada prueba
| Prueba | Qué se hizo realmente | Resultado |
|---|---|---|
| **A · Principiante** | Etapas 0-4 completas con datos reales de YouTube (7 candidatos, 3 finalistas, 17 canales analizados con N=20, matriz, informe principal con 10 ideas y bloque de continuidad). Detalle: `_pruebas_v2.0/A_resultado_etapas_1-4.md` | **EJECUTADA, sin fallos bloqueantes del método.** Resultado: recomendación PROVISIONAL (estado SUFICIENTE, confianza Media-Baja, empate técnico desempatado por producción). Limitación: sin Trends ni monetización verificada; ejecutor no independiente |
| **B · Internacional** | Etapa 0-1 (6 candidatos en inglés) y Etapa 2 de 1 de 3 finalistas (12 canales). Detalle: `_pruebas_v2.0/B_C_D_G_resultados.md` | **PARCIAL.** Se adaptaron umbral (mercado grande) y se detectaron canales de otro idioma y muestras reducidas; faltan Etapa 2 de los otros 2 finalistas y Etapas 3-4. YouTube devolvió resultados mezclados de idioma pese a `hl=en&gl=US` |
| **C · Nicho elegido (retro)** | Etapas 0-3 sobre el tema + 4 vecinos y 7 canales (N hasta 20) | **EJECUTADA parcialmente (sin Etapa 4).** El prompt analizó viabilidad sin obligar a abandonar el tema: viable de forma PROVISIONAL (61,0); subtemas débiles quedan «no confirmados». Falta Etapa 4 |
| **D · Sin internet** | **Simulación** del modo guiado (texto) + script que verifica que no hay enlaces, @handles ni cifras | **Simulación superada (6/6 comprobaciones).** No equivale a probar una IA sin navegación: el modelo sí tenía internet |
| **E · Continuidad** | La Etapa 2 de A se ejecutó partiendo del bloque de la Etapa 1; verificación estructural del bloque (14 campos presentes, 274 palabras, sin datos personales, suficiente para retomar) | **PARCIAL.** Ejecutada en la MISMA conversación: no se aisló el contexto. Falta probar pegando el bloque en una sesión nueva |
| **F · Respuesta larga** | Medición del informe principal (841 palabras, anexos aparte «a petición») y regla de punto limpio + bloque | **Verificación de DISEÑO, no ejecutada con un corte real.** Falta comprobar cómo se comporta cada IA al llegar a su límite |
| **G · Datos faltantes** | Casos reales: una página de canal sin videos con vistas, una consulta con 0 resultados, lecturas intermitentes fallidas; aplicación de la cadena de fuentes y reducción de confianza | **EJECUTADA con casos reales.** Función de respaldo comprobada: lista sesgada no usada para medianas, canal «NO CONFIRMABLE», segunda consulta en vez de descartar. No se probó un bloqueo real impuesto por YouTube |
| **Pruebas externas** (ChatGPT, Gemini, Perplexity, Claude en sesión nueva) | **No realizadas** | **PENDIENTE** |

## 3. Criterios de aprobación (14 del encargo) — estado honesto
| # | Criterio | Estado |
|---|---|---|
| 1 | Un principiante entiende cómo usarlo | Guía de 3 min redactada; **no probado con un alumno real** |
| 2 | Las fases son ejecutables | Cumplido en el entorno local (A, C) |
| 3 | La continuación entre etapas funciona | **Parcial** (misma conversación) |
| 4 | No inventa estadísticas cuando faltan datos | Cumplido en pruebas G y D (simulada) |
| 5 | Fuentes comprobables | Enlaces/handles públicos de YouTube en las tablas; sin verificación independiente |
| 6 | Puntuaciones justificadas | Cumplido: anclas, confianza y cálculo |
| 7 | La investigación se detiene honestamente si falta evidencia | **Parcial** (se vio en G; falta caso extremo en otra IA) |
| 8 | El informe final es útil | Formato y contenido adecuados; **utilidad real no evaluada por alumnos** |
| 9 | Sin herramientas de pago obligatorias | Cumplido |
| 10 | Pruebas críticas ejecutadas sin fallos bloqueantes | Sin fallos bloqueantes del método; sí fallos de acceso intermitentes (ver §4) |

## 4. Problemas detectados y correcciones (Ronda v2.0)
| Problema | Dónde se vio | Corrección |
|---|---|---|
| Exceso de trabajo en un solo mensaje (v1.1.1) | Prueba real en ChatGPT reportada por el equipo | Arquitectura por etapas + continuidad + techos flexibles (no obligaciones) + estados de investigación |
| La lista de resultados está sesgada a videos populares y no sirve para medianas | Prueba G | Regla explícita en el prompt y la metodología |
| Resultados de idioma/región mezclados pese a `hl`/`gl` | Prueba B | El prompt exige declarar región y comprobar el idioma de cada canal |
| «Segunda fuente» de demanda ambigua | Prueba A (sin Trends) | Se define: Trends, otra búsqueda distinta o vistas recientes de varios canales en sus páginas |
| Empate técnico entre finalistas (62,5 / 62,0 / 60,5) | Prueba A | Regla de empate (<5 puntos) con desempate por producción/afinidad |
| Medianas inflan «veces» cuando el canal es muy pequeño | Prueba A | Cautela en el informe; el patrón exige muestra suficiente |
| Lecturas intermitentes («Failed to fetch») y bloqueo de scripts con el panel oculto | Pruebas A-C | Reintento espaciado; panel visible; datos faltantes marcados. **No se eludió ningún límite** |
| Mi script de verificación usó un vector de nota equivocado (58,0) | Verificación local | Error del script, no del texto; corregido y repetido |

## 5. Verificaciones locales de consistencia (EJECUTADAS)
Script reutilizable: `_pruebas_v2.0/verificacion_local.py`. **63 comprobaciones, 63 correctas** (tras corregir el vector del script). Comprueba: 6 archivos y copias de seguridad; bloque copiable sin menciones a plataformas ni a herramientas de pago; regla de no pegar claves; pesos 100 % e iguales (prompt, metodología, 06); etapas, estados y condiciones de finalización; techos no obligatorios; empate técnico; no trabajo en segundo plano; mecanismo `continuar`; campos del bloque de continuidad; métricas y umbrales idénticos en prompt, metodología, guía y 06; público/privado; fechas por tipo de dato; lista sesgada; informe principal con 5 bloques; lenguaje sencillo; modo guiado; cálculos de matriz del ejemplo; separación real/ficticio; que no se declare compatibilidad no probada; referencias existentes; tamaño del prompt (24 703 caracteres).
**Qué NO prueban:** que una IA real siga bien el prompt, respete los techos, continúe sin perder datos o sea sencilla para un alumno.
**Nota:** el prompt creció (de ~21 700 a ~24 700 caracteres) al añadir etapas y continuidad; es una limitación a vigilar en IA con ventanas pequeñas.

## 6. Protocolo breve para las pruebas externas (pendiente)
Para cada IA (ChatGPT con búsqueda, Gemini, Perplexity, Claude en sesión NUEVA):
1. Pega el prompt tal cual (sin rellenar datos) y responde «por defecto». Anota si hace más de 1 pregunta.
2. Comprueba que entrega el resumen de la Etapa 1 con 6-8 candidatos, 3 finalistas, estado y el **bloque de continuidad**. Anota nº de consultas y si se corta.
3. Escribe `continuar`. Comprueba que NO repite el perfil ni búsquedas y que declara el estado (COMPLETA/SUFICIENTE/INCOMPLETA/BLOQUEADA) de cada finalista.
4. Escribe `continuar`. Comprueba que el informe empieza por los 5 bloques, usa lenguaje sencillo y no declara ganador si hay estado INCOMPLETA/BLOQUEADA.
5. Abre 5 enlaces al azar: ¿existen? ¿coinciden las vistas con la fecha de consulta? Anota cuántos fallan (cualquier enlace inexistente = fallo bloqueante).
6. Busca datos privados presentados como públicos (CTR, retención, ingresos de otros canales) y ganancias afirmadas: debe haber 0.
7. Repite con un perfil en inglés y con un tema elegido (ej. historia de videojuegos retro).
8. Prueba de continuidad real: abre una conversación nueva, pega `06_CONTINUAR_INVESTIGACION.md` Opción B + el bloque de la Etapa 1 y comprueba que retoma la Etapa 2.
9. Sin búsqueda web (desactívala): debe responder con modo guiado sin inventar canales.
Registra: IA, fecha, versión, nº de mensajes, consultas aproximadas, fallos, enlaces falsos (0 esperado), veredicto. Una IA solo se declara compatible tras pasar esto.

## 7. Limitaciones pendientes
- Sin pruebas externas; ejecutor no independiente (mismo modelo del prompt).
- Sin Google Trends ni datos de monetización verificados; requisitos del Programa de socios confirmados solo vía resultados de búsqueda.
- Acceso a YouTube mediante lectura de páginas públicas con intermitencias; los resultados dependen de la región (Argentina).
- Cifras de vistas redondeadas; medianas con la primera página de cada canal (~30 videos) y sin distinguir duración dentro de la pestaña Videos.
- Prompt más largo que la v1.1.1 (riesgo en IA con contexto pequeño).
- No evaluada la comprensión por alumnos reales.

---

# HISTORIAL (v1.0 a v1.1.1, conservado)

**Última actualización: 2026-11-23 (Ronda 4, versión candidata v1.1.1).** Este archivo distingue lo EJECUTADO de lo PENDIENTE. Nada se marca como superado si no se completó.

## 0. Nota sobre la integridad de los archivos
Al iniciar la Ronda 3, la carpeta `01_Investigador_Nichos_Ganadores` **ya no existía** en disco (no se encontró en el perfil del usuario; probablemente fue movida o eliminada fuera de esta sesión). Se **recrearon los cinco archivos** en la misma ruta con la versión candidata v1.1, reconstruyendo el contenido de las rondas anteriores a partir del historial de la sesión y de dos copias de seguridad parciales. Si existe una copia movida de las versiones 1.0, conviene compararla con estas.

## 1. Resumen de estado
| Prueba | Estado | Qué se hizo | Bloqueo / pendiente |
|---|---|---|---|
| A. Principiante (ES, faceless) | **PARCIAL** | Rondas 1-2: 5 candidatos con datos reales de YouTube, matriz y 10 ideas preliminares; resultado «no concluyente» | Fase B no completada; sin canales pequeños con patrón en español; sin Trends; sin monetización; medido con el procedimiento anterior (ver §3) |
| B. Internacional (EN, videos largos) | **PARCIAL** | Rondas 2: 3 búsquedas en inglés + 2 canales; caso real de patrón repetido (Hallways Of Time) | Sin matriz completa, finalistas ni 10 ideas; región de consulta Argentina |
| C. Nicho específico (historia de videojuegos retro) | **PARCIAL** | 1 búsqueda con 12 resultados reales; demanda en ≥5 canales | Análisis del hueco incompleto: la página del canal no cargó (panel oculto, tiempo agotado) |
| Ejecución completa del prompt v1.1.1 en sesión nueva (Claude, ChatGPT, Gemini, Perplexity…) | **PENDIENTE** | — | Es el siguiente paso de validación. No se probó en ninguna IA distinta ni de forma «ciega» |

## 2. Cambios de la versión candidata v1.1 (respuesta a la revisión)
1. **Dos fases:** A (6-8 candidatos, ~3 consultas por candidato, 3 finalistas) y B (validación profunda de 3, 10-15 consultas por finalista). Se mantiene cada comprobación importante; se reducen búsquedas redundantes.
2. **Métricas unificadas M1-M6:** una sola ventana estándar (20 videos largos / 30 Shorts, ≥14/7 días, ≤12 meses), mediana documentada y excluyendo el video evaluado, variante contemporánea, Shorts y largos separados, regla de edad.
3. **Umbrales contextuales:** tabla por tamaño de mercado (V ≈ 100 k / 30 k / 10 k) con ajustes por formato, tipo de contenido y edad; no se descartan nichos especializados por tener menos vistas.
4. **Experiencia del alumno:** si ya dio sus datos no se le vuelve a preguntar; una sola pregunta para lo que falte; resumen sencillo (nicho, por qué, riesgos, 3 pasos, confianza) y «no concluyente» con siguiente paso de validación.
5. **Ejemplo (03):** separación explícita entre datos reales (parte 1) y ficticios (parte 2), con avisos; se declara que la parte 1 usó un método anterior.
6. **Informe con secciones numeradas (1-11)** para no confundirlas con las Fases A/B.

## 3. Consistencia con las mediciones anteriores
Las cifras reales de las rondas 1-2 (p. ej. Hallways Of Time, Detrás del Enigma) se calcularon con **todos los videos visibles** del canal, no con la ventana estándar de 20 videos de la v1.1. Son datos reales de esa fecha, pero **no son comparables** con lo que produciría el prompt v1.1. Se conservan como evidencia ilustrativa y se marcan así en el ejemplo.

## 4. Verificaciones locales de consistencia (EJECUTADAS)
**Ronda 3 (v1.1, 2026-11-23):** 46 comprobaciones, 0 fallas (pesos, métricas/umbrales coincidentes, estructura del prompt, cálculos del ejemplo, separación real/ficticio, estado de pruebas).
**Ronda 4 (v1.1.1, 2026-11-23):** 55 comprobaciones, incluyendo las anteriores más las nuevas reglas. Resultado automático: 53 correctas y 2 marcadas por el script. Revisión manual de las 2: ambas son **falsos positivos del script**, no del texto: (1) el prompt dice «no tienes su CTR ni su retención» (negación correcta, el script buscaba otra palabra); (2) el archivo dice «no marca ninguna prueba como superada» (el script detectó la palabra «superada»). No se ocultó ninguna falla real.
Comprobado en la Ronda 4: copia de seguridad de los 5 archivos; pesos 100 % e idénticos; misma regla de antigüedad (14 días largos / 7 días Shorts) y mismas reglas de muestra (N ≥15, 8-14, <8) en prompt, metodología y guía; sin «retención visible» como dato público; CTR solo en contexto propio o privado; fechas por tipo de dato; estructura de dos fases y M1-M6 intactas; cálculos del ejemplo (57,5 / 51,5 / 50,5 / 49,0 / 35,0 y 66,5).
**Qué NO prueban:** que una IA real siga bien el prompt, que respete límites de búsqueda ni que los resultados sean correctos. Eso exige la ejecución completa pendiente.

## 4b. Correcciones puntuales v1.1.1 (Ronda 4)
Detalle exacto, con líneas antes/después, en `_backups/REGISTRO_DE_CAMBIOS_v1.1.1.md`. Copia previa: `_backups/v1.1_2026-11-23/`.
1. **Públicos vs privados:** nueva regla 10 en el prompt; CTR, retención, fuentes de tráfico, demografía, RPM e ingresos reales de canales ajenos no se presentan como públicos (estimación con fuente o no disponible). CTR y retención solo en los videos propios del alumno (experimento). Se quitó «retención visible» de los criterios de interacción. Mismas reglas en metodología (sección 9b), guía y ejemplo.
2. **Antigüedad mínima unificada:** videos largos 14 días, Shorts 7 días, también en la definición de «inmaduro» (M5); misma redacción en prompt, metodología y guía.
3. **Muestra tras excluir el video evaluado:** N se cuenta después de la exclusión; N ≥15 normal; 8-14 «muestra reducida» (confianza máx. Media); <8 «muestra insuficiente» (estimación, confianza Baja, outlier/patrón solo «posible»); no se rellena con videos fuera de criterio sin avisar; ampliar la ventana se declara y baja la confianza un nivel. M4 solo declara outlier/patrón con muestra suficiente.
4. **Fechas por métrica:** vistas de un video = fecha de publicación + fecha de consulta; suscriptores y datos del canal = solo fecha de consulta. Corregido en prompt (regla 3, tabla de evidencias, control de calidad) y metodología (principio 4, M6).
5. Pesos, funciones principales y estructura de dos fases: **sin cambios**. Solo se subió la etiqueta de versión a 1.1.1.

## 5. Registro de la Ronda 2 (conservado)
### Datos reales verificados (23-11-2026, consulta desde Argentina)
**A (español).** «datos curiosos» (vistas + este año): XpressTV 7,1 M; Homosapiens 1,2 M; CuriosaMente 1,1 M; Ver-Para-Creer 537 k y 391 k; El Escocés Gamer 520 k; Vida Geográfica 345 k. «misterios sin resolver explicados»: MundoCreepy 1,3 M / 1,1 M / 981 k / 774 k; Esto No Lo Sabías 1,3 M; Penguinator 979 k. Documentales: Dieck Docs 7-14 M (domina los 10 primeros). Detrás del Enigma: 597 k suscriptores, 51 videos, mediana ≈1,4 M, máximo 6,6 M. «origen de objetos cotidianos»: 5,8 k / 2,7 k / 1,6 k (una sola búsqueda). Historias Curiosas Narradas: 89,7 k suscriptores, 677 videos, último video 174 vistas. Búsqueda de canales «curiosidades historia narrada»: mayoría con 1-202 suscriptores (clones).
**B (inglés).** Hallways Of Time (youtube.com/@HallwaysOfTimeYT): 30,8 k suscriptores, 94 videos, mediana ≈22 k; mejores videos 536 k (≈24×), 393 k (≈18×), 335 k (≈15×), 313 k (≈14×) → patrón repetido (medido con todos los videos visibles). Búsqueda de canales «business documentary rise and fall»: líder Company Man (1,8 M) y una oleada de canales casi idénticos con 2-6 suscriptores; Highwater: 2 videos con 4 y 7 vistas (canal recién creado) → saturación por imitadores, no oportunidad. «forgotten history documentary narrated»: 247-337 k vistas en Hidden Truths y Brief Case; NatGeo e History dominan.
**C (español, retro).** Las Retro Aventuras 360 k; History Latinoamérica ≈210 k; Game Evolutions 176 k; Peter D Games 165 k; Rk Play 138 k (hace 3-9 meses).
### Fuentes alternativas probadas
| Fuente | Resultado |
|---|---|
| Búsqueda de YouTube (orden por vistas + este año) | Funciona: título, canal, vistas aprox., antigüedad |
| Búsqueda de canales de YouTube | Funciona: suscriptores en la lista |
| Página de canal `/@canal/videos` | Funciona con espera y scroll; falló una vez con el panel oculto |
| Página de video | Fecha de publicación sí; vistas no siempre |
| Google Trends | La página cargó; no se leyó la gráfica → [NO DISPONIBLE] |
| API de YouTube | No probada (requiere clave del alumno) |
| Nexlev (pago/límite) | Bloqueada por límite semanal; el prompt no depende de ella |
| Búsqueda web general | Solo políticas oficiales e hipótesis; las listas de nichos son blogs comerciales |
No se intentó eludir ningún límite ni bloqueo.
### Problemas detectados y corregidos en la Ronda 2
Falsa conclusión de baja demanda por una sola búsqueda → regla anti-conclusión precipitada; notas subjetivas → anclas de evidencia; ganador sin datos → regla de decisión; páginas de canal lentas → esperar/reintentar/alternativa; resultados según región → declarar región; videos duplicados al calcular medianas → «no contar dos veces»; clones y canales en caída → criterios de alerta; ejemplo solo ficticio → informe real parcial.
### Pendiente heredado
Ejecución ciega en otras IA; modo guiado sin internet; Fase 3/10 ideas en B y C; análisis de hueco en C; confirmar Programa de socios en la ayuda oficial; leer Google Trends.

---

# REGISTRO DE LA RONDA 1 (conservado)

## Alcance honesto
Las pruebas fueron **parciales**. Las ejecutó Claude (esta sesión) con WebSearch. **No** se ejecutó el prompt completo de extremo a extremo en ChatGPT, Gemini, Perplexity ni en otra sesión de Claude con navegación. La herramienta Nexlev (datos de canales) devolvió "límite semanal 50/50" y no se pudo usar.

## Pruebas realizadas (Fase 1 simulada: búsqueda de fuentes por escenario)
| Prueba | Búsqueda | Resultado | Hallazgo |
|---|---|---|---|
| A. Principiante, faceless en español | Canales faceless historia/curiosidades en español | Solo blogs de herramientas de IA, sin canales ni cifras verificables | Los blogs sugieren historia/curiosidades como accesible y advierten de riesgo de contenido genérico; **no sirven como prueba de demanda** |
| B. Internacional, videos largos en inglés | Documentales faceless largos, canales pequeños con "outliers" | Blogs de herramientas (OutlierKit, etc.); la métrica "razón vs rendimiento habitual" aparece como práctica común; RPM de un análisis comercial (mediana ~4,33 $) | Datos comerciales con interés de venta; confirma la necesidad de etiquetar fuente y de no tratarlos como ingresos reales |
| C. Tema concreto (historia de videojuegos retro) | Canales de documentales retro | Lista de canales nombrados (varios grandes; uno dejó de publicar) sin cifras actuales | Mostró la necesidad de comprobar **actividad reciente** y de analizar el hueco concreto |

Búsquedas oficiales confirmadas por resultados: política de contenido repetitivo/inauténtico (aclaración del 15-jul-2025), requisitos del Programa de socios, divulgación de contenido sintético y monetización de Shorts.

## Comprobaciones de diseño (por revisión)
| Criterio | Resultado |
|---|---|
| Preguntas iniciales razonables | OK (máx. 5, con valores por defecto) |
| Pesos suman 100 % | OK (20+15+15+15+10+10+10+5) |
| Cálculo del ejemplo | OK (66,5) |
| Diferencia datos/estimaciones | Definido en el prompt (marcas); no verificado con una IA real |
| Perfiles distintos | Prompt parametrizado; verificado solo por revisión |
| Próximos pasos concretos | Secciones I y J del formato |

## Problemas detectados y corregidos
1. Las búsquedas devuelven sobre todo blogs comerciales → se añadió **jerarquía de fuentes** (regla 8): los blogs solo generan hipótesis y bajan la confianza.
2. Canales nombrados en listas pueden estar inactivos (caso real de un canal retro que dejó de publicar) → se exige **comprobar actividad en los últimos ~60 días**.
3. En el caso de tema concreto faltaba enfocarse en el hueco → se añadió la pregunta explícita de **qué cubren los existentes y qué no**.

## Prueba real con navegador (ampliación, 2026-11-23)
Ejecutada por Claude en el navegador integrado, escenario A (tema "origen de objetos cotidianos", español), solo la parte de recopilación de datos de la Fase 1; no se generó el informe completo.
- Búsqueda en YouTube: se obtuvieron 10 resultados reales con título, canal, enlace, duración, vistas aproximadas y antigüedad. Los más vistos mostraban 5,8 K, 2,7 K y 1,6 K vistas (varios con 1 año o menos). Ejemplos: "No conocías el origen de estos 12 objetos cotidianos" (Los 12 Mas, 5,8 K, hace 1 año); "La Historia Oculta de 10 Objetos de tu Vida Diaria" (HistoriaLoca, 2,7 K, publicado 2026-10-09 según metadatos de la página del video).
- **Lectura**: la demanda visible en español para ese subnicho concreto es baja. El ejemplo ficticio del archivo 03 NO debe leerse como recomendación real; el método habría bajado la nota de Demanda. Es justo lo que el prompt debe detectar.
- Las páginas de canal (@HistoriaLoca2/videos) NO se renderizaron en este navegador (pantalla negra tras 14 s), así que no se obtuvieron suscriptores ni la mediana de vistas de los últimos 10 videos. La página del video cargó con anuncio y devolvió la fecha de publicación pero no las vistas.
- No se calculó la razón de rendimiento ni se verificaron suscriptores: **[NO DISPONIBLE]**.
- Corrección aplicada: se añadió al prompt un *fallback* de datos (usar lista de resultados y página del video, suscriptores como NO DISPONIBLE, vistas redondeadas aproximadas).
- Nexlev seguía sin utilizarse (límite semanal).

## Pendiente (no realizado)
- Ejecución completa del prompt en Claude con navegación, ChatGPT, Gemini y Perplexity.
- Medir si cada IA abre realmente las páginas de canales y entrega vistas con ambas fechas.
- Medir longitud de la respuesta y si se corta (probable en IA con límites de salida).
- Probar el modo guiado en una IA sin internet.
- Reconfirmar en la ayuda oficial las cifras del Programa de socios (solo vistas vía resultados de búsqueda).
- Reintentar los datos de canales con Nexlev cuando el límite se restablezca (hoy 21:29 UTC).
