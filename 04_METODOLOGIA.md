# METODOLOGÍA — versión 2.0 (candidata)

Este documento explica los criterios del prompt v2.0. **Debe coincidir con `01_PROMPT_PARA_ALUMNOS.md`**; si cambias uno, cambia el otro. El historial de la v1.1.1 está en `_backups/`.

## 1. Principios
1. Evidencia antes que opinión; cada dato lleva marca ([VERIFICADO], [ESTIMACIÓN], [OPINIÓN], [NO DISPONIBLE]).
2. Demanda y competencia se miden por separado: poca competencia ≠ alta demanda.
3. Un patrón repetido vale más que un caso aislado.
4. Fechas: en las vistas de un video, dos (publicación del video y consulta); en suscriptores y otros datos del canal, solo la fecha de consulta.
7. Datos públicos y privados se distinguen siempre (ver sección 9b).
5. Se prefiere un informe con huecos honestos a uno completo e inventado.
6. Los umbrales son referencias contextuales, no reglas universales.

## 2. Ejecución por etapas (v2.0)
Problema de la v1.1.1: pedía en un solo mensaje 6-8 nichos, 18-24 consultas iniciales, ~36 consultas de validación, medianas, matriz, ideas e informe. Muchas IA no completan tanto trabajo de forma fiable. Solución: **investigación progresiva y reanudable**, repartida en mensajes sucesivos sin perder el trabajo.
| Etapa | Contenido | Condición de finalización | Mensaje típico |
|---|---|---|---|
| 0 Perfil | Solo lo que falte; valores por defecto | Perfil o defectos fijados | 1.º |
| 1 Exploración | 6-8 candidatos, señales rápidas (sin medianas), nota preliminar, 3 finalistas | Señales suficientes para elegir 3 | 1.º |
| 2 Validación | Por finalista: 3-5 canales, medianas M1-M6 de 2-3 canales clave, saturación, huecos, producción, monetización, riesgos, experimento | Estado de cada finalista (ver §2b) | 2.º |
| 3 Comparación | Matriz de 8 criterios, anclas, decisión | Matriz con confianza | 3.º |
| 4 Informe | Resumen sencillo, tabla de finalistas, 10 ideas, plan, fuentes; anexos aparte | Informe principal entregado | 3.º |
Al terminar cada etapa se entrega un **bloque de continuidad** (formato fijo, sin datos personales, ~300-1.200 palabras) con perfil, nichos, finalistas, fuentes y datos verificados con fecha, puntuaciones provisionales, búsquedas hechas, datos faltantes y siguiente tarea. El alumno solo escribe `continuar`; en una conversación nueva usa `06_CONTINUAR_INVESTIGACION.md`. La IA no trabaja en segundo plano y no repite lo ya verificado.

### 2b. Estados de la investigación
- **COMPLETA:** comprobaciones de la etapa con muestra suficiente (≥3 canales con N ≥15 y ≥2 fuentes de demanda).
- **SUFICIENTE (provisional):** ≥2 canales con mediana válida (N ≥8), demanda en ≥1 fuente fiable y comprobación básica de saturación. Permite una recomendación PROVISIONAL.
- **INCOMPLETA:** faltan datos clave; solo hipótesis preliminar.
- **BLOQUEADA:** sin acceso a fuentes; se piden datos al alumno o modo guiado.

### 2c. Presupuesto flexible
«Investigar hasta reunir evidencia suficiente, no hasta alcanzar un número de consultas.» Los techos (~20-24 consultas en la Etapa 1; ~12 por finalista en la Etapa 2) son límites razonables, no obligaciones. La búsqueda se detiene si dos consultas seguidas no aportan datos nuevos, si se alcanza el estado SUFICIENTE o COMPLETA, o si una fuente alternativa también falla. Sin evidencia suficiente la IA lo explica y dice qué falta.

## 3. Métricas unificadas (M1-M6)
- **M1 Formato.** Shorts (verticales ≤3 min) y videos largos se miden por separado. Se excluyen directos, estrenos recientes y trailers.
- **M2 Rendimiento habitual = mediana de vistas** (no el promedio, que lo distorsionan los outliers). Ventana estándar: **últimos 20 videos del mismo formato** (30 en Shorts), con ≥14 días de antigüedad (7 en Shorts) y ≤12 meses. El video evaluado se excluye de su propia mediana y N se cuenta **después** de esa exclusión. Muestra: N ≥15 normal; N de 8 a 14 «muestra reducida», confianza máx. Media; N <8 «muestra insuficiente»: razón = estimación, confianza Baja, solo outlier/patrón «posible». No se rellena la muestra con videos fuera de criterio sin avisar; si se amplía la ventana se declara y se baja la confianza un nivel. Opción preferida: **mediana contemporánea** (≈10 videos antes y ≈10 después del video evaluado).
- **M3 Cálculo.** Ordenar las vistas de menor a mayor; N impar: valor central; N par: promedio de los dos centrales. Registrar «mediana de N videos, de fecha a fecha». Control de duplicados: no contar videos dos veces.
- **M4 Razón y patrón.** Razón = vistas del video ÷ mediana. Outlier = ≥5×. Patrón = ≥3 videos distintos (12 meses) con razón ≥3× y al menos uno ≥5×. Solo se declaran con muestra suficiente (M2).
- **M5 Edad.** Las vistas brutas de videos de distinta antigüedad no son comparables sin explicación. Se rankea con videos de los últimos 12 meses, se indica la antigüedad y se marca «inmaduro» lo de <14 días (<7 en Shorts: la misma antigüedad mínima de M2). Las vistas por mes son solo referencia secundaria.
- **M6 Registro.** Cada análisis declara ventana, N (tras excluir el video evaluado), fechas de publicación de los videos incluidos, formato y fecha de consulta del canal.
*Por qué una sola ventana:* la versión anterior mencionaba 10, 30 y 90 videos. Ahora hay una ventana estándar (20) con una variante opcional (contemporánea) declarada siempre. Con 20 videos, la mediana es estable y refleja el rendimiento actual.
*Limitación:* si un canal cambió mucho de tamaño o formato en 12 meses, la mediana de la ventana puede no representar la etapa de un video antiguo; por eso se prefiere la mediana contemporánea.

## 4. Umbrales contextuales
| Mercado | V (vistas de referencia por video largo reciente) | «Canal pequeño» |
|---|---|---|
| Grande (inglés global, español Latinoamérica amplio) | ~100 000 | < 100 000 suscriptores |
| Medio (español España, portugués, francés, alemán, un solo país) | ~30 000 | < 30 000 |
| Pequeño o subnicho especializado | ~10 000 | < 10 000 |
Ajustes: Shorts ×5 en V; contenido técnico o de alto valor por espectador, V puede ser la mitad si se justifica; videos muy largos o evergreen, explicar la edad. Mejor referencia: techo propio del nicho (mediana de sus 5 canales mayores). **No se descarta un nicho especializado por tener menos vistas que uno masivo**: se valora frente a su techo, interacción, crecimiento, valor por espectador (RPM, productos, servicios) y facilidad de dominarlo. Estos valores son puntos de partida elegidos por la academia; la IA debe declarar el que usa y justificar ajustes.

## 5. Criterios y pesos (suman 100 %)
| Criterio | Peso | Razón del peso |
|---|---|---|
| Demanda verificable | 20 | Sin público no hay canal; es lo más medible con datos públicos |
| Oportunidad competitiva | 15 | Un hueco real permite crecer con un canal nuevo |
| Diferenciación | 15 | En la era de IA, el contenido genérico es el mayor riesgo |
| Monetización | 15 | Importa, pero es difícil de verificar; por eso no pesa más |
| Facilidad de producción | 10 | Determina si el alumno sostendrá el ritmo |
| Compatibilidad con IA | 10 | La IA ayuda sin volver el contenido masivo o repetitivo |
| Sostenibilidad | 10 | Evergreen y volumen de temas |
| Afinidad con el alumno | 5 | Importa, pero la evidencia de mercado manda |
Total = Σ(nota/10 × peso). Los pesos son una decisión razonada de la academia; pueden ajustarse a un objetivo siempre sumando 100.
Escala: 0-2 sin evidencia o muy débil · 3-4 débil · 5-6 aceptable/mixto · 7-8 fuerte · 9-10 excepcional y demostrado.

## 6. Anclas de evidencia (la nota no es solo opinión)
- **Demanda ≥7:** ≥5 canales distintos (del idioma del mercado) con videos de 12 meses sobre V (o su techo propio en nichos especializados) y una segunda comprobación independiente (Trends, otra búsqueda distinta o las vistas recientes de varios canales en sus páginas). 1-2 canales: máx. 5. Sin datos: máx. 3.
- **Oportunidad ≥7:** ≥2 canales pequeños con patrón (M4) o un hueco temático demostrado. Un solo outlier: máx. 4. Clones recientes con muy pocos suscriptores = saturación.
- **Diferenciación y Monetización ≥7:** razón concreta comprobable; si no, máx. 6.
- **Alerta:** canal con muchos suscriptores y vistas recientes mínimas = riesgo (agotamiento, cambio de audiencia o contenido masivo) [OPINIÓN].
## 7. Confianza y regla de decisión
Alto: varias fuentes verificadas coherentes. Medio: pocas fuentes o datos parciales. Bajo: sobre todo estimación (se da un rango). **Sin ganador** si la investigación es INCOMPLETA o BLOQUEADA, si la confianza global es Baja, si Demanda tiene confianza Baja o nota <6, o si hay un riesgo invalidante sin resolver: «NO CONCLUYENTE» + siguiente paso de validación. Con estado SUFICIENTE la recomendación es PROVISIONAL. **Empate técnico:** si los dos primeros difieren menos de 5 puntos no se declara ganador por décimas; se desempata con Facilidad de producción y Afinidad o se propone un experimento. Si faltan métricas pero el resto de la evidencia basta, se continúa marcando [NO DISPONIBLE] y bajando la confianza.

## 8. Fuentes (por prioridad) y alternativas
1. Páginas públicas de YouTube (listas de resultados ordenadas por vistas + «este año», filtro Canales para suscriptores, pestaña Videos de cada canal, página del video para la fecha).
2. Documentación oficial de YouTube: Programa de socios (support.google.com/youtube/answer/72851), contenido inauténtico/repetitivo (…/answer/1311392), divulgación de contenido sintético (…/answer/14328491), monetización de Shorts (…/answer/12504220).
3. Google Trends cuando sea accesible.
4. Estadísticas públicas con metodología clara (citar fuente y fecha).
5. Búsqueda web general (apoyo; blogs y herramientas comerciales solo para hipótesis).
6. Datos aportados por el propio alumno (ficha para copiar a mano).
La API de datos de YouTube es opcional y nunca se piden claves en la conversación. Ninguna herramienta de pago es obligatoria. No se eluden límites ni bloqueos. **La lista de resultados está sesgada hacia videos populares: no sirve para calcular medianas.** Los parámetros de región/idioma no siempre bastan: se declara la región de consulta y se comprueba el idioma de cada canal.

## 9. Reglas contra información inventada
No inventar canales, enlaces ni cifras; cada canal con enlace abierto en la sesión; sin búsqueda web, modo guiado; auto-revisión final con «Qué NO pude comprobar»; el alumno verifica 3-5 enlaces al azar.

## 9b. Datos públicos y privados
Públicos (visibles en YouTube): título, miniatura, duración, vistas aproximadas, fecha de publicación, comentarios visibles, suscriptores (a veces ocultos o redondeados), nº de videos, frecuencia. **Privados** (solo el dueño en YouTube Studio): CTR de impresiones, retención y tiempo de visualización, fuentes de tráfico, demografía, RPM e ingresos reales. Nunca se presentan datos privados de canales ajenos como públicos; solo pueden aparecer como estimación con fuente o como no disponibles. CTR y retención se miden únicamente en los videos del propio alumno (experimento).

## 10. Ingresos y RPM
Solo el dueño del canal conoce sus ingresos. RPM/CPM varía por país, época, contenido, anunciantes y formato. Los Shorts usan un reparto distinto y su RPM suele ser mucho menor; las cifras de terceros son orientativas. Las calculadoras externas son estimaciones. Todo RPM cita fuente, mercado, formato y supuestos.

## 11. Riesgos de monetización (contenido inauténtico)
En julio de 2025 YouTube aclaró que su política cubre contenido repetitivo o producido en masa (plantillas con poca variación, fácil de replicar a escala). No prohíbe usar IA, pero exige valor propio: guion original, criterio, edición. El contenido realista alterado o sintético requiere divulgación en YouTube Studio. Verificar siempre en la ayuda oficial.

## 12. Investigación consultada para diseñar este recurso (23-11-2026)
Política de contenido inauténtico y su aclaración de 2025; requisitos del Programa de socios (1.000 suscriptores + 4.000 horas públicas o 10 M de vistas de Shorts en 90 días; nivel inferior de 500 suscriptores con requisitos menores) **confirmados solo mediante resultados de búsqueda: el alumno debe confirmarlos en la página oficial**; divulgación de contenido sintético; monetización de Shorts (reparto desde el feed de Shorts; RPM de terceros muy inferiores, orientativos); metodología de outliers (razón frente al rendimiento habitual), adoptada como heurística.

## 13. Lenguaje para el alumno
La IA usa internamente conceptos como mediana, outlier, RPM, confianza o umbral, pero los explica en lenguaje sencillo («este video consiguió unas seis veces más vistas que los videos habituales del canal»). El informe principal empieza con: mi nicho recomendado, por qué lo elegiría, principales riesgos, mis primeros 3 pasos y confianza de la recomendación; los datos técnicos van en anexos.
