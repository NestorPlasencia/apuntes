#### 1. Descarga el código del proyecto

[Codigo del proyecto ](https://github.com/platzi/invie-responsive/archive/master.zip)

#### 2. Bienvenidos al curso de responsive design
#### 3. ¿Qué es responsive design?

> Motivación de Responsive Design

* La rápida adopción de smartphones
* Múltiples tipos de pantalla
* No solo pantallas pequeñas sino pantallas más grandes
* El avance de la tecnología
* Problemas con SEO y desarrollo en sitios m.dominio.com 
* Internet móvil

> Patrones de diseño:

* **Mostly fluid**: Elementos que están a la derecha van a ir bajando para formar una columna.

  ![1527440475265](C:\Users\Nestor\AppData\Local\Temp\1527440475265.png)

* **Column drop:** Columnas una al lado de la otra que van cayendo para hacer un sitio mas sencillo. Se estiran a lo largo del ancho de la pantalla.

  ![1527440665087](C:\Users\Nestor\AppData\Local\Temp\1527440665087.png)

* **Layout shifter:** Sitios web más complejos. Tienen multiples diseños de acuerdo al ancho de la pantalla.

  ![1527440799372](C:\Users\Nestor\AppData\Local\Temp\1527440799372.png)

* **Tiny tweaks:** Patron más sencillo. Hace pequeños cambios, como cambiar el tamaño de imagenes, ajustar el texto o desplazar elementos de multiples formas.

  ![1527440873867](C:\Users\Nestor\AppData\Local\Temp\1527440873867.png)

* **Off canvas:** sacar nuevos paneles haciendo swipe hacia los costados.

  ![1527440908947](C:\Users\Nestor\AppData\Local\Temp\1527440908947.png)

> Consideraciones de desarrollo

* En smartphones vamos a tener que trabajar en portrait (vertical) y landscape (horizontal).
* Viewport: area visible de nuestro navegador.
* Unidades de medida: para responsive debemos utilizar medidas relativas como %, em, rem, vh y vw
* Densidad de pixeles: hay que tener presente que muchas pantallas tienen 2 pixeles por capa pixel, por lo que algunas imagenes pueden verse alteradas.
* Tab: ya no son clicks, los eventos de interaccion ahora son tabs (touch events).
* Gestos: Hay multiples eventos llamados gestos, como pueden ser tocar con 2, 3, 4 dedos, hacer swipe, zoom, entre otros.
* Estrategias: Hay que saber hacia que dispositivos va enfocado nuestro sitio web en su mayoria: hacia desktop o mobile. Para empezar con él y adaptarlo a las otros dispositivos.
* Carga del sitio: el sitio debe ser ligero, la idea es que el sitio cargue lo más rápido posible.

> Graceful degradation = Desktop first 

> Progressive enhancement = Mobile first 

#### 4. Presentación del proyecto
#### 5. Tipos y formas de agregar media queries

> Agregar viewport para mobiles

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0"> 
```

> Incluir mediaqueries

* Ccs externo

```html
<link rel=“stylesheet” href=“css/invie.css”/>
<link rel=“stylesheet” media="(max-width: 800px)" href=“css/media-querie.css”>

```

Los cambios se agregan a media-quierie.css

* Dentro del ccs original

```css
@media screen and (max-width: 800px) {
	body{
		background: peru;
		border:15px solid lightblue;
	}
}
```

> Los media types más típicos son:

* **all:** para todo (valor por defecto).
* **print:** en la vista previa de impresión y a la hora de imprimir.
* **screen:** para las pantallas de ordenador.
* **tv:** para televisores.

#### 6. Adaptando nuestro proyecto para Tablets

Inicio de cajas

* **box-sizing: content-box;** en el cual el ancho del elemento se incluye solo el contenido. 
* **box-sizing: border-box;** en el ancho se incluye el contenido, padding y border. 

Medidas mas utilizadas para cortes

* 1366 1080 1024 768 480 y 320  

Pueden probar como se ve su pagina en distintos dispositivos con la siguiente utilidad online  

* [Quirktools](http://quirktools.com/screenfly/)

#### 7. Adaptando nuestro proyecto para dispositivos móviles

Medidas  de Boostrap

* Móvil

``` css
 @media (min-width: 576px) { … }
```

* tablets, 768px a +

```css
@media (min-width: 768px) { … }
```

* desktops 992px a +

```css
@media (min-width: 992px) { … }
```

* desktops, 1200px a +

```css
@media (min-width: 1200px) { … }
```

#### 8. Utilizando el patrón off-canvas en el menú superior

```css
@media (max-width: 500px) { 
	.menu {
        position: fixed;
        background-color: rgba(0,0,0,0.8);
        top: 0;
        bottom: 0;
        right: 0;
        width: 100%;
        left: -100%; 
        z-index: 10;
        transition: .3s; 
    }
    .menu.active {
        left: 0;
    }
}
```

Cambiar clase y evento touch con JavaScript

```javascript
var $burguerButton = document.getElementById('burguer-button');
var $menu = document.getElementById('menu');
$burguerButton.addEventListener('touchstart',toggleMenu);
```

```javascript
function toggleMenu(){
	$menu.classList.toggle('active')
};
```

#### 9. Corrigiendo resoluciones con meta-viewport

Emmet pueden escribir “meta:vp” y presionar tab y se les autocompletará de esta forma:

```html
<meta name="viewport"content="width=device-width,user-scalable=no,initial-scale=1.0,maximum-scale=1.0,minimum-scale=1.0">
```

####10. Cómo utilizar media queries con JavaScript

```javascript
let consulta = window.matchMedia('(max-width: 500px)');
consulta.addListener(mediaQuery);         
```
```javascript
function mediaQuery() {
	if(consulta.matches) {
    	$burguerButton.addEventListener('touchstart',toggleMenu);
	}else {
    	$burguerButton.removeEventListener('touchstart',toggleMenu);
	}    
}        
```

#### 11. Optimizando la carga de imágenes con lazy loading

```html
<img data-src="image.jpg"
	 alt="Image description" />		
```

``` html
<script src="https://cdnjs.cloudflare.com/ajax/libs/blazy/1.8.2/blazy.min.js"></script>
```

```javascript
var bLazy = new Blazy({
    selector: 'img'
});
```

 [Documentación Be Lazy](http://dinbror.dk/blazy/)

####12. Agregando videos de manera responsive

```html
<div class="contenedor-iframe">
     <iframe class ="iframe" 
             src="ruta del archivo" 
             width="560" 
             height="315" >
	</frame>
</div>
```

```css
.contenedor-iframe{
    position:relative;
	padding-top: 56.25%; /* = (height(px)x100)/width(px)*/
}
```

```css
.iframe{
    position:absolute;
    top:0;
    right:0;
    bottom:0;
    left:0;
    height: 100%;
    width: 100%;
}
```
#### 13. Soportando múltiples resoluciones de pantalla

Resolucion Apple Products

- iPhone 4: 326 PPI
- iPod Touch 4 generación: 326 PPI
- Nuevo iPad: 264 PPI
- MacBook Pro: 220 PPI

```html 
<img srcset="imagen1 1x, imagen2 2x" />
```
> Be lazy

```html 
<img data-src="image.jpg | imagen2x.jpg"
	 alt="Image description" />		
```

Crear un servidor estatico en python, para servir web y visualizar en otros disposiitivos.

python 3
```python 
python python -m http.server 80
```
python 2
```python 
python -m SimpleHTTPServer 8080
```

 Obtener el radio de pantalla con JavaScript

```javascript
let value = window.devicePixelRatio;
```
Media query para patallas retina 

```css  
@media screen and (-webkit-min-device-pixel-ratio: 2) {
    /* Ex. Imagenes en 2x retina*/
}
```

####14. Construyendo tablas responsive

```html	
<section class="tabla">
	<div class="contenedor">
		<table>
			...
         </table>
	</div>
</section>   
```

```css
.tabla.contendor { 
	overflow: auto;
} 
```

#### 15. Testeando nuestro sitio con Remote Debugging 

**IOS**

> Safari en iPhone

Settings > Avanzado > Inspector Web

> Safari Mac

Settings > Avanzado > Mostrar el menú de desarrollo

Desarrollo > iPhone de xxxx > Website (Abierto en iPhone)

**ANDROID**

> Para entrar en modo programador

Settings > Información del Sistema > Numero de compilación (mas de 6 Touch) 

Settings > Operaciones del programador > Depuracion por USB [check]

Chrome PC

[chrome://inspect/#devices](chrome://inspect/#devices)  > Inspeccionar

#### 16. Añadiendo gestos touch a nuestro menú con HammerJS

[HammerJS](https://hammerjs.github.io/)

* Swipe 
* Pan
* Tap
* Press 
* Rotate
* Pitch / Zoom

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/hammer.js/2.0.8/hammer.js
"></script>
```
```javascript
var $body = document.body; 
var gestos = new Hammer($body);
gestos.on('swipeleft',hideMenu); 
gestos.on('swiperight',showMenu);
```
```javascript
function showMenu(){
    $menu.classList.add('active');
}
```

```javascript
function hideMenu(){
    $menu.classList.remove('active');
}
```

#### 17. Refinando detalles

Añadir una clase al body cuando pulsamos el burguer-button para que se abra el menú (pongamos “opened”) y que *body.opened* tenga la propiedad *overflow:hidden*. De este modo, cuando el menú se muestra, el scroll de la página por debajo del menú deja de estar activo. 

```css
.opened {
	overflow: hidden;
}
```

````javascript
function toogleMenu(event) {
    $menu.classList.toggle('active');
    document.body.classList.toggle('opened');
    $burguerButton.classList.toggle('icon-close');
}
````

#### 18. Deploy to Github Pages
#### 19. Optimizando la carga del sitio

>  Reducir el tamaño de las imagenes

[tinypng.com](tinypng.com)

> Para minificar css

[http://csscompressor.com/](http://csscompressor.com/) 

```html
<link rel="stylesheet" href="css/invie.min.css"/>
```

Poner al final del los scripts

> Estilos para above the fold

En términos de diseño web, “*above the fold*” se refiere a **toda la información que aparece en pantalla en una primera carga,** o lo que es lo mismo: la porción de la página que un usuario puede ver al acceder a la misma **sin necesidad de hacer scroll** (de ahí que también se refiera a este concepto como *above the scroll*).  

Herramienta para extraer el CSSCritical perteneciente al Above

[https://jonassebastianohlsson.com/criticalpathcssgenerator/](https://platzi.com/clases/responsive-design/concepto/construyendo-nuestro-proyecto3842/optimizando-la-carga-del-sitio/material/url) 

```HTML
<style>
      @font-face{font-family:'icomoon'; ...
</style>
```

> Carga asincrona de google fonts

```html
<script type="text/javascript">
	WebFontConfig = {
        google: { families: [ 'Montserrat:400,700:latin', 'Allerta::latin' ] }
    };
    (function() {
         var wf = document.createElement('script');
         wf.src = 'https://ajax.googleapis.com/ajax/libs/webfont/1/webfont.js';
         wf.type = 'text/javascript';
		wf.async = 'true';
		var s = document.getElementsByTagName('script')[0];
		s.parentNode.insertBefore(wf, s);
     })(); 
</script>
```

#### 20. Cierre del curso
#### 21. Desafio 1:  Mezclas de transiciones con responsive
#### 22. Desafío 2:  Hacer una transición al cargar las imagenes con bLazy
#### 23. Stream 1: Resolviendo el primer desafío
#### 24. Stream 2: Resolviendo el segundo desafí