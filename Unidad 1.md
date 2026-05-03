<h1 align="center">🚀 Unidad 1: Inmersión a la Programación 🚀</h1>

<p align="center">
  <img src="https://unl.edu.ec/sites/default/files/logogris%20copia.png" alt="Logotipo UNL" width="350">
</p>

<p align="center">
  <a href="#glosario">📚 Glosario con Ejemplos</a> • 
  <a href="#ejercicio">💻 Caso Práctico</a> • 
  <a href="#reflexion">🤔 Reflexión</a> • 
  <a href="#recursos">📂 Recursos</a>
</p>

---

<a name="glosario"></a>
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
<i>Como se observa, al ingresar 75, el sistema procesa correctamente los ahorros semanal, mensual y anual.</i>
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

<a name="reflexion"></a>
## 🤔 3. Reflexión Crítica
> [!NOTE]
> La transición del pensamiento lógico al pseudocódigo se facilitó gracias a las herramientas visuales. Comprender que cada instrucción debe ser finita y precisa es la base para avanzar hacia lenguajes más complejos.

<br>

<p align="center">
  <a href="#">🔼 Volver al inicio</a>
</p>
