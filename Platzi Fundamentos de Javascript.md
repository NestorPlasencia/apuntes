#### 1. Bienvenido al curso#### 
#### 2. Calcula el área de un triángulo. Creando funciones

Declaración de función ES5

```javascript
function triangleArea(base, height) {
	return base * height / 2
}
```

Llamado de función

```javascript
triangleArea(5,7)
```

Declaración de función ES6

```javascript
let triangleArea = (base, height) => base * height / 2
```

#### 3. ¿Quiénes pueden pasar a ver una película? Ejercicio con condicionales, expresiones y booleanos

#### 
#### 4. Inventar un idioma manipulando strings

* Concatenar

Podemos unir dos string utilizando el operador +, por ejemplo:

```javascript
const palabra = 'Pla' + 'tzi' 
```

```javascript
palabra  |=> 'Platzi'
```

* Convertir a arrays (Split)

Podemos convertir los arrays a caracteres con el metodo split diciéndole por cual carácter dividirlo, por ejemplo

```javascript
let str = 'hola'
```

```javascript
str.split('')  |=>  ['h','o','l','a']
```

* Unir a partir de array (Join)

También podemos unir un array y convertirlo en un array usando el metodo join

```javascript
let arr = ['h','o','l','a']
```

``

```javascript
arr.join('') |=> 'hola'
```

* Metodos utiles

```javascript
str.toUpperCase() // convierte el texto a mayúscula
str.toLowerCase() // convierte el texto en minúsculas
str.endsWith('') // evalúa si el string termina con un texto
str.startsWith('') // evalúa si un string comienza con un texto
str.slice(inicio, final) // partir un carácter
str.length // cuantos caracteres tiene el string
```

#### 5. ¿Cuántos kms corre una persona en promedio? Entendiendo el ciclo 'for'
const dias = ['lunes','martes','miércoles','jueves','sábado','domingo']

for (let i=0; i < dias.length; i++) {
  console.log('dia: ', dias[i])
}



math.floor	//rendondea hacia abajo 3.9 = 3
math.ceil	//redondea para arriba 3.1 = 4
math.round	// redondea dependiendo 3.1 = 3, 3.5 = 4

#### 
6. ¿Quién gana en una pelea: Gokú o Superman? Resolviendo este problema con ciclos while

let vidaGoku = 100;
let vidaSuperman = 100;

const min_power = 5;
const max_power = 12;

const ambosSiguenVivos = () => vidaGoku > 0 && vidaSuperman > 0;
const calcularGolpe = () => Math.round(Math.random() * (max_power - min_power) + min_power);
const gokuSigueVivo = () => vidaGoku > 0

let round = 0;

while(ambosSiguenVivos())
{
  round++

  console.log(`Round: ${round}`)

  const golpeGoku = calcularGolpe();
  const golpeSuperman = calcularGolpe();

  if (golpeGoku > golpeSuperman) {
    console.log(`Goku ataca a Superman con un golpe de ${golpeGoku}`);
    vidaSuperman -= golpeGoku;
    console.log(`Superman queda en ${vidaSuperman} puntos de vida`);
  }
  else {
    console.log(`Superman ataca a Goku con un golpe de ${golpeSuperman}`);
    vidaGoku -= golpeSuperman;
    console.log(`Goku queda en ${vidaGoku} puntos de vida`);
  }
}

if(gokuSigueVivo()) {
  console.log(`Goku gano la pel#### ea. su vida es de: ${vidaGoku}`);
}
else {
  console.log(`Superman gano la pel#### ea. su vida es de: ${vidaSuperman}`);
}

#### 
7. ¿Cuánto tiempo pasó desde tu fecha de nacimiento?

const dias = [
  "domingo",
  "lunes",
  "martes",
  "miercoles",
  "jueves",
  "viernes",
  "sabado"
]

const nacimiento = new Date(1991,6,2);
const hoy = new Date(); 	
const tiempomil = hoy - nacimiento
const tiemposeg = tiempomil /1000
const tiempomin = tiemposeg / 60
const tiempohor = tiempomin / 60
const tiempodias = tiempohor / 24
const tiempoyear = tiempodias / 365
const proximo = new Date(hoy.getFullYear(), nacimiento.getMonth(), nacimiento.getDate())
console.log(dias[proximo.getDay()])

#### 
8. Calcular la distancia entre dos puntos - Objetos en JavaScript

const p1 = {
  x:0,
  y:4
}

const p2 = {
  x:3,
  y:4
}

function distancia(p1,p2) {
  const x = p1.x - p2.x
  const y = p1.y - p2.y

  return Math.sqrt(x * x + y * y)
}

distancia(p1, p2)
#### 
9. Agrega métodos para mover los puntos - Objetos Avanzado en JavaScript

const p1 = {
  x: 0,
  y: 1,
  moverEnX: function(x) { this.x = this.x + x }
}

#### 10. Definiendo la clase Punto - Prototipos en JavaScript

function Prototipo(parametroA, parametroB){
	this.atributo   = parametroA,
	this.atributo2 = parametroB
}

function Punto(x,y) {
  this.x = x
  this.y = y
}

Punto.prototype.moverEnX = function moverEnX(x) {
  this.x += x
}

Punto.prototype.moverEnY = function moverEnY(y) {
  this.y += y
}

Punto.prototype.distancia = function distancia(p) {
  const x = this.x - p.x
  const y = this.y - p.y
  return Math.sqrt(x * x + y * y)
}

const p1 = new Punto(0, 4)
const p2 = new Punto(3, 0)

console.log(p1.distancia(p2))
console.log(p2.distancia(p1))
p1.moverEnX(10)
console.log(p1.distancia(p2))
p2.moverEnY(-4)
console.log(p1.distancia(p2))


#### 11. Definiendo la clase Punto - Object.create en JavaScript

const Punto = {
  init: function init(x,y) {
    this.x = x
    this.y = y    
  },
  moverEnX: function moverEnX(x) {
    this.x += x
  },
  moverEnY: function moverEnY(y) {
    this.y += y
  }
}
const p1 = Object.create(Punto)
p1.init(0,4)



const Punto = {
  init: functioninit (x,y){
    let obj = Object.create(this)
    obj.x = x;
    obj.y =y;
    return obj
  },
  moverEnX: functionmoverEnX(x) {
    this.x += x
  },
}
let p1 = Punto.init(1,4) 

#### 12. Definiendo la clase Punto - Class en JavaScript

class Punto {
  constructor(x,y) {
    this.x = x
    this.y = y
  }
  moverEnX(x) {
    this.x += x
  }
  moverEnY(y) {
    this.y += y
}

const p1 = new Punto(0,4)
const p2 = new Punto(3,0)

#### 13. Entiende el scope de las variables


#### 14. Operaciones con arrays

function suma(...params) {
  return params.reduce((acumulativo, actual) => {acumulativo + actual}, 0)
}

suma(4,5,6,23,26,7,8)

function doble(...params) {
  return params.map(x=>x*2)
}
const dobles = (...numeros) => numeros.map(numero => numero * 2)

doble(2,3,4,5,6,7,5)

const pares = (...numeros) => numeros.filter(x => x % 2 == 0)

#### 15. Entiende los closures de JavaScript

function saludarFamilia(apellido) {
  return function(nombre) {
    console.log(`Hola ${nombre} ${apellido}`)
  }
}
let saludarPerez = saludarFamilia('Perez')
saludarPerez('Carlos')


De esta forma podemos crear nuevas funciones partiendo de funciones que recuerdan variables internas

#### 16. Estructura del lenguaje

const nombre = "Sacha"

';'[
  "lunes",
  "martes",
  "miércoles"
].forEach(function (dia) {
  console.log(dia)
})

#### 17. This, _this y los arrow functions

class Persona {
  constructor(nombre, amigos = []) {
    this.nombre = nombre
    this.amigos = amigos
  }

  listarAmigos() {
    const _this = this

    this.amigos.forEach((amigo) => {
      // console.log(`Hola, mi nombre es ${_this.nombre} y soy amigo de ${amigo}`)
      console.log(`Hola, mi nombre es ${this.nombre} y soy amigo de ${amigo}`)
    }/* .bind(this) */)
  }
}

const sacha = new Persona("Sacha", [ "Pedro", "Juan", "Pepe" ])

#### 18. La función bind

<html>
  <head>
    <style>
      * {
        font-size: 24px;
      }
    </style>
  </head>
  <body>
    <button id="boton">Off</button>
    <script src="index.js"></script>
  </body>
</html>

class Toggable {
  constructor(el) {
    // inicializar el estado interno
    this.el = el
    this.el.innerHTML = 'Off'
    this.activated = false
    this.onClick = this.onClick.bind(this)
    this.el.addEventListener('click', this.onClick)
  }

  onClick(ev) {
    this.activated = !this.activated
    this.toggleText()
  }

  toggleText() {
    this.el.innerHTML = this.activated ? 'On' : 'Off'
  }
}

const button = document.getElementById('boton')

const miBoton = new Toggable(button)

#### 19. call y apply

const sacha = {
  nombre: 'Sacha',
  apellido: 'Lifszyc'
}

function saludar(veces, uppercase) {
  let str = `Hola ${this.nombre} ${this.apellido}`
  str = uppercase ? str.toUpperCase() : str
  for (let i = 0; i < veces; i++) {
    console.log(str)
  }
}

const params = [3, true]
saludar.call(sacha, ...params)



const newFunction = fun.bind(contexto, primerParametro)

// Establece el scope y el-los parametros de fun

newFunction(segundoParametro) 

// Ejecuta fun pero con la caracteristica de que ya esta establecido el scope y los parametr#### os. Igualmente nos permite enviarle más parametros a fun si es el caso

fun.call(contexto, primerParametro, segundoParametro)

//Ejecuta fun en el scope establecido y con los parametros enviados

fun.apply(contexto, [primerParametro, segundoParametro)

//Ejecuta fun en el scope establecido y con los parametros enviados en el array

#### 20. ECMAScript: El estándar en el que se basa JavaScript
#### 21. Babel al rescate: logrando la compatibilidad buscada
#### 22. Distintas formas de escribir módulos en JavaScript
#### 23. No generes un cuello de botella en el EventLoop
#### 24. Los callbacks de JavaScript
#### 25. Callback a un servidor externo 

function get(URL, callback){
	const xhr = new XMLHttpRequest();
	xhr.onreadystatechange = function () {
		const DONE = 4
		const OK = 200
		if (this.readyState === DONE) {
			if(this.status === OK){
				callback(null, JSON.parse(this.responseText))
			}else {
				callback(new Error(`Se produjo un error al realizar el request ${this.status}`))
			}
		}
	}
	xhr.open('GET', URL);
	xhr.send(null);
}

function handleError(err){
	console.log(`Request failed: ${err}`)
}
get('https://www.swapi.co/api/people/1/', function onResponse(err, luke){
	if(err) return handleError(err)
	get(luke.homeworld, function onHomeworldResponse(err, homeworld){
		if(err) return handleError(err)
		luke.homeworld = homeworld
		console.log(`${luke.name} nació en ${luke.homeworld.name}`)
	})
	console.log(`Request succeded`)
	console.log('luke', luke)
})

#### 26. Promesas


let luke
fetch('https://www.swapi.co/api/people/1/')
    .then( response => response.json())
	.then(json => {
		luke = json
		return fetch(luke.homeworld)
	})
    .then( response => response.json())
	.then( json => {
		luke.homeworld = json
		console.log(`${luke.name} nació en ${luke.homeworld.name}`)
	})
	.catch((err)=> console.log(`Request failed: ${err}`))


#### 27. Async-await

function handleError(err) {
  console.log(`Request failed: ${err}`)
}

async function getLuke() {
  try {
    const response = await fetch('http://swapi.co/api/people/1/')
    const luke = await response.json()
    const responseHomeworld = await fetch(luke.homeworld)
    luke.homeworld = await responseHomeworld.json()
    console.log(`${luke.name} nació en ${luke.homeworld.name}`)
  } catch (err) {
    handleError(err)
  }
}

#### 28. Implementación de set timeout en JavaScript

const timeout = setTimeout(() => {
  alert('han pasado 5 segundos')
}, 5000)

#### 29. Implementación de set interval en JavaScript

let counter = 0
const interval = setInterval(() => {
  counter++
  alert(`han pasado ${counter} segundos`)
}, 1000)

#### 30. Cancelando el Timeout y el Timeinterval

clearTimeout(timeout)
clearInterval(interval)

#### 31. Qué son y cómo se implementan el callbacks  en JavaScript

const DESPERTAR = 3000;
const DUCHA = 2000;
const VESTIRSE = 2000;
const DESAYUNAR = 3000;
const PLATZI = 5000;
const $agenda = document.getElementById('agenda');

setTimeout(()=> {
  $agenda.textContent = 'Ahora me estoy duchando...';
  setTimeout(()=> {
    $agenda.textContent = 'Me estoy vistiendo...';
    setTimeout(() => {
      $agenda.textContent = 'Ahora estoy desayunando...';
      setTimeout(()=> {
        $agenda.textContent = 'Que lindo es estudiar en Platzi...';
        setTimeout(()=> {
          $agenda.textContent = 'Y javascript es mi lenguaje favorito <3';
        }, PLATZI)
      }, DESAYUNAR)
    }, VESTIRSE);
  }, DUCHA)
}, DESPERTAR)

#### 32. Eliminando el callback hell usando promesas en JavaScript

    function despertar() {
      return new Promise((resolve, reject)=>{
        setTimeout(() => {
          resolve('Ahora me estoy duchando...')
        }, DESPERTAR)
      });
    }
    
    function ducha(message) {
      $agenda.textContent = message;
      return new Promise((resolve, reject)=>{
        setTimeout(() => {
          resolve('Me estoy vistiendo...')
        }, DUCHA)
      });
    }
    
    function vestirme(message) {
      $agenda.textContent = message;
      return new Promise((resolve, reject)=>{
        setTimeout(() => {
          reject('no hay comida');
          // resolve('Ahora estoy desayunando')
        }, VESTIRSE)
      });
    }
    function desayunar(message) {
      $agenda.textContent = message;
      return new Promise((resolve, reject)=>{
        setTimeout(() => {
          // reject('no hay comida');
          resolve('Estoy estudiando')
        }, DESAYUNAR)
      });
    }
    
    function error(message) {
      $agenda.style.color = 'red';
      $agenda.textContent = message;
    }
    
    despertar()
    .then(ducha)
    .then(vestirme)
    .then(desayunar)
    .catch(error)


#### 33. Funciones Recursivas

function fibonacci(num) {
	if (num == 1) return 0
	if (num == 2) return 1
	return fibonacci(num - 1) + fibonacci(num - 2)
}

#### 34. Memoizacion

let contadorMemo = 1
function fibonacciMemo(num, memoria = {}) {
  contadorMemo++
  if (memoria[num]) return memoria[num]
  if (num == 1) return 0
  if (num == 2) return 1

  return memoria[num] = fibonacciMemo(num - 1, memoria) +
            fibonacciMemo(num - 2, memoria)
}

let contadorRec = 1
function fibonacciRecursivo(num) {
  contadorRec++
  if (num == 1) return 0
  if (num == 2) return 1

  return fibonacciRecursivo(num - 1) +
      fibonacciRecursivo(num - 2)
}

#### 35. Iteradores en JavaScript

functionfibonacci(){
	let a=0, b=1
	return{
		next: function() {
		 let f= a
		 a = b
		 b = f + a
		 return{ value: f, done: false}
		}
	}
}

const fibo = {}
fibo[Symbol.iterator] = fibonacci 

let i=0
for (let value of fibo) {
	console.log(value)
	i++
	if(i>20) break
}

#### 36. Generadores en JavaScript

function* fibonacci(){
	let a=0, b=1
	while (true) {
		let f= a
		a = b
		b = f + a
		let reset = yield f
		if(reset) a=0, b=1
	}
}

const fibo = fibonacci()
fibo 
fibo.next()
fibo.next(reset)

#### 37. Estructuras de Datos Inmutables en JavaScript
#### 38. Requisitos Técnicos 
#### 39. Creando nuestro paquete
#### 40. Escribiendo el código de nuestro paquete
#### 41. Testeando el paquete
#### 42. Publicando el paquete en NPM
#### 43. ¿Qué vamos a construir?
#### 44. Inicializando el juego
#### 45. A una ronda le sigue otra ronda
#### 46. Añadir una librería 
#### 47. Cierre del Curso
#### 48. Crear un modulo para convertir medidas de peso
#### 49. Crear un juego en HTML, tic tac toe
#### 50. Crear un tutorial




