# Comparación de estilos web: CSS, Tailwind CSS y Bootstrap

> Guía práctica para reconocer, escribir y nombrar estilos al
> desarrollar páginas web con HTML.

## 1. ¿Qué es cada uno y para qué se utiliza?

  -----------------------------------------------------------------------
  Tecnología              ¿Qué es?                ¿Para qué se utiliza?
  ----------------------- ----------------------- -----------------------
  **CSS tradicional**     Lenguaje de hojas de    Crear estilos propios:
                          estilo que controla la  colores, tamaños,
                          presentación de HTML.   espacios, distribución,
                                                  animaciones y diseño
                                                  adaptable.

  **Tailwind CSS**        Framework de CSS basado Construir diseños
                          en clases utilitarias.  directamente en el HTML
                                                  usando clases pequeñas
                                                  que representan
                                                  propiedades CSS.

  **Bootstrap**           Framework de CSS (y     Crear interfaces
                          también incluye         rápidamente con una
                          componentes             cuadrícula, clases
                          JavaScript).            prediseñadas y
                                                  componentes como
                                                  botones, tarjetas,
                                                  menús y formularios.
  -----------------------------------------------------------------------

**Idea clave:** CSS es la base del diseño web. Tailwind y Bootstrap son
herramientas construidas sobre CSS que ayudan a escribir estilos de
maneras diferentes.

------------------------------------------------------------------------

## 2. CSS tradicional

### ¿Cómo funciona?

Se selecciona un elemento HTML y se escriben sus reglas dentro de un
archivo `.css`, normalmente enlazado al HTML.

### ¿Cómo se nombra?

En CSS se utilizan **selectores** para indicar qué elemento se va a
modificar:

  -----------------------------------------------------------------------
  Selector                Cómo se escribe         Qué selecciona
  ----------------------- ----------------------- -----------------------
  Etiqueta                `h1`                    Todos los elementos
                                                  `<h1>`.

  Clase                   `.titulo`               Los elementos que
                                                  tengan
                                                  `class="titulo"`.

  ID                      `#guardar`              El elemento que tenga
                                                  `id="guardar"`.

  Descendiente            `.menu a`               Los enlaces `<a>` que
                                                  estén dentro de un
                                                  elemento con clase
                                                  `menu`.

  Pseudoclase             `button:hover`          El botón cuando el
                                                  cursor pasa sobre él.
  -----------------------------------------------------------------------

**Regla importante:** en HTML la clase se escribe sin punto
(`class="titulo"`), pero en CSS se selecciona con punto (`.titulo`).
Para un ID, HTML usa `id="guardar"` y CSS lo selecciona con `#guardar`.


Ejemplos de propiedades:

  ----------------------------------------------------------------------------
  Propiedad               Uso                     Ejemplo
  ----------------------- ----------------------- ----------------------------
  `color`                 Color del texto         `color: white;`

  `background-color`      Color de fondo          `background-color: black;`

  `font-size`             Tamaño de letra         `font-size: 18px;`

  `margin`                Espacio exterior        `margin: 20px;`

  `padding`               Espacio interior        `padding: 12px;`

  `border`                Borde                   `border: 1px solid gray;`

  `display`               Tipo de distribución    `display: flex;`

  `justify-content`       Alineación en el eje    `justify-content: center;`
                          principal de Flexbox    
  ----------------------------------------------------------------------------

## 3. Tailwind CSS

### ¿Cómo funciona?

Tailwind permite aplicar estilos mediante **clases utilitarias**
directamente en el atributo `class` del HTML. Cada clase representa una
utilidad, como color, margen, tamaño, alineación o diseño.

**Ejemplo en HTML:**

``` html
<h1 class="text-3xl font-bold text-blue-700 text-center">
    Hola, mundo
</h1>

<button class="bg-green-600 text-white px-4 py-2 rounded-lg hover:bg-green-700">
    Guardar
</button>
```

En este ejemplo no se creó una clase propia en un archivo CSS. Las
clases de Tailwind aplican directamente las propiedades.

### ¿Cómo se nombra?

Tailwind utiliza nombres de clases predefinidos. Algunos ejemplos:

  ----------------------------------------------------------------------------
  Clase de Tailwind       ¿Qué hace?              Equivalente aproximado en
                                                  CSS
  ----------------------- ----------------------- ----------------------------
  `text-center`           Centra el texto         `text-align: center;`

  `font-bold`             Pone texto en negrita   `font-weight: bold;`

  `text-xl`               Define un tamaño de     `font-size: ...;`
                          texto                   

  `bg-blue-500`           Aplica un fondo azul    `background-color: ...;`

  `text-white`            Pone el texto blanco    `color: white;`

  `p-4`                   Agrega espacio interior `padding: ...;`

  `m-4`                   Agrega espacio exterior `margin: ...;`

  `rounded-lg`            Redondea las esquinas   `border-radius: ...;`

  `flex`                  Activa Flexbox          `display: flex;`

  `items-center`          Alinea elementos en el  `align-items: center;`
                          eje transversal         

  `justify-center`        Centra en el eje        `justify-content: center;`
                          principal               

  `w-full`                Ocupa todo el ancho     `width: 100%;`
                          disponible              

  `hover:bg-blue-700`     Cambia el fondo al      Regla CSS con `:hover`
                          pasar el cursor         
  ----------------------------------------------------------------------------


### ¿Cuándo conviene utilizarlo?

-   Cuando se quiere diseñar rápidamente sin crear muchas reglas CSS
    propias.
-   Cuando se necesita personalizar bastante la apariencia.
-   Cuando el equipo conoce y maneja sus clases utilitarias.
-   En proyectos donde se desea mantener los estilos cerca del HTML.
------------------------------------------------------------------------

## 4. Bootstrap

### ¿Cómo funciona?

Bootstrap es un framework que ofrece clases CSS ya preparadas y
componentes para construir interfaces. Se pueden usar sus clases en el
HTML sin escribir desde cero todos los estilos.

**Ejemplo en HTML:**

``` html
<div class="container mt-4">
    <div class="card">
        <div class="card-body">
            <h5 class="card-title">Mi tarjeta</h5>
            <p class="card-text">Descripción del contenido.</p>
            <button class="btn btn-primary">Guardar</button>
        </div>
    </div>
</div>
```

En este caso, `container`, `card`, `card-body`, `btn` y `btn-primary`
son clases que Bootstrap ya define.

### ¿Cómo se nombra?

Bootstrap tiene nombres de clases propios y convenciones bastante
reconocibles:

  -----------------------------------------------------------------------
  Clase de Bootstrap                  ¿Qué hace?
  ----------------------------------- -----------------------------------
  `container`                         Crea un contenedor con ancho
                                      adaptable.

  `row`                               Crea una fila dentro de la
                                      cuadrícula.

  `col`                               Define una columna flexible.

  `col-md-6`                          Ocupa 6 de las 12 columnas desde el
                                      punto de quiebre `md`.

  `btn`                               Aplica el estilo base de botón.

  `btn-primary`                       Aplica el estilo de botón
                                      principal.

  `btn-success`                       Aplica el estilo de botón de éxito.

  `card`                              Crea una tarjeta.

  `card-body`                         Define el cuerpo de una tarjeta.

  `text-center`                       Centra el texto.

  `mt-3`                              Agrega margen superior.

  `p-3`                               Agrega espacio interior.

  `d-flex`                            Activa Flexbox.

  `justify-content-center`            Centra elementos en el eje
                                      principal.
  -----------------------------------------------------------------------

### Ejemplo de cuadrícula (Grid)

Bootstrap divide el ancho de una fila en 12 columnas. Por ejemplo:

``` html
<div class="container">
    <div class="row">
        <div class="col-md-6">Columna izquierda</div>
        <div class="col-md-6">Columna derecha</div>
    </div>
</div>
```

Cada `col-md-6` ocupa la mitad de la fila a partir del tamaño de
pantalla `md`. En pantallas más pequeñas, las columnas pueden apilarse
según las reglas de la cuadrícula.

### ¿Cuándo conviene utilizarlo?

-   Cuando se necesita crear una interfaz rápidamente.
-   Cuando sirven los componentes prediseñados, como tarjetas, botones,
    menús y formularios.
-   Cuando se quiere usar una cuadrícula adaptable sin construirla desde
    cero.
-   En proyectos académicos, prototipos y aplicaciones donde la rapidez
    y la consistencia son importantes.

**Nota:** Bootstrap ofrece componentes JavaScript interactivos ---por
ejemplo, menús desplegables o modales--- que requieren incluir su
JavaScript y, según la instalación, sus dependencias.

------------------------------------------------------------------------

## 5. Comparación directa

  -----------------------------------------------------------------------
  Característica    CSS tradicional   Tailwind CSS      Bootstrap
  ----------------- ----------------- ----------------- -----------------
  Forma de aplicar  Selectores y      Clases            Clases y
  estilos           reglas en CSS     utilitarias en    componentes
                                      HTML              prediseñados

  ¿Hay que escribir Sí, normalmente   No siempre; se    No siempre; se
  CSS propio?                         puede             puede
                                      complementar      personalizar

  Personalización   Muy alta          Alta              Alta, aunque
                                                        parte de una
                                                        apariencia
                                                        predeterminada

  Rapidez inicial   Depende de lo que Rápida cuando se  Muy rápida con
                    se construya      conocen las       componentes
                                      clases            listos

  Clases            Las define el     `bg-blue-500`,    `btn`, `card`,
  características   desarrollador     `p-4`, `flex`     `container`,
                                                        `row`

  Diseño adaptable  Se construye con  Utilidades        Cuadrícula y
                    media queries y   responsivas como  clases
                    otras técnicas    `md:flex`         responsivas como
                                                        `col-md-6`

  Ideal para        Control detallado Diseños           Interfaces
                    y estilos propios personalizados    rápidas con
                                      con utilidades    componentes
                                                        comunes
  -----------------------------------------------------------------------

## 6. El mismo botón en las tres opciones

**Con CSS tradicional**

HTML:

``` html
<button class="boton">Guardar</button>
```

CSS:

``` css
.boton {
    background-color: #0d6efd;
    color: white;
    padding: 10px 16px;
    border: none;
    border-radius: 6px;
}
```

**Con Tailwind CSS**

``` html
<button class="bg-blue-600 text-white px-4 py-2 rounded-md">
    Guardar
</button>
```

**Con Bootstrap**

``` html
<button class="btn btn-primary">
    Guardar
</button>
```

Los tres ejemplos buscan un resultado similar, pero cada tecnología
organiza y nombra los estilos de manera diferente.

------------------------------------------------------------------------

## 7. ¿Se pueden combinar?

Sí, pero conviene hacerlo con orden.

-   **CSS + Bootstrap:** es una combinación común. Bootstrap aporta
    componentes y CSS permite personalizarlos.
-   **CSS + Tailwind:** también se puede combinar, por ejemplo, para
    crear estilos especiales que no se resuelvan cómodamente con
    utilidades.
-   **Bootstrap + Tailwind:** técnicamente pueden coexistir, pero no
    suele ser necesario. Sus estilos y convenciones pueden competir o
    generar confusión.

Para un proyecto grupal, es recomendable acordar una estrategia antes de
empezar: qué framework se utilizará, cómo se nombrarán las clases
propias y en qué archivo se escribirán los estilos personalizados.

## 8. ¿Cuál debería utilizar?

No existe uno que sea siempre mejor. Depende del objetivo:

-   **Elige CSS tradicional** si quieres aprender los fundamentos y
    tener control completo del diseño.
-   **Elige Tailwind CSS** si quieres construir diseños personalizados
    usando clases utilitarias directamente en el HTML.
-   **Elige Bootstrap** si quieres avanzar rápido con componentes y una
    cuadrícula ya preparados.

### Truco para reconocerlos al revisar un proyecto

-   Si encuentras reglas como `.menu { ... }` o `#principal { ... }`
    dentro de archivos `.css`, estás viendo CSS tradicional.
-   Si encuentras muchas clases como `flex`, `p-4`, `text-lg`,
    `bg-red-500` o `md:grid-cols-2`, probablemente estás viendo Tailwind
    CSS.
-   Si encuentras clases como `container`, `row`, `col-md-6`,
    `btn btn-primary` o `card`, probablemente estás viendo Bootstrap.

------------------------------------------------------------------------

## 9. Glosario rápido

  -----------------------------------------------------------------------
  Término                             Significado
  ----------------------------------- -----------------------------------
  HTML                                Lenguaje que estructura el
                                      contenido de una página.

  CSS                                 Lenguaje que define la apariencia
                                      de los elementos HTML.

  Framework                           Conjunto de herramientas y
                                      convenciones que facilita el
                                      desarrollo.

  Clase (`class`)                     Atributo HTML que permite asociar
                                      uno o varios nombres de clase a un
                                      elemento.

  Selector                            Patrón CSS que identifica los
                                      elementos a los que se aplican
                                      reglas.

  Propiedad                           Aspecto que se quiere modificar,
                                      por ejemplo `color` o `margin`.

  Valor                               Configuración asignada a una
                                      propiedad, por ejemplo `red` o
                                      `20px`.

  Responsive                          Adaptación de una página a
                                      diferentes tamaños de pantalla.

  Componente                          Elemento de interfaz reutilizable,
                                      como una tarjeta o un menú.

  CDN                                 Forma de cargar archivos de una
                                      biblioteca desde una red de
                                      distribución de contenido.
  -----------------------------------------------------------------------

**Conclusión:** CSS es el lenguaje que permite dar estilo a una página;
Tailwind y Bootstrap son frameworks que facilitan ese trabajo, pero lo
hacen con métodos y nombres de clases diferentes.
