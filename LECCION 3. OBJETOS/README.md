![Diapositiva4](https://github.com/user-attachments/assets/715455f8-138b-49c9-8b18-a60269832df3)

# Objetos en JavaScript
# Objetivo general 📕
Almacenar y organizar datos en pares clave-valor. Los objetos permiten agrupar propiedades y metodos relacionados, facilitando la gestion y manipulacion de informacion en una estructura flexible y extensible.

# Objetivos especificos 📒
* **Permitir el almacenamiento de multiples valores bajo una unica identidad.**
* **Agrupar propiedades y metodos relacionados en una sola estructura.**
* **Proporcionar un medio para acceder y modificar datos mediante claves.**
* **Permitir la creacion de objetos basados en otros objetos.**
* **Incorporar comportamientos y funcionalidades directamente dentro de los objetos.**

# ¿Que es un objeto en JS?
Un <strong>objeto</strong> es una estructura de datos que permiten almacenar y organizar informacion en pares de clave-valor. Cada clave (conocida como propiedad) es un string que se asocia a un valor que puede ser de cualquier tipo de datos, incluyendo otros objetos o funciones. Los objetos son fundamentales en JS porque permiten la agrupacion de datos y funcionalidades relacionadas, facilitando la construccion de aplicaciones mas complejas y organizadas.

# Declaracion. 
Los objetos en JS se pueden declarar de varias maneras. La forma mas comun es mediante la notacion de objeto literal, donde se define el objeto usando llaves `{}`.
<pre><code>
  const persona = {
    nombre: "Andrea",
    edad: 30,
    saludo: function() {
      return `Hola, mi nombre es ${this.nombre}`;
    }
  };
</code></pre>
En este ejemplo, `persona` es un objeto con tres propiedades: `nombre`, `edad` y `saludo`. La propiedad `saludo` es una funcion que utiliza la palabra clave `this` para referirse al objeto `persona`.

Otra forma de crear objetos es mediante el constructor `Object()`:
<pre><code>
  const coche = new Object();
  coche.marca = "Toyota";
  coche.modelo = "Corolla";
  coche.annio = 2022;
</code></pre>

# Ejemplos
* **Objeto con propiedades y metodos.**
<pre><code>
  const libro = {
    titulo: "1984",
    autor: "George Orwell",
    anioPublicacion: 1949,
    descripcion: function() {
      return `${this.titulo} fue escrito por ${this.autor} en ${this.anioPublicacion}`;
    }
  };
  
console.log(libro.descripcion()); // "1984 fue escrito por George Orwell en 1949"
</code></pre>

* **Objeto anidado.**
<pre><code>
  const estudiante = {
    nombre: "Ana",
    edad: 22,
    direccion: {
      calle: "Av. Principal",
      numero: 123
    }
  };

console.log(estudiante.direccion.calle); // "Av. Principal"
</code></pre>

* **Objeto con un metodo.**
<pre><code>
  const calculadora = {
    suma: function(a, b) {
      return a + b;
    }
  };

console.log(calculadora.suma(5, 3)); // 8
</code></pre>

# Depuracion y errores
La depuracion de objetos en JS puede implicar varias estrategias para identificar y corregir problemas. Aqui hay algunos enfoques comunes:
* **Uso de console.log().** Imprimir el objeto o sus propiedades en la consola puede ayudar a verificar su contenido y estructura.
<pre><code>
  const usuario = { nombre: "Carlos", edad: 28 };
  console.log(usuario);
  console.log(usuario.nombre); // "Carlos"
</code></pre>
* **Inspeccion en herramientas de desarrollo.** Los navegadores modernos ofrecen herramientas de desarrollo que permiten inspeccionar objetos en tiempo real y explorar sus propiedades.
* **Manejo de errores.** Los errores comunes al trabajar con objetos incluyen el intento de acceder a propiedades no definidas, o llamar metodos que no existen. Los errores se pueden manejar usando estructuras de control como `try` y `catch`.
<pre><code>
  try {
    console.log(usuario.direccion.calle); // Error: no se puede leer la propiedad 'calle' de undefined
  } catch (error) {
    console.error("Error al acceder a la propiedad:", error);
  }
</code></pre>
* **Validacion de propiedades.** Asegurate de que las propiedades y metodos se definen correctamente antes de usarlos. Pueden usar operadores como `in` o metodos como `hasOwnProperty()` para verificar la existencia de propiedades.
<pre><code>
  if ('nombre' in usuario) {
    console.log(usuario.nombre);
  }
</code></pre>
<pre><code>
  if (usuario.hasOwnProperty('edad')) {
    console.log(usuario.edad);
  }
</code></pre>

# Errores comunes.
* **Acceso a propiedades inexistentes.** Intenta acceder a una propiedad que no existe en el objeto puede devolver `undefined` y provocar errores en el codigo.
<pre><code>
  console.log(usuario.direccion); // undefined
</code></pre>
* **Modificacion incorrecta.** Intentar modificar propiedades no definidas pueden llevar a errores inesperados.
<pre><code>
  usuario.edad = 30; // Esto funciona, pero si 'usuario' es una constante definida como `const`, no podrás reasignar el objeto entero.
</code></pre>
* **Metodos no definidos.** Llamar a metodos que no existen en el objeto resultara en errores.
<pre><code>
  usuario.saludar(); // Error si `saludar` no está definido
</code></pre>
* **Confusion entre metodos y propiedades.** A veces, los metodos se confuden con propiedades, especialmente cuando se omiten los parentesis al llamarlos.
<pre><code>
  console.log(usuario.saludo); // Esto devuelve la referencia a la función, no el resultado de su ejecución
  console.log(usuario.saludo()); // Esto devuelve el resultado de la función
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
        <a href="https://github.com/MarioAlive99/curso-javascript/tree/main/LECCION%202.%20TIPOS%20DE%20DATOS">Leccion 2</a>
      </td>
      <td align="center">
        <a href="#">-</a>
      </td>
      <td align="center">
        <a href="#">Leccion 4</a>
      </td>
    </tr>
  </table>
</div>
