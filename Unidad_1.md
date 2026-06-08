<h1 align="center">🚀 Unidad 1: Inmersión a la Programación 🚀</h1>

<p align="center">
  <img src="https://unl.edu.ec/sites/default/files/logogris%20copia.png" alt="Logotipo UNL" width="350">
</p>


<p align="center">
📚 Glosario con Ejemplos</a> •
💻 Ejercicio Práctico</a> •
🧐 Reflexión</a>
</p>


---


## 📂 1. Glosario Interactivo de Conceptos
*Despliega cada concepto para ver su definición y la evidencia visual del ejemplo **Ahorro Anual**.*

<details>
<summary><b>🔵 ¿Qué es un Algoritmo?</b></summary>
<blockquote>
Es una secuencia lógica y finita de pasos para solucionar un problema.
<br><br>
<b>Evidencia de Algoritmo en PSeInt:</b>
<p align="center">
  <img src="https://raw.githubusercontent.com/alisonramivilla-arch/Imagenes/refs/heads/main/Algoritmo.png" width="650" alt="Pseudocódigo Ahorro Anual">
</p>
</blockquote>
</details>

<details>
<summary><b>🟢 ¿Qué es el Pseudocódigo?</b></summary>
<blockquote>
Es un lenguaje de alto nivel (cercano al humano) que describe la lógica de un programa.
<br><br>
<b>Evidencia de Pseudocódigo en PSeInt:</b>
<p align="center">
  <img src="https://raw.githubusercontent.com/alisonramivilla-arch/Imagenes/refs/heads/main/pseucodigo.png" width="650" alt="Pseudocódigo Ahorro Anual">
</p>
</blockquote>
</details>

<details>
<summary><b>🟡 ¿Qué es un Diagrama de Flujo?</b></summary>
<blockquote>
Es la representación gráfica del algoritmo. Utiliza símbolos como paralelogramos para entradas y rectángulos para procesos.
<br><br>
<b>Representación Gráfica:</b>
<p align="center">
  <img src="https://raw.githubusercontent.com/alisonramivilla-arch/Imagenes/refs/heads/main/diagrama%20de%20flujo.png" width="450" alt="Diagrama de Flujo">
</p>
</blockquote>
</details>

<details>
<summary><b>🔴 ¿Qué es una Prueba de Escritorio?</b></summary>
<blockquote>
Es la ejecución manual o controlada para verificar que la lógica produce los resultados esperados.
<br><br>
<b>Resultados:</b>
<p align="center">
  <img src="https://raw.githubusercontent.com/alisonramivilla-arch/Imagenes/refs/heads/main/Prueba%20de%20escritorio.png" width="550" alt="Consola PSeInt">
</p>
<br>

</blockquote>
</details>

<details>
<summary><b>💻 ¿Qué es un Lenguaje de Programación?</b></summary>
<blockquote>
Es un sistema de signos, reglas sintácticas y semánticas que permiten escribir instrucciones para que una computadora realice tareas específicas. Es el puente de comunicación entre el pensamiento humano y la ejecución binaria.
</blockquote>

<br>

#### 🔹 Lenguaje C
Es un lenguaje de nivel medio (combina características de alto y bajo nivel) conocido por su eficiencia y control total sobre el hardware. Es la base de muchos sistemas operativos.
*   **Ejemplo (Venta de Vehículos):** 
    ```c
    #include <stdio.h>

    int main() {
        // Variables
        int comision1, comision2, comision3, v1=30000, v2=29000, v3=33000, total;

        // Proceso
        comision1 = v1 * 0.04;
        comision2 = v2 * 0.04;
        comision3 = v3 * 0.04;
        total = comision1 + comision2 + comision3;

        // Salida
        printf("La comision del vendedor 1 es: %i\n", comision1);
        printf("La comision del vendedor 2 es: %i\n", comision2);
        printf("La comision del vendedor 3 es: %i\n", comision3);
        printf("El pago total en conjunto es: %i\n", total);

        return 0;
    }
    ```

#### 🔹 Lenguaje Java
Lenguaje orientado a objetos diseñado para ser multiplataforma bajo el lema "escríbelo una vez, ejecútalo en cualquier lugar".
*   **Ejemplo (Venta de Vehículos):** 
    ```java
    public class VentaVehiculos {
        public static void main(String[] args) {
            int v1=30000, v2=29000, v3=33000;
            
            int comision1 = (int)(v1 * 0.04);
            int comision2 = (int)(v2 * 0.04);
            int comision3 = (int)(v3 * 0.04);
            int total = comision1 + comision2 + comision3;

            System.out.println("La comision del vendedor 1 es: " + comision1);
            System.out.println("La comision del vendedor 2 es: " + comision2);
            System.out.println("La comision del vendedor 3 es: " + comision3);
            System.out.println("El pago total en conjunto es: " + total);
        }
    }
    ```

#### 🔹 Lenguaje Python
Lenguaje de alto nivel cuya filosofía hace hincapié en la legibilidad del código. Es extremadamente versátil y fácil de aprender.
*   **Ejemplo (Venta de Vehículos):** 
    ```python
    # Variables y Proceso
    v1, v2, v3 = 30000, 29000, 33000

    comision1 = int(v1 * 0.04)
    comision2 = int(v2 * 0.04)
    comision3 = int(v3 * 0.04)
    total = comision1 + comision2 + comision3

    # Salida
    print(f"La comision del vendedor 1 es: {comision1}")
    print(f"La comision del vendedor 2 es: {comision2}")
    print(f"La comision del vendedor 3 es: {comision3}")
    print(f"El pago total en conjunto es: {total}")
    ```
</details>

<details>
<summary><b>🧩 ¿Qué es la Programación por Bloques?</b></summary>
<blockquote>
Es un entorno de programación visual donde se utilizan "piezas" o bloques de construcción en lugar de escribir código de texto. Esto permite aprender la lógica de programación sin preocuparse por los errores de sintaxis.
<br><br>
<b>Ejemplo Interactivo (Pilas Bloques):</b> 
En este video se observa la resolución del desafío "Dieta a base de churrascos", construyendo un algoritmo secuencial paso a paso.
</blockquote>

<br>

<div align="center">
  <video src="https://github.com/user-attachments/assets/96694286-6ea0-4f41-a2d6-de6dfa881820" width="80%" controls>
   
  </video>
</div>

<br>
</details>


---

## 🚀 2. Ejercicio Práctico: Estructura Secuencial

<details>
<summary><b>📐Desarrollo completo del ejercicio</b></summary>

### 📑 Definición: ¿Qué es una Estructura Secuencial?
> La **Estructura Secuencial** es la forma más simple de programación, donde las instrucciones se ejecutan una tras otra, en el orden en que aparecen escritas. En este modelo, la salida de una sentencia es la entrada de la siguiente, sin saltos ni desviaciones, siguiendo el flujo: **Inicio → Entrada de datos → Proceso → Salida de resultados → Fin**.

### 📝 A. Planteamiento del Problema
Diseñar un programa que permita calcular la distancia entre dos puntos $( X_1, Y_1 )$ y $(X_2, Y_2)$ en el plano cartesiano, utilizando la fórmula de la distancia euclidiana.

### 🔍 B. Análisis del Problema
* **Entradas:** Coordenadas `x1`, `y1`, `x2`, `y2`.
* **Proceso:** Aplicar la fórmula: `distancia = sqrt((x2 - x1)^2 + (y2 - y1)^2)`.
* **Salidas:** Resultado de la distancia calculada.
* 
### 📐 C. Diseño del Algoritmo
*Lógica estructurada para resolver el problema antes de la codificación.*
<details>
<summary><b>ver Pseudocódigo en Pseint</b></summary>
<br>

<p align="center">
  <img src="https://raw.githubusercontent.com/alisonramivilla-arch/Imagenes/refs/heads/main/Algoritmo_Distancia.png" width="600" alt="Pseudocódigo Distancia">
</p>
</details>

<details>
<summary><b>ver Diagrama de Flujo</b></summary>
<br>
<p align="center">
  <img src="https://raw.githubusercontent.com/alisonramivilla-arch/Imagenes/refs/heads/main/Diagrama_Distancia.png" width="400" alt="Diagrama de Flujo Distancia">
</p>
</details>

### 💻 D. Codificación (Código Fuente en C)
*Implementación del algoritmo en lenguaje C, haciendo uso de la librería `<math.h>` para funciones matemáticas.*


```c
#include <stdio.h>
#include <math.h>

int main(){
    // Variables
    float x1, x2, y1, y2, distancia;

    // Entrada
    printf("Ingrese x1: ");
    scanf("%f", &x1);
    printf("Ingrese y1: ");
    scanf("%f", &y1);
    printf("Ingrese x2: ");
    scanf("%f", &x2);
    printf("Ingrese y2: ");
    scanf("%f", &y2);

    // Proceso
    distancia = sqrt(pow(x2 - x1, 2) + pow(y2 - y1, 2));

    // Salida
    printf("La distancia es: %f", distancia);

    return 0;
}
```
### ⚙️ E. Compilación y Ejecución en Windows (PowerShell)
Para transformar el código fuente en un programa funcional, se utiliza el compilador **GCC**. Basado en la terminal, el proceso sigue esta estructura:

#### 1. Compilación: `gcc .\nombre.c -o nombre`
Este comando es la base de la creación del software. El compilador traduce el lenguaje C a instrucciones binarias que el procesador puede entender.
* **`gcc`**: Invoca el compilador GNU Compiler Collection.
* **`.\Calculardistancia.c`**: Indica la ruta del archivo fuente en el directorio actual.
* **`-o`**: Bandera de "Output" que define el nombre del archivo de salida.
* **`Calculardistancia`**: Nombre del archivo **ejecutable (.exe)** que se generará.

#### 2. Ejecución: `.\nombre`
Una vez que el compilador genera el archivo ejecutable de forma exitosa, se utiliza este comando para iniciar el programa.
* **`.\Calculardistancia`**: Ejecuta el archivo binario (en Windows se trata internamente del archivo **Calculardistancia.exe**).
> !IMPORTANTE
> 
> **El archivo .exe**: Es el resultado final de la compilación. Es un archivo independiente que contiene la lógica del programa lista para ser procesada por el sistema operativo Windows sin necesidad de abrir el código fuente nuevamente. Si realizas cambios en el código, es obligatorio repetir el proceso de compilación para actualizar el ejecutable.

  ### 🖥️ F. Resultado en Terminal
A continuación, se muestra la evidencia de la compilación y ejecución exitosa del algoritmo en la terminal de Windows, utilizando los comandos `gcc` para generar el ejecutable y `.\` para correr el programa:

<p align="center">
  <img src="https://raw.githubusercontent.com/alisonramivilla-arch/Imagenes/refs/heads/main/Terminal.png" width="700" alt="Resultado Terminal Distancia">
</p>
> !NOTA

> **Como se observa en la captura, el programa solicita las coordenadas de dos puntos y devuelve el cálculo exacto de la distancia, confirmando que la lógica del código fuente es correcta.**

  ### 🔍 G. Prueba de escritorio
  
<p align="center">
  <img src="https://raw.githubusercontent.com/alisonramivilla-arch/Imagenes/refs/heads/main/Prueba%20de%20escritorio%20C.png" width="700" alt="Resultado Terminal Distancia">
</p>

</details>

---

## 🧠 3. Principales Dificultades y Reflexión Crítica

#### ❗ Dificultades Encontradas
Durante el desarrollo de esta unidad, se presentaron retos significativos en el manejo de nuevas herramientas tecnológicas:
* **Entorno de Visual Studio Code:** Aprender a configurar correctamente el editor y entender el flujo de trabajo entre el editor de texto y la terminal integrada fue un proceso que requirió paciencia.
* **Manejo de GitHub:** La gestión del repositorio, asegurar que los archivos se visualizaran correctamente y el uso de Markdown para documentar el portafolio representó una curva de aprendizaje importante.
* **Memorización de Estructuras:** Internalizar la sintaxis estricta del lenguaje C y la estructura lógica de los algoritmos para evitar errores de sintaxis durante la compilación.

#### 📝 Reflexión Crítica
El proceso de aprendizaje en esta unidad ha sido fundamental para mi formación en este primer ciclo:

1.  **Dominio de Visual Studio Code:** Un aprendizaje práctico clave fue la incorporación de **combinaciones de teclas (shortcuts)**. Estas facilidades del teclado permiten navegar más rápido por el código, ahorrar tiempo en la escritura y organizar mejor el espacio de trabajo en el monitor.
2.  **Influencia de la Guía Docente:** La metodología y claridad de la **docente al mando de la asignatura** han sido determinantes. Una enseñanza bien estructurada facilita la transición de conceptos abstractos a aplicaciones prácticas, permitiendo que la lógica de programación sea más fácil de asimilar.
3.  **Importancia de la Compilación:** Entender que la computadora no lee el código directamente, sino que necesita un proceso de traducción (compilación), me ha dado una visión más clara de cómo funciona realmente el software.

<p align="center">
**<strong><a href="Portafolio.md">**INICIO**</a></strong>**
</p>
