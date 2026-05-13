# P2_APE3_Arbol
# Guía Práctica de Estructuras de Datos: Árboles

[![C++](https://img.shields.io/badge/C++-11-blue.svg)](https://isocpp.org/)
[![Java](https://img.shields.io/badge/Java-11-orange.svg)](https://www.oracle.com/java/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Descripción

Este repositorio contiene la implementación completa de **5 ejercicios fundamentales** sobre estructuras de datos jerárquicas (árboles) en los lenguajes **C++** y **Java**. Cada ejercicio incluye código funcional con métodos `main` de prueba integrados para verificar su correcto funcionamiento.

## Objetivos de Aprendizaje

Al completar estos ejercicios, serás capaz de:

1.  Comprender y manipular la estructura de **árboles N-arios** (nodos con múltiples hijos)
2.  Implementar **inserciones en Árboles Binarios de Búsqueda (BST)**
3.  Utilizar **recursividad** para calcular métricas estructurales (altura)
4.  Extraer datos mediante **recorridos estándar** (In-Order)
5.  Modificar la estructura de punteros para **transformar árboles** (inversión/espejo)

# Estructura del Repositorio
````
/arboles-guia-practica/
│
├── cpp/ # Implementaciones en C++
│ ├── Ejercicio1_Basico.cpp # Árboles N-arios (conteo de nodos)
│ ├── Ejercicio2_Binario.cpp # BST - Inserción
│ ├── Ejercicio3_Binario.cpp # BST - Cálculo de altura
│ ├── Ejercicio4_Recorridos.cpp # BST - Recorrido In-Order
│ └── Ejercicio5_Transformacion.cpp # BST - Árbol espejo
│
├── java/ # Implementaciones en Java
│ ├── Ejercicio1_Basico.java # Árboles N-arios (conteo de nodos)
│ ├── Ejercicio2_Binario.java # BST - Inserción
│ ├── Ejercicio3_Binario2.java # BST - Cálculo de altura
│ ├── RecorridoInOrder.java # BST - Recorrido In-Order
│ └── Ejercicio5_Transformacion.java # BST - Árbol espejo
│
├── INFORME_TECNICO.md # Documentación técnica detallada
└── README.md # Este archivo

````
#  Ejercicios

### Ejercicio 1: Conteo de Nodos (Árboles N-arios)
Contar la cantidad total de nodos en un árbol N-ario mediante recursividad.

**Estructura del árbol de prueba:**
````
1 (raíz)
/ |
2 3 4
/
5 6
````

**Resultado esperado:** 6 nodos

### Ejercicio 2: Inserción en BST
Insertar valores en un Árbol Binario de Búsqueda manteniendo su propiedad.

**Secuencia de inserción:** 10 → 5 → 15 → 3

**Estructura resultante:**
````
10
/
5 15
/
3
````

### Ejercicio 3: Cálculo de Altura
Calcular la profundidad máxima (altura) de un árbol binario.

**Árbol de prueba:** 1 → 2 → 3 (estructura sesgada)
**Resultado esperado:** 3 niveles

### Ejercicio 4: Recorrido In-Order
Listar los elementos del árbol en orden (Izquierda → Raíz → Derecha).

**Árbol de prueba:**
````
4
/
2 6
/ \ /
1 3 5 7
````

**Resultado esperado:** 1, 2, 3, 4, 5, 6, 7

### Ejercicio 5: Transformación (Árbol Espejo)
Invertir el árbol intercambiando los hijos izquierdo y derecho.

**Transformación:**
Antes: Después:
  1       1
/  \    /  \
2   3 → 3    2


## Instalación y Ejecución

### Requisitos Previos

| Herramienta | Versión | Comando de verificación |
|-------------|---------|------------------------|
| **C++ Compiler** | C++11 o superior | `g++ --version` |
| **Java JDK** | 11 o superior | `java --version` |
| **Git** | Cualquier versión | `git --version` |

### Clonar el Repositorio

```bash
git clone https://github.com/Steven9tp/arboles-guia-practica.git
cd arboles-guia-practica
Ejecutar en C++
bash
# Compilar
cd cpp
g++ Ejercicio1_Basico.cpp -o ejercicio1
g++ Ejercicio2_Binario.cpp -o ejercicio2
g++ Ejercicio3_Binario.cpp -o ejercicio3
g++ Ejercicio4_Recorridos.cpp -o ejercicio4
g++ Ejercicio5_Transformacion.cpp -o ejercicio5

# Ejecutar
./ejercicio1
./ejercicio2
./ejercicio3
./ejercicio4
./ejercicio5
Ejecutar en Java
bash
# Compilar
cd java
javac Ejercicio1_Basico.java
javac Ejercicio2_Binario.java
javac Ejercicio3_Binario2.java
javac RecorridoInOrder.java
javac Ejercicio5_Transformacion.java

# Ejecutar
java Ejercicio1_Basico
java Ejercicio2_Binario
java Ejercicio3_Binario2
java RecorridoInOrder
java Ejercicio5_Transformacion
Compilación y Ejecución en un Solo Paso (Linux/Mac)
bash
# C++
cd cpp && for file in *.cpp; do g++ "$file" -o "${file%.cpp}"; ./"${file%.cpp}"; done

# Java
cd java && for file in *.java; do javac "$file"; java "${file%.java}"; done
* Resultados Esperados
C++
Ejercicio	Salida Esperada
1	Nodos calculados: 6
2	Raiz: 10, Izq: 5, Der: 15, Izq-Izq: 3
3	Altura calculada: 3
4	1 2 3 4 5 6 7
5	Izq: 3, Der: 2
Java
Ejercicio	Salida Esperada
1	Nodos calculados: 6
2	Raiz: 10, Izq: 5, Der: 15, Izq-Izq: 3
3	Altura calculada: 3
4	[1, 2, 3, 4, 5, 6, 7]
5	Izq: 3, Der: 2
* Conceptos Clave
Complejidad Algorítmica
Operación	Complejidad Temporal	Complejidad Espacial
Conteo de nodos	O(n)	O(h)
Inserción BST	O(log n) promedio	O(h)
Cálculo de altura	O(n)	O(h)
Recorrido In-Order	O(n)	O(n)
Inversión de árbol	O(n)	O(h)
Donde n = número de nodos, h = altura del árbol

Terminología
Término	Definición
Raíz	Nodo superior sin padre
Hoja	Nodo sin hijos
Nodo interno	Nodo con al menos un hijo
Nivel	Distancia desde la raíz
Altura	Máximo número de niveles
BST	Binary Search Tree (Árbol Binario de Búsqueda)
*  Diferencias C++ vs Java
Aspecto	C++	Java
Gestión de memoria	Manual (new/delete)	Automática (GC)
Punteros	Explícitos (*, ->)	Referencias implícitas
Colecciones	std::vector	ArrayList
Valor nulo	nullptr	null
Máximo de números	std::max()	Math.max()
* Próximas Mejoras (Roadmap)
Implementar operación de búsqueda en BST

Agregar recorridos Pre-Order y Post-Order

Implementar eliminación de nodos (3 casos)

Crear árbol balanceado (AVL)

Agregar persistencia (guardar/cargar árbol desde archivo)

Visualización gráfica de árboles

Pruebas unitarias automatizadas


