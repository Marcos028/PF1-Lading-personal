# Portafolio personal — PFO1

## Descripción

Landing de portafolio personal desarrollada **solo con HTML semántico y CSS
propio** (sin frameworks ni JavaScript), para la consigna PFO1. 

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



## Cómo publicar en Vercel

1. Subir esta carpeta a un repositorio de GitHub (puede ser público o privado).
2. Entrar a [vercel.com](https://vercel.com) e iniciar sesión con tu cuenta de
   GitHub.
3. Click en **Add New… → Project**, elegir el repositorio recién creado.
4. Como es HTML/CSS/JS plano, en **Framework Preset** dejar `Other` (no hace
   falta build command ni output directory).
5. Click en **Deploy** y esperar a que termine.
6. Copiar la URL que te da Vercel (`https://tu-proyecto.vercel.app`) y
   pegarla en la sección "URL de despliegue" de este README.
