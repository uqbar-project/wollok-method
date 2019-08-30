# Intro: ¿qué es un objeto? 
Algunos conceptos
- *Estado* (datos) + *comportamiento*. Comparamos con estructurado en donde esas cosas están siempre separadas. 
- Está encapsulado, el estado es *interno*.
- Sólo podemos accederlo a través de *mensajes*.

Una vez hecho eso, podemos presentar a pepita y mostrar como la usamos en un proyector, partiendo del uso, de mandarle mensajes. 

Lo que sigue está basado en el código de ejemplo en https://github.com/npasserini/pepita.

> **Idea para 2020c1**: Si podemos hacer este ejercicio en Mumuki podríamos tener mediciones precisas de todo esto.

## Bienvenidos al Wollok IDE
Pero para llegar a los mensajes primero tenemos que contar algo (mínimo) del entorno.
- ¿Qué es un IDE?
- Mostrar la vista de proyectos, buscar a `pepita.wlk` y ejecutar en el REPL
- ¿Entonces qué es un REPL?

> A esta altura ni muestro el editor, quiero *usar* el objeto *antes* de ver cómo está definido.

## Hablemos con pepita
Ejecutamos a pepita en un REPL y le mandamos algunos mensajes.
1. Lo primero que podemos hacer es preguntarle a pepita si está feliz, de esta manera: `pepita.estaCansada()`.
  a. Vemos que al hacerlo el REPL *imprime* el resultado.
  b. Mencionar que `estaCansada` es una *pregunta* o *consulta*.
2. Luego podemos decirle que vuele `pepita.volar(42)`.
  a. Vemos que no imprime nada, reflexionar que es una *orden* o *acción*.
  b. ¿Cómo podemos ver si pasó algo entonces? Una forma es volver a preguntarle si está cansada.
3. Pepita está cansada, démosle de comer `pepita.comer(alpiste)`. Y volvámosle a preguntar si está cansada.
  a. Reflexionar: ¿comer es una pregunta o una orden?.
  
## Estado interno
Lo anterior da pie a repasar los conceptos de pregunta y orden, y definir *efecto*: mandar ese mensaje produce cambios (en este caso en el objeto) que perduran en el tiempo. ¿Cómo pasa eso? Lo podemos ver en el *diagrama dinámico•.
- Abrir el diagrama.
- Mandarle algunos mensajes a pepita, ver que cambia la energia.
- Por ahora una definición superficial: ¿qué es eso que se llama energia? => el estado interno de pepita.
  - Cuando le pedimos a pepita que vuele o coma, cambia su estado interno (la `energia`)
  - Eso hace que cambie la forma de responder a `estaCansada`.
  - Desde el REPL es imposible acceder a la energía de pepita, sólo podemos mandarle los mensajes definidos (aunque sí se puede ver en el diagrama, guiño, guiño).

## Háganlo ustedes
Este link tiene las instrucciones para los estudiantes: 
https://docs.google.com/document/d/1_alIoyWBbsuN8rbv1Putx17nBx-DfiCk3Z8IgYYqPrA/edit?usp=sharing. 
Sólo para jugar, los lleva a hacer las cosas que ya hicimos.

# ¿Y cómo se define esto?
Ahora podemos ver la definición de pepita abriendo `pepita.wlk` en el editor. Varias ideas:
- Para cada mensaje se define un método, los métodos no deberían diferenciarse demasiado de las funciones o procedimientos que ya saben.
- Volver a pensar en consultas vs. acciones.
  > El ejemplo no usa `return`, eso dependerá de la elección de cada docente.
  > Podemos notar que los métodos de acción tienen una sintaxis distinta a los métodos de consulta.
- El objeto se compone de *métodos* (=comportamiento) y *referencias* (=datos o estado).

> *Al pasar:* el método `estaFeliz` manda el mensaje `between` a `energia` que esperamos que sea un número. 
> Eso nos ayuda a reforzar que los números son objetos que entienden mensajes.
> Más allá de que hay algunos mensajes como `+` o `>` que tienen una sintaxis especial, más similar a la matemática con la que ya estamos acostumbrados. Es sólo un detalle sintáxtico, son tan mensajes como los otros.

# Más sobre referencias
Volvamos al diagrama:
- Podemos ver que los objetos son las bolitas y las referencias son las flechas.
- Diferentes tipos de referencias: globales y atributos de un objeto (también parámetros pero no aparecen en el diagrama).
- *Bonus:* las referencias pueden ser constantes o variables.
- Al ejecutar una acción, cambia el diagrama, cambian las referencias (las flechas!).
- ¿La suma es una pregunta o una orden? 

  *Demostración:* 
  - Definir una variable x que apunte al mismo número de energía que tenga pepita.
  - En el diagrama se ve que apuntan al mismo objeto, dos flechas al mismo globito.
  - Y preguntarnos, ¿si le doy de comer a pepita, debería cambiar el valor de x? => Espero que todos digan que no.
  - Lo que cambia es la flecha!
  
## Práctica
- Agregar a pepita el mensaje `estaViva` que es verdadero si su energía es mayor que cero.
- Agregar un objeto `manzana` que cuando pepita se lo coma le dé 80 calorías.

> Cuando hayan hecho la manzana podemos preguntarnos cómo hicieron, por qué le pusieron el mensaje energía. Y tirar una primera definición de **polimorfismo**.

# Tarea para la clase que viene
- Instalar el entorno Wollok (y probar pepita en casa).
- Del capítulo 1 de Mumuki hacer las lecciones 1 y 2.
- *Para repasar:* leer los apuntes 1 y 2 de la página de Wollok.
- *Desafío:* modelar el mijo, que es otro objeto que pepita se puede comer. El mijo puede estar seco o mojado. Cuando está seco me da 10 calorías, mojado sólo 2.
