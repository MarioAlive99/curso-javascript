![Diapositiva2](https://github.com/user-attachments/assets/d2e2d1d3-e87c-44a8-b99a-9f9580f66808)

# Union de objetos
# Objetivo general 📒
Combinar sus propiedades y valores en un solo objeto para simplificar la gestión de configuraciones, datos o para extender funcionalidades.

# Objetivos especificos 📕
* **Fusionar configuraciones predeterminadas con personalizadas para una mayor flexibilidad.**
* **Reunir información de diferentes fuentes en un solo objeto para su fácil acceso y manipulación.**
* **Añadir o modificar propiedades en un objeto existente para crear nuevas funcionalidades.**
* **Reducir la redundancia al unificar propiedades comunes de varios objetos en uno solo.**
* **Actualizar valores de propiedades existentes con las más recientes o relevantes.**

# ¿Que es la union de objetos en JS?
La <strong>unión de dos o más objetos</strong> en JavaScript es el proceso de combinar las propiedades y valores de esos objetos en un único objeto. Esto implica tomar las propiedades de cada objeto y fusionarlas en un nuevo objeto, donde las propiedades con el mismo nombre pueden ser sobrescritas por los valores del último objeto unido. Este proceso permite consolidar configuraciones, datos o funcionalidades en un solo lugar.

# Tecnicas para el uso de union de objetos
En JavaScript, hay varias técnicas para unir objetos. Aquí te presento algunos ejemplos comunes:
* **Object.assign().** copia todas las propiedades de uno o más objetos de origen a un objeto de destino.
<pre><code>
  const obj1 = { a: 1, b: 2 };
  const obj2 = { b: 3, c: 4 };
  const merged = Object.assign({}, obj1, obj2);
  console.log(merged); // { a: 1, b: 3, c: 4 }
</code></pre>

* **Operador Spread(`...`).** descompone los objetos en sus propiedades, permitiendo unirlos de manera simple y concisa.
<pre><code>
  const obj1 = { a: 1, b: 2 };
  const obj2 = { b: 3, c: 4 };
  const merged = { ...obj1, ...obj2 };
  console.log(merged); // { a: 1, b: 3, c: 4 }
</code></pre>

* **Metodo recursivo.** Si necesitas hacer una unión profunda (donde también se fusionen objetos anidados), puedes usar una función recursiva personalizada.
<pre><code>
  function deepMerge(target, ...sources) {
    sources.forEach(source => {
        for (let key in source) {
            if (source[key] instanceof Object && key in target) {
                Object.assign(source[key], deepMerge(target[key], source[key]));
            }
        }
        Object.assign(target || {}, source);
    });
    return target;
}

const obj1 = { a: 1, b: { x: 2 } };
const obj2 = { b: { y: 3 }, c: 4 };
const merged = deepMerge({}, obj1, obj2);
console.log(merged); // { a: 1, b: { x: 2, y: 3 }, c: 4 }
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
        <a href="https://github.com/MarioAlive99/curso-javascript/tree/main/LECCION%205.%20MANIPULACION%20DE%20OBJETOS">Leccion 5</a>
      </td>
      <td align="center">
        <a href="#">-</a>
      </td>
      <td align="center">
        <a href="">Leccion 7</a>
      </td>
    </tr>
  </table>
</div>
