![Diapositiva1](https://github.com/user-attachments/assets/6b3b4d32-65d4-40bc-858a-ee1b3cd1012c)

# Manipulacion de objetos
# Objetivo general 📒
Permitir la creacion, modificación y acceso eficiente a datos estructurados, facilitando la organizacion y gestion de informacion compleja dentro de una aplicacion.

# Objetivos especificos 📕
* **Aprender a crear objetos utilizando la sintaxis literal o constructores para representar entidades complejas con propiedades y metodos.**
* **Dominar las tecnicas para acceder, actualizar, agregar y eliminar propiedades en un objeto.**
* **Utilizar diferentes metodos para recorrer las propiedades de un objeto, como `for... in` y `Object.keys()`, para realizar operaciones en sus valores.**
* **Implementar metodos para la clonacion, fusion y comparacion de objetos, permitiendo un manejo mas sofisticado y flexible de los datos.**
* **Comprender como utilizar prototipos para extender objetos y crear jerarquias de herencia, promoviendo la reutilizacion de codigo.**

# ¿Que es la manipulacion de objetos en JS?
La <strong>manipulacion de objetos</strong> en JS se refiere al conjunto de operaciones que se pueden realizar sobre los objetos, que son estructuras de datos que permiten almacenar pares de clave-valor. Estas operaciones incluyen la creacion de objetos, la modificacion de sus propiedades, el acceso a los valores almacenados, la eliminacion de propiedades, y la iteracion sobre las propiedades de un objeto. Ademas, incluyen tecnicas mas avanzadas como la clonacion, fusion y manejo de la herencia a traves de prototipos.

# Ejemplos
* **Para crear un objeto.**
<pre><code>
  let persona = {
      nombre: "Juan",
      edad: 30,
      profesion: "Desarrollador"
  };
</code></pre>

* **Para acceder a sus propiedades.**
<pre><code>
  console.log(persona.nombre); // "Juan"
  console.log(persona["edad"]); // 30
</code></pre>

* **Para modificar propiedades.**
<pre><code>
  persona.edad = 31;
  persona["profesion"] = "Ingeniero de Software";
  console.log(persona); 
  // { nombre: 'Juan', edad: 31, profesion: 'Ingeniero de Software' }
</code></pre>

* **Para agregar nuevas propiedades.**
<pre><code>
  persona.nacionalidad = "Mexicano";
  console.log(persona);
  // { nombre: 'Juan', edad: 31, profesion: 'Ingeniero de Software', nacionalidad: 'Mexicano' }
</code></pre>

* **Para eliminar propiedades.**
<pre><code>
  delete persona.profesion;
  console.log(persona);
  // { nombre: 'Juan', edad: 31, nacionalidad: 'Mexicano' }
</code></pre>

* **Para iterar sobre un objeto.**
<pre><code>
  for (let clave in persona) {
      console.log(`${clave}: ${persona[clave]}`);
  }
// nombre: Juan
// edad: 31
// nacionalidad: Mexicano
</code></pre>

* **Para clonar un objeto.**
<pre><code>
  let clonPersona = { ...persona };
  console.log(clonPersona);
  // { nombre: 'Juan', edad: 31, nacionalidad: 'Mexicano' }
</code></pre>

* **Para fusionar un objeto.**
<pre><code>
  let direccion = {
      ciudad: "Ciudad de México",
      pais: "México"
  };
  
  let personaConDireccion = { ...persona, ...direccion };
  console.log(personaConDireccion);
  // { nombre: 'Juan', edad: 31, nacionalidad: 'Mexicano', ciudad: 'Ciudad de México', pais: 'México' }
</code></pre>

* **Para el uso de prototipos.**
<pre><code>
  function Persona(nombre, edad) {
      this.nombre = nombre;
      this.edad = edad;
  }
  
  Persona.prototype.saludar = function() {
      console.log(`Hola, me llamo ${this.nombre}`);
  };
  
  let maria = new Persona("María", 28);
  maria.saludar(); // "Hola, me llamo María"
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
        <a href="https://github.com/MarioAlive99/curso-javascript/tree/main/LECCION%204.%20DESTRUCTIRING">Leccion 4</a>
      </td>
      <td align="center">
        <a href="#">-</a>
      </td>
      <td align="center">
        <a href="">Leccion 6</a>
      </td>
    </tr>
  </table>
</div>
