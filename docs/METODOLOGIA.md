# Metodología del banco de preguntas

## Fuente
Guía de Estudio para el Examen de Idoneidad, versión 5, publicada por la CNV. Contiene 735 preguntas con su respuesta correcta (sin opciones incorrectas), en seis módulos.

## Fidelidad a la guía
- Cada pregunta del simulador se cruzó una por una con la guía: enunciado y respuesta correcta.
- Se corrigieron 16 preguntas cuya clave no coincidía con la guía (entre ellas datos actualizados por la RG 1088/2025, ejercicios numéricos de opciones y bonos, y topes de inversión en fondos comunes de dinero).
- Las 22 preguntas que la guía formula como Verdadero/Falso se presentan con dos opciones y el enunciado textual.
- Se eliminaron preguntas que no estaban en la guía y se corrigieron opciones duplicadas.
- Inconsistencias internas de la guía (por ejemplo, I-74 vs. I-126 sobre el número de destinatarios de una oferta privada) se mantienen tal como están en el material oficial.

## Distractores
Objetivo: que la forma de las opciones no delate la respuesta. Reglas aplicadas a cada distractor nuevo:
- Es falso según la guía, y no introduce datos (números, normas, plazos) que no existan en la guía o en la norma.
- Misma forma gramatical y registro que la respuesta correcta, con longitud comparable.
- Tipado en `dt`: `numero` (cambia un plazo, porcentaje o monto), `sujeto` (cambia el organismo o rol), `inversion` (invierte la condición), `alcance` (amplía o restringe).
- "Ninguna opción es correcta" se eliminó como distractor (aparecía 204 veces y nunca era correcta).

## Compuertas automáticas (se aplican a cada módulo)
1. Enunciados y claves idénticos a la versión validada contra la guía.
2. Estrategia ciega (opción más larga + descartar "ninguna" + descartar absolutos) por debajo del 32 %.
3. Correcta estrictamente más larga en menos del 35 % y estrictamente más corta entre el 15 % y el 35 %.
4. Sin opciones duplicadas ni equivalentes.
5. Ningún distractor nuevo con similitud textual alta contra la clave de otra pregunta de la guía, salvo revisión manual documentada.
6. El HTML parsea; recuentos por módulo iguales a la guía.
7. Cada pregunta tocada lleva `src` y `dt`.

## Resultado global (713 preguntas de opción múltiple)
| Métrica | Antes | Después |
|---|---|---|
| Estrategia ciega | 52 % | 25 % |
| Correcta más larga | 50 % | 24 % |
| Correcta más corta | 14 % | 21 % |
| "Ninguna" como distractor | 204 | 0 |
| Absolutos en distractores / en correctas | 336 / 18 | 188 / 18 |

Se reescribieron 878 distractores en 409 preguntas; 304 preguntas quedaron sin cambios.
