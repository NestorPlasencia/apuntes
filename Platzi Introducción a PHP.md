#### 1. Presentación, contenidos y proyecto
#### 2. Características de PHP

* Php es un lenguaje de programación que fue pensado originalmente para la web, generalmente lo utilizamos a través de un servidor web. 
* Es un lenguaje interpretado, esto significa que el lenguaje se ejecutará cuando hagamos peticiones al servidor. También quiere decir que necesitaremos un intérprete para poder ejecutar el código.
* Php es un lenguaje multiplataforma, lo que significa que podemos utilizarlo sobre plataformas Linux, Windows o MacOS. 
* Es un lenguaje OS (Open Source) ud pueden encontrar el código en <http://git.php.net/>.
* Php cuenta, además con integraciones con múltiples bases de datos y soporta muchos protocolos.

¿Qué no es PHP?

* Aunque es posible que ustedes hagan aplicaciones de escritorio usando PHP, no es muy recomendable. Yo les recomiendo que utilicen la herramienta más optima para el trabajo que necesitan hacer.
* PHP no es compilado, lo que quiere decir que siempre vamos a necesitar un intérprete.

#### 3. Antes de comenzar y Sintáxis

¿Qué necesitamos para programar en PHP?

Usaremos:

- **PHP: ** Lenguaje de programación
- **HTML :** Que es un lenguaje demarcado para crear páginas web.
- **JavaScript :** Que nos ayuda a programar cosas del lado del cliente.
- **CSS :** Que nos ayuda a dar estilo a nuestro sitio
- **Apache: ** Un servidor web que nos permitirá recibir peticiones, interpretarlas y devolverlas al cliente.
- **MySQL:** En bases de datos comenzaremos a utilizar MySQL.
- **XAMPP:**  Entorno de Desarrollo.

> Instalar XAMPP 

Vamos a <https://www.apachefriends.org/>, XAMPP nos ofrece un entorno de desarrollo completo de una forma muy sencilla. Este está disponible para diferentes plataformas. En este caso descarguen XAMPP que soporte PHP 7 porque esa es la versión del lenguaje que estaremos trabajando. Una vez la hayan descargado ya tienen un entorno funcional y encontrarán una pequeña consola que les permitirá manejar el estado de sus servidores. En la segunda pestaña que es para administrar servidores. Correr el servidor de Apache.

Cuando se haya instalado XAMPP ustedes pueden ir al navegador y dirigirse a localhost, el cual es el nombre del servidor que estaremos utilizando.

Desde el panel de control ustedes verán ustedes verán una opción para abrir el folder de la aplicación, esto les abrirá una carpeta en donde encontrarán un acceso directo a **htdocs**, esta es la carpeta en donde se encuentran todos los archivos que serán servidos a través del servidor web.

Vamos a crear aquí una carpeta que se llame `Curso PHP`  y con esto comenzaremos a trabajar.

- Visual Studio Code / Sublime Text - **Editor de Código**
- PHPStorm - **IDE** 

Estos son ejemplos de editores de código que podemos usar para trabajar con desarrollos en PHP.

**Sintáxis:**

Vamos a crear una nueva carpeta a la cual llamaremos `Hello-world` y dentro vamos a crear nuestro archivo `index.php`.

```php
// Un archivo de Php siempre comienza con el tag:
<?php
 	// Esto quiere decir que después de esa línea todo el código que se escriba será 			interpretado por php.
	// En este ejemplo sola utilizaremos:
	echo ‘Hello World’;
	//Php se puede cerrar utilizando el tag de cierre de php:
?>
```

Otra forma en la que podemos usar PHP es haciéndolo dentro de código HTML:

```php+HTML
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	<?php 
		echo 'Hello World';
 	?>		
</body>
</html>
```

Dentro del tag body, vamos a abrir líneas en php. De esta manera podemos entrar o salir del modo PHP.

Aunque aquí se vea así, para el cliente el código siempre será interpretado y ejecutado dentro de la interfaz.

#### 4. Manejo de Variables y Tipos de Datos en PHP

**Variables y Tipos de Datos **

* Concentramos en las variables de PHP y los tipos de datos que se utilizan con este lenguaje. 

* Conocer la función var_dump ( ).

* PHP es un lenguaje dinámicamente tipado y débilmente tipado.

* Las variables en php se construyen a partir de el signo pesos `($)` y el nombre de la variable.

  ```php
  $nombreDeLaVariable
  ```

* Cuando utilizamos `//` es una forma a de ingresar notas dentro de nuestro código. 

* Un nombre de variable válido comienza con un guión bajo o con una letra.

Por ejemplo en este caso vamos a utilizar:

```php
$intVar = 1; 
```

Ahora vamos a utilizar la variable var_dump para saber el valor de la variable que acabamos de utilizar.

```php
var_dump($intVar);
```

De la misma manera, para crear un flotante, es decir un número con decimales se utiliza:

```php
$floatVar = 1.2;
```

Y para saber cuál es su valor simplemente invocamos var_dump( ).

```php
var_dump($floatVar);
```

Con una variable tipo string:

```php
$stringVar = 'Sample Text';
var_dump($stringVar);
```

Tenemos además, otro tipo de dato conocido como Boleano:

```php
$boolVar = true;
var_dump($boolVar);
```

Arreglos son valores que se guardan dentro de una sola variable. Un ejemplo de un arreglo es:

```php
$arrayVar = ['valor1', 12, 1.3];
Var_dump($arrayVar);
```

Es importante notar que php empieza a contar desde cero cuando hacemos arreglos.

> Variables para formularios 
>
> ```php
> $_GET['input'];
> ```
>
> ```php
> $_POST['input'];
> ```
>
> ```php
> $_REQUEST['input'];
> ```

> **Constantes**
>
> ```php
> define('nombre','Juan Carlos');
> ```

> **Existencia de una variable**
>
> ```php
> isset($nombreDeLaVariable);
> ```

#### 5. Utilización de Cadenas de Caractéres en PHP

Diferencia entre comillas dobles (“) y comillas simples (‘).

* Cuando ustedes usan comillas simples (‘) todo el texto que ustedes escriben aparecerá tal cual del lado del cliente.
* Cuando se usan comillas dobles (“) PHP tratará de expandir las variables, es decir, traer valor de una variable y ponerlo en la cadena. Php tratará de evaluar la cadena para ver si existen caracteres de escape o variables.

```php
$intVar = 5;
echo 'Hello $intVar'; //Hello $intVar
echo "Hello $intVar"; //Hello 5
```

Una de las cosas más interesantes de PHP es que es dinámincamente tipado, eso quiere decir que le podemos cambiar el tipo de dato que le asignamos a una variable.

```PHP
$newVar = 6;
$newVar = 'String';
```

Otro detalle importante es que PHP tratará de hacer cast cuando ustedes quieran hacer operaciones entre ellas. **Cast** significa cambiar el tipo de una variable a otro.

Si ustedes intentan concatenar una cadena con un entero, PHP intentará convertir el entero en cadena para crear esa concatenación.

```php
$intVar = 5;
$stringVar = 'Hello' . $intVar;
echo $stringVar; //Hello 5
```

En otros lenguajes de programación tendríamos un error aquí debido a que estamos tratando de concatenar una cadena con un entero, pero en Php esto no pasa. El resultado sigue siendo el mismo.

```php
$stringVar = 'Hello';
$intVar = 5;
$stringVar .= $intVar;
echo $stringVar; // Hello5
```



#### 6. Arreglos

Crearemos una variable llamada $arrayVar, dentro de esta vamos a definir unos valores.

Nosotros podemos modificar las llaves por cadenas sin ningún problema. Php solo usa relaciones entre llaves y valores, por eso no importa que exista un orden específico.

¿Cómo accedemos a un elemento individualmente?
Para acceder a un elemento individualmente lo que necesitamos hacer es utilizar los corchetes:

```php
$arrayVar = [
	'Color1' => 'red',
	'Color2' => 'blue',
	3 => 'black',
];
var_dump($arrayVar[3]);
```

De esta manera podemos imprimir el valor que corresponde a la cadena o el número que hemos definido como la llave de el arreglo individual.

> Otra forma de declarar arrays
>
> ```php
> $arrayVar = array(
> 	'Color1' => 'red',
> 	'Color2' => 'blue',
> 	3 => 'black',
> );
> ```

Arreglos multidimensionales:

```php
$multiArray = [
    'primer grupo' => array(
        'chicos' => array('Eduardo','Francisco','Jhon'),
        'chicas' =>array('Jhoana','Ana','Abril')
    ),
    'segundo grupo' => array(
        'chicos' => array('Bernardo','Pablo','Edgar'),
        'chicas' => array('Susana','Clara','Bety')
    )
];
echo $multiArray['primer grupo']['chicas'][1];
```

#### 7. Operadores - Aritméticos

-Un operador es algo que toma uno o más valores para producir como resultado otro valor.
-La clasificación de operadores se da normalmente con base en su uso.

**Operadores Aritméticos:**

Los operadores aritméticos son operaciones que se pueden realizar dentro de php. Se pueden hacer sumas, restas, multiplicaciones y divisiones que nos permiten saber determinados datos.

````php
+$a	     // Identidad Conversión de $a a int o float según el caso. 
-$a	     // Negación Opuesto de $a. 
$a + $b	 // Adición	Suma de $a y $b. 
$a - $b	 // Sustracción	Diferencia de $a y $b. 
$a * $b	 // Multiplicación	Producto de $a y $b. 
$a / $b	 // División Cociente de $a y $b. 
$a % $b	 // Módulo Resto de $a dividido por $b. 
$a ** $b //	Exponenciación Resultado de elevar $a a la potencia 
````

En algunos casos, los resultados de las operaciones matemáticas nos dan números con decimales, por eso, se puede utilizar un comando que haga del número flotante un número entero con int:

```php
$a = 10;
$b = 3;
$c = (int) ($a / $b);
var_dump($c);
```

Si queremos sacar el residuo de una división podemos utilizar la operación módulo con el signo de %.

#### 8. Asignación

```php
$a = 3;
$b = 4;
$c = 6;
$d = 8;
$e = 7;
$f = ‘Hello ’;

$a -= 3; // sustracción
$b *= 5; // multiplicación
$c /= 5; // división
$d %= 2; // modulo
$e += 7; // suma
$f .= ‘World ’; // contatenación
```

#### 9. Comparación

```php
var_dump(10 == 10); // bool(true)
var_dump('10' == 10); // bool(true)
var_dump('10' === 10); // bool(false)
var_dump(10 != 10); // bool(false)
var_dump('10' != 10); // bool(false)
var_dump('10' !== 10); // bool(true)
var_dump(10 <=> 10); // int(0)
var_dump(5 <=> 10); // int(-1)
var_dump(15 <=> 10); // int(1)
```

#### 10. Arrays

````php
$array1 = [
	0 => 'a',
	1 => 'b',
	2 => 'c',
];
$array2 = [
	3 => 'd',
	4 => 'e',
];
var_dump($array1 + $array2)
/*array(5) { 
	[0]=> string(1) "a" 
	[1]=> string(1) "b" 
	[2]=> string(1) "c" 
	[3]=> string(1) "d" 
	[4]=> string(1) "e" 
}*/
````

> ```php
> $array = [
> 	0 => 'a',
> 	1 => 'b',
> 	2 => 'c',
> ];
> count($array); // 5
> ```

Ahora bien, si utilizamos valores similares para comparar los valores que tenemos dentro de los arreglos tendríamos la siguiente información:

````php
$array1 = [
	2 => 'c',
	1 => 'b',
	0 => 'a',
];
$array2 = ['a','b','c'];
$result = $array1 == $array2;
var_dump($result); // bool(true)
var_dump($array1 === $array2); // bool(false)
````

#### 11. Incremento

````php
++$a	// Incrementa $a en uno, y luego retorna $a.
$a++	// Retorna $a, y luego incrementa $a en uno.
--$a	// Decrementa $a en uno, luego retorna $a.
$a--	// Retorna $a, luego decrementa $a en uno.
````

```php
$a = 1;
var_dump($a++); // int(1)
$a = 1;
var_dump(++$a); // int(2)
```

#### 12. Lógicos

```php
$a and $b   // And 'true' si tanto de $a o $b es 'true'
$a && $b    // And 'true' si tanto de $a o $b es 'true'
$a or $b    // Or  'true' si cualquiera de $a o $b es 'true'
$a || $b    // Or  'true' si cualquiera de $a o $b es 'true'
$a Xor $b   // Xor 'true' si cualquiera de $a o $b es 'true', pero no ambos.
!$a         // Not 'true' si $a no es 'true'.
```

#### 13. Null

```php
$a = null;
$result = $a ?? 'default';
var_dump($result); // string(7) 'default'
```

#### 14. Funciones en PHP

```php
function hello($name) {
	echo 'Hello ' . $name;
}
hello('Mary'); // Hello Mary
hello('Elizabeth'); // Hello Elizabeth
```

```php
function sum($a, $b) {
	return = $a + $b;
}
$c = sum(1,2);
var_dump($c); // int(3) 
```

Scope de una variable

```php
$x = 100;
function sum($a, $b) {
	$x = $b + $a;
	return $x;
}
$c = sum(1,2);
var_dump($c); // int(3) 
var_dump($x); // int(100)
```

> **Declaraciones de tipo escalar y tipo de retorno**
>
> ```php
> function suma(int $a, int $b):int {
> 	return $a + $b;
> }
> ```
>
> 

#### 15. Estructuras Condicionales

```php
$color = 'white';
if ($color == 'white'){
    echo 'Color is Black';
}elseif ($color == 'white') {
    echo 'Color is White';  
}else {
    echo 'Color not found';
} 
```

```php
$color = 'red';
switch($color) {
    case 'blue':
    	echo 'Color is blue';
    	break;
	case 'red':
    	echo 'Color is red';
    	break;
  	default:
    	echo 'Other case';
    	break;
}
```

> **Sintaxis Alternativa**
>
> ```` php
> $num = 30;
> echo ($num > 50) ? $num. " es mayor que 50" : $num. " es menor que 50"; // 30 es menor que 50
> ````
>
> Para la existencia de una variable
>
> ````php
> echo isset($variable) ? $variable : null;
> echo $variable ?? $variable
> ````

#### 16. Estructuras de Ciclos

````php
for ($i = 0; $i <= 10; $i++) {
	echo $i . '<br>';
}
````

```php
$i = 0;
while ($i <= 10) {
	echo $i . '<br>';
	$i++;
}
```

````php
$i = 11;
do {
	echo $i . '<br>';
	$i++;
} while ($i <= 10); 
// 11
````

```php
$names = ['Alex','Elizabeth','Mary'];
foreach ($names as $key => $name) {
    echo  $key." - ".$name.'<br>';
}
```

#### 17. Cargas de Archivos Externos

**Require:** Establece que el código que estas importando es absolutamente requerido, es decir, es vital para el funcionamiento de tu programa, es por ello que si el archivo especificado en la función require() no se encuentra o contiene algún error php arrojará un “Fatal Error” y la ejecución se detendrá.

```php
require 'functions.php';
```

**Include:** Por el contrario, si existe algún error en el código o el archivo no se encuentra php solo mostrará un “Warning” y programa seguirá ejecutandose. (Hay que ser cauteloso con esto, ya que si el archivo que estas incluyendo es vital para el funcionamiento del programa no sé ejecutará de la manera adecuada).

```php
include 'functions.php'';
```

**Include_once & require_once:** funcionan de la misma forma que include y require, salvo que a utilizar la version _once se impide la carga de un mismo archivo más de una vez, esto nos permite evitar errores de redeclaración de variables, funciones o clases (Es importante saber que el uso de estas versiones son mucho más pesadas y consumen más recursos, por lo que es recomendable utilizarlas solo cuándo sea necesario). 

#### 18. Manejo de Sesiones

Inicio de sesión

```php
session_start();
$_SESSION['count'] = 0;
```

Modificar la sesión

```php
session_start();
$_SESSION['count']++;
```

Resultado

```php
session_start();
echo 'Result: ' . $_SESSION['count'];
```

Eliminar 

```php
session_start();
unset ($_SESSION ['count']); // Solo count
session_destroy(); // Toda la sesión
```

#### 19. Manejo de Cookies

Inicio

```php
setcookie('count', '1', time() + 3600);
```

Modificar

```php
$value = $_COOKIE['count'];
$value++;
setcookie('count', $value);
```

Resultado

```php
echo 'Cookie value: ' . $_COOKIE['count'];
```

Eliminar 

```php
setcookie('count', null, time() - 1);
```

#### 20. Funciones Anónimas

```php
$var = function() {
	echo 'This is a closure';
};
$var(); // This is a closure
```

Incluir variable en el scope 

```php
$var2 = 1;
$var = function() use ($var2) {
	echo 'Value: '. $var2;
};
$var(); // Value: 1
```

````php
$x = 3;
$numbers = [1, 2, 3, 4, 5];
$closure = function ($n) use ($x){
	return $n * $x;
};
$result = array_map($closure, $numbers);
var_dump($result); 
/*array(5) { 
	[0]=> int(3) 
	[1]=> int(6) 
	[2]=> int(9) 
	[3]=> int(12) 
	[4]=> int(15) 
}*/
````

#### 21. Introducción a Programación Orientada a Objetos

Es un paradigma de programación que nos permite generar un código más modular y más reutilizable. 

**Clases:** Una plantilla de una entidad abstracta. 

```php
class Car {
    public $owner;
    public function move() {
        echo 'moving <br>';
    }
}
```

**Instancias:** Elementos concretos de esa clase. 

```php
$car = new Car();
$car -> move(); // moving
$car -> owner = 'Alex';
echo 'Owner: '.$car -> owner; // Owner: Alex 
```

**Métodos de Acceso**

**Public**
Los elementos declarados como Public son accesibles tanto desde fuera como desde dentro de la clase.

**Private**
Los elementos declarados como Private son accesibles sólo desde la misma clase donde fueron definidos.

**Protected**
Los elementos declarados como Protected son accesibles desde la misma clase donde fueron definidos y en sus subclases.

```php
class Car {
	private $owner = 'Mike';
	public function move() {
		echo "moving";
		echo "<br>";
	}
	public function getOwner(){
		return $this->owner;
	}
	public function setOwner($owner){
		$this->owner = $owner;
	}		
}

$car = new Car();
$car2 = new Car();
$car->setOwner('Alex');
$car2->setOwner('Max');
echo 'Owner car: '.$car->getOwner(); // Owner car: Alex
echo 'Owner car: '.$car2->getOwner(); // Owner car: Max
```

#### 22. Constructor y Destructor

Construct será llamado inmediatamente después de que nosotros creamos un nuevo objeto.

Destruct, por otro lado, será llamado en el momento en el que ya no exista ninguna referencia a nuestro objeto o en el momento en el que se termine nuestro script.

````php
class Car {
	private $owner;
    public function __construct($ownerName){
        $this->owner = $ownerName;
        echo 'construct<br>';
    }
    public function __destruct(){
    	echo 'destruct<br>';
    }    
	public function move() {
		echo "moving";
		echo "<br>";
	}
	public function getOwner(){
		return $this->owner;
	}
	public function setOwner($owner){
		$this->owner = $owner;
	}		
}

$car = new Car('Alex');
$car2 = new Car('Max');
echo 'Owner car: '.$car->getOwner(); // Owner car: Alex
echo 'Owner car: '.$car2->getOwner(); // Owner car: Max
````

#### 23. Herencia

La herencia es un proceso que nos ayuda a reutilizar código. Por medio de la herencia podemos hacer que una clase obtenga los métodos de otra clase.

Pensemos que tenemos una clase “Padre” y unas clases que sean “hijas”que ser derivan de esa clase.

A estas nuevas clases las podemos modificar y adicionar cosas nuevas sin necesidad de cambiar la clase padre. 

```php
class Vehicle {
    protected $owner;
    public function __construct($ownerName){
        $this -> owner = $ownerName;
        echo 'construct<br>';
    }
    public function move() {
        echo 'moving<br>';
    }
    public function getOwner() {
        return $this->owner;
    }
    public function setOwner($owner) {
        $this->owner = $owner;
    }
}
```

```php
class Car extends Vehicle{
    public function move() {
        echo 'Car: moving<br>';
    }
}
```

```php
class Truck extends Vehicle {
    private $type;
    public function __construct($ownerName, $type) {
        $this->type = $type;
        $this->owner = $ownerName;
    }
    public function move() {
        echo 'Truck '. $this->type . ': moving<br>';
    }
}
```

```php
$car = new Car('Alex'); //construct
$car -> move(); // Car: moving
echo 'Owner car: '.$car->getOwner(); // Owner car: Alex

$truck = new Truck('Max','Pickup'); //
$truck -> move(); // Truck Pickup: moving
echo 'Owner car: '.$truck->getOwner(); // Owner car: Max
```

#### 24. Namespaces

Los namespaces son una forma en la que podemos encapsular clases o funciones dentro de nuestro código.

Dar nombres muy genéricos a nuestro código puede ser muy problemático. Esto, generalmente, sucede cuando importamos librerías de otras personas en las que ellos han declarado una función o una variable con el mismo nombre y en ese caso habría una redeclaración.

Con los namespaces podemos dividir el código y encapsularlo. Le asignamos un nombre de espacio a nuestro código para que cuando usemos el código de alguien más no existan conflictos.

`VehicleBase.php`

```php
namespace Vehicles; //namespaces

class VehicleBase {
    protected $owner;
    public function __construct($ownerName){
        $this -> owner = $ownerName;
        echo 'construct<br>';
    }
    public function move() {
        echo 'moving<br>';
    }
    public function getOwner() {
        return $this->owner;
    }
    public function setOwner($owner) {
        $this->owner = $owner;
    }
}
```

`Car.php`

```php
namespace Vehicles; //namespaces

require_once 'VehicleBase.php';
class Car extends VehicleBase {
    public function move() {
        echo 'Car: moving<br>';
    }
}
```

`Truck.php`

```php
namespace Vehicles; //namespaces

require_once 'VehicleBase.php';
class Truck extends VehicleBase {
    private $type;
    public function __construct($ownerName, $type) {
        $this->type = $type;
        $this->owner = $ownerName;
    }
    public function move() {
        echo 'Truck '. $this->type . ': moving<br>';
    }
}
```

`index.php`

```php
include 'Car.php';
include 'Truck.php';

use Vehicles\{Car,Truck}; //namespaces   
/*
namespace en instancia
$car = new \Vehicles\Car('Alex');
$car = new \Vehicles\Truck('Max','Pickup');
*/
$car = new Car('Alex');
echo 'Owner car: '.$car->getOwner(); // Owner car: Alex

$truck = new Truck('Max','Pickup');
echo 'Owner car: '.$truck->getOwner(); // Owner car: Max
```

#### 25. Static

Definir propiedades o métodos estáticos nos permiten crear métodos y propiedades que son accesibles sin la necesidad de instanciar una clase. Pero recuerden que estos métodos no serán únicos para cada instancia, es decir que si ustedes de alguna forma modifican la propiedad estática, esta será cambiada para todos los objetos. 

`Truck.php`

```php
namespace Vehicles;
require_once 'VehicleBase.php';
class Truck extends VehicleBase {
    private static $count = 0; // static
    private $type;
    public function __construct($ownerName, $type) {
        $this->type = $type;
        $this->owner = $ownerName;
         self::$count++; // static
    }
    public function move() {
        echo 'Truck '. $this->type . ': moving<br>';
    }
    public static function getTotal() { // static
        return self::$count;
    }
}
```

`index.php`

```php
include 'Truck.php';
use Vehicles\Truck; 
$truck1 = new Truck('Alex','Pickup');
echo '<br>Total Trucks: ' . Truck::getTotal() . '<br>'; // Total Trucks: 1
$truck2 = new Truck('Max','Pickup'); 
echo '<br>Total Trucks: ' . Truck::getTotal() . '<br>'; // Total Trucks: 2
```

#### 26. Abstract y Polimorfismo

Una clase abstracta es como una clase parcialmente construida. El tipo de clases definidas como abstractas, si una clase contiene al menos un método abstracto debe ser definida como una clase abstracta.  

`VehicleBase.php`

```php
namespace Vehicles;
abstract class VehicleBase { // abstract
    protected $owner;
    public function __construct($ownerName){
        $this -> owner = $ownerName;
        echo 'construct<br>';
    }
    public function move() {
        echo $this->startEngine() . '<br>'; // abstract
        echo 'moving<br>';
    }
    public function getOwner() {
        return $this->owner;
    }
    public function setOwner($owner) {
        $this->owner = $owner;
    }
    public abstract function startEngine(); // abstract
}
```

`Car.php`

```php
namespace Vehicles; 
require_once 'VehicleBase.php';
class Car extends VehicleBase {
    public function move() {
        echo 'Car: moving<br>';
    }
    public function startEngine() { // abstract
        return 'Car: start engine';
    }
}
```

`Truck.php`

```php
namespace Vehicles; 
require_once 'VehicleBase.php';
class Truck extends VehicleBase {
    private $type;
    public function __construct($ownerName, $type) {
        $this->type = $type;
        $this->owner = $ownerName;
    }
    public function move() {
        echo $this->startEngine() . '<br>'; // abstract
        echo 'Truck '. $this->type . ': moving<br>';
    }
    public function startEngine() { // abstract
        return 'Truck: start engine';
    }
}
```

`index.php`

```php
include 'Car.php';
include 'Truck.php';
use Vehicles\{Car,Truck};
$car = new Car('Alex');
$car -> move();   // Car: start engine
                  // moving
$truck = new Truck('Max','Pickup');
$truck -> move(); // Truck: start engine
                  // Truck Pickup: moving
```

#### 27. Interface

Las interfaces nos permiten definir qué métodos debe implementar ciertas clases sin necesidad de decir cómo deben ser implementados.

Se pueden utilizar las interfaces pensando en una especia de contrato, y no en una herencia.

`VehicleBase.php`

```php
namespace Vehicles;
abstract class VehicleBase { 
    protected $owner;
    public function __construct($ownerName){
        $this -> owner = $ownerName;
        echo 'construct<br>';
    }
    public function move() {
        echo $this->startEngine() . '<br>';
        echo 'moving<br>';
    }
    public function getOwner() {
        return $this->owner;
    }
    public function setOwner($owner) {
        $this->owner = $owner;
    }
    public abstract function startEngine();
}
```

 `Car.php`

```php
namespace Vehicles; 
require_once 'VehicleBase.php';
class Car extends VehicleBase implements \Serializable {  // interface
    public function startEngine() { // abstract
        return 'Car: start engine';
    }
    public function serialize() { // interface
        echo 'Serialize<br>';
        return $this->owner;
    }
    public function unserialize($serialized) { // interface
        echo 'Unserialize<br>';
        $this->owner = $serialized;
    }
}
```

`index.php`

```php
include 'Car.php';
use Vehicles\Car;
$car = new Car('Alex'); // construct
echo 'Car Owner: ' . $car->getOwner() . '<br>'; // Car Owner: Alex
$ser = serialize($car);  // Serialize
$newCar = unserialize($ser); // Unserialize
echo 'NewCar Owner: ' . $newCar->getOwner() . '<br>'; // NewCar Owner: Alex
```

#### 28. Excepciones

Muchas veces nos podemos encontrar con una nueva forma de enfrentar errores. Esto se conoce como excepciones.

Cuando comprendemos cómo funcionan las excepciones, podremos saber cómo reaccionar a diferentes tipos de errores.

`toyCar.php`

```php
namespace Vehicles;
require_once 'VehicleBase.php';
class ToyCar extends VehicleBase {
    public function move() {
        echo $this -> startEngine() . '<br>';
        echo 'Car: moving<br>';
    }
    public function startEngine() {
        throw new \Exception('Engine not found'); // exception
    }
}
```

`index.php`

```PHP
include 'ToyCar.php';
use Vehicles\ToyCar;
$toyCar = new ToyCar('Alex'); // construct
try {
    $toyCar->move();
} catch (Exception $e) {
    echo 'This is a toy <br>'; // This is a toy
} finally {
    echo 'Finally<br>'; // Finally
}
```

#### 29. Traits

Muchos lenguajes de programación orientada a objetos utilizan un modelo de herencia. En el que usen una funcionalidad llamada trait que nos permite agregar o extender la funcionalidad de una clase sin tener la limitante de la herencia.

Agrupan funcionalidades específicas, se puede considerar que estos son clases especiales que no pueden ser especialmente llamados, estos no pueden ser instanciados de ninguna forma.

 `GPSTrait.php`

```php
namespace Vehicles;
trait GPSTrait {
    public function getPos() {
        return 'lat, long';
    }
}
```

`Car.php`

````php
namespace Vehicles; 
require_once 'VehicleBase.php';
require_once 'GPSTrait.php'; // Trait
class Car extends VehicleBase implements \Serializable {
    use GPSTrait; // Trait
    public function startEngine() { 
        return 'Car: start engine';
    }
    public function serialize() {
        echo 'Serialize<br>';
        return $this->owner;
    }
    public function unserialize($serialized) {
        echo 'Unserialize<br>';
        $this->owner = $serialized;
    }
}
````

`index.php`

````php
include 'Car.php';
use Vehicles\Car;
$car = new Car('Alex'); // construct
echo 'GPS pos: ' . $car -> getPos(); // GPS pos: lat, long
````

#### 30. Introducción a bases de datos SQL con PHP
#### 31. Conexión desde PHP a una base de datos SQL
#### 32. Insertar datos en nuestra de base de datos
#### 33. Listar nuestros usuarios de la base de datos
#### 34. Actualizar un Usuario en Nuestra Base de Datos
#### 35. Borrar un usuario de nuestra base de datos
#### 36. Cómo proteger nuestra base de datos ante ataques de SQL Injection
#### 37. Creando la vista principal del Blog usando Bootstrap
#### 38. Administrando los artículos del blog
#### 39. Guardando los blogposts en la base de datos
#### 40. Composer y carga automática de archivos
#### 41. Introducción a Front Controller
#### 42. Introducción a Router
#### 43. Renderizando las vistas desde un método
#### 44. Agregando el resto de las rutas a nuestro Router
#### 45. El patrón de diseño Model-View-Controller en PHP
#### 46. ¿Por qué usar un motor de templates en PHP?
#### 47. Instalación y configuración de Twig
#### 48. Templates de vistas con Twig
#### 49. Extendiendo layouts con Twig
#### 50. Modelos con Eloquent
#### 51. Configuración de variables de entorno
#### 52. Validaciones de formularios en PHP
#### 53. Agregando un modelo para los usuarios del blog
#### 54. Crear usuarios para el blog
#### 55. Autenticación de usuarios en PHP
#### 56. Logout de usuarios
#### 57. Protege ciertas rutas con middlewares y filtros
#### 58. Subir archivos al servidor
#### 59. Guardando un log de errores en el servidor
#### 60. Página para el detalle del blogpost
#### 61. Paginación
#### 62. Editar y borrar blogposts
#### 63. Agregar validación del lado del cliente
#### 64. Cierre del Curso