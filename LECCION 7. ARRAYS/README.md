![Diapositiva3](https://github.com/user-attachments/assets/8edcdfed-e7bd-4482-acd7-b240dbc13c92)

# Arrays
# Objetivo general 📒
Almacenar y manipular colecciones de datos de manera ordenada y accesible.

# Objetivos especificos 📕
* **Permiten guardar un conjunto de valores bajo una sola variable, facilitando el manejo de listas de datos.**
* **Permiten acceder a elementos individuales mediante su índice, lo que facilita la manipulación de datos.**
* **Ofrecen métodos como forEach, map y filter para recorrer y procesar los elementos de manera eficiente.**
* **Permiten añadir, eliminar y modificar elementos utilizando métodos como push, pop, splice, y shift.**
* **Proporcionan métodos como sort y find para organizar y buscar elementos según criterios específicos.**
* **Facilitan la transformación y mapeo de datos mediante métodos como map y reduce.**

# ¿Que es un array en JS?
Un <strong>array</strong> es una estructura de datos que permite almacenar y organizar múltiples valores en una sola variable. Los valores en un array pueden ser de cualquier tipo, incluidos números, cadenas de texto, objetos y otros arrays. Los arrays en JavaScript son dinámicos y pueden cambiar de tamaño, lo que significa que puedes añadir, eliminar y modificar elementos fácilmente.

Un array se define utilizando corchetes [], y los elementos dentro del array están separados por comas. Por ejemplo:
<pre><code>
  let frutas = ['manzana', 'banana', 'naranja'];
</code></pre>
En este ejemplo, frutas es un array que contiene tres elementos: 'manzana', 'banana' y 'naranja'. Los elementos en un array tienen índices numéricos que comienzan en 0, por lo que 'manzana' está en el índice 0, 'banana' en el índice 1, y 'naranja' en el índice 2.

# Operaciones sobre arrays
* **Crear un array.**
<pre><code>
  let vacio = []; // Array vacío
  let numeros = [1, 2, 3, 4, 5]; // Array de números
  let frutas = ['manzana', 'banana', 'naranja']; // Array de cadenas
</code></pre>

* **Acceder a elementos.**
<pre><code>
  console.log(frutas[0]); // 'manzana'
  console.log(frutas[1]); // 'banana'
</code></pre>

* **Modificar elementos.**
<pre><code>
  frutas[1] = 'fresa'; // Cambia 'banana' a 'fresa'
</code></pre>

* **Para añadir elementos.** El operador `push` añade uno o mas elementos al final del array y devuelve la nueva longitud del array. El operador `unshift` añade uno o mas elementos al principio o inicio del array y devuelve la nueva longitud del array.
<pre><code>
  frutas.push('kiwi'); // Añade 'kiwi' al final
  frutas.unshift('mango'); // Añade 'mango' al principio
</code></pre>

* **Para eliminar elementos.** El operador `pop` elimina el ultimo elemento del array y lo devuelve, y en cuanto a `shift` elimina el primer elemento del array, y lo devuelve.
<pre><code>
  frutas.pop(); // Elimina el último elemento ('kiwi')
  frutas.shift(); // Elimina el primer elemento ('mango')
</code></pre>

* **Transformacion.** El operador `map` crea un nuevo array con los resultados de aplicar la funcion de callback a cada elemento del array original.
<pre><code>
  let numerosDoblados = numeros.map(num => num * 2); // [2, 4, 6, 8, 10]
</code></pre>

* **Filtrado.** El operador `filter` crea un nuevo array con todos los elementos que pasan la prueba implementada por la funcion de callback.
<pre><code>
  let numerosPares = numeros.filter(num => num % 2 === 0); // [2, 4]
</code></pre>

* **Buscar elementos.** El operador `find` devuelve el primer elemento que cumple con la condicion dada en la funcion de callback. Si no encuentra ningun elemento, devuelve `undefined`.
<pre><code>
  let encontrado = frutas.find(fruta => fruta === 'banana'); // 'banana'
</code></pre>

* **Ordenar elementos.** El operador `sort` ordena los elementos del array en su lugar y devuelve el array. La funcion de comparacion original opcional permite definir el criterio de ordenacion.
<pre><code>
  numeros.sort((a, b) => a - b); // Ordena de menor a mayor
</code></pre>

* **Reducir un array a un valor.** El operador `reduce` ejecuta la funcion de callback para cada elemento del array (de izquierda a derecha) y reduce el array a un unico valor.
<pre><code>
  let suma = numeros.reduce((acc, num) => acc + num, 0); // Suma de todos los números
</code></pre>

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
        <a href="https://github.com/MarioAlive99/curso-javascript/tree/main/LECCION%206.%20UNION%20DE%20OBJETOS">Leccion 6</a>
      </td>
      <td align="center">
        <a href="#">-</a>
      </td>
      <td align="center">
        <a href="">Leccion 8</a>
      </td>
    </tr>
  </table>
</div>
