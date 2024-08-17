![Diapositiva2](https://github.com/user-attachments/assets/674e4c96-5128-49df-a627-68822ad3a4b8)

# Leccion 1 🎓
# Objetivo general 📒
<strong>Comprender y aplicar el manejo de variables en JavaScript para desarrollar aplicaciones web interactivas y eficientes.</strong>

# Objetivos especificos 📕
* **Identificar los diferentes tipos de variables en JS.**
* **Aplicar buenas practicas en la declaracion y uso de variables.**
* **Gestionar el tipo de datos y conversiones.**
* **Implementar variables en contextos funcionales y de bloque.**
* **Realizar depuracion y resolucion de errores relacionadas con variables.**

# ¿Que son las variables en JS? 🤔
En JavaScript, una <strong>variable</strong> es un espacio de almacenamiento que se utiliza para guardar datos que puedan cambiar durante la ejecucion de un programa. Piensa que una variable como en una caja en la que puedes poner diferentes cosas (datos) y luego usar esos datos cuando los necesites.

Para declarar una variable, tiene que usar lo siguiente:
* **var.** Es la forma mas antigua de declarar variables en JS. Las variables declaradas con <strong>var</strong>, tienen un alcance global o de funcion, lo que significa que pueden ser accesibles en todo el codigo si estan en el ambito global, o solo dentro de una funcion si estan dentro de una funcion.
* **let.** Introducido en ECMAScript 6 (ESE6). Permite declarar variables con un alcance de bloque. Esto significa que la variable solo esta disponible dentro del bloque de codigo (como dentro de un if o un for) donde se han declarado.
* **const.** Tambien introducido en ES6. Se utiliza para declarar variables cuyo valor no debe cambiar despues de su inicializacion. Es decir, una vez que se le asigna un valor a una variable declarada con 'const', no puede asignar un nuevo valor a esa variable.

# ¿Como se inicializan?
En JS, la inicializacion de variables se refiere al proceso de asignar un valor a una variable en el momento en que se declara. Puedes inicializar una variable de diferentes maneras, dependiendo de la palabra clave que utilices para declararla. Te voy a explicar como inicializar variables con las palabras claves que mencionamos anteriormente, y doy ejemplos cada uno.

* **Inicializacion con var.**
La palabra clave <strong>var</strong> es la forma tradicional de declarar variables en JS. Puedes inicializarlas de la siguiente manera:
<div align="center">
  <img src="https://github.com/user-attachments/assets/08e9649d-c74f-4aa8-b9c8-3d38e2bf171f" alt="Ejemplo de variables 1 JS">
</div>
<p>Si no proporcionas un valor al declarar una variable con `var`, su valor inicial sera undefined.</p>
<br>
<div align="center">
  <img src="https://github.com/user-attachments/assets/da022a81-24ec-4e63-8d59-ebb5f90f1892">
</div>

* **Inicializacion con let.**
La palabra clave <strong>let</strong> fue introducida en ECMAScript 6 (ESE6) y permite declarar variables con un alcance de bloque. Debes inicializar una variable `let` al momento de su declaracion o posteriormente en el codigo.
<div align="center">
  <img src="https://github.com/user-attachments/assets/40a9c23b-a4fe-4bfb-9306-f42ea87092f4">
</div>
<p>Lo mismo que el anterior, pero sin inicializarla, saldra con un undefined</p>
<div align="center">
  <img src="https://github.com/user-attachments/assets/9cd89832-2668-44d6-8e23-5bcf6984bfdc">
</div>

* **Inicializacion con const.**
La palabra <strong>const</strong> se utiliza para declarar variables cuyo valor no debe cambiar despues de su inicializacion. Al usar `const`, debes inicializar la variable en el momento de su declaracion.
<div align="center">
  <img src="https://github.com/user-attachments/assets/a1d05387-5698-495a-82d1-fe63b1cb43b0">
</div>
<p>Si intentas reasignar un valor a la variable const, obtendras un error.</p>
<div align="center">
  <img src="https://github.com/user-attachments/assets/fd3a38bd-865d-40de-8bd0-c5a8609f6dbb">
</div>

# ¿Que es ECMAScript 6? 🤔
<strong>ECMAScript 6 (ES6)</strong>, tambien conocido como ECMAScript 2015, es una version importante del estandar ECMAScript que define el lenguaje de JavaScript. Fue publicado en junio del 2015 e introdujo una serie de mejoras significativas y nuevas caracteristicas que han enriquecido el lenguaje y mejorado la forma en que se escribe JavaScript.
Aqui te mencionamos algunas caracteristicas que va a funcionar en este curso:

* **Declaracion de variables con let y const**
* **Funciones de flecha**
* **Clases**
* **Desestructuracion**
* **Templates Literals**
* **Parametros por defecto**
* **Operador Spread y Rest**
* **Modulos**

# Antes de terminar... Un dato curioso 😍
Aunque el nombre sugiere una relacion estrecha con Java, JavaScript y Java no estan directamente relacionados. JavaScript fue creada por <strong>Brendan Eich en 1995</strong>, <i>(al igual que Java y PHP, que nacieron el mismo año XD)</i> y originalmente se llamaba `Mocha` antes de ser renombrado por `LiveScript` y luego a `JavaScript`. La razon de porque llamaron JavaScript, fue debido a que fue elegido como una campaña de marketing para sacar algo de popularidad de Java en esos tiempos.

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
        <a href="#">-</a>
      </td>
      <td align="center">
        <a href="#">-</a>
      </td>
      <td align="center">
        <a href="https://github.com/MarioAlive99/curso-javascript/tree/main/LECCION%202.%20TIPOS%20DE%20DATOS">Leccion 2</a>
      </td>
    </tr>
  </table>
</div>
