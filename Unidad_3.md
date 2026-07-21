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
### 📌 Ejemplo Práctico
```c
#include <stdio.h>
void intercambiarValores(int *a, int *b){
    int c;
    c=*a;
    *a=*b;
    *b=c;
    printf("El valor de a es: %i\n", *a);
    printf("El valor de b es: %i\n", *b);
}
int main (){
    int x =5, y =7;
    intercambiarValores(&x,&y);
    printf("El valor de x es: %i\n", x);
    printf("El valor de y es: %i\n", y);
    return 0;
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

<p align="center">
  <img src="https://prog-o-manuais-plantillas-daw-bed5b048cbcd5bc455e9794fac9da239d.pages.iessanclemente.net/arrays/arraysuni/array.png" alt="Logotipo UNL" width="350">
</p>


### 💻 Ejemplo

```c
int edades[5]={18,20,19,22,21};
```

### 📌 Ejemplo Práctico

```c
#include <stdio.h>
int main(){
    int lista[5], i;
    for(i=0; i<5; i++){
        printf("Ingrese el valor de posicion %i\n", i);
        scanf("%i", &lista[i]);

    }
    for(i=0; i<5 ; i++ ){
        printf("posicion %i = %i\n", i, lista[i]);
    }

    return 0;
}
```
---

# 🔹 Arreglo Bidimensional (Matriz)

Organiza los datos en filas y columnas.

<p align="center">
  <img src="https://www.programandojava.com/images/ArregloInt2x3Vacio.png" alt="Logotipo UNL" width="350">
</p>


### 💻 Ejemplo

```c
int matriz[3][3];
```

### 📌 Ejemplo Práctico

```c
int main () {
    // Matriz 
    int matrizA[2][3], matrizC[2][3];
    int matrizB[2][3], i, j,pq;

    // Datos de entrada
    for(i = 0; i < 2; i++){        
        for(j = 0; j < 3; j++){    
            printf("Ingrese el valor de posicion [%i][%i] de la Matriz A\n", i, j);
            scanf("%i", &matrizA[i][j]);
        }
    
    }
    printf("---------------------------------\n");
      for(i = 0; i < 2; i++){        
        for(j = 0; j < 3; j++){    
            printf("Ingrese el valor de posicion [%i][%i] de la Matriz B\n", i, j);
            scanf("%i", &matrizB[i][j]);
        }
    }
    
    printf("----------------------------------------------------------\n");
    // Datos de salida 
    for(i = 0; i < 2; i++){
        for(j = 0; j < 3; j++){
            printf("MATRIZ A posicion [%i][%i] = %i\n", i, j, matrizA[i][j]);
           
        }
    }
    printf("----------------------------------------------------------\n");
    for(i = 0; i < 2; i++){
        for(j = 0; j < 3; j++){
            printf("MATRIZ B posicion [%i][%i] = %i\n", i, j, matrizB[i][j]);
           
        }
    }
    
    return 0;
}
```

---

# 🔹 Arreglo Multidimensional

Permite representar información con tres o más dimensiones.

Es utilizado en gráficos 3D, videojuegos, simulaciones científicas y procesamiento de imágenes.

<p align="center">
  <img src="https://miro.medium.com/v2/resize:fit:1400/1*VbVvxuuT7L2k-imWZKNp8w.png" alt="Logotipo UNL" width="350">
</p>

```text
matriz[x][y][z]
```
### 📌 Ejemplo Práctico
```c
    int main(){
    //matrices
    int matriz[2][2][3];
    //Datos de entrada
    int i,j,k;

    for(i = 0; i < 2; i ++){
        for(j = 0; j < 2; j ++){
            for (k = 0; k < 3; k ++){
            printf("Ingrese el valor para:[%i] [%i] [%i]: \n", i, j,k);
            scanf("%i", &matriz[i][j][k]);
            }
        }
    }

    //Datos de salida
    for(i = 0; i < 2; i ++){
        for(j = 0; j < 2; j ++){
            for(k = 0; k < 3; k ++){
            printf("[%i]", matriz[i][j][k]);
            }
            printf("\n");
        }
        printf("\n");

    }
        return 0;
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


