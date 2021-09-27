# ¿Qué son los componentes?
En un principio HTML, CSS y JS eran diferentes para cada navegador, hasta que se fueron volvieron estándares. Pero jQuery fue la tecnología que hacía que JS fuese compatible en todos los navegadores.

jQuery ya murió, es inútil.

JS está tan bien que ya empieza a reemplazar a HTML. Cada vez escribimos más JS que HTML.

Los componentes son aplicar un concepto muy parecido a las funciones pero para maquetar.

Composición de componentes: Es poder crear componentes que estén hechos de otros componentes.

# ¿Cómo estructurar un componente?
Podemos identificar componentes que tienen un mismo objetivo, entonces podemos hacer composición de componentes, en el caso del ejemplo visto en clase sería:

* Logo: Esta construido por el logo de Platzi y el banner del logo (el que nos avisa si hay un live).
* Navbar: cada enlace es su propio componente y además juntos forman el navbar.
* Componente de autenticación: Engloba a los botones de iniciar plan e inicio de sesión.
* Componente de búsqueda: Compuesto por un input y un botón diseñados especialmente para estar juntos.

Hechos estos componentes podemos llegar a lo que es el menú que es otro componente que está formado por el conjunto de todo el resto de componentes que acabamos de ver. Menú cambia, es diferente dependiendo del usuario, si es nuevo le mostramos los botones de login o suscripciones, pero si ya es un estudiante entonces debemos mostrarle los puntos, notificaciones y todo lo demás.

Al igual que con el menú los componentes internos puedan variar dependiendo de lo que necesitemos, para esto nos ayuda tratarlos como funciones a las cuales les pediremos lo que necesitamos en especial.

Podemos darle atributos a un componente usando otros componentes.

NOTA: Si se tienen muchos tipos de un solo componente es señal de desorden, hay que estandarizar las cantidades de componentes.
# ¿Qué es reactividad?
**Reactividad**: Es un paradigma, una forma de pensar nuestras aplicaciociones. Deben seguir 2 reglas:

1. Responsive, es decir, deben ser resilientes (siempre sabe qué hacer) y escalables (no importa con cuánta información debemos trabajar o cuántos usuarios entran a la aplicación, la aplicación debe poder seguir funcionando sin problemas).
2. Message Driven (Arquitectura basada en mensajes). Deben de haber emisores y receptores de mensajes. Los mensajes se entregan de manera asíncrona.

**Recuerda**: La arquitectura no es ajena a la programación.

**Estado**: Es el lugar donde vamos a guardar la información reactiva de nuestros componentes. Son variables a las que nos suscribimos para recibir una notificación cada vez que cambian sus valores.

**Render**: o renderizado, es el proceso por el cual nuestro HTML, pasan a ser información visual en el DOM.

**Estrategias de render**: Virtual DOM y No Virtual DOM. Ninguna es mejor, depende del caso en particular.

Componente -> Estado -> Render -> Usuario (y vuelve a “Estado”)
# Librería vs Frameworks
## Framework

Es un conjunto de piezas de codigo que se centra en la elaboración o construción todo un proyecto a través de un conjunto de herramientas que nos brinda el framework (puede incluir librerías) como si de una receta se tratase.

## Librería

Es una porción o pieza de codigo que nos ayuda a resolver un problema en específico como trabajar con HTMLmediaElement (video o audio) por ejemplo.

# Ecosistema de frameworks y librerías JavaScript
Existen empaquetadores que nos ayudan a tener todos los archivos en produccion pero al momento de mandar al navegador sea lo mas ligero posible

* Webpack: Requiere que configuremos un archivo para especificar como queremos nuestro archivo.
* Parcel: Es evitarnos cualquier configuracion, trae todo listo para que construya toda su magia. No tenemos control de como empaqueta.
* Rollup: Se especializa en tener todo optimizado con una tecnica especial donde elimina el codigo inutil
Se dice que usemos webpack para paginas web y aplicaciones y Rollup para librerias.

Compiladores que transforman codigo Javascript que no es exactamente JS que los navegadores si pueden entender:

* Babel: Nos permite usar el codigo del futuro en proyectos que utilizan otra version, unificando todo en una version que entiendan los programadores
* TypeScript: Es un lenguaje de programacion con sus nuevas reglas que nos permiten entender mas facil los errores en JavaScript

Las herramientas para UI son para encargarse de las vistas e interaccion con los usuarios, puede ser JS solito pero si trabajamos en Frameworks se suelen usar:

* React
* Vue
* Svelt

Estan los estilos donde se pueden usar diferentes cosas, pero hay que tener en cuenta que a veces escribimos mas JS que CSS:

* CSS
* SASS
* LESS
* STYLUS

En CSS-in-JS normalmente el html, el css y el JS estaria en cada archivo individual pero esto nos permite desarrollar en los 3 lengaujes en un mismo componente, que necesariamente no es un mismo archivo.

* Styled Components
* Emotion

En los Routers son la forma en la que hacemos la navegacion de la aplicacion, muestra cierto contenido dependiendo de la URL

* React Router
* Vue Router
* Svelte Router
* LitElement Router
* Whatever Router

Los frameworks son elementos todos en uno, que se encargan de todos los apartados ya que todo lo contiene. Trabajar con un Framework acelera tu desarrollo.

Angular: Es todo poderoso pero por ser tan grande es bastante dificil de integrar con otras herramientas que no sean especiales para ANGULAR.
Los entornos de desarrollo completos son un todo en uno, un grupo de librerias configuradas para trbajar con mas librerias. se llaman mas CLI y desde la consola podemos elegir lo que queremos y configurar todo por nuestro lado.

* Create React App
* Vue CLI
* Svelte CLI
* Polymer CLI
* Whatever CLI

En el manejo de estado son las librerias que podremos definir un estandar de flujo de datos constante y predecible dentro de la aplicacion, en vez de que todos sean diferentes podremos definir un patron comun

* Redux
* XState
* MobX

En la consulta de datos son formas o protocolos para comunicarnos con el backend para enviar y recibir informacion, hay herramientas para hacer peticiones que no hacen diferencia, pero estas herramientas si hacen diferencia:

* API REST
* GraphQL

## Porque React es una librería y no un framework?
Muchas veces podemos llegar a confundir a React con un framework, cuando realmente no lo es.

La principal diferencia cuando usamos un framework a una librería, es que el framework nos va a dar todas las herramientas que necesitamos por defecto. En otras palabras, el framework nos va a estar dando todo lo que necesitamos y lo que necesitaremos para crear nuestra aplicación web desde el momento en que creamos el proyecto.

Por otro lado, la librería no, ya que es solo una herramienta aislada. La principal razón por la cual se suele confundir a React con un framework, es porque React tiene todas esas herramientas que se necesitan para hacer tu aplicación completa, pero no vienen incluidas al momento de crear el proyecto. Unos ejemplos de esas herramientas son: React DOM, React Proto, etc.

Entonces, al momento de que tu hagas tu webapp con React, puedes decidir si usar las herramientas hechas por los desarrolladores de React, o usar otras herramientas hechas por la comunidad. Esa es una gran ventaja, ya que cuando se trabaja con Angular, solo puedes usar herramientas oficiales de Angular y ya, con limitaciones para agregar librerías ajenas.

# ¿Qué es React y cómo se construyó?
ECMAScript es el estándar en el cuál se basa JS, es la especificación. Lo que conocemos como JS es la implementación que hace cada navegador de esta especificación.

En 2004/2005 se inventó ECMAScript for XML un estándar para agregarle soporte nativo de ECMAScript a XML, era como una alternativa al DOM.

En el 2010 Facebook trabajaba en XHP una “mejora” a PHP con la que querían crear componentes personalizados y reutilizables de HTML y lo integraron a su stack oficial de programación.

En 2011 bajo la influencia de XHP y los problemas de mantenimiento de código, concretamente los anuncios se crea el prototipo de React.js una herramienta para hacer aplicaciones con muy buena UX mejorando la eficiencia de los equipos de programación de FB (buena developer experience).

En 2012 cuando FB compró Instagram, React se desarrollo para ser Open Source

Llega 2014 y se crean las React Developer Tools una herramienta para debuggear los componentes en React.

En 2015 salió React Native y muchas empresas importantes deciden usar React.

## React

Todos los frameworks tienen uno o varios objetivos en específico, en el caso de React son:

* Declarativo: Se refiere a que sea fácil de leer, o sea que con su sintaxis se nos facilite entender lo que hace.
* Basado en Componentes: Que usemos componentes (los que hemos visto a lo largo de este curso).
* Multiplataforma o “Learn Once, Write Anywhere”: Al aprender React lo vamos a poder usar en todas partes con un poco de cambios minúsculos, esto pasa porque aunque es una librería no está solo, hay muchas herramientas alrededor de React, algunas son oficiales de FB y otras son de la comunidad.

Cuando usemos React para Web es juntarlo con React DOM, que es la herramienta oficial de FB para hacer el render en el DOM, si queremos hacer una app móvil debemos usar React Native y si queremos hacer aplicaciones en VR usamos React VR. La diferencia entre web, móvil y VR es que en lugar de usar div, p o etiquetas de HTML tenemos que usar componentes que nos da React, que en esencia son lo mismo.

Hay dos formas de crear componentes con React:

* Con clases: Solía ser la más popular, creamos clases de JS que extienden de React.Component y por dentro solo debemos escribir algunos métodos (como render) para indicarle a React que contenido debe renderizar. Para poder escribirlo como si fuera HTML normal usamos jsx. Los componentes de React o cualquier otro Framework tienen la característica de que pueden mostrar un contenido fijo o dinámico.
* Con estados: Nos permite es cambiar el contenido de una variable dependiendo de las interacciones de un usuario. En el ejemplo de la clase, cada vez que un usuario le de click al botón vuelve a hacer render de nuestro componente con el nuevo estado que surgió.
* React Hooks: Hoy en día esta es la formula más popular, que en lugar de usar clases, métodos, ahora usamos los React Hooks , son funciones que nos permiten leer y escribir nuestro estado de manera muy limpia, además de que lo que normalmente escribiríamos en el método render lo podemos escribir en el return de la función.

# Qué es Angular y cómo se construyó
En el 2009 un grupo de amigos Desarrolladores inventaron una herramienta para que personas que no sabian programar pero si HTML pudieran hacer aplicaciones, esto no tuvo exito. Despues uno de ellos fue a trabajar a Google Feedback. Pero para esto necesitaron 17k lineas de codigo en frontend, usando un Google Web Toolkit, pero por esto apostaron que podian hacerlo en 2 semanas, pero logro hacerlo en 3 y con 1.5k lineas de codigo, y asi nacio Angular JS, que se volvio Open Source y patrocinado por google. Es como REACT pero FB depende totalmente de este, pero Google no depende de angular. Google solo lo patrocina.

Entre 2012 y 2014 Angular era bastante popular pero con el paso del tiempo empezo su decaida, y anunciaron que lo iban a hacer desde 0 y empezar a usar componente, pero los que iban a usar a angular no sabian que iba a pasar porque no iba a tener compatibilidad.

Es dificil convinar angualar con alguna libreria o algo que no se haya hecho especificamente para angular.

Angular tiene un sistema para crear componentes que se llaman Engine Modulos o Modulos de angular, que agrupan componentes y servicios a un mismo fin o a un mismo dominio. Los componentes son la logica y la interfaz de usuario para cada pedazo de la aplicacion.

Los componentes tienen dos partes, las logicas y las partes de UI, esto lo haremos con una clase en TS. Lo definimos con algo parecido a HTML.

Los servicios son agrupaciones de codigo. Agrupaciones de logica que podemos usar en varios componentes por toda la aplicaion. Esto lo inyectamos a los componentes que usamos Inyeccion de dependencias.

Angular tiene a Angular Ivy que se encarga de renderizar los componentes en angular con Incremental DOM. Como React usa JSX, Angular tiene su variacion de HTML que no es puro. Lo que hace Angular Ivy es convertir este HTML en un JS para renderizar los componentes en el DOM.

Angular explica que crear una copia de todo el DOM es innecesario, con el Incremental DOM cada componente se convierte en Instrucciones y estas hacen que se ejecute y renderice y actualice el componente, en ningun momento crea copia del DOM y ahorra memoria.

En angular 9 reescribieron el motor completamente. Antes habia que compilar muchas veces cada que cambiabamos componentes. Con Angular Ivy cambio la forma en la que se describe para que los componentes solo se afecten asi mismos y no a los demas.

# ¿Qué es Vue y cómo se construyó?
“El Framework progresivo”

No es un framework tan abrumador como Angular, pero aún así puede ir escalando progresivamente a medida que lo vamos necesitando.

Escalable pero no flexible.

Se integra bien con cualquier herramienta que queramos utilizar.

Es completamente Reactivo.

Vue también usa el Virtual DOM.

En pocas palabras, al principio Vue nos deja trabajar al principio casi como si siguiéramos usando HTML común y corriente pero poco a poco le vamos metiendo JS usando Vue hasta que llega un momento en el que prácticamente todo la aplicación está hecha en JS con componentes de Vue.

Nos deja trabajar con componentes pero no es obligatorio en un inicio.

“El mejor performance”
# ¿Qué es Svelte y cómo se construyó?
Su principal característica es que no crea intermediarios entre el código escrito en Svelte y el DOM.

Usa el tiempo de compilación en la etapa de desarrollo mientras nosotros estamos desarrollando para que el código compilado sea el código ideal que necesita el DOM para renderizarse y actualizarse.

No usa el Virtual DOM

Svelte es muy bueno para hacer sitios web donde lo importante es el contenido que vamos a mostrar.

No es muy bueno en aplicaciones web donde lo más importante es la interacción intensiva con los usuarios.

## Arquitectura Svelte

Es un compilador, y como cualquier compilador necesita generar un AST(una representación de todo el código de nuestros componentes) en forma de árbol; Para está compilación necesita tres parse, uno para el HTML, otro para JS y el otro para CSS, combina estos 3 árboles y obtiene toda la información que necesita de nuestros componentes.

Envuelve todo el código de cada componente en fragments, una interfaz de API del navegador que nos sirve para encapsular nodos y pedazos del DOM, sin afectar la interfaz de la página. Los fragments no se transforman en algo que los usuarios puedan ver, o en algo que afecte el contenido o estilos de nuestra página. Es como un nodo imaginario.

# CSS-in-JS
CSS-in-JS es una técnica de diseño en la que se usa JavaScript para diseñar componentes. Cuando se analiza este JavaScript, se genera CSS y se adjunta al DOM. Permite abstraer CSS al nivel de componente en sí, usando JavaScript para describir estilos de una manera declarativa y mantenible.

# Tipos de aplicaciones según su router: SPAs vs. SSR
Antes de las aplicaciones web modernas se usaba el SSR “viejo” (Server Side Rendering), con el que el backend usaba una plantilla de HTML le daba a la plantilla los datos específicos requeridos en cada petición y le enviaba el HTML al navegador. Está forma de hacer render es rápida solo al principio porque el backend no le entrega al navegador la forma de interactuar con los usuarios

## SPAs y CSR

Single Page Applications: Se inventa el Client Side Routing aquí gracias en parte a las API’s se empezó a renderizar el contenido desde JS directamente en el navegador. Es decir, el backend le entregaba al navegador un HTML prácticamente vacío, que tenía solo la petición de un script o alguna hoja de estilos. Entonces el navegador recibía el HTML en blanco, descargaba el JS y CSS y entonces JS podía empezar a renderizar la aplicación, entonces la carga inicial es lentísima, pero luego se hace bastante rápida, no necesita recargarse y cuando requiere información del backend solo hace la consulta a una API (que son fundamentales para estas aplicaciones).

Para trabajar de esta forma tenemos dos componentes:

Los routers son herramientas para manejar las rutas de nuestra aplicación, normalmente de eso se encargaría el servidor.

Si no se tiene control servidor se usa

* Hash Router: Con “#” definimos en que parte de la aplicación estamos (en el home, logout, clientes, admin, etc.).

Si tienes control sobre el servidor

* Browser Router: Sin importar la ruta puedes pedirle al servidor que siempre de el mismo index.html, y con JS podemos determinar en que ruta estamos y que ruta debemos mostrar dependiendo de la ruta que nos dio el servidor o navegaron e interactuaron los usuarios.
## Progressive SSR

Gracias al CSR de la SPA se invento el SSR (Server Side Rendering combinado con Client Side Rendering).

En lugar de mandar un documento HTML vacío al navegador y tardara mucho en descargarlo, se podía acelerar el proceso, desde el backend enviamos al navegador una versión de la aplicación en HTML que los usuarios puedan ver mientras el navegador descarga los archivos de JS y vuelve a hacer render de la aplicación. Entonces, el backend le envía al navegador una versión de la app que solo se puede ver pero no tocar, es decir, los usuarios no pueden interactuar inmediatamente con la app.

NOTA: Para esto se necesita Node.js.

## Generación de Sitios Estáticos

Estos generadores nos permiten usar el Progressive SSR mientras estamos desarrollando el sitio, pero cuando lo compilamos nos generan páginas estáticas que ya tienen cargados los datos que normalmente le pediríamos al backend y cuando hacemos deploy las aplicaciones funcionan de una. Si hay algún dato que nos daba el servidor pero que sabemos que casi no va a cambiar (como un blogpost) podemos volver a hacer deploy si queremos editar el contenido no habrá problema alguno.

> "*El indice de muertes en frontend developers por no querer aprender backend es muy alto*" -Juan D. C. 
# Organización de archivos en el frontend

Hay herramientas para el manejo del estado que nos ayudan a evitar a tener codigo espaguetti. Esto se le llama Deuda tecnica, por que en el futuro tendremos problemas en el futuro. Nos demoraremos un poco mas pero siempre es bueno tener una buena organizacion.

Se divide entre **logico** vs **interfaz**. Es bueno tener una capa de UI y otra una capa de Datos. En react es bueno dividir todo entre componentes contenedores y presentacional.

## File Type First

Tipo de organizacion donde cada tipo de archivo.Una de componentes, una de contenedores, otra para rutas.
```
/components
-MenuComponent.js
-FormComponent.js

/containers
-MenuContainer.js
-FormContainer.js

/routes
-HomeRoute.js
-AboutRoute.js
```
## Feature First

donde cada componente de nuestra aplicacion es dividir una carpeta para cada elemento que tengamos. Una carpeta de Menu, una carpeta de Form, una carpeta de Button. Esta forma es buena ya que cada carpeta sera independiente y no sera tan difiicil de entender.
```
/Menu
-MenuComponent.js
-FormComponent.js

/Form
-FormUI.js
-FormLogic.js

/Button
-Button.js
-Button.styles.js
```
## Apps For Apps

Una carpeta para cada aplicacion
```
/StudentPlatform
-/components
-/containers

/BusinessPlatform
-/Form
-/Button

/SalesLanding
-/html
-/css
-/js
```
### Bonus, forma de organizar archivos en un proyecto hecho en vue
```
/assets
-/css
-/fonts
-/img
/components
-/HeaderBar
-/FooterBar
-BaseLoading.vue
/layout
/plugins
/router
/utils
/views

```
> revisa el codigo [aquí](https://github.com/baumannzone/diablo3-vue-platzi)