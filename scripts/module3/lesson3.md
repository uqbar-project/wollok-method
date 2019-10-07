# Introducción
Esta clase propone ser una práctica integradora sobre la unidad 3: clases.
El objetivo es utilizar un dominio más voluminoso que los anteriores, 
por ejemplo se puede utilizar https://github.com/wollok/inscripcionMaterias.
En la descripción que sigue se considera ese ejemplo.

# Algunas notas de cómo llevar adelante el ejercicio
## ¿Cómo comenzar?
Los estudiantes podrían tener dificultades al ser la primera vez que se enfrentan a un ejercicio de este volumen, por lo tanto conviene tomarse unos minutos para charlar con ellos sobre cómo comenzar.

Es un buen momento para fomentar la _metacognición_ sobre sus propios procesos de construcción de un programa preguntándoles, qué herramientas usan para hacerlo. Algunos ejemplos pueden ser:

- Escribir código.
- Proponer objetos candidatos.
- Realizar un diagrama de clases.
- Escribir tests unitarios (TDD).

Para el ejercicio de materias se sugiere comenzar con un diagrama de clases en el que se modelen las relaciones. 
Si no se hizo antes, este es un buen momento para explicar el diagrama más detalladamente.

También, por ser un problema más grande, conviene hablar sobre procesos iterativos.

De mínima, algunas aclaraciones para los estudiantes:
- Este ejercicio no se puede resolver escribiendo código "de una", conviene con una vista de más alto nivel, pensar qué objetos/clases necesitan y quién conoce a quién.
- Cuando escriban tests, van a notar que el _setup_ del test es largo, hay que tomarse tiempo para eso.

## Notas de 2019s1 @ UNSAM
> Esto es material a tener en cuenta, pero una vez procesado lo borramos.

El ejercicio es complicado. Al principió dejé que lo lean todo y que entren en tema. 
Luego les dejé otro rato para que avanzaran, ya con una idea en la cabeza (para algunas cosas planteamos alternativas, así que tampoco quería acotarlos mucho, tal vez eso no estuvo bueno porque...)
Al rato me di cuenta que la mayoría estaba en la nada. Algunos habían podido agregar algunas colecciones e implementar algunos métodos que iban a ser necesarios, pero la gran mayoría seguía perdido. Así que puse el proyector y nos pusimos a resolver el primer punto entre todos.
Al toque me di cuenta que para eso necesitamos saber cómo se iba a inscribir un estudiante a una materia (dónde se guarda la información y blah). Así que comenzamos por el punto 3: Inscribir un alumno a un curso.
Comenzamos con los tests y de a poco fuimos llegando a un modelo de objetos que cerraba. Surgieron dudas con cómo modelar los pre-requisitos (1 clase, 4 clases, 4 objetos). charlamos un poco entre todos y decidimos comenzar por dividir en 4 clases (tal vez el "sin requisitos" podría ser un objeto, pero no me interesaba aclararlo en ese momento, lo dejé para después). Creo que hicimos solo los primeros 2.
Hasta acá, ya algunos estaban re quemados. Stephanie se fue, porque no les salían las cosas (supongo). Quise volver al primer punto pero ya nadie me seguía. Algunos se quedaron copiando lo que estaba en el pizarrón, como volviendo a ver toda la solución y comprendiendo de a poco. No sé, tal vez fui rápido, a mi no me pareció, porque estuvimos toda la clase para resolver solamente ese punto...
Les terminé diciendo que avancen en sus casas, que el modelo ya estaba casi todo planteado, que lo demás no debería ser difícil ahora. Y que seguramente lo seguiríamos la clase que viene, que quería retomarlo para explicar excepciones el Martes.

El ejercicio que tiene una barrera alta: (para comenzar necesitás tomar muchísimas decisiones de las cuales muchas no estás seguro, tenés que tener todos los puntos en la cabeza). Además de que, comparado con los ejercicios que veníamos haciendo, no es incremental: ya el primer punto te hace tener en cuenta cosas que se ven en los otros. No digo que eso esté mal, pero agrega una complejidad que no sé si me sienta cómodo. Bah, tal vez yo no supe cómo manejar la situación, pero toda una clase para hacer un solo punto y que la gente se vaya diciendo "ya no me da el bocho", me hace un toque de ruido, no estaban preparados para eso.
No sé, para mi habría que revisar ese ejercicio: sacar cosas (cada punto agrega un montón de cosas) u ordenarlo un toque más (que sea más guiado y que parta de requerimientos más chicos tal vez).
