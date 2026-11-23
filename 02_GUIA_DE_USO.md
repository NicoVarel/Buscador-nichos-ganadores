# GUÍA DE USO — Investigador de Nichos Ganadores (v2.1 candidata)

## Lectura de 3 minutos

**Qué hace:** te ayuda a decidir qué canal de YouTube crear, con evidencia. Investiga **por etapas** (no todo de golpe) y puede continuar sin perder el progreso. **No** promete viralidad, ingresos ni éxito.

### Paso a paso
1. Abre una IA **con búsqueda web** (ChatGPT, Claude, Gemini, Perplexity…). **No necesitas** pagar herramientas, claves de API ni buscar canales: la IA los descubre y mide por su cuenta.
2. Abre `01_PROMPT_PARA_ALUMNOS.md` y copia **una sola vez** el bloque entre INICIO y FIN. (Opcional: rellena antes «Datos que ya te doy»; lo que rellenes no te lo preguntarán de nuevo.)
3. Envíalo. Si falta algún dato, te harán **una sola pregunta** (o escribe «por defecto»).
4. **Mensaje 1:** la IA explora 6-8 nichos y elige 3 finalistas. Te da un resumen y un **bloque de continuidad**. Guárdalo en un archivo.
5. Escribe `continuar`. **Mensaje 2:** valida a fondo los 3 finalistas.
6. Escribe `continuar`. **Mensaje 3:** compara, recomienda, te da 10 ideas y un plan de 4-6 semanas. Los anexos técnicos se piden aparte («anexos»).
Si la respuesta se corta: `continúa desde donde te quedaste`. Si cambias de conversación: usa `06_CONTINUAR_INVESTIGACION.md` (no hace falta pegar el prompt otra vez).

## Qué debe contener tu informe
Empieza con: **MI NICHO RECOMENDADO · POR QUÉ LO ELEGIRÍA · PRINCIPALES RIESGOS · MIS PRIMEROS 3 PASOS · CONFIANZA DE LA RECOMENDACIÓN**. Luego una tabla de los 3 finalistas, ideas y plan.

## Cómo leerlo
- **Estado de la investigación:** COMPLETA (todo comprobado), SUFICIENTE (se puede decidir de forma **provisional**), INCOMPLETA (solo hipótesis) o BLOQUEADA (no se pudo acceder a los datos).
- **«NO CONCLUYENTE»** es una respuesta válida: significa que falta evidencia. Haz el siguiente paso que indique y pide «completa lo que faltaba». No elijas un nicho solo por su puntuación si la confianza es Baja.
- **Empate técnico:** si dos nichos están a menos de 5 puntos, la IA no inventa un ganador; desempata por facilidad de producción o propone probar ambos.
- **Marcas:** [VERIFICADO] lo vio la IA con enlace; [ESTIMACIÓN] cálculo aproximado; [OPINIÓN] criterio; [NO DISPONIBLE] falta el dato.
- **Abre 3-5 enlaces al azar** y comprueba que existen y que las cifras coinciden. Si fallan, pide: «Revisa y elimina lo que no puedas comprobar».
- Un video viral aislado no es una oportunidad; un patrón repetido sí. Las cifras de YouTube son aproximadas (redondeadas) y dependen del país desde el que se consulta.
- Los umbrales de vistas dependen del mercado: un nicho especializado con menos vistas no es peor por eso.
- Los números de ingresos/RPM son estimaciones, nunca promesas.
- **Datos públicos vs privados:** la IA solo ve lo público (vistas, fechas, suscriptores, títulos). El CTR, la retención y los ingresos reales de otros canales NO son visibles; si aparecen deben estar marcados como estimación o no disponibles. Tu CTR y tu retención los verás tú, en tu YouTube Studio, cuando publiques.
- **Antigüedad mínima:** para calcular el rendimiento habitual de un canal solo cuentan videos con al menos 14 días (7 en Shorts); los más nuevos se marcan «inmaduros».
- **Muestras pequeñas:** con menos de 15 videos comparables (tras excluir el evaluado) el informe avisa y baja la confianza; con menos de 8 solo habla de patrones «posibles».
- **Fechas:** las vistas de un video llevan fecha de publicación y de consulta; los suscriptores, solo la fecha de consulta.

## ¿Qué hace la IA por ti?
Descubre canales (búsqueda web y páginas públicas de YouTube), comprueba que existen y siguen activos, mira su fecha de creación, suscriptores y vistas, calcula su rendimiento habitual y detecta canales pequeños o recientes con resultados repetidos (no un solo video viral). **Si la IA te pide enviarle canales, estadísticas, una herramienta de pago o una clave, responde:** «Investígalo tú con las fuentes gratuitas (búsqueda web y páginas públicas de YouTube) y dime qué no pudiste comprobar». Herramientas como Nexlev o la API de YouTube son opcionales; nunca pegues claves en el chat.

- **Alerta de concentración:** si un solo video reúne más de la mitad de las vistas de un canal, la IA lo avisa y baja la confianza; solo lo descarta si, sin ese video, el canal no tiene patrón.
- **Shorts:** si no se puede saber cuándo se publicó un Short, el informe lo dice y no confirma patrones de Shorts.
- **Datos heredados:** al continuar en otra conversación, lo que viene del bloque es «heredado» hasta que la IA lo reconfirma.

## Si algo falla
| Problema | Qué hacer |
|---|---|
| La IA no puede abrir YouTube o un canal | Es normal: usará la lista de resultados y otras fuentes, y bajará la confianza. Si quieres, pega tú los datos (busca el tema, orden por «Número de visualizaciones», filtro «Este año»; filtro «Canales» para suscriptores) |
| Google Trends no carga | Sigue sin él; la confianza baja |
| La IA repite búsquedas | «Usa el bloque de continuidad y no repitas búsquedas ya hechas» |
| Tu IA no tiene internet | Modo guiado: te da una ficha para rellenar a mano |
| Resultados de otro idioma o país | La IA debe separarlos; pide «revisa el idioma de cada canal» |
| Nunca pegues claves API ni contraseñas en la conversación | No hacen falta |

## Estado de pruebas
Versión **candidata**: las pruebas locales con navegador están documentadas en `05_TESTS.md`; **no** se ha probado aún en sesiones nuevas de ChatGPT, Gemini, Perplexity ni Claude. Hasta entonces úsala como versión de prueba y reporta cualquier problema.

## Limitaciones
- La IA puede equivocarse o no acceder a datos de YouTube. Las métricas cambian cada día.
- Un informe no sustituye probar en la práctica (plan de validación).
- Las reglas de monetización de YouTube cambian: confírmalas en la ayuda oficial.

## Después
Lleva a la **Clase 2 (crear tu canal)**: nicho/subnicho, público, formato y las 10 ideas. Publica el experimento de 5-8 videos y evalúa antes de comprometerte a largo plazo.
