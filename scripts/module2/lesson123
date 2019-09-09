# Introducción a bloques utilizando Wollok game

## Clase 1 con WG
Tutorial 1: Familiarizarse con el framework
Comienza Pepita como character y el cambio de imagen cuando Pepita llega al nido
Desafíos:
Meter a Silvestre que se mueve siempre a la altura del piso y persigue a Pepita en el eje x. 
Hacer que pepita se vea "muerta" cuando la alcanza Silvestre.
POSIBLE IDEA: Meter una pared en x=3 y hacer que silvestre no pueda estar x <= 3 .

Tutorial 2: Agregar acciones con teclas
Motivador: Queremos que Pepita gaste energía a medida que se mueve -> ya no nos sirve el character (necesitamos control de lo que se ejecuta)
Ya le damos las configs para mover a pepita Izq y Der y llaman al método irA(pos) que cambia la energía
Desafíos:
Configurar la tecla Arriba para que pepita vaya 1 posición hacia arriba.
Si pepita está muerta (energía <= 0) entonces no se puede mover y se muestra "gris".
Configurar la tecla C para que cuando esté arriba de una comida la coma: aumente su energía y desaparezca del juego. (Darles un método para obtener UN collider, en vez de una lista).
BONUS: Al morir pepita, esperar 2 segundos y terminar el juego (stop + schedule(? ).

- Clase 2 con WG
Tutorial 3: Intro colisiones
Motivador: Queremos manejar otro tipo de acciones: las colisiones
Ya les damos la colisión con el nido que gana -> Doble distpach + game.stop.
Teórica: Problematizar las colisiones con otra cosa que no sea un nido -> ver cómo se rompe el polimorfismo.
Desafíos:
Arreglar la colisión con las comidas (que no pase nada / no explote).
Agregar la colisión con Silvestre que pierde -> game.stop (directo).
BONUS: Al perder / ganar agregar un game.say + schedule (delay del stop).

Nivel 1: Eventos
Desafíos:
Meter la gravedad -> onTick
Hacer los BONUS anteriores

- Para después del ejercicio de colecciones
Nivel 2: Colecciones
Desafíos:
Pepita puede llevar cosas consigo. Parada sobre una cosa (por ahora comidas) presionas la A (de agarrar, ponele, nótese que no digo guardar ni mochila, esto habilita a que se lleve consigo a un hijo, un amigo, lo que fuere).
TODO...

La idea es mañana llevar los enunciados (y el código de base) armados. Cuando los tenga en un repo paso links. Estamos en contacto!
