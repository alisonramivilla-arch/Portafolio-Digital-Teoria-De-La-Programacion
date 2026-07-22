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

## 📌 Ejemplo aplicado

```c
#include <stdio.h>

void mostrarMenu();
float depositar(float saldo, float cantidad);
float retirar(float saldo, float cantidad);
void consultarSaldo(float saldo);

int main() {
    int opcion;
    float saldo = 1000.0f;
    float cantidad;

    do {
        mostrarMenu();
        if (scanf("%d", &opcion) != 1) {
            break;
        }

        switch (opcion) {
            case 1:
                printf("Ingrese cantidad a depositar: ");
                scanf("%f", &cantidad);
                saldo = depositar(saldo, cantidad);
                break;
            case 2:
                printf("Ingrese cantidad a retirar: ");
                scanf("%f", &cantidad);
                saldo = retirar(saldo, cantidad);
                break;
            case 3:
                consultarSaldo(saldo);
                break;
            case 4:
                printf("Saliendo...\n");
                break;
            default:
                printf("Opcion invalida.\n");
        }
    } while (opcion != 4);

    return 0;
}

void mostrarMenu() {
    printf("\n--- BANCO MODULAR ---\n");
    printf("1. Depositar\n");
    printf("2. Retirar\n");
    printf("3. Consultar saldo\n");
    printf("4. Salir\n");
    printf("Elija una opcion: ");
}

float depositar(float saldo, float cantidad) {
    if (cantidad > 0) {
        saldo += cantidad;
        printf("Deposito exitoso. Nuevo saldo: %.2f\n", saldo);
    } else {
        printf("Cantidad invalida.\n");
    }
    return saldo;
}

float retirar(float saldo, float cantidad) {
    if (cantidad > 0 && cantidad <= saldo) {
        saldo -= cantidad;
        printf("Retiro exitoso. Nuevo saldo: %.2f\n", saldo);
    } else {
        printf("Fondos insuficientes o cantidad invalida.\n");
    }
    return saldo;
}

void consultarSaldo(float saldo) {
    printf("Saldo actual: %.2f\n", saldo);
}

```

# 🎯 Paso de Parámetros

El **paso de parámetros** es el mecanismo mediante el cual un programa principal o una función envía datos (*argumentos*) a otra función para que esta pueda procesarlos y ejecutar su tarea. Los valores que recibe la función en su definición se denominan *parámetros*.

## Características Principales

* **Comunicación y Modularidad:** Permite la reutilización de código al enviar diferentes entradas a una misma función para obtener resultados adaptados a cada caso.
* **Ámbito Local:** Por defecto, los parámetros actúan como variables locales dentro de la función receptora, existiendo únicamente mientras la función está en ejecución.
* **Mecanismos de Transferecia:** Dependiendo del lenguaje de programación y de la necesidad del algoritmo, los parámetros se pueden transferir principalmente de dos formas: **por valor** (copiando el dato) o **por referencia** (compartiendo la dirección de memoria).

---

## 🔹 Paso por Valor

El **paso de parámetros por valor** es un mecanismo de comunicación con funciones donde se realiza una **copia exacta del valor** de la variable original y se le asigna al parámetro local de la función receptora. 

## Características Principales

* **Independencia de Variables:** Como la función trabaja con una copia ubicada en otra dirección de memoria, cualquier modificación que sufra el parámetro dentro de la función **no afecta** a la variable original del código que la llamó.
* **Seguridad de Datos:** Previene efectos secundarios accidentales (*side effects*), ya que el estado original de la variable permanece intacto fuera del ámbito de la función.
* **Consumo de Memoria y Rendimiento:** Para tipos de datos primitivos es muy eficiente; sin embargo, al tratarse de estructuras grandes (como arreglos o estructuras complejas), copiar todo el contenido puede disminuir el rendimiento.

### 📊 Esquema

<p align="center">
  <img src="blob:https://web.whatsapp.com/68875b54-9e17-4e91-9e81-8be1fa17a20a" alt="Logotipo UNL" width="350">
</p>

### 💻 Ejemplo

```c
#include <stdio.h>

void modificarValor(int x);

int main() {
    int numero = 10;

    printf("Antes de la funcion: numero = %d\n", numero);
    modificarValor(numero);
    printf("Despues de la funcion: numero = %d\n", numero);

    return 0;
}

void modificarValor(int x) {
    x = 20;
    printf("Dentro de la funcion: x = %d\n", x);
}
```

---

## 🔸 Paso por Referencia

El paso por referencia en **C** se simula explícitamente utilizando **punteros** para pasar la dirección de memoria de la variable original a la función. Esto permite que la función llamada acceda y modifique directamente el valor almacenado en esa dirección. Como resultado, los cambios realizados en los parámetros sí persisten fuera de la función, afectando a las variables originales.

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

### 💻 Ejemplo aplicado

```c
#include <stdio.h>

void modificarPorReferencia(int *x);

int main() {
    int numero = 10;

    printf("Antes de la funcion: numero = %d\n", numero);
    modificarPorReferencia(&numero);
    printf("Despues de la funcion: numero = %d\n", numero);

    return 0;
}

void modificarPorReferencia(int *x) {
    *x = 20;
    printf("Dentro de la funcion (*x): x = %d\n", *x);
}
```
---

### 📌 Ejemplo aplicado de ambos conceptos
```c
#include <stdio.h>

void operar(int valor, int *referencia);

int main() {
    int a = 5;
    int b = 10;

    printf("Antes - a (por valor): %d, b (por referencia): %d\n", a, b);
    operar(a, &b);
    printf("Despues - a (por valor): %d, b (por referencia): %d\n", a, b);

    return 0;
}

void operar(int valor, int *referencia) {
    valor = valor * 2;
    *referencia = *referencia * 2;
    printf("Dentro - valor modificado localmente: %d, referencia modificada en memoria: %d\n", valor, *referencia);
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

Un **arreglo unidimensional** (también llamado vector) es una estructura de datos estática que almacena una **colección finita, homogénea y ordenada** de elementos. Esto significa que todos los elementos ocupan posiciones consecutivas en la memoria RAM y pertenecen al mismo tipo de dato (por ejemplo, enteros, flotantes, caracteres).

## Características Principales

* **Homogeneidad:** Todos los elementos del arreglo comparten exactamente el mismo tipo de dato.
* **Secuencialidad:** Los elementos se almacenan en bloques de memoria contiguos.
* **Indexación:** Cada posición del arreglo se identifica mediante un **índice** numérico (que comúnmente empieza desde `0` en la mayoría de lenguajes de programación modernos como C, Java o Python).

<p align="center">
  <img src="https://prog-o-manuais-plantillas-daw-bed5b048cbcd5bc455e9794fac9da239d.pages.iessanclemente.net/arrays/arraysuni/array.png" alt="Logotipo UNL" width="350">
</p>


### 💻 Ejemplo

```c
int edades[5]={18,20,19,22,21};
```

### 📌 Ejemplo Aplicado

```c
#include <stdio.h>

int numeros[5] = {1, 2, 3, 4, 5};

void mostrarArreglo() {
    for (int i = 0; i < 5; i++) {
        printf("%d ", numeros[i]);
    }
    printf("\n");
}

void duplicarArreglo() {
    for (int i = 0; i < 5; i++) {
        numeros[i] = numeros[i] * 2;
    }
}

int main() {
    printf("Arreglo original: ");
    mostrarArreglo();

    duplicarArreglo();

    printf("Arreglo modificado: ");
    mostrarArreglo();

    return 0;
}
```
---

# 🔹 Arreglo Bidimensional (Matriz)

Un **arreglo bidimensional** (comúnmente llamado **matriz** o tabla) es una estructura de datos que extiende el concepto de los vectores al utilizar **dos dimensiones**. Se puede visualizar como una cuadrícula compuesta por filas y columnas, donde cada elemento requiere de dos índices para ser identificado: uno para la fila y otro para la columna.

## Características Principales

* **Homogeneidad:** Al igual que los vectores, todos los elementos almacenados en una matriz deben ser estrictamente del mismo tipo de dato.
* **Estructura Matricial:** Los datos se organizan en $m$ filas y $n$ columnas, formando un total de $m \times n$ elementos.
* **Doble Indexación:** Se accede a cada elemento mediante un par de índices: el primero indica la fila (`i`) y el segundo la columna (`j`).

<p align="center">
  <img src="https://www.programandojava.com/images/ArregloInt2x3Vacio.png" alt="Logotipo UNL" width="350">
</p>


### 💻 Ejemplo

```c
int matriz[3][3] = {
                    {1, 2, 3},
                    {4, 5, 6},
                    {7, 8, 9}
                   };
```

### 📌 Ejemplo Práctico

```c
#include <stdio.h>

void mostrarMatriz(int matriz[3][3], int filas, int columnas);
void duplicarMatriz(int matriz[3][3], int filas, int columnas);

int main() {
    int matriz[3][3] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    printf("Matriz original:\n");
    mostrarMatriz(matriz, 3, 3);

    duplicarMatriz(matriz, 3, 3);

    printf("Matriz modificada:\n");
    mostrarMatriz(matriz, 3, 3);

    return 0;
}

void mostrarMatriz(int matriz[3][3], int filas, int columnas) {
    for (int i = 0; i < filas; i++) {
        for (int j = 0; j < columnas; j++) {
            printf("%d ", matriz[i][j]);
        }
        printf("\n");
    }
}

void duplicarMatriz(int matriz[3][3], int filas, int columnas) {
    for (int i = 0; i < filas; i++) {
        for (int j = 0; j < columnas; j++) {
            matriz[i][j] = matriz[i][j] * 2;
        }
    }
}
```

---

# 🔹 Arreglo Multidimensional

Un **arreglo multidimensional** es una estructura de datos que extiende el concepto de las matrices a **tres o más dimensiones** ($N$ dimensiones). Se puede visualizar conceptualmente como un "cubo" de datos (3D), un arreglo de cubos (4D), y así sucesivamente, donde cada elemento requiere $N$ índices para ser localizado de forma unívoca.

## Características Principales

* **Homogeneidad:** Todos los elementos contenidos en el arreglo pertenecen estrictamente al mismo tipo de dato.
* **Dimensionalidad Múltiple:** Utiliza tres o más índices independientes para representar relaciones de datos más complejas (por ejemplo: coordenadas espaciales $(x, y, z)$, series temporales con matrices, o voxels en gráficos 3D).
* **Almacenamiento Continuo:** A pesar de su representación lógica en múltiples dimensiones, la memoria RAM sigue siendo lineal; el compilador mapea estos índices multidimensionales a un bloque de memoria contiguo (típicamente en orden de filas principales - *row-major order*).

<p align="center">
  <img src="https://miro.medium.com/v2/resize:fit:1400/1*VbVvxuuT7L2k-imWZKNp8w.png" alt="Logotipo UNL" width="350">
</p>

```text
matriz[x][y][z] = {
    {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    },
    {
        {10, 11, 12},
        {13, 14, 15},
        {16, 17, 18}
    }
};
```
### 📌 Ejemplo Práctico
```c
#include <stdio.h>

void mostrarCubo(int cubo[2][3][3], int capas, int filas, int columnas);
void duplicarCubo(int cubo[2][3][3], int capas, int filas, int columnas);

int main() {
    int cubo[2][3][3] = {
        {
            {1, 2, 3},
            {4, 5, 6},
            {7, 8, 9}
        },
        {
            {10, 11, 12},
            {13, 14, 15},
            {16, 17, 18}
        }
    };

    printf("Cubo original:\n");
    mostrarCubo(cubo, 2, 3, 3);

    duplicarCubo(cubo, 2, 3, 3);

    printf("Cubo modificado:\n");
    mostrarCubo(cubo, 2, 3, 3);

    return 0;
}

void mostrarCubo(int cubo[2][3][3], int capas, int filas, int columnas) {
    for (int k = 0; k < capas; k++) {
        printf("Capa %d:\n", k + 1);
        for (int i = 0; i < filas; i++) {
            for (int j = 0; j < columnas; j++) {
                printf("%d ", cubo[k][i][j]);
            }
            printf("\n");
        }
        printf("\n");
    }
}

void duplicarCubo(int cubo[2][3][3], int capas, int filas, int columnas) {
    for (int k = 0; k < capas; k++) {
        for (int i = 0; i < filas; i++) {
            for (int j = 0; j < columnas; j++) {
                cubo[k][i][j] = cubo[k][i][j] * 2;
            }
        }
    }
}
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

<details>

<summary><b>⚠️ CLIC AQUÍ para explorar Ejercicio Práctico</b></summary>

---

# Sistema Bancario en C - Modularidad y Paso de Parámetros

## Planteamiento del Problema

Se requiere desarrollar un programa modular en el lenguaje de programación C que permita gestionar y actualizar el saldo de una cuenta bancaria digital. El sistema debe cumplir con los siguientes requerimientos:

1. **Modularidad:** El código debe estar dividido en funciones independientes para organizar la lógica del programa (por ejemplo, mostrar el menú, realizar un depósito y realizar un retiro).
2. **Paso por Valor:** Se debe utilizar para enviar datos que solo necesitan ser leídos o mostrados por la función (como mostrar el saldo actual o validar montos informativos), sin que la función tenga la capacidad de alterar la variable original del programa principal.
3. **Paso por Referencia:** Se debe utilizar (mediante el uso de punteros) cuando una función necesite modificar directamente el valor de una variable original en la memoria del programa principal (como actualizar el saldo tras un depósito o un retiro).

---

## Análisis del Problema

* **Entradas:**
  * Opción del menú seleccionada por el usuario (entero).
  * Monto de dinero a depositar (número con decimales, tipo `float`).
  * Monto de dinero a retirar (número con decimales, tipo `float`).

* **Salidas:**
  * Mensajes informativos en consola y el saldo actual de la cuenta actualizado de forma persistente a lo largo de las operaciones.

* **Identificación del Paso de Parámetros:**
  * **Paso por valor:** Se usará en funciones como `mostrarMenu()` o al validar si un monto es positivo, donde solo se requiere consultar el valor recibido sin modificarlo.
  * **Paso por referencia:** Se usará en las funciones `depositarDinero` y `retirarDinero`, recibiendo la dirección de memoria de la variable `saldo` (usando `float *saldo`) para modificar su contenido de manera efectiva en la función `main`.

---

## Código Fuente en C

```c
#include <stdio.h>

// Prototipos de funciones (Modularidad)
void mostrarMenu();
void depositarDinero(float *saldo, float monto);
int retirarDinero(float *saldo, float monto);

int main() {
    float saldoActual = 500.00; // Saldo inicial de la cuenta
    int opcion;
    float cantidad;

    do {
        mostrarMenu();
        printf("Seleccione una opcion: ");
        scanf("%d", &opcion);

        switch (opcion) {
            case 1:
                printf("\nSu saldo actual es: $%.2f\n", saldoActual);
                break;
            case 2:
                printf("Ingrese la cantidad a depositar: $");
                scanf("%f", &cantidad);
                
                if (cantidad > 0) {
                    // Paso por referencia: se envia la direccion de saldoActual
                    depositarDinero(&saldoActual, cantidad);
                    printf("Deposito exitoso. Nuevo saldo: $%.2f\n", saldoActual);
                } else {
                    printf("Error: El monto debe ser mayor a cero.\n");
                }
                break;
            case 3:
                printf("Ingrese la cantidad a retirar: $");
                scanf("%f", &cantidad);
                
                if (cantidad > 0) {
                    // Paso por referencia: se envia la direccion de saldoActual
                    if (retirarDinero(&saldoActual, cantidad)) {
                        printf("Retiro exitoso. Nuevo saldo: $%.2f\n", saldoActual);
                    } else {
                        printf("Error: Fondos insuficientes.\n");
                    }
                } else {
                    printf("Error: El monto debe ser mayor a cero.\n");
                }
                break;
            case 4:
                printf("\nSaliendo del sistema. Gracias por preferirnos.\n");
                break;
            default:
                printf("\nOpcion invalida. Intente de nuevo.\n");
        }
        printf("\n----------------------------------------\n");
    } while (opcion != 4);

    return 0;
}

// Funcion que utiliza paso por valor implicito al desplegar opciones estaticas
void mostrarMenu() {
    printf("\n=== SISTEMA BANCARIO ===\n");
    printf("1. Consultar saldo\n");
    printf("2. Depositar dinero\n");
    printf("3. Retirar dinero\n");
    printf("4. Salir\n");
}

// Funcion con paso por referencia (*saldo) y paso por valor (monto)
void depositarDinero(float *saldo, float monto) {
    *saldo += monto; // Modifica el valor original en memoria
}

// Funcion con paso por referencia (*saldo) y paso por valor (monto)
int retirarDinero(float *saldo, float monto) {
    if (*saldo >= monto) {
        *saldo -= monto; // Modifica el valor original en memoria
        return 1; // Retiro exitoso
    }
    return 0; // Fondos insuficientes
}
```

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


