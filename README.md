# Practicas-Fundamentos-de-Computadores
En este repositorio van a estar las prácticas que hice el curso 2021-2022 sobre **Fundamentos de Computadores**. Voy a añadir los códigos y los correspondientes organigramas, a continuación explicaré el contenido de cada práctica.

### Cada práctica es sobre un ejercicio diferente que teníamos que conseguir que funcionase en un microprocesador 8085 con teclado.


1. La primera práctica simplemente consistía en cambiar el valor de dos posiciones de memoria con un número diferente en cada uno, en nuestro caso fue con un 3 en la dirección 1200H y un 5 en la dirección 1201H.

2. La segunda práctica consistía en hacer lo mismo que en la primera pero con un 9 y un 10, en vez de un 3 y un 5, pero debíamos hacerlo con el simulador en vez de con el microprocesador en clase. Por tanto esta práctica nos sirvió para entender a cómo usar el simulador (Añadiré una imagen del simulador al final de la descripción de las prácticas).

3. La tercera práctica consistía en sumar dos números en memoria y el resultado ajustarlo a [BCD](https://es.wikipedia.org/wiki/Decimal_codificado_en_binario) y guardarlo en la memoria en otra dirección. Además, a partir de esta práctica ya tuvimos que saber demostrar que podíamos hacerlo tanto en el simulador como en el microprocesador con el teclado.

4. La cuarta práctica consistía en multiplicar dos datos de 4 bits sin signo. Usamos el algoritmo de suma por desplazamiento (Incluyendo o no las sumas parciales 0). Los operandos debían quedar en las posiciones 1200H y 1201H y el resultado en la dirección 1202H. Para poder entregar esta práctica tuvimos que demostrar también que sabíamos cómo funcionaba el algoritmo de suma por desplazamiento en papel.

5. La quinta práctica consistía en realizar la tabla de multiplicar de un número elegido por el usuario. En realidad consistía en almacenar el número y hacer las multiplicaciones como en la práctica 4 pero hasta acabar la tabla del número en cuestión. Esto nos enseñó a manejar bien los bucles. Probamos los números del 1 al 9.

6. La sexta práctica consistía en que al pulsar una tecla del teclado, tanto en el simulador como en el microprocesador, se representase esa tecla en la pantalla. El teclado actúa sobre la interrupción RST 5.5 cada vez que se produce una pulsación, tuvimos que desenmascarar esa interrupción, habilitar la atención de interrupciones para poder saber si se había producido y luego llamar a una rutina contenida en el programa monitor en la posición 044EH que nos dejó en el acumulador el valor de la tecla. De la misma manera la rutina situada en la dirección 04D5H nos permitía visualizar en la pantalla el contenido del acumulador. Además, mejoramos el programa propuesto incluyendo una condición de salida al pulsar la tecla del número "0" abortando la ejecución (HLT).

7. No hay séptima práctica pero he subido también un examen parcial que hice. Es una mezcla de las prácticas en realidad ya que lee un número introducido por teclado por el usuario y realiza la tabla de multiplicar de ese número. Es una mezcla de las prácticas 5 y 6 ya que en la 5 no usábamos input para añadir el número de la tabla de multiplicar. Además, incluí un comentario en cada línea para saber lo que estaba haciendo en todo momento en el examen, por si me resultaba confuso, así que no creo que tenga que explicar nada más.

> Por si alguien quiere entender mejor cómo hemos hecho las siguientes prácticas puede mirar esta página en la que hay recopilados todos los comandos que hemos usado para resolver los ejercicios [Comandos ensamblador](https://exa.unne.edu.ar/ingenieria/circuitos_logicos/archivos/instrucciones8085.pdf) o este repositorio de GitHub en el que está el manual donde se explica para qué sirve cada comando y cómo usarlo [Manual del Intel 8085](https://github.com/Mervill/Net8080/blob/master/docs/Intel%208080-8085%20Assembly%20Language%20Programming%201977%20Intel.pdf)
>
> Además, por si alguien quiere saber cómo funciona el algoritmo de suma por desplazamiento puede ver [este video](https://www.youtube.com/watch?v=T_r0B_uYdO4) de la universidad Rey Juan Carlos de Madrid en el que se explica cómo se hace en papel. Nuestra solución es con los registros, pero también tuvimos que hacerlo a papel.
