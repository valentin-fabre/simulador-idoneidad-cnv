# Simulador — Examen de Idoneidad CNV

Herramienta de práctica para el Examen de Idoneidad de la Comisión Nacional de Valores (Argentina). Un solo archivo HTML, sin dependencias ni servidor: se abre en el navegador y funciona.

**En línea:** https://valentin-fabre.github.io/simulador-idoneidad-cnv/

Desarrollado por [Valentin Fabre](https://www.linkedin.com/in/fabrevalentin). Versión 3.0 (21/10/2026).

## Avisos

- **Herramienta independiente.** No es material oficial de la Comisión Nacional de Valores (CNV) ni cuenta con su aval. La CNV no avala cursos ni materiales de preparación.
- **Basada en la Guía de Estudio v5** (PDF oficial fechado 25/06/2026). La [RG 1173/2026](https://www.boletinoficial.gob.ar/detalleAviso/primera/348987/20261015), vigente desde el 15/10/2026, modificó normativa posterior a esa guía (en particular el régimen del Registro de Idóneos) y reorganiza la administración del examen a partir de 2027. Cuando la CNV publique una nueva versión de la guía, este simulador quedará desactualizado hasta que se adapte.
- **Ante contradicciones o errores de la guía** (por ejemplo, el cálculo de convexidad o el número de destinatarios de una oferta privada), el simulador marca la respuesta publicada por la CNV, porque esa publicación es la referencia válida para la corrección del examen.
- **Errores u omisiones:** reportalos en los [issues del repositorio](https://github.com/valentin-fabre/simulador-idoneidad-cnv/issues/new/choose), indicando módulo y número de pregunta. Desde cada pregunta hay un enlace "Reportar un error en esta pregunta" que abre el issue con el número cargado.
- No se utiliza el logo ni ningún signo distintivo de la CNV.
- Los avisos completos se muestran al pie de la pantalla de inicio de la herramienta.

**Usar sin conexión:** descargá `index.html` y abrilo con cualquier navegador moderno. En el teléfono, abrí la dirección en el navegador (no el archivo) y usá "Agregar a pantalla de inicio".

## Qué incluye

- **735 preguntas** en seis módulos (127 / 112 / 106 / 137 / 128 / 125), con los enunciados y las respuestas correctas de la [Guía de Estudio oficial v5 publicada por la CNV](https://www.argentina.gob.ar/sites/default/files/guia_de_estudio_v5.pdf). Las opciones incorrectas son de elaboración propia.
- **Simulador de examen:** 60 preguntas (10 por módulo), 45 minutos, aprobación al 70 %. Opciones mezcladas en cada intento. Corrección al final o inmediata.
- **Práctica por módulo:** todas las preguntas, en orden de la guía o aleatorio, con posibilidad de elegir números o rangos (`1-20, 35, 84-106`).
- **Mis errores:** las preguntas falladas en prácticas y simulacros se acumulan y se pueden repasar juntas, o por módulo, hasta acertarlas.
- **Historial:** puntaje de cada simulacro y promedio, rendimiento reciente por módulo.
- **Atajos de teclado** para responder, navegar y marcar preguntas.

Todo el progreso se guarda en el navegador (`localStorage`). No hay cuentas, no se envía nada a ningún servidor.

## Sobre el banco de preguntas

Los enunciados y las claves siguen la guía oficial de forma literal. Las 22 preguntas que la guía plantea como Verdadero/Falso conservan ese formato. Los distractores fueron escritos para que no delaten la respuesta: la opción correcta es la más larga en un 24 % de las preguntas y la más corta en un 21 %, y una estrategia de adivinación por forma (opción más larga, descartar "ninguna", descartar absolutos) acierta el 25 %, igual que el azar. Ver `docs/METODOLOGIA.md`.

Cada pregunta lleva `src` (posición en el módulo, que coincide con la numeración de la guía salvo en el módulo II, donde la guía numera 1–99 y luego 71–83) y, cuando corresponde, `dt` con el tipo de cada distractor.

## Estructura

```
index.html                 la herramienta completa (datos + lógica + estilos)
.github/ISSUE_TEMPLATE     plantilla para reportar errores en preguntas
icon-180.png, icon-512.png, manifest.webmanifest   ícono e instalación como app en el teléfono
og-image.png               imagen de vista previa para redes sociales
docs/design-tokens.json    tokens de diseño de la interfaz (también embebidos en index.html)
docs/METODOLOGIA.md        cómo se construyó y validó el banco de preguntas
CHANGELOG.md               historial de versiones
```

## Editar el banco

Las preguntas están en `index.html`, en los arreglos `MOD1_Q` … `MOD6_Q`. Formato de cada entrada:

```js
{mod:1, q:"Enunciado", opts:["Correcta","Distractor","Distractor","Distractor"], ans:0, src:"I-12", dt:["numero","sujeto","alcance"]}
```

La respuesta correcta es siempre `opts[0]` (`ans:0`); el orden se mezcla al mostrar. Para una pregunta Verdadero/Falso, `opts` tiene dos elementos.

## Licencias

- **Consignas: Guía de Estudio v5, CNV, CC BY 4.0.** Los enunciados y las respuestas correctas provienen de la [Guía de Estudio v5](https://www.argentina.gob.ar/sites/default/files/guia_de_estudio_v5.pdf) publicada por la Comisión Nacional de Valores en argentina.gob.ar, cuyo contenido se publica bajo [Creative Commons Atribución 4.0 Internacional (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/deed.es).
- **Distractores (opciones incorrectas):** elaboración de Valentin Fabre, bajo [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es).
- **Código y diseño:** Valentin Fabre, bajo licencia [MIT](LICENSE).
