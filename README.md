# PFO Nº1 - Desarrollo de Sistemas Web - Frontend

Este repositorio contiene la Práctica Formativa Obligatoria N.º 1 (PFO1) de la materia Desarrollo de Sistemas Web – Frontend. Soy Marcos Aquino, desarrollador frontend, esta landing funciona como mi carta de presentación: un espacio pensado para mostrar quién soy, qué habilidades manejo y cómo contactarme.

## Descripción

Landing de portafolio personal desarrollada **solo con HTML semántico y CSS
 para la consigna PFO1. 



URL del proyecto: https://pf-1-lading-personal.vercel.app/



## Decisiones tomadas

- **Concepto:** en vez de un portafolio genérico, se eligió un hilo conductor
  entre el perfil (desarrolladora frontend) y la sección personal (afición por
  la observación astronómica): la sección de habilidades se representa como
  una **constelación** — cada habilidad es un punto ("estrella") y las líneas
  que los conectan se "dibujan" en secuencia al cargar la página, con una
  animación CSS pura (`stroke-dasharray` / `stroke-dashoffset` + `@keyframes`,
  sin JavaScript), reforzando la idea de que las herramientas se combinan
  entre sí en un mismo proyecto.
- **Sin JavaScript, a propósito:** todo el proyecto es HTML + CSS. El menú
  mobile se resuelve con el "checkbox hack" (un `<input type="checkbox">`
  oculto + un `<label>` que actúa de botón, combinados con el selector `~` en
  CSS) y el formulario de contacto usa el atributo nativo `action="mailto:"`
  del `<form>` en vez de armar el mail con JavaScript.
- **Paleta:** azul noche (`#0B1026`, `#141B3A`) con acentos dorado (`#F2C572`,
  "luz de estrella") y violeta (`#8C8CE6`), evitando las paletas por defecto
  más comunes en diseños generados con IA (crema+terracota / negro+neón).
- **Tipografía:** `Fraunces` (serif, con itálicas) para títulos y momentos de
  jerarquía; `Space Mono` para navegación, etiquetas y textos técnicos —
  evocando coordenadas/catálogos astronómicos; `Inter` para el cuerpo de
  texto, por legibilidad.
- **Layout:** Flexbox para la navegación y las tarjetas; CSS Grid para las
  secciones de dos columnas (bitácora personal y contacto) en pantallas
  medianas/grandes; en mobile todo colapsa a una sola columna.
- **Accesibilidad:** foco visible en todos los elementos interactivos,
  etiquetas (`label`) asociadas a cada campo del formulario, texto alternativo
  descriptivo en las imágenes, y soporte de `prefers-reduced-motion` para
  desactivar animaciones a quienes lo necesiten. El menú mobile con checkbox
  es funcional con teclado y mouse, aunque al ser una técnica sin JavaScript
  no expone un estado `aria-expanded` dinámico como lo haría un botón
  controlado por script — es la limitación conocida de este patrón, aceptada
  a cambio de no usar JavaScript.
- **Responsive:** mobile-first, con un menú de navegación colapsable
  (hamburguesa, resuelto 100% en CSS) por debajo de los 900px y un breakpoint
  que reemplaza la constelación (poco legible en pantallas muy chicas) por una
  lista simple de habilidades.
- **Formulario de contacto:** no hay backend ni JavaScript, así que el
  `<form>` usa directamente `action="mailto:..."` con
  `enctype="text/plain"`, el comportamiento nativo del HTML para este caso.
  El soporte varía según el cliente de correo predeterminado del sistema
  operativo; como respaldo, el mail también está disponible como link directo
  en "Contacto".

## Declaración de uso de IA

- **Herramienta usada:** Claude (Anthropic), modelo Sonnet 4.6, a través del
  chat web de Claude.ai.
- **Plan de la cuenta:** `[Free]`.
- **Para qué se usó:** generación completa del HTML semántico y el CSS
  (tokens de color/tipografía, layout con Flexbox/Grid, animaciones, menú
  mobile con checkbox hack) a partir de un brief con la consigna de la PFO1,
  incluyendo el pedido explícito de resolver todo sin JavaScript. También se
  usó para inventar un set de datos de ejemplo (nombre, textos, habilidades)
  a pedido explícito, como punto de partida para iterar antes de cargar la
  información real.


## Experiencia previa con IA

Hasta ahora solo había usado inteligencia artificial para corregir texto (ortografía, redacción) y para consultar o corregir fragmentos de código puntuales. Esta es la primera vez que la uso para generar un proyecto completo desde cero (código, diseño y contenido) y después ir revisando para  modificar lo generado según mi propio criterio.

