![Diapositiva2](https://github.com/user-attachments/assets/77d46f66-9aae-4fff-b532-146b9a2a8fd3)

# Array Methods en JS
# Objetivo general 📕
Proporcionar herramientas para manipular, transformar y gestionar colecciones de datos de manera eficiente y flexible.

# Objetivos especificos 📒
* **Acceder y manipular arrays**
* **Transformar datos en arrays.**
* **Ordenar y buscar en arrays.**
* **Modificar estructuralmente en arrays.**
* **Iterar eficiente en arrays.**
* **Combinar y reducir en arrays.**

# ¿Que son array methods en JS?
Los <strong>métodos de arrays</strong> en JavaScript son funciones incorporadas que permiten realizar operaciones sobre los elementos de un array. Estos métodos simplifican la manipulación de arrays al proporcionar una interfaz para ejecutar tareas comunes como iterar, modificar, buscar y transformar datos dentro del array. Algunos ejemplos de estos métodos incluyen:

# ¿Como permitir acceder y modificar elementos dentro del array de manera directa y sencilla? 🤔
Para acceder y modificar elementos dentro de un array en JavaScript de manera directa y sencilla, puedes usar el índice del array. Los índices en un array comienzan en 0, por lo que el primer elemento tiene el índice 0, el segundo tiene el índice 1, y así sucesivamente. Aquí te muestro cómo hacerlo:
* **Acceder a elementos.** Para acceder a un elemento en un array, simplemente usa el índice entre corchetes `[]`.
<pre><code>
  let fruits = ['apple', 'banana', 'cherry'];
  let firstFruit = fruits[0]; // 'apple'
  let secondFruit = fruits[1]; // 'banana'
</code></pre>

* **Modificar elementos.** Para modificar un elemento, asigna un nuevo valor al índice correspondiente.
<pre><code>
  let fruits = ['apple', 'banana', 'cherry'];
  fruits[1] = 'blueberry'; // Cambia 'banana' por 'blueberry'
</code></pre>

Hay una consideracion, si intentas acceder a un índice que no existe en el array, devolverá undefined. Modificar un índice fuera del rango del array ampliará el array con undefined en ese índice.
<pre><code>
  let colors = ['red', 'green'];
  console.log(colors[5]); // undefined
  
  colors[5] = 'blue'; // El array ahora es ['red', 'green', undefined, undefined, undefined, 'blue']
  console.log(colors);
</code></pre>
Estos métodos te permiten manipular arrays de manera efectiva y son fundamentales para trabajar con colecciones de datos en JavaScript.

# ¿Como facilitar la transformación de los elementos del array mediante métodos? 🤔
Para facilitar la transformación de los elementos de un array en JavaScript, puedes usar métodos como `map()`, `filter()` y `reduce()`. Cada uno de estos métodos ofrece una forma poderosa de manipular arrays y realizar operaciones comunes. Aquí te explico cómo usar cada uno de ellos:

* **map().** Transformar cada elemento del array y devolver un nuevo array con los resultados.
<pre><code>
  let numbers = [1, 2, 3, 4, 5];
  
  // Usar map() para duplicar cada número
  let doubled = numbers.map(num => num * 2);
  
  console.log(doubled); // [2, 4, 6, 8, 10]
</code></pre>

* **filter().** Filtrar elementos del array basados en una condición y devolver un nuevo array con los elementos que cumplen esa condición.
<pre><code>
  let numbers = [1, 2, 3, 4, 5];
  
  // Usar filter() para obtener números mayores de 3
  let greaterThanThree = numbers.filter(num => num > 3);
  
  console.log(greaterThanThree); // [4, 5]
</code></pre>

* **reduce().** Reducir el array a un único valor acumulando los resultados de una función aplicada a cada elemento.
<pre><code>
  let numbers = [1, 2, 3, 4, 5];

  // Usar reduce() para calcular la suma de todos los números
  let sum = numbers.reduce((accumulator, num) => accumulator + num, 0);
  
  console.log(sum); // 15
</code></pre>

Aqui tienes un ejemplo combinado con estas funciones:
<pre><code>
  let numbers = [1, 2, 3, 4, 5];

  // Usar filter() para obtener números mayores de 3
  let greaterThanThree = numbers.filter(num => num > 3);
  
  // Usar map() para obtener los cuadrados de esos números
  let squared = greaterThanThree.map(num => num * num);
  
  // Usar reduce() para sumar los cuadrados
  let sumOfSquares = squared.reduce((accumulator, num) => accumulator + num, 0);
  
  console.log(sumOfSquares); // 41
</code></pre>

# ¿Como ofrecer capacidades para ordenar elementos en el array? 🤔
* **sort().** Ordenar los elementos del array en su lugar según un criterio específico.
<pre><code>
  let numbers = [4, 2, 5, 1, 3];

  // Ordenar en orden ascendente
  numbers.sort((a, b) => a - b);
  
  console.log(numbers); // [1, 2, 3, 4, 5]
  
  // Ordenar en orden descendente
  numbers.sort((a, b) => b - a);
  
  console.log(numbers); // [5, 4, 3, 2, 1]
</code></pre>

* **find().** Encontrar el primer elemento en el array que cumple con una condición específica.
<pre><code>
  let numbers = [10, 20, 30, 40, 50];

  // Encontrar el primer número mayor que 25
  let found = numbers.find(num => num > 25);
  
  console.log(found); // 30
</code></pre>

* **includes().** Determinar si un array contiene un elemento específico.
<pre><code>
  let fruits = ['apple', 'banana', 'cherry'];

  // Verificar si el array contiene 'banana'
  let hasBanana = fruits.includes('banana');
  
  console.log(hasBanana); // true
  
  // Verificar si el array contiene 'grape'
  let hasGrape = fruits.includes('grape');
  
  console.log(hasGrape); // false
</code></pre>

Tambien esta otro ejemplo con tres funciones:
<pre><code>
  let numbers = [10, 50, 20, 30, 40];

  // Encontrar el primer número mayor que 25
  let found = numbers.find(num => num > 25);
  
  console.log(found); // 30
  
  // Ordenar el array en orden descendente
  numbers.sort((a, b) => b - a);
  
  console.log(numbers); // [50, 40, 30, 20, 10]
  
  // Verificar si el número 30 está en el array
  let hasThirty = numbers.includes(30);
  
  console.log(hasThirty); // true
</code></pre>

# ¿Como permitir modificar elementos en la estructura del array? 🤔
* **push().** Añadir uno o más elementos al final del array.
<pre><code>
  let fruits = ['apple', 'banana'];
  // Añadir 'cherry' y 'date' al final del array
  fruits.push('cherry', 'date');
  
  console.log(fruits); // ['apple', 'banana', 'cherry', 'date']
</code></pre>

* **unshift().** Añadir uno o más elementos al principio del array.
<pre><code>
  let fruits = ['apple', 'banana'];

  // Añadir 'strawberry' al principio del array
  fruits.unshift('strawberry');
  
  console.log(fruits); // ['strawberry', 'apple', 'banana']
</code></pre>

* **pop().** Eliminar el último elemento del array.
<pre><code>
  let fruits = ['apple', 'banana', 'cherry'];
  // Eliminar el último elemento ('cherry')
  let last = fruits.pop();
  
  console.log(last); // 'cherry'
  console.log(fruits); // ['apple', 'banana']
</code></pre>

* **shift().** Eliminar el primer elemento del array.
<pre><code>
  let fruits = ['apple', 'banana', 'cherry'];
  
  // Eliminar el primer elemento ('apple')
  let first = fruits.shift();
  
  console.log(first); // 'apple'
  console.log(fruits); // ['banana', 'cherry']
</code></pre>

* **splice().** Añadir o eliminar elementos en cualquier posición del array.
<pre><code>
  let fruits = ['apple', 'banana', 'cherry', 'date'];
  // Eliminar 2 elementos a partir del índice 1 ('banana', 'cherry')
  let removed = fruits.splice(1, 2);
  
  console.log(removed); // ['banana', 'cherry']
  console.log(fruits); // ['apple', 'date']
  
  // Añadir 'blueberry' y 'kiwi' en la posición 1
  fruits.splice(1, 0, 'blueberry', 'kiwi');
  
  console.log(fruits); // ['apple', 'blueberry', 'kiwi', 'date']
</code></pre>

# Como facilitar la iteración sobre los elementos del array? 🤔
* **forEach().**  Ejecutar una función para cada elemento del array.
<pre><code>
  let numbers = [1, 2, 3, 4, 5];
  
  // Usar forEach() para imprimir cada número
  numbers.forEach(num => {
      console.log(num);
  });
  
  // Resultado:
  // 1
  // 2
  // 3
  // 4
  // 5
</code></pre>

* **some().** Verificar si al menos un elemento del array cumple con una condición específica.
<pre><code>
  let numbers = [1, 2, 3, 4, 5];
  
  // Verificar si hay algún número mayor de 3
  let hasNumberGreaterThanThree = numbers.some(num => num > 3);
  
  console.log(hasNumberGreaterThanThree); // true
  
  // Verificar si hay algún número mayor de 6
  let hasNumberGreaterThanSix = numbers.some(num => num > 6);
  
  console.log(hasNumberGreaterThanSix); // false
</code></pre>

* **every().** Verificar si todos los elementos del array cumplen con una condición específica.
<pre><code>
  let numbers = [2, 4, 6, 8, 10];

  // Verificar si todos los números son pares
  let allAreEven = numbers.every(num => num % 2 === 0);
  
  console.log(allAreEven); // true
  
  // Verificar si todos los números son mayores de 5
  let allGreaterThanFive = numbers.every(num => num > 5);
  
  console.log(allGreaterThanFive); // false
</code></pre>

# ¿Como permitir combinar elementos y reducir el array a un único valor? 🤔
* **reduce().** Reducir todos los elementos del array a un único valor aplicando una función de acumulación.
<pre><code>
  let numbers = [1, 2, 3, 4, 5];

  // Usar reduce() para calcular la suma de todos los números
  let sum = numbers.reduce((accumulator, num) => accumulator + num, 0);
  
  console.log(sum); // 15
</code></pre>

* **reduceRight().**  Reducir todos los elementos del array a un único valor aplicando una función de acumulación, pero recorriendo el array de derecha a izquierda.
<pre><code>
  let numbers = [1, 2, 3, 4, 5];
  
  // Usar reduceRight() para concatenar todos los números como una cadena
  let concatenated = numbers.reduceRight((accumulator, num) => accumulator + num, '');
  
  console.log(concatenated); // '54321'
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
        <a href="https://github.com/MarioAlive99/curso-javascript/tree/main/LECCION%208.%20TEMPLATE%20STRINGS">Leccion 8</a>
      </td>
      <td align="center">
        <a href="#"></a>
      </td>
      <td align="center">
        <a href="">Leccion 10</a>
      </td>
    </tr>
  </table>
</div>
