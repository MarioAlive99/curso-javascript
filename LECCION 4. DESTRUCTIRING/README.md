![Diapositiva5](https://github.com/user-attachments/assets/2176a0e7-539e-4d65-988e-b338eaa4aa3e)

# Destructiring en JavaScript
# Objetivo general 📒
Simplificar el acceso a propiedades de objetos y elementos de arrays, permitiendo extraer valores de forma mas directa y concisa, y mejorar la legibilidad del codigo.

# Objetivos especificos 📕
* **Extraer valores especificos de objetos o arrays sin necesidad de acceder a cada propiedad o indice de forma manual.**
* **Reducir la cantidad de codigo repetitivo y mejorar la legibilidad al desestructurar valores en una sola linea.**
* **Permitir la asignacion simultanea de multiples variables a partir de un objeto u array.**
* **Simplificar el trabajo con datos complejos al extraer y utilizar solo los elementos necesarios.**

# ¿Que es el destructiring?
La desestructuracion en JS es una caracteristica del lenguaje que permite extraer valores de arrays o propiedades de objetos y asignarlos a variables de manera mas concisa y legible. Esta tecnica simplifica el proceso de asignacion y mejora en la claridad del codigo al evitar la necesidad de acceder a los valores mediante indices o claves de forma repetitiva.

# Declaracion.
La desestructuracion puede aplicarse tanto a arrays como a objetos. La sintaxis basica para desestructurar un array es utilizando corchetes `[]`, mientras que para los objetos se utilizan llaves `{}`.
* **Desestructuracion de Arrays.**
<pre><code>
  const colores = ['rojo', 'verde', 'azul'];
  const [primerColor, segundoColor, tercerColor] = colores;
  console.log(primerColor); // 'rojo'
  console.log(segundoColor); // 'verde'
  console.log(tercerColor); // 'azul'
</code></pre>
* **Desestructuracion de Objetos.**
<pre><code>
  const persona = {
    nombre: 'Juan',
    edad: 30,
    ciudad: 'Madrid'
  };
  const { nombre, edad, ciudad } = persona;
  console.log(nombre); // 'Juan'
  console.log(edad); // 30
  console.log(ciudad); // 'Madrid'
</code></pre>

# Depuracion y errores.
* **Desestructuracion de propiedades inexistentes.**
Si se intenta desestructurar una propiedad que no existe, igualmente se asignara `undefined` a la variable correspondiente.
<pre><code>
  const { nombre, altura } = persona; // 'altura' no existe en el objeto 'persona'
  console.log(altura); // 'undefined'
</code></pre>
* **Desestructuracion incorrecta de Arrays.**
Si se desestructuran mas elementos de los que hay en el array, las variables adicionales recibiran `undefined`.
<pre><code>
  const numeros = [1, 2, 3];
  const [uno, dos, tres, cuatro] = numeros; // 'cuatro' no tiene valor
  console.log(cuatro); // 'undefined'
</code></pre>
* **Uso de valores por defecto.**
Se puede asignar valores por defecto a las variables desestructuradas para manejar casos en los que la propiedad no esta presente en el objeto.
<pre><code>
  const persona = { nombre: 'Ana' };
  const { nombre, edad = 25 } = persona;
  console.log(edad); // 25
</code></pre>
* **Desestructuracion anidada.**
La desestructuracion anidada permite extraer valores de objetos anidados. Es importante asegurarse de que la estructura del objeto coincida con la desestructuracion para evitar errores.
<pre><code>
  const datos = {
    usuario: {
      nombre: 'Carlos',
      edad: 28
    }
  };
const { usuario: { nombre, edad } } = datos;
console.log(nombre); // 'Carlos'
console.log(edad); // 28
</code></pre>

# Destructiring de dos o mas objetos
El <strong>destructiring de dos o mas objetos</strong> en JS es una tecnica que permite extraer propiedades especificas de multiples objetos y asignarlas en variables de manera concisa. En lugar de acceder a cada propiedad de los objetos mediante la notacion de punto o corchetes, puedes usar la sintaxis de destructuring para obtener los valores directamente y asignarlos a variables.

<pre><code>
  const obj1 = { a: 1, b: 2 };
  const obj2 = { c: 3, d: 4 };
  
  // Destructuring de ambos objetos
  const { a, b } = obj1;
  const { c, d } = obj2;
  
  console.log(a, b, c, d); // 1 2 3 4
</code></pre>
En este ejemplo, las propiedades `a` y `b` se extraen de `obj1` y las propiedades `c` y `d` se extraen de `obj2`, asignadolas a variables con el mismo nombre.

# Ejemplos y tecnicas de destructuring de dos o mas objetos
* **Destructuring simple.**
<pre><code>
  const obj1 = { a: 1, b: 2 };
  const obj2 = { c: 3, d: 4 };
  
  const { a, b } = obj1;
  const { c, d } = obj2;
  
  console.log(a, b, c, d); // 1 2 3 4
</code></pre>

* **Destructuring con alias.**
Puedes usar alias para asignar propiedades a variables con nombres diferentes.
<pre><code>
  const obj1 = { a: 1, b: 2 };
  const obj2 = { c: 3, d: 4 };
  
  const { a: alpha, b: beta } = obj1;
  const { c: gamma, d: delta } = obj2;
  
  console.log(alpha, beta, gamma, delta); // 1 2 3 4
</code></pre>

* **Destructuring en parametros de funcion.**
Puedes usar destructuring directamente en los parametros de una funcion para extraer propiedades de objetos pasados como argumentos.
<pre><code>
  function printValues({ a, b }, { c, d }) {
    console.log(a, b, c, d);
  }
  
  const obj1 = { a: 1, b: 2 };
  const obj2 = { c: 3, d: 4 };
  
  printValues(obj1, obj2); // 1 2 3 4
</code></pre>

* **Destructuring con valores por defecto.**
Puedes establecer valores por defecto en caso de que las propiedades no existan en los objetos
<pre><code>
  const obj1 = { a: 1 };
  const obj2 = { c: 3 };
  
  const { a = 0, b = 2 } = obj1;
  const { c = 0, d = 4 } = obj2;
  
  console.log(a, b, c, d); // 1 2 3 4
</code></pre>

* **Destructuring de propiedades anidadas.**
Si los objetos tienen propiedades anidadas, puedes extraer valores directamente de las propiedades internas.
<pre><code>
  const obj1 = { a: { x: 10, y: 20 }, b: 2 };
  const obj2 = { c: 3, d: { z: 40 } };
  
  const { a: { x, y }, b } = obj1;
  const { c, d: { z } } = obj2;
  
  console.log(x, y, b, c, z); // 10 20 2 3 40
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
        <a href="https://github.com/MarioAlive99/curso-javascript/tree/main/LECCION%203.%20OBJETOS">Leccion 3</a>
      </td>
      <td align="center">
        <a href="#">-</a>
      </td>
      <td align="center">
        <a href="#">Leccion 5</a>
      </td>
    </tr>
  </table>
</div>
