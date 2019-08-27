## Respondimos dudas

Surgieron dudas con el ejercicio [Volando lejos de Mumuki](https://mumuki.io/wollok-obj1/exercises/2669-objetos-y-mensajes-metodos-y-estado-volando-lejos) para completar el método `volarHacia(destino)`.

Salió la idea de **separar la lógica** del cálculo de los kilómetros en otro método, lo cual nos permitió recordar la idea general de _dividir el problema grande en otros más chicos_.
```Wollok
// Primera versión
  method volarHacia(destino) {
    energia = energia - self.kilometrosARecorrer(destino).abs() / 10
    ciudad = destino
  }
  
  method kilometrosARecorrer(destino) {
    return ciudad.kilometro() - destino.kilometro()
  }
```

> También habían tirado la de pasarle dos parámetros al método: origen y destino, lo cual me parece más asertado por como termina la guía.

La mayoría ya conocía `self` pero igual haba dudas de dónde salía. Las aclaramos con unn diagrama en el pizarrón. También recordamos la idea de _acción vs consulta_.

Si bien esto pasaba todas las pruebas, problematizamos dónde tenía que ir el `abs()` probando por consola el mensaje `pepita.kilometrosARecorrer(cordoba)`. Decidimos que debía estar dentro del método. Todo esto permitió hablar de _expresiones_ (porque hace falta paréntesis) pero no dije esa palabra, sino que di la idea de _objetos que van apareciendo en el medio del cálculo_.

```Wollok
// Versión final
  method volarHacia(destino) {
    energia = energia - self.kilometrosARecorrer(destino) / 10
    ciudad = destino
  }
  
  method kilometrosARecorrer(destino) {
    return (ciudad.kilometro() - destino.kilometro()).abs()
  }
```

También hablamos un poco del **polimorfismo entre las ciudades**.

-----

Todo esto nos vino re bien con otra duda del último ejercicio [Responsabilidades: ¿Quién se encarga?](https://mumuki.io/wollok-obj1/exercises/2686-objetos-y-mensajes-metodos-y-estado-responsabilidades-quien-se-encarga) que nos hizo hablar sobre la **responsabilidad de los objetos**, en este caso la de calcular los kilómetros.

> Este ejercicio hace una mención a un problema que se soluciona con clases y lo termina delegando en otro objeto. Todo eso me hizo un poco de ruido:
> - Deja la idea de duplicar el código por la mitad (no se ve implementada).
> - Termina creando un objeto específicamente para hacer este cálculo, que no sé si está bueno en este momento (ver comentarios del Sueldo de Pepe).

En esta versión, pepita habla directamente con el mapa "sin referenciarlo":
```Wollok
  method volarHacia(destino) {
    energia = energia - mapa.distanciaEntre(ciudad, destino)/10
    ciudad = destino
  }
```

Hubo dudas de cómo conocía pepita al mapa y hablamos de las 3 formas que tiene un objeto de conocer a otro:
1. Por medio de un atributo (o variable local, esto no lo dijimos porque no aparecieron **(*)**)
2. Por medio de un parámetros
3. Por medio de una referencia global


## Puesta en común del Mijo

Comenzamos repasando lo que haban hehco de pepita y la idea de **polimorfismo** entre las comidas.

Hicimos una puesta en común del enunciado del mijo:
> Desafío: modelar el mijo, que es otro objeto que pepita se puede comer. El mijo puede estar seco o mojado. Cuando está seco me da 10 calorías, mojado sólo 2.

Propusieron varias soluciones:
- Tener 2 objetos: `mijoSeco` y `mijoMojado`
- Tener un objeto que se guarda `energía`
- Tener un objeto que se guarda `estaMojado`
- Tener un objeto que se guarda un `estado` que pueden ser otros 2 objetos: `seco` o `mojado`

Charlamos sobre las desventajas de las primeras dos frente a las últimas dos en cuanto a **modelado del estado**. Y en la charla mencionamos el _tener como guía el **requerimiento**_.
También discutimos un poco de _modelo vs realidad_.

> **(*)** Para mi en este desafío faltó el `cuantoQuiereVolar()` que mete la idea de _referencias locales_.

## El sueldo de Pepe

Luego tiramos el enunciado del [Sueldo de Pepe](https://github.com/wollok/polimorfismoSueldoDePepe) para que resuelvan. Solamente llegamos a resolver el _sueldo neto_.

### Sueldo neto

Acá surgió una primera solución que:
- Tenía un objeto `contador` encargado de hacer la suma de las 3 partes del sueldo y otro objeto `neto` que se guardaba un booleano `esCadete`.
- Pepe se guardaba el sueldo en un atributo.

Lo que primero hicimos es probar si funcionaba pero rápidamente vimos que no siempre por **el problema del pre-cálculo**. Hablamos de eso y de las ventajas de calcular lo que nos piden en el momento.

Luego problematizamos el Booleano al sugerir una nueva categoría _director_. En palabras de un alumno: "el Booleano te queda chico". Y vimos como acá la idea de **dividir y conquistar** se perdía porque _estábamos dividiendo pero no conquistando_.

**Luego de ir escuchando otras soluciones llegamos a que pepe conozca una categoría con objetos polimórficos** :D

El resto quedó de tarea.
