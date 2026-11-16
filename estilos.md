# Guía Comparativa Definitiva: CSS vs Tailwind vs Bootstrap

## 1. Colores y Fondos
| CSS                             | Tailwind           | Bootstrap                 | Descripción       
| ------------------------------- | ------------------ | ------------------------- | 
| `color: black;`                 | `text-black`       | `text-black`              | Color de texto  
| `color: rgba(0, 0, 0, 0.5);`  | `text-black/50`    | `text-black-50`           | Texto con opacidad 50% 
| `color: transparent;`           | `text-transparent` | *No existe clase directa* | Texto transparente. 
| `background-color: white;`      | `bg-white`         | `bg-white`                | Color de fondo
| `background-color: rgba(0,0,0,.5);` | `bg-black/50`| `bg-black bg-opacity-50`  | Fondo con opacidad 
| `background-color: transparent;`| `bg-transparent`   | `bg-transparent`          | Fondo transparente. 
| `opacity: 0.5;`                 | `opacity-50`       | `opacity-50`              | Opacidad general del elemento (50%).

## 2. Texto, Alineación y Tipografía
| CSS                         | Tailwind           | Bootstrap              | Descripción
| ----------------------------| -------------------| ---------------------- | 
| `text-align: center;`       | `text-center`      | `text-center`          | Alineación horizontal del texto
| `font-weight: 700;`         | `font-bold`        | `fw-bold`              | Grosor de fuente (negrita)
| `font-style: italic;`       | `italic`           | `fst-italic`           | Estilo de fuente (cursiva)
| `text-transform: uppercase;`| `uppercase`        | `text-uppercase`       | Transformación de texto (mayúsculas)
| `text-decoration: none;`    | `no-underline`     | `text-decoration-none` | Decoración de texto (quitar subrayado en enlaces)
| `font-size: 16px;`          | `text-base`        | `fs-6`                 | Tamaño de fuente estándar (`1rem`)
| `line-height: 1.5;`         | `leading-normal`   | `lh-base`              | Interlineado estándar
| `white-space: nowrap;`      | `whitespace-nowrap`| `text-nowrap`          | Evitar salto de línea en el texto
| `overflow: hidden; text-overflow: ellipsis; white-space: nowrap;`|`truncate`| `text-truncate`| Cortar texto largo con puntos suspensivos (`...`)

## 3. Margin (Espacio Exterior)
> **Nota:** En Tailwind `4 = 16px`, mientras que en Bootstrap `3 = 16px`.
| CSS                                     | Tailwind  | Bootstrap | Descripción                           |
| ----------------------------------------| --------- | --------- | ------------------------------------- |
| `margin: 16px;`                         | `m-4`     | `m-3`     | Margen exterior en los 4 lados (16px).|
| `margin-left: auto; margin-right: auto;`| `mx-auto` | `mx-auto` | Centrar un bloque horizontalmente.    |
| `margin-top: 16px; margin-bottom: 16px;`| `my-4`    | `my-3`    | Margen vertical (arriba y abajo).     |
| `margin-top: 16px;`                     | `mt-4`    | `mt-3`    | Margen superior.                      |
| `margin-bottom: 16px;`                  | `mb-4`    | `mb-3`    | Margen inferior.                      |
| `margin-left: 16px;`                    | `ml-4`    | `ms-3`    | Margen izquierdo (Start).             |
| `margin-right: 16px;`                   | `mr-4`    | `me-3`    | Margen derecho (End).                 |
| `margin-left: -16px;`                   | `-ml-4`   | `ms-n3`   | Margen negativo.                      |

## 4. Padding (Espacio Interior)
| CSS                                       | Tailwind | Bootstrap | Descripción                            |
| ------------------------------------------| -------- | --------- | -------------------------------------- |
| `padding: 16px;`                          | `p-4`    | `p-3`     | Relleno interior en los 4 lados (16px).|
| `padding-left: 16px; padding-right: 16px;`| `px-4`   | `px-3`    | Relleno horizontal (izquierda/derecha).|
| `padding-top: 16px; padding-bottom: 16px;`| `py-4`   | `py-3`    | Relleno vertical (arriba y abajo).     |
| `padding-top: 16px;`                      | `pt-4`   | `pt-3`    | Relleno superior.                      |
| `padding-bottom: 16px;`                   | `pb-4`   | `pb-3`    | Relleno inferior.                      |
| `padding-left: 16px;`                     | `pl-4`   | `ps-3`    | Relleno izquierdo (Start).             |
| `padding-right: 16px;`                    | `pr-4`   | `pe-3`    | Relleno derecho (End).                 |

## 5. Ancho y Alto (Width & Height)
| CSS                   | Tailwind       | Bootstrap    | Descripción                             |
| --------------------- | -------------- | ------------ | --------------------------------------- |
| `width: 100%;`        | `w-full`       | `w-100`      | Ancho completo respecto al padre.       |
| `width: 100vw;`       | `w-screen`     | `vw-100`     | Ancho total de la pantalla (Viewport).  |
| `max-width: 100%;`    | `max-w-full`   | `mw-100`     | Ancho máximo permitido.                 |
| `min-width: 100vw;`   | `min-w-screen` | `min-vw-100` | Ancho mínimo de pantalla.               |
| `height: 100%;`       | `h-full`       | `h-100`      | Alto completo respecto al padre.        |
| `height: 100vh;`      | `h-screen`     | `vh-100`     | Alto total de la pantalla (Viewport).   |
| `min-height: 100vh;`  | `min-h-screen` | `min-vh-100` | Alto mínimo igual al de la pantalla.    |
| `max-height: 100%;`   | `max-h-full`   | `mh-100`     | Alto máximo permitido.                  |

## 6. Bordes, Radios y Sombras
| CSS                        | Tailwind       | Bootstrap              | Descripción    
| -------------------------- | -------------- | -----------------------| --------------------------------
| `border: 1px solid;`       | `border`       | `border`               | Borde en los 4 lados
| `border-bottom: 1px solid;`| `border-b`     | `border-bottom`        | Borde en un solo lado (ej. inferior)
| `border-width: 2px;`       | `border-2`     | `border-2`             | Grosor del borde
| `border-color: black;`     | `border-black` | `border-black`         | Color del borde 
| `border-style: dashed;`    | `border-dashed`| *No existe en Bootstrap| Estilo de borde punteado con guiones
| `border-radius: 8px;`      | `rounded-lg`   | `rounded-3`            | Esquinas redondeadas estándar
| `border-radius: 50%;`      | `rounded-full` | `rounded-circle`       | Forma circular completa
| `box-shadow: 0 4px 6px rgba(0,0,0,.1);`| `shadow-md` | `shadow`    | Sombra paralela negra estándar

## 7. Flexbox (Alineación Horizontal y Vertical)
| CSS                              | Tailwind         |Bootstrap    | Descripción
| -------------------------------- | -----------------| ----------- | -------------------
| `display: flex;`                 | `flex`           |`d-flex`      | Activar contenedor Flexbox
| `flex-direction: column;`        | `flex-col`       |`flex-column` | Dirección en columna vertical
| `flex-wrap: wrap;`               | `flex-wrap`      |`flex-wrap`   | Permitir salto de línea si no caben los hijos
| `justify-content: center;`       | `justify-center` |`justify-content-center`| Centrar horizontalmente (en fila)
| `justify-content: space-between;`| `justify-between`|`justify-content-between`| Distribuir espacio entre extremos
| `align-items: center;`           | `items-center`   |`align-items-center`| Centrar verticalmente (en fila)
| `display: flex; justify-content: center; align-items: center;` | `flex justify-center items-center` | `d-flex justify-content-center align-items-center` | Centrado perfecto (horizontal y vertical).   |
| `align-self: center;`            | `self-center`    |`align-self-center`| Alinear individualmente un elemento hijo
| `flex: 1 1 0%;`                  | `flex-1`         |`flex-fill`        | Hacer que el elemento ocupe el espacio sobrante
| `order: 1;`                      | `order-1`        |`order-1`          | Cambiar el orden visual de un elemento
| `gap: 16px;`                     | `gap-4`          |`gap-3`            | Separación uniforme entre elementos flex

## 8. Grid y Distribución de Columnas
| CSS                                     | Tailwind     | Bootstrap       | Descripción  
| --------------------------------------- | ------------ | --------------- | -----------------------------
| `display: grid;`                        | `grid`       |`d-grid`                   | Activar CSS Grid nativo
| `display: flex; flex-wrap: wrap;`       | `grid`       | `row`                     | Fila contenedora del sistema de 12 columnas
| `grid-template-columns: repeat(3, 1fr);`| `grid-cols-3`| `row-cols-3` *(en `.row`)*| Cuadrícula de columnas iguales (ej. 3 columnas)
| `grid-column: span 6 / span 6;`         | `col-span-6` | `col-6`                   | Elemento que ocupa la mitad del ancho (6 de 12)
| `grid-row: span 2 / span 2;`            | `row-span-2` | *No existe en grid estándar*| Elemento que abarca varias filas hacia abajo
| `gap: 16px;`                            | `gap-4`      | `g-3` *(en `.row`)*        | Espacio entre celdas de la cuadrícula
| `place-items: center;`           | `place-items-center`| *No existe clase directa*  | Centrar contenido dentro de las celdas Grid

## 9. Diseño Responsive (Puntos de Ruptura / Breakpoints)
| CSS (`@media`)                   | Tailwind                    | Bootstrap                  | Descripción  
| ---------------------------------| --------------------------- | -------------------------- | -----------------
| *Sin media query (`0px+`)*       | *(Sin prefijo)*             | *(Sin prefijo)*            | Estilos base (Mobile-First)
| `@media (min-width: 768px)`      | `md:*` *(ej. `md:grid-cols-2`)* | `*-md-*` *(ej. `col-md-6`)*| Aplicar estilo desde tamaño Tablet (`768px+`)
| *Ocultar en móvil, mostrar en PC*| `hidden md:block`           | `d-none d-md-block`        | Visibilidad condicional según dispositivo

## 10. Botones y sus Estados
| CSS                   |Tailwind               | Bootstrap            | Descripción  
| --------------------- | --------------------- | -------------------- | --------------------------------
| `padding: 8px 16px; border-radius: 6px; cursor: pointer;`| `px-4 py-2 rounded-md cursor-pointer`| `btn`| Estructura base de un botón
| `background: black; color: white;`|`bg-black text-white px-4 py-2 rounded`| `btn btn-dark`| Botón sólido principal (negro con texto blanco)
| `background: transparent; color: black; border: 1px solid black;` | `bg-transparent text-black border border-black px-4 py-2 rounded` | `btn btn-outline-dark` | Botón secundario delineado (Outline negro).        |
| `padding: 4px 8px; font-size: 14px;` | `px-2 py-1 text-sm`|`btn btn-sm`|Modificador de tamaño de botón (pequeño)
| `opacity: 0.5; pointer-events: none;`|`opacity-50 pointer-events-none` |`btn disabled`| Estado de botón deshabilitado

## 11. Tarjetas (Cards)
| CSS                         | Tailwind              | Bootstrap   | Descripción   
| --------------------------- | --------------------- | ----------- | -----------------------------
| `background: white; color: black; border: 1px solid black; border-radius: 8px; overflow: hidden;` | `bg-white text-black border border-black rounded-lg overflow-hidden` | `card bg-white text-black border-black` | Contenedor principal de tarjeta (blanca, borde negro)
| `padding: 12px 16px; border-bottom: 1px solid black;` | `px-4 py-3 border-b border-black`| `card-header border-black`  | Encabezado de la tarjeta
| `padding: 16px;`            | `p-4`                 | `card-body`  | Cuerpo principal de la tarjeta
| `font-size: 20px; font-weight: bold; margin-bottom: 8px;` | `text-xl font-bold mb-2` | `card-title` | Título de la tarjeta
| `font-size: 16px; margin-bottom: 16px;` | `text-base mb-4`  | `card-text`  | Texto descriptivo de la tarjeta
| `padding: 12px 16px; border-top: 1px solid black;` | `px-4 py-3 border-t border-black` | `card-footer border-black`| Pie de la tarjeta
| `width: 100%; display: block;`| `w-full block`      | `card-img-top` | Imagen superior de la tarjeta

## 12. Tablas
| CSS                                                 | Tailwind                          | Bootstrap                      | Descripción                                          |
| --------------------------------------------------- | --------------------------------- | ------------------------------ | ---------------------------------------------------- |
| `width: 100%; border-collapse: collapse;`           | `w-full border-collapse text-left`| `table`                        | Estructura base de tabla.                            |
| `background: black; color: white;`                  | `bg-black text-white`             | `table-dark`                   | Encabezado o tabla oscura (negro con texto blanco).  |
| `border: 1px solid black;` *(en celdas)*            | `border border-black` *(en celdas)*| `table-bordered border-black`  | Bordes en todas las celdas de la tabla.              |
| `tr:nth-child(even) { background: rgba(0,0,0,.05); }`| `even:bg-black/5` *(en `<tr>`)*   | `table-striped`                | Filas alternas (efecto cebra).                       |
| `tr:hover { background: rgba(0,0,0,.1); }`          | `hover:bg-black/10` *(en `<tr>`)* | `table-hover`                  | Resaltar fila al pasar el ratón.                     |
| `overflow-x: auto; width: 100%;` *(en div padre)*   | `overflow-x-auto w-full` *(en div)*| `table-responsive` *(en div)*  | Scroll horizontal para tablas en móvil.              |


## 13. Display y Posicionamiento
| CSS                                                       | Tailwind                                              | Bootstrap                            | Descripción                                            |
| --------------------------------------------------------- | ----------------------------------------------------- | ------------------------------------ | ------------------------------------------------------ |
| `display: block;`                                         | `block`                                               | `d-block`                            | Mostrar como bloque.                                   |
| `display: none;`                                          | `hidden`                                              | `d-none`                             | Ocultar elemento completamente.                        |
| `visibility: hidden;`                                     | `invisible`                                           | `invisible`                          | Ocultar visualmente manteniendo su espacio.            |
| `position: relative;`                                     | `relative`                                            | `position-relative`                  | Posicionamiento relativo (padre).                      |
| `position: absolute;`                                     | `absolute`                                            | `position-absolute`                  | Posicionamiento absoluto (hijo).                       |
| `position: fixed;`                                        | `fixed`                                               | `position-fixed`                     | Fijo respecto a la ventana del navegador.              |
| `position: sticky; top: 0;`                               | `sticky top-0`                                        | `sticky-top`                         | Pegado al borde superior al hacer scroll.              |
| `top: 50%; left: 50%; transform: translate(-50%, -50%);`  | `top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2`  | `top-50 start-50 translate-middle`   | Centrar un elemento absoluto en medio de su padre.     |
| `z-index: 10;`                                            | `z-10`                                                | `z-1`                                | Orden de apilamiento (profundidad).                    |
| `overflow: hidden;`                                       | `overflow-hidden`                                     | `overflow-hidden`                    | Ocultar contenido que desborde.                        |

## 14. Imágenes
| CSS                                                      | Tailwind                                   | Bootstrap          | Descripción                                    |
| -------------------------------------------------------- | ------------------------------------------ | ------------------ | ---------------------------------------------- |
| `max-width: 100%; height: auto;`                         | `max-w-full h-auto`                        | `img-fluid`        | Imagen adaptable (responsive).                 |
| `border-radius: 50%;`                                    | `rounded-full`                             | `rounded-circle`   | Imagen circular (avatar).                      |
| `padding: 4px; border: 1px solid black; background: white;` | `p-1 border border-black rounded bg-white` | `img-thumbnail`    | Imagen con marco estilo miniatura.             |
| `object-fit: cover;`                                     | `object-cover`                             | `object-fit-cover` | Ajustar imagen recortando sin deformar.        |
| `filter: grayscale(100%);`                               | `grayscale`                                | *No existe clase*  | Filtro blanco y negro (escala de grises).      |

## 15. Formularios e Inputs
| CSS                                                                                       | Tailwind                                                               | Bootstrap                  | Descripción                                |
| ----------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | -------------------------- | ------------------------------------------ |
| `display: block; width: 100%; padding: 8px 12px; border: 1px solid black; background: white; color: black;` | `block w-full px-3 py-2 border border-black bg-white text-black rounded-md` | `form-control border-black`| Campo de entrada de texto (`<input>`).     |
| `display: block; width: 100%; padding: 8px 12px; border: 1px solid black; background: white; color: black;` | `block w-full px-3 py-2 border border-black bg-white text-black rounded-md` | `form-select border-black` | Selector desplegable (`<select>`).         |
| `display: block; margin-bottom: 8px; font-weight: 500;`                                   | `block mb-2 font-medium`                                               | `form-label`               | Etiqueta de campo (`<label>`).             |
| `accent-color: black; width: 16px; height: 16px;`                                         | `accent-black w-4 h-4 rounded`                                         | `form-check-input`         | Casilla de verificación (`checkbox`).      |
| `display: flex; align-items: stretch; width: 100%;`                                       | `flex items-stretch w-full`                                            | `input-group`              | Agrupar input con botón o prefijo.         |

## 16. Listas y Navegación
| CSS                                                                                                            | Tailwind                                                       | Bootstrap                    | Descripción                                       |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------- | ---------------------------- | ------------------------------------------------- |
| `list-style: none; padding-left: 0;`                                                                           | `list-none pl-0`                                               | `list-unstyled`              | Quitar viñetas y margen a una lista.              |
| `display: flex; flex-direction: column; border: 1px solid black;`                                              | `flex flex-col border border-black divide-y divide-black`      | `list-group`                 | Grupo de lista en caja.                           |
| `display: flex; list-style: none; padding: 0;`                                                                 | `flex list-none p-0`                                           | `nav`                        | Contenedor base de enlaces de navegación.         |
| `display: flex; justify-content: space-between; align-items: center; padding: 12px 16px; background: black; color: white;` | `flex justify-between items-center px-4 py-3 bg-black text-white` | `navbar bg-black navbar-dark`| Barra de navegación superior (Navbar oscura).     |
| `display: flex; gap: 8px; list-style: none;`                                                                   | `flex gap-2 list-none`                                         | `breadcrumb`                 | Ruta de navegación (migas de pan).                |

## 17. Estados Interactivos: Hover, Focus y Active
| CSS                                         | Tailwind                                             | Bootstrap                         | Descripción                                      |
| ------------------------------------------- | ---------------------------------------------------- | --------------------------------- | ------------------------------------------------ |
| `.el:hover { background-color: black; }`    | `hover:bg-black`                                     | *No existe como clase utilitaria* | Cambio de fondo al pasar el cursor (`:hover`).   |
| `.el:focus { outline: 2px solid black; }`   | `focus:outline-none focus:ring-2 focus:ring-black`   | *Automático en `.form-control`*   | Resaltado al seleccionar elemento (`:focus`).    |
| `.el:active { transform: scale(0.95); }`    | `active:scale-95`                                    | *No existe como clase utilitaria* | Efecto al mantener presionado (`:active`).       |
| `.grupo:hover .hijo { color: white; }`      | `group` *(padre)* / `group-hover:text-white` *(hijo)*| *No existe en Bootstrap*          | Cambiar hijo al hacer hover en el padre.         |
| `transition: all 0.2s ease;`                | `transition duration-200`                            | *No existe como clase utilitaria* | Transición suave entre estados.                  |

## 18. Componentes Prediseñados
| CSS (Concepto)   | Tailwind                  | Bootstrap       | Descripción  
| ---------------- | ------------------------- | --------------- |-------------------------
| Caja de aviso con relleno | `p-4 bg-black text-white rounded-md`| `alert bg-black text-white`| Mensaje de alerta
| Etiqueta pequeña redondeada | `px-2 py-0.5 text-xs font-bold bg-black text-white rounded-full` | `badge rounded-pill bg-black text-white` | Insignia / contador (Badge)
| Barra de progreso | `<div class="w-full bg-white border border-black h-4"><div class="bg-black h-full w-1/2"></div></div>` | `progress` + `progress-bar bg-black` | Indicador de progreso
| Círculo animado de carga | `animate-spin h-6 w-6 border-2 border-black border-t-transparent rounded-full` | `spinner-border text-black` | Indicador de carga (Spinner)
| Ventana emergente superpuesta | *No existe componente nativo (requiere JS)*| `modal`| Ventana modal
| Menú desplegable flotante    | *No existe componente nativo (requiere JS)* | `dropdown` | Menú desplegable
| Paneles plegables | *No existe componente nativo (usar `<details>` o JS)* | `accordion` | Acordeón desplegable
| Pase de diapositivas | *No existe componente nativo (requiere JS)*        | `carousel`  | Carrusel de imágenes
| Panel lateral oculto | *No existe componente nativo (requiere JS)* | `offcanvas`  | Menú lateral deslizante

## 19. Tabla General de Equivalencias Rápidas (Resumen Esencial)

| CSS                       | Tailwind         | Bootstrap                | Descripción                       |
| ------------------------- | ---------------- | ------------------------ | --------------------------------- |
| `color: black;`           | `text-black`     | `text-black`             | Color de texto.                   |
| `background-color: white;`| `bg-white`       | `bg-white`               | Color de fondo.                   |
| `text-align: center;`     | `text-center`    | `text-center`            | Centrar texto.                    |
| `display: flex;`          | `flex`           | `d-flex`                 | Activar Flexbox.                  |
| `justify-content: center;`| `justify-center` | `justify-content-center` | Centrar horizontalmente en fila.  |
| `align-items: center;`    | `items-center`   | `align-items-center`     | Centrar verticalmente en fila.    |
| `margin: 0 auto;`         | `mx-auto`        | `mx-auto`                | Centrar bloque horizontalmente.   |
| `padding: 16px;`          | `p-4`            | `p-3`                    | Espacio interior.                 |
| `margin: 16px;`           | `m-4`            | `m-3`                    | Espacio exterior.                 |
| `width: 100%;`            | `w-full`         | `w-100`                  | Ancho completo.                   |
| `height: 100vh;`          | `h-screen`       | `vh-100`                 | Alto de pantalla.                 |
| `border: 1px solid black;`| `border border-black` | `border border-black`| Borde sólido.                     |
| `border-radius: 8px;`     | `rounded-lg`     | `rounded-3`              | Esquinas redondeadas.             |
| `display: grid;`          | `grid`           | `d-grid`                 | Activar CSS Grid.                 |
| `display: none;`          | `hidden`         | `d-none`                 | Ocultar elemento.                 |