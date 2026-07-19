<h1 align="center">🚀 Unidad 3: Programación Modular y Estructuras de Datos Estáticas 🚀</h1>

<p align="center">
  <img src="https://unl.edu.ec/sites/default/files/logogris%20copia.png" alt="Logotipo UNL" width="350">
</p>


<p align="center">
📚 Glosario de contenidos • 💻 Ejercicios Prácticos • 🧐 Reflexión
</p>

---

# 🎨 1. Glosario Interactivo de Contenidos

*Haz clic sobre cada apartado para conocer los fundamentos teóricos de la Unidad 3.*

<details>

<summary><b>🧩 CLIC AQUÍ para explorar la Programación Modular</b></summary>

---

# 📖 ¿Qué es la Programación Modular?

La **programación modular** es una metodología de desarrollo de software que consiste en dividir un programa grande en pequeñas partes llamadas **módulos** o **funciones**, donde cada una realiza una tarea específica.

En lugar de escribir todo el código dentro de la función `main()`, el programa se organiza en funciones independientes que pueden ser llamadas cuando sea necesario. Esta metodología facilita el mantenimiento del código, mejora la legibilidad y permite reutilizar funciones en diferentes proyectos.

---

#### 📈 Ventajas de la Modularización
* **Reutilización de Código:** Evita la redundancia al escribir un bloque lógico una sola vez y permitir su invocación infinitas veces desde cualquier sección del software.
* **Fácil Depuración y Mantenimiento:** Facilita el aislamiento de errores (bugs). Si un cálculo falla, se corrige directamente el módulo afectado sin alterar el resto de la arquitectura del programa.

---

#### 🧩 Anatomía de una Función en C
Toda función consta de tres componentes esenciales e interconectados:
1. **Cabecera (Header):** Define el tipo de dato de retorno, el identificador de la función y la lista de parámetros formales con sus respectivos tipos (ej. `float calcularPromedio(int nota1, int nota2)`).
2. **Cuerpo (Body):** Bloque de código delimitado por llaves `{ }` donde se ejecutan las operaciones e instrucciones algorítmicas locales.
3. **Retorno (Return):** Sentencia implícita u explícita (`return expresión;`) que envía el resultado calculado de vuelta al módulo invocador y finaliza la ejecución de la función. En procedimientos sin retorno se utiliza el tipo de dato `void`.

---

## 🧩 Estructura general de una función en C++

<p align="center">
  <img src="https://sensoricx.com/wp-content/uploads/2022/07/funciones.png" alt="Logotipo UNL" width="350">
</p>

---

## 📊 Estructura general de la modularidad

<p align="center">
  <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjUI5g8euGSEZsDNJiYSQwpAelALiqrhBYzoHoRprA0muXsbCI-lW3RQLFY8cFbmhPHnM1Wn6xehHUE07xzCeVDhMm8UItF4aJuVyhWvsVyajj8UMMmxHXMpKmsqx3YIJSXd5PpD1kJ5AY/s1600/slide_6.jpg" alt="Logotipo UNL" width="350">
</p>

# 🎯 Transmisión de Parámetros

Cuando una función necesita trabajar con información externa, se utilizan **parámetros**.

Existen dos formas principales de pasar parámetros:

---

## 🔹 Paso por Valor

En este método la función recibe **una copia** del dato original.

Los cambios realizados dentro de la función **NO modifican** la variable original.

### 📊 Esquema

```text
main()

numero = 10

↓

Función(numero)

↓

Copia = 10

↓

Se modifica la copia

↓

numero sigue valiendo 10
```

### 💻 Ejemplo

```c
void duplicar(int numero){
    numero = numero * 2;
}
```

---

## 🔸 Paso por Referencia

En este método la función recibe la **dirección de memoria** de la variable utilizando punteros.

Los cambios realizados dentro de la función **sí modifican** la variable original.

### 📊 Esquema

```text
main()

numero = 10

↓

&numero

↓

Función(&numero)

↓

*numero = 20

↓

numero ahora vale 20
```

### 💻 Ejemplo

```c
void duplicar(int *numero){
    *numero = *numero * 2;
}
```

---

> 💡 **Dato curioso**
>
> El paso por referencia es ampliamente utilizado cuando se trabaja con arreglos, estructuras y grandes cantidades de datos, ya que evita realizar copias innecesarias en la memoria.

</details>

---

<details>

<summary><b>📚 CLIC AQUÍ para explorar los Arreglos</b></summary>

---

# 🧮 ¿Qué es un Arreglo?

Un **arreglo** es una estructura de datos que permite almacenar múltiples valores del mismo tipo bajo un único nombre.

Cada elemento ocupa una posición consecutiva en memoria y puede accederse mediante un índice.

---

## 🎯 Ventajas

📌 Organización de datos.

📌 Acceso rápido mediante índices.

📌 Facilita el procesamiento masivo de información.

📌 Reduce la cantidad de variables.

---

# 🔹 Arreglo Unidimensional (Vector)

Es una colección de datos organizada en una sola dimensión.

```text
Índice

0    1    2    3    4

┌───┬───┬───┬───┬───┐

│10 │25 │18 │40 │50 │

└───┴───┴───┴───┴───┘
```

### 💻 Ejemplo

```c
int edades[5]={18,20,19,22,21};
```

---

# 🔹 Arreglo Bidimensional (Matriz)

Organiza los datos en filas y columnas.

```text
      Col

      0   1   2

Fila

0    12  15  20

1    10  18  25

2    30  22  14
```

### 💻 Ejemplo

```c
int matriz[3][3];
```

---

# 🔹 Arreglo Multidimensional

Permite representar información con tres o más dimensiones.

Es utilizado en gráficos 3D, videojuegos, simulaciones científicas y procesamiento de imágenes.

```text
matriz[x][y][z]
```

---

## 🌍 Aplicaciones

🎮 Videojuegos

📷 Procesamiento de imágenes

📊 Bases de datos

🤖 Inteligencia Artificial

📡 Redes

📈 Estadística

---

> 💡 **Importante**
>
> Los arreglos almacenan únicamente datos del mismo tipo y sus posiciones comienzan desde el índice **0** en lenguaje C.

</details>

---

# 📈 4. Principales Dificultades Encontradas

<details>

<summary><b>⚠️ CLIC AQUÍ para explorar las dificultades</b></summary>

Durante el desarrollo de esta unidad se presentaron diversos retos relacionados con la programación modular y el manejo de arreglos.

* Comprender cuándo utilizar una función y cuándo mantener el código dentro de `main()`.
* Diferenciar claramente el paso de parámetros por valor y por referencia.
* Entender el funcionamiento de los punteros durante el paso por referencia.
* Manipular correctamente los índices de los arreglos evitando errores fuera de rango.
* Recorrer matrices mediante ciclos anidados sin perder el control de filas y columnas.

> ⚠️ **Lección aprendida**
>
> Una mala organización del código dificulta el mantenimiento del programa y aumenta la probabilidad de errores.

</details>

---

# 🧠 5. Reflexión Crítica

<details>

<summary><b>💭 CLIC AQUÍ para explorar la reflexión</b></summary>

El estudio de la programación modular permitió comprender que desarrollar software no consiste únicamente en escribir instrucciones, sino en construir soluciones organizadas, reutilizables y fáciles de mantener.

La utilización de funciones fortaleció mi capacidad para dividir problemas complejos en tareas más pequeñas, facilitando el diseño de algoritmos claros y eficientes. Por otra parte, el aprendizaje de los arreglos permitió almacenar y procesar grandes cantidades de información de forma ordenada, aspecto fundamental en el desarrollo de aplicaciones reales.

Considero que esta unidad representa un paso importante en mi formación como futura Ingeniera en Computación, ya que introduce principios de organización del código que serán indispensables en asignaturas posteriores como Estructuras de Datos, Programación Orientada a Objetos, Bases de Datos y Desarrollo de Software.

</details>

---

<p align="center">

**<strong><a href="Portafolio.md">INICIO</a></strong>**

</p>




<p align="center">
**<strong><a href="Portafolio.md">**INICIO**</a></strong>**
</p>
