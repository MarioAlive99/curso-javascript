![Diapositiva3](https://github.com/user-attachments/assets/5d759053-7650-4a3e-ac88-0f7dd5fb35e8)

# Tipos de datos en JavaScript
# Objetivo general 📕
Clasificar y gestionar la informacion que un programa maneja, permitiendo realizar operaciones y manipulaciones adecuadas segun la naturaleza del valor, como numeros, cadenas de texto, booleanos, objetos y mas. Esto asegura un funcionamiento correcto y precedible del codigo.

# Objetivos especificos 📒
* **Optimizar la memoria y rendimiento.**
* **Facilitar el control de flujo.**
* **Garantizar la coherencia en las operaciones.**
* **Promover la integridad de datos.**
* **Mejorar la legibilidad y mantenibilidad del codigo.**

# ¿Que son los tipos de datos en JavaScript?
Los <strong>tipos de datos</strong> en JavaScript son categorias que definen la naturaleza y el comportamiento de los valores que se pueden almacenar y manipular en el lenguaje. Estos tipos se determinan como se pueden operar y procesar los datos dentro de un programa. JavaScript tiene varios tipos de datos como:

# Datos primitivos
Los <strong>datos primitivos</strong> son valores que no son objetos y tienen un comportamiento inmutable. Incluyen:
* **Number.** Representa numeros, tanto enteros como decimales (2,9,2.3)
* **String.** Representa cadenas de texto (por ejemplo, '¡Hola Mundo!')
* **Boolean.** Representa valores logicos, por ejemplo True o False.
* **Undefined.** Indica que una variable ha sido declarada pero aun no ha sido asignada a un valor. Por defecto, el valor de una variable sin asignar es `undefined`.
* **Null.** Representa la ausencia intencionada de un valor. Es un valor especial que se asigna explicitamente a una variable.
* **Symbol.** Introducido en ECMAScript 6, representa un valor unico e inmutable. Se usa para crear identificadores unicos como propiedades de objetos.
* **BigInt.** Introducido en ECMAScript 2020, representa numeros enteros que pueden ser muy grandes, mas alla del rango de los numeros estandar de `Number`.

# Datos complejos
En JavaScript, los <strong>datos complejos</strong> se refieren a los datos que no son primitivos y que pueden almacenar colecciones de datos o entidades mas estructuradas. Los principales tipos de datos complejos incluyen:
* **Object.** Es el tipo de dato mas general que pueden almacenar pares clave-valor. Los objetos pueden contener propiedades y metodos.
<pre><code>
  const persona = {
    nombre: 'Juan',
    edad: 30,
    saludar: function() { console.log('Hola'); }
  };
</code></pre>
* **Array.** Es un tipo especial de objeto utilizado para almacenar listas ordenadas de valores. Los elementos pueden ser de cualquier tipo y el array puede cambiar su tamaño dinamicamente.
<pre><code>
  const frutas = ['manzana', 'banana', 'cereza'];
</code></pre>
* **Function.** Es un tipo de objeto que representa una funcion de codigo que puede ser ejecutada. Las funciones en JS son ciudadanos de primera clase, lo que significa que pueden ser asignadas a variables, pasadas como argumentos y devueltas por otras funciones.
<pre><code>
  function saludar(nombre) {
    return `Hola, ${nombre}`;
  }
</code></pre>
* **Date.** Es un objeto especial para manejar fechas y horas.
<pre><code>
  const ahora = new Date();
</code></pre>
* **RegExp.** Representa expresiones regulares que se utilizan para realizar operaciones de busqueda y manipulacion de texto basado en patrones.
<pre><code>
  const patron = /abc/;
</code></pre>
* **Map.** Es una coleccion de pares clave-valor, donde las claves pueden ser de cualquier tipo y mantienen el orden de insercion.
<pre><code>
  const mapa = new Map();
  mapa.set('clave1', 'valor1');
</code></pre>
* **Set.** Es una coleccion de valores unicos, sin duplicados, que mantienen el orden de insercion.
<pre><code>
  const conjunto = new Set();
  conjunto.add('valor1');
</code></pre>
* **WeakMap.** Similar a `Map`, pero con claves que son referencias debiles a los objetos, lo que permite que los objetos sean recolectados por el recolector de basura si no tiene otras referencias.
<pre><code>
  const weakmap = new WeakMap();
</code></pre>
* **WeakSet.** Similar a `Set`, pero con valores que son referencias debiles a los objetos.
<pre><code>
  const weakset = new WeakSet();
</code></pre>

# ¿Cual es la diferencia entre inmutable y mutable?
Un valor <strong>inmutable</strong> no puede ser cambiado una vez que se haya creado. En JavaScript, los tipos primitivos como `Number`, `String`, `Boolean`, `Undefined`, `Null`, `Symbol` y `BigInt` son inmutables. Esto significa que cualquier operacion que parezca modificar el valor en realidad crea un nuevo valor en lugar de alterar el existente.
<pre><code>
  let cadena = 'Hola';
  cadena = cadena + ' Mundo'; // 'cadena' ahora es 'Hola Mundo', pero el valor original 'Hola' no se ha modificado.
</code></pre>
Un valor <strong>mutable</strong> puede ser modificado despues de su creacion. En JavaScript, los objetos como `Object`, `Array`, `Function` y otros tipos complejos son mutables. Esto significa que puedes cambiar sus propiedades o elementos sin crear un nuevo objeto.
<pre><code>
  let persona = { nombre: 'Juan' };
  persona.nombre = 'Pedro'; // La propiedad 'nombre' de 'persona' se ha modificado.
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
        <a href="https://github.com/MarioAlive99/curso-javascript/tree/main/LECCION%201.%20VARIABLES">Leccion 1</a>
      </td>
      <td align="center">
        <a href="#">-</a>
      </td>
      <td align="center">
        <a href="www.google.com">Leccion 3</a>
      </td>
    </tr>
  </table>
</div>
