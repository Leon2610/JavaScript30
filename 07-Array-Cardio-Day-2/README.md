# Array Cardio Day 2

# some()

Este método se encarga de comprobar si al menos un elemento del array cumple con la condición implementada por la función proporcionada. Este método no modifica el array original.

El método `some()` regresa `true` (y se detiene) si la función regresa `true` para uno de los elementos de la matriz.

Ejemplo:

```jsx
const numeros = [1,15,29,31,6,11,5];

const esmayorA30 = numeros.some(numero => {
    if (numero > 30) {
        return true;
    }
});

//La función anterior también se puede resumir de la siguiente manera:

// const esmayorA30 = numeros.some(numero => numero > 30);

console.log(esmayorA30);
```

Otro ejemplo:

```jsx
const people = [
      { name: 'Wes', year: 1988 },
      { name: 'Kait', year: 1986 },
      { name: 'Irv', year: 1970 },
      { name: 'Lux', year: 2015 }
    ];

const isAdult = people.some(person => {
      const currentYear = new Date().getFullYear();
      if (currentYear - person.year >= 19) {
        return true;
      }
    });
    console.log({isAdult});
```

## Referencias

[Array.prototype.some() - JavaScript | MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/some)

# every()

Determina si todos los elementos en el array satisfacen una condición.

💡 **Precaución**: ¡Llamar este método en un array vacío devuelve `true`
 para cualquier condición!

`every` no modifica el arreglo sobre el cual es llamado.

Ejemplo:

```jsx
const people = [
      { name: 'Wes', year: 1988 },
      { name: 'Kait', year: 1986 },
      { name: 'Irv', year: 1970 },
      { name: 'Lux', year: 2015 }
    ];

const allAdulst = people.every(person => {
      const currentYear = new Date().getFullYear();
      if (currentYear - person.year >= 19) {
        return true;
      }
    });
    console.log({allAdulst});
```

## Referencias

[Array.prototype.every() - JavaScript | MDN](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/every)

# find()

Devuelve el valor del primer elemento del array que cumple la función de prueba proporcionada.

Ejemplo:

```jsx
const comments = [
      { text: 'Love this!', id: 523423 },
      { text: 'Super good', id: 823423 },
      { text: 'You are the best', id: 2039842 },
      { text: 'Ramen is my fav food ever', id: 123523 },
      { text: 'Nice Nice Nice!', id: 542328 }
    ];

const comment = comments.find(comment => comment.id === 823423);
    console.log({comment});
```

# findIndex()

El método **`findIndex()`** devuelve el **índice** del **primer elemento** de un array que cumpla con la función de prueba proporcionada. En caso contrario devuelve -1.

Ejemplo:

```jsx
const comments = [
      { text: 'Love this!', id: 523423 },
      { text: 'Super good', id: 823423 },
      { text: 'You are the best', id: 2039842 },
      { text: 'Ramen is my fav food ever', id: 123523 },
      { text: 'Nice Nice Nice!', id: 542328 }
    ];

const index = comments.findIndex(comment => comment.id === 823423);
    console.log({index});
```

# splice()

El método **`splice()`**cambia el contenido de un array eliminando elementos existentes y/o agregando nuevos elementos.

Para agregar elementos:

Ejemplo:

```jsx
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");

//Salida
//Arreglo original = Banana,Orange,Apple,Mango
//Usando splice para agregar = Banana,Orange,Lemon,Kiwi,Apple,Mango
```

El primer parámetro (2) define la posición **en** la que se deben **agregar** (empalmar) nuevos elementos.

El segundo parámetro (0) define **cuántos** elementos se deben **eliminar** .

El resto de parámetros ("Limón", "Kiwi") definen los nuevos elementos a **añadir** .

El método  `splice()` devuelve un arreglo con los elementos eliminados:

Para eliminar elementos:

Ejemplo:

```jsx
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 2, "Lemon", "Kiwi");
/*Salida
Original Array:
Banana,Orange,Apple,Mango

New Array:
Banana,Orange,Lemon,Kiwi

Removed Items:
Apple,Mango
*/
```

### Valor devuelto

Un array que contiene los elementos eliminados. Si sólo se ha eliminado un elemento, devuelve un array con un solo elemento. Si no se ha eliminado ningún elemento, devuelve un array vacío.

 En este [enlace](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array/splice#ejemplos) se pueden ver más ejemplos de su uso.