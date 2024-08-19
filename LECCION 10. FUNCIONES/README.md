![Diapositiva2](https://github.com/user-attachments/assets/61afcfa8-f0c0-4a20-a5d9-50366e4ced53)

# Funciones en JS
# Objetivo general 📕
Encapsular bloques de código reutilizable que realizan tareas específicas, permitiendo modularidad, organización y reducción de la repetición en el código.

# Objetivos especificos 📒
* **Reutilizacion de codigo.**
* **Modularidad.**
* **Abstraccion.**
* **Flexibilidad.**
* **Legibilidad.**

# ¿Que es una funcion en JS?
Una función en JavaScript es un bloque de código que se define una vez y puede ejecutarse (o invocarse) en cualquier momento dentro del programa. Las funciones permiten realizar una tarea específica y pueden aceptar entradas (parámetros) y devolver un valor de salida.

La estructura básica de una función en JavaScript incluye:
* **Declaracion.** Se define la función con la palabra clave function, seguida del nombre de la función, paréntesis para los parámetros, y un bloque de código entre llaves `{}`.
* **Invocacion.** Una vez definida, la función puede ser llamada o ejecutada en cualquier parte del programa.

Ejemplo de una funcion simple:
<pre><code>
  function sumar(a, b) {
    return a + b;
  }
  
  // Invocación de la función
  let resultado = sumar(3, 4); // resultado será 7
</code></pre>

En este ejemplo, la función sumar toma dos parámetros `a` y `b`, y devuelve la suma de ambos.

# Tipos de funciones en JS
En JavaScript, hay varios tipos de funciones que puedes utilizar, cada una con características particulares:
* **Funciones declarativas.** Se definen usando la palabra clave <strong>function</strong> seguida de un nombre. Pueden ser invocadas antes de su definición debido a su hoisting (elevación).
<pre><code>
  function saludo(nombre) {
    return `Hola, ${nombre}`;
  }
</code></pre>
* **Expresiones de funcion.** Se definen asignando una función a una variable. No son elevadas, por lo que deben ser definidas antes de su invocación.
<pre><code>
  const saludo = function(nombre) {
    return `Hola, ${nombre}`;
  };
</code></pre>

* **Funciones flecha.** Introducidas en ES6, ofrecen una sintaxis más concisa y no tienen su propio contexto de `this`, por lo que son útiles para funciones que no necesitan su propio `this`.
<pre><code>
  const saludo = (nombre) => `Hola, ${nombre}`;
</code></pre>

* **Funciones anonimas.** Son funciones sin nombre, que se suelen usar como argumentos para otras funciones o en eventos. Pueden ser expresiones de función o funciones flecha.
<pre><code>
  setTimeout(function() {
    console.log("Hola después de 1 segundo");
  }, 1000);
</code></pre>

* **Funciones de constructor.** Se definen con la palabra clave `function` y se utilizan con el operador `new` para crear instancias de objetos. Tienen un contexto propio y se utilizan menos en la actualidad.
<pre><code>
  function Persona(nombre) {
    this.nombre = nombre;
  }
  
  const persona1 = new Persona("Juan");
</code></pre>

* **Funciones generadoras.** Introducidas en ES6, utilizan la sintaxis de asterisco (*) y pueden pausar su ejecución con `yield`, permitiendo iterar sobre valores en una secuencia.
<pre><code>
  function* contar() {
    yield 1;
    yield 2;
    yield 3;
  }
  
  const contador = contar();
  console.log(contador.next().value); // 1
</code></pre>

# Funciones que retornan valores.
En JavaScript, las funciones que retornan valores son aquellas que devuelven un resultado cuando se les invoca. El valor retornado puede ser cualquier tipo de dato válido en JavaScript (números, cadenas, objetos, etc.). Aquí te explico cómo funcionan y cómo se pueden utilizar:
* **Funcion que retorna un valor simple.** Estas funciones devuelven un valor específico, como un número o una cadena.
<pre><code>
  function multiplicar(a, b) {
    return a * b;
  }
  
  let resultado = multiplicar(5, 3); // resultado será 15
</code></pre>

* **Funcion que retorna un objeto.** Puedes retornar un objeto para encapsular múltiples valores.
<pre><code>
  function crearPersona(nombre, edad) {
    return {
      nombre: nombre,
      edad: edad
    };
  }
  
  let persona = crearPersona("Ana", 30);
  // persona es { nombre: "Ana", edad: 30 }
</code></pre>

* **Funcion que retorna una funcion.** Las funciones pueden retornar otras funciones, lo que es útil para crear funciones más complejas o para la creación de closures.
<pre><code>
  function crearSaludo(saludo) {
    return function(nombre) {
      return `${saludo}, ${nombre}!`;
    };
  }
  
  let saludoHola = crearSaludo("Hola");
  console.log(saludoHola("Juan")); // "Hola, Juan!"
</code></pre>

* **Funcion que retorna `undefined`.** Si no se usa `return` explícitamente en una función, o si `return` no tiene un valor, la función retornará `undefined` por defecto.
<pre><code>
  function imprimirMensaje(mensaje) {
    console.log(mensaje);
    // No hay un return explícito, por lo que el retorno será undefined
  }
  
  let resultado = imprimirMensaje("Hola"); // resultado será undefined
</code></pre>

# ¿Como permitir el uso del mismo bloque de código en diferentes partes de un programa sin duplicación?
Para permitir el uso del mismo bloque de código en diferentes partes de un programa sin duplicación, puedes encapsular ese bloque de código en una función. Esto permite que el código se ejecute múltiples veces a lo largo del programa sin necesidad de reescribirlo. Aquí te muestro cómo hacerlo:
* **Definir una funcion.** Encapsula el bloque de código en una función, dándole un nombre descriptivo y especificando los parámetros necesarios.
<pre><code>
  function calcularAreaRectangulo(ancho, alto) {
    return ancho * alto;
  }
</code></pre>

* **Llamar a la funcion.** En lugar de duplicar el código, simplemente llama a la función cuando necesites ejecutar ese bloque de código.
<pre><code>
  let area1 = calcularAreaRectangulo(5, 10);
  let area2 = calcularAreaRectangulo(8, 12);
</code></pre>

* **Reutilizacion en diferentes contextos.** Puedes llamar a la misma función en diferentes partes de tu programa, pasando diferentes argumentos si es necesario.
<pre><code>
  function imprimirResultado(ancho, alto) {
    let area = calcularAreaRectangulo(ancho, alto);
    console.log(`El área del rectángulo es ${area}`);
  }
  
  imprimirResultado(5, 10);
  imprimirResultado(8, 12);
</code></pre>

* **Modularizacion.** Para proyectos más grandes, considera dividir tu código en módulos. En JavaScript, puedes usar módulos ES6 para exportar funciones y reutilizarlas en diferentes archivos.
En `utils.js`:
<pre><code>
  export function calcularAreaRectangulo(ancho, alto) {
    return ancho * alto;
  }
</code></pre>
En `app.js`:
<pre><code>
  import { calcularAreaRectangulo } from './utils.js';
  
  let area = calcularAreaRectangulo(5, 10);
</code></pre>

Al encapsular el código en funciones, no solo evitas la duplicación, sino que también haces que tu código sea más organizado, modular y fácil de mantener.

# Proximas lecciones
<div align="center">
  <table>
    <tr>
      <th>Leccion anterior</th>
      <th>Leccion actual</th>
      <th>Leccion siguiente</th>
    </tr>
    <tr>
      <td align="center">
        <a href="https://github.com/MarioAlive99/curso-javascript/tree/main/LECCION%208.%20TEMPLATE%20STRINGS">Leccion 8</a>
      </td>
      <td align="center">
        <a href="#">-</a>
      </td>
      <td align="center">
        <a href="">Leccion 10</a>
      </td>
    </tr>
  </table>
</div>
