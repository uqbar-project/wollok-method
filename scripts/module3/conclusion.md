# Resumen final del módulo 3
Estas son notas de cierre del módulo, utilizables en contexto de devolución del ejercicio final evaluatorio de la unidad.
Surgen de la corrección del ejercicio de [Servicios Profesionales](https://github.com/wollok/serviciosProfesionales), 
pero son aplicables a otros ejercicios posibles.

## Repaso de conceptos básicos
A esta altura no podemos fallar en:
- Usar polimorfismo
- Usar excepciones

## Repaso sobre uso de nombres:
- Para las **consultas en general**, proponemos usar sustantivo + adjetivo, sin verbos. 
  Por ejemplo `unProfesional.provinciasEnLasQuePuedeTrabajar()`
  
  > Algunas nomenclaturas agregan un `get` o `consultar` delante de las consultas. 
    Nosotros preferimos evitarlo, pero es aceptable si se usa consistentemente.
    
- Para **consultas booleanas** suele ser más interesante utilizar un verbo en tercera persona del presente del indicativo.
  Por ejemplo: `unProfesional.puedeAtenderA(unSolicitante)`
    
- Para las **acciones** proponemos usar un verbo en infinitivo + objeto directo.
  Por ejemplo: `unaEmpresa.atenderA(unSolicitante)`

## Herencia vs. composición
En el ejemplo elegido aparecen un uso de polimorfiso (entre los profesionales) que tiene potencial para ser pensado como 
herencia, pero aún no saben herencia.
Por eso algunos estudiantes pueden proponer usar composición.
Es interesante destacar el descubrimiento del *strategy*/*type object* sin asistencia del docente.

A continuación, esta problemática se puede usar para introducir el concepto de herencia y si apareció la composición se puede
usar para discutir ventajas y desventajas de cada camino.

Conviene destacar también que la interfaz del profesional no debería cambiar en función de la implementación de los 
profesionales. 
En particular, no debería hacer nada del estilo `profesional.tipo().honorarios()`. 
Siempre debe quedarme `profesional.honorarios()` y el profesional delegará en el tipo si correspondiere, 
de forma transparente.

### Delegación
Debido a la falta de herencia, algún estudiante puede estar tentado de no delegar en los profesionales para no repetir el 
código. Conviene mencionar que a partir de incorporar la herencia ese problema desaparece y debemos ser cuidadosos de no 
perder oportunidades de delegar.
