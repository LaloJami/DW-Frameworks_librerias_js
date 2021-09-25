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
