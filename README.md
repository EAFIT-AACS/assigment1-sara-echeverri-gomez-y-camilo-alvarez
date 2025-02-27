[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/95BWY5mA)

**DFA**

**1. Información de los Estudiantes del equipo**
*Nombre del estudiante:* Camilo Álvarez Villegas, Sara Echeverri

*Número de clase:* Camilo Alvarez Villegas(Lunes de 6pm-9pm SI2002-1 (7308)), Sara Echeverri(Miercoles de 6pm-9pm SI2002-2 (7309))

**2. Versiones del Sistema Operativo, Lenguaje de Programación y Herramientas**
- Sistema Operativo: Windows 10 (64 bits)
- Lenguaje de programación: Python 3.9.7
- Herramientas y Librerías Utilizadas:
  Biblioteca sys

**3. Instrucciones para Ejecutar la Implementación**
  1. Descargar o clonar

  2. Asegurarse de tener Python 3 instalado

  3. Ubicar el archivo input.txten la misma carpeta donde está el códigominimiza_dfa.py

  4.Ejecutar el script con el siguiente comando:

*python minimiza_dfa.py
o instalar la extensión code runner y ejecutar normalmente el código*

5. El programa leerá el archivo input.txty mostrará los resultados en la consola.

***Formato del archivoinput.txt***
El archivo de entrada debe seguir el siguiente formato:

1. La primera línea contiene un número entero, que indica la cantidad de casos de prueba.
2. Para cada caso de prueba:
- Una línea con un número entero, que representa la cantidad de estados.
- Una línea con los símbolos del alfabeto (separados por espacios).
- Una línea con los estados finales (separados por espacios).
- n líneas, cada una con las transiciones de un estado (una fila por estado, con una columna por cada símbolo del alfabeto).

**4. Explicación del algoritmo**
Este programa implementa el algoritmo de minimización de DFA .

***1. Marcar pares de estados distinguibles (Paso Inicial)***

Se marcan como diferentes aquellos pares (p, q)donde uno es un estado final y el otro no lo es.

***2. Propagar diferencias***
Si un par (p, q)no está marcado, pero al hacer una transición con algún símbolo lleva a un par (r, s)ya marcado, entonces (p, q)también se marca.

***3. Repetir hasta estabilidad***
Este proceso se repite hasta que en una iteración completa no haya más cambios en la tabla de marcados.

***4. Determinar los estados equivalentes***
Los pares de estados que no han sido marcados son equivalentes y pueden ser fusionados en el DFA minimizado.


El programa imprime los pares de estados equivalentes.
