![Diapositiva1](https://github.com/user-attachments/assets/803facf7-fa3d-4a3d-bc39-8e7d74b7ae76)

# Template Strings y Concatenacion
# Objetivo general 📒
Permitir la creacion de cadenas de texto dinamicas de manera sencilla y eficiente.

# Objetivos especificos 📕
* **Simplificar la integracion de variables y expresiones en cadenas de texto.**
* **Mejorar la legibilidad del codigo.**
* **Soportar cadenas multilinea.**
* **Facilitar la interpolacion de resultados complejos.**

# ¿Que son los Template Strings y la concatenacion en JS?
Los <strong>Template Strings</strong> son una forma avanzada de manejar cadenas de texto que permiten integrar variables y expresiones de manera sencilla. Utilizan las comillas invertidas (``) en lugar de comillas simples o dobles, y permiten la interpolacion de variables mediante la sintaxis `${}`. Ademas, soportan cadenas multilinea sin necesidad de caracteres especiales.
<pre><code>
  const nombre = "Juan";
  const mensaje = `Hola, ${nombre}! ¿Cómo estás?`;
</code></pre>

La <strong>concatenacion</strong> es el metodo tradicional de combinar cadenas de texto y variables utilizando el operador `+`. Este enfoque puede volverse complicado y menos legible cuando se manejan multiples variables o largas cadenas de texto.
<pre><code>
  const nombre = "Juan";
  const mensaje = "Hola, " + nombre + "! ¿Cómo estás?";
</code></pre>

# ¿Como facilitar la inclusion de valores dinamicos sin tener que usar el operador de concatenacion (+)? 🤔
Para facilitar la inclusion de valores dinamicos sin tener que usar el mismo operador, puedes utilizar los <strong>Templates Strings</strong> en JS.
<pre><code>
  const nombre = "Ana";
  const edad = 25;
  
  // Usando Template Strings para incluir valores dinámicos
  const mensaje = `Hola, mi nombre es ${nombre} y tengo ${edad} años.`;
  
  console.log(mensaje); // Salida: Hola, mi nombre es Ana y tengo 25 años.
</code></pre>
En este ejemplo, las variables `nombre` y `edad` se insertan directamente en la cadena sin necesidad de concatenar manualmente con el operador +. Esto hace que el codigo sea mas limpio y facil de leer.

# ¿Como hacer que las cadenas largas y complejas sean más fáciles de escribir y leer, reduciendo la probabilidad de errores? 🤔
Tomemos como ejemplo este codigo:
<pre><code>
  const producto = "laptop";
  const precio = 1200;
  const cliente = "Carlos";
  
  // Usando Template Strings para una cadena larga y compleja
  const mensaje = `
  Estimado ${cliente},
  
  Gracias por tu compra de la ${producto}. El monto total es $${precio}.
  
  Esperamos que disfrutes tu nueva adquisición.
  
  Saludos cordiales,
  El equipo de ventas
  `;
  
  console.log(mensaje);
</code></pre>
Esto hace que el código sea más limpio, fácil de mantener y menos propenso a errores comunes que pueden surgir con la concatenación manual.

# ¿Como permitir la creación de cadenas que se extienden en múltiples líneas sin necesidad de caracteres especiales como \n? 🤔
<pre><code>
  // Usando Template Strings para una cadena multilínea
  const mensaje = `
  Este es un mensaje
  que se extiende
  en varias líneas
  sin necesidad de usar \n.
  `;
  
  console.log(mensaje);
</code></pre>

# ¿Como permitir la ejecución de expresiones JavaScript dentro de las cadenas para generar resultados dinámicos sin esfuerzo adicional? 🤔
Para permitir la ejecución de expresiones JavaScript dentro de las cadenas y generar resultados dinámicos sin esfuerzo adicional, puedes usar <strong>Template Strings</strong>.
<pre><code>
  const a = 10;
  const b = 20;
  
  // Usando Template Strings para ejecutar expresiones dentro de la cadena
  const resultado = `La suma de ${a} y ${b} es ${a + b}.`;
  
  console.log(resultado); // Salida: La suma de 10 y 20 es 30.
</code></pre>
En este ejemplo, `${a+b}` ejecuta la expresion `a + b` y el resultado `30` se inserta en la cadena, y mientras que puedes realizar cualquier tipo de operacion o funcion dentro de la expresion, lo que te permite generar contenido dinamico facilmente.

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
        <a href="https://github.com/MarioAlive99/curso-javascript/tree/main/LECCION%207.%20ARRAYS">Leccion 7</a>
      </td>
      <td align="center">
        <a href="#">-</a>
      </td>
      <td align="center">
        <a href="">Leccion 9</a>
      </td>
    </tr>
  </table>
</div>
