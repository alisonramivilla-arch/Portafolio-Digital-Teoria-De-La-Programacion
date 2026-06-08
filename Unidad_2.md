<h1 align="center">🚀 Unidad 2: Estructuras Algorítmicas de Control 🚀</h1>

<p align="center">
  <img src="https://unl.edu.ec/sites/default/files/logogris%20copia.png" alt="Logotipo UNL" width="350">
</p>
<p align="center">
📚 Glosario de contenidos</a> •
💻 Ejercicio Práctico</a> •
🧐 Reflexión</a>
</p>

---

### 🎨 1. Glosario interactivo de contenidos

*Haz clic en cada sección para desplegar los fundamentos conceptuales, pseudocódigos y la lógica estructural de esta unidad.*

<details>
<summary><b>🔍 CLIC AQUÍ para explorar las Estructuras Condicionales</b></summary>
    
> 💡 **Definición:** Las estructuras condicionales permiten bifurcar el flujo de ejecución de un algoritmo basándose en la evaluación de una expresión lógica o booleana (Verdadero/Falso).

#### 🔵A. Condicional Simple (`if`)
Evalúa una condición. Si es verdadera, ejecuta el bloque interno; si es falsa, ignora las instrucciones y continúa de forma secuencial.
* **Pseudocódigo:**
    ```text
    Si (condicion_logica) Entonces
        instrucción_1
        instrucción_2
    FinSi
    ```
* **Diagrama de flujo**
<p align="center">
  <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgCiRvV0_cBePmzLbfgVTHWwbh_vWIJLehgoLUs1915CA3ZukkPi9jQ2SGHtUz7n9s2k_7699FuhWNrSi0_yBSCIsMpHn2Xo9r5xkn68mqC5p6Xhhr8ZDDSfWLSz4rlUSk8gEWyyi6fDrc/s1600/ordinograma_si.gif" width="650" alt="Pseudocódigo Ahorro Anual">
</p>

#### 🟢B. Condicional Doble o Compuesta (`if-else`)
Define un camino alternativo obligatorio. Si la condición evaluada resulta falsa, se ejecuta de manera estricta el bloque dentro de la cláusula `Sino`.
* **Pseudocódigo:**
    ```text
    Si (condicion_logica) Entonces
        instrucciones_Ruta_Verdadera
    Sino
        instrucciones_Ruta_Falsa
    FinSi
    ```
* **Diagrama de flujo**
<p align="center">
  <img src="https://www.tutorialesprogramacionya.com/pythonya/imagentema/foto018.jpg" width="650" alt="Pseudocódigo Ahorro Anual">
</p>

    
#### 🔴C. Condicional Múltiple por Casos (`switch`)
Se emplea cuando el algoritmo requiere evaluar múltiples alternativas consecutivas para una variable o expresión.
* **Pseudocódigo**
    ```text
    Segun variable_control Hacer
        caso_1:
            instrucciones_1
        caso_2:
            instrucciones_2
        De Otro Modo:
            instrucciones_por_defecto
    FinSegun
    ```
* **Diagrama de flujo**
<p align="center">
  <img src="https://lab.anahuac.mx/~hselley/ayp/img/diagramaDeFlujo/condicionalMultiple.png" width="650" alt="Pseudocódigo Ahorro Anual">
</p>

#### 🟡D. Condicionales Anidados
Se presentan cuando, al cumplirse o no una condición inicial, se requiere evaluar una nueva condición interna para determinar la ruta final del flujo.

* **Pseudocódigo:**
    ```text
    Si (condicion_externa) Entonces
        // Primera capa de lógica
        Si (condicion_interna) Entonces
            instrucciones_bloque_A
        Sino
            instrucciones_bloque_B
        FinSi
    Sino
        instrucciones_bloque_C
    FinSi
    ```
* **Diagrama de flujo**
<p align="center">
  <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEieiM7mQCp2g4BFcyVcB94sXR-PmmEQNUJ8wNmxIbVLtrFY9hppRuZ6HYsjwlaYLr3AqnuhvKs8zkRmZLPaA0ssCnrP7STa_CYw9q9Uxg15hXSvX9z_5iG7rZyhEHot-ym25XUlqcByCns/s1600/si3.png" width="650">
</p>
</details>

<details>
<summary><b>🔄 CLIC AQUÍ para explorar las Estructuras Repetitivas</b></summary>

<br>


> 💡 **Concepto Clave:** Los bucles permiten ejecutar un bloque de instrucciones múltiples veces de forma automatizada. Se rigen bajo una condición de parada para evitar ciclos infinitos que saturen la memoria.

#### A. Variables de control
> **¿Qué son?** Son variables especiales que cambian su valor de forma progresiva dentro de un bucle. Aunque ambas realizan sumas, su propósito lógico y la forma en que incrementan son completamente diferentes.

#### 🔢 Contadores 
Un contador es una variable que incrementa o decrementa en una **cantidad constante** (generalmente de 1 en 1) en cada iteración del bucle. Se utiliza para registrar cuántas veces ocurre un evento o para controlar el número de vueltas de un ciclo.

* **Sintaxis matemática:** `contador = contador + constante` (o de forma simplificada `contador++`)
* **Pseudocódigo:**
    ```text
    // Inicialización antes del bucle
    cant_estudiantes <- 0 
    
    // Dentro del bucle
    cant_estudiantes <- cant_estudiantes + 1
    ```

---

#### 💰 Acumuladores (o Sumadores) 
Un acumulador es una variable que incrementa o decrementa en una **cantidad variable**. Se utiliza para agrupar o sumar valores numéricos que cambian en cada iteración, como calificaciones, precios o estaturas.

* **Sintaxis matemática:** `acumulador = acumulador + variable` (o de forma simplificada `acumulador += variable`)
* **Pseudocódigo:**
    ```text
    // Inicialización antes del bucle
    suma_notas <- 0.0 
    
    // Dentro del bucle
    suma_notas <- suma_notas + nota_ingresada
    ```

---

### 🔍 Cuadro Comparativo de Diferencias

| Criterio | Contadores 🔢 | Acumuladores 💰 |
| :--- | :--- | :--- |
| **Valor de incremento** | Es **fijo y constante** (ej. $+1$, $+2$, $-1$). | Es **variable y dinámico** (ej. $+nota$, $+precio$). |
| **Propósito Principal** | Contar repeticiones o verificar límites. | Totalizar sumatorias o promedios masivos. |
| **Inicialización típica** | Habitualmente en `0` o `1`. | Habitualmente en `0` o `0.0` (para números reales). |

> [!WARNING]
> **¡Regla de Oro en Programación!** 🚨 
> Tanto los contadores como los acumuladores **deben inicializarse obligatoriamente** antes de que inicie el bucle. Si no se hace, la variable contendrá "basura" de la memoria y los cálculos del programa serán erróneos.


#### 🔄1. Bucle Mientras (`while`)
Es una estructura con **precondición**. Evalúa la condición lógica *antes* de ingresar al bucle. Si la condición es falsa desde el primer intento, el bloque de código jamás se ejecuta.

* **Pseudocódigo:**
    ```text
    Mientras (condicion_logica) Hacer
        instrucción_1
        instrucción_2
        // Modificación de la variable de control
    FinMientras
    ```
* **Diagrama de flujo**
<p align="center">
  <img src="https://www.tutorialesprogramacionya.com/delphiya/imagentema/foto037.jpg" width="650" alt="Pseudocódigo Ahorro Anual">
</p>
    

---

#### 🔄2. Bucle Hacer-Mientras (`do-while`)
Es una estructura con **postcondición**. Ejecuta el bloque de instrucciones **al menos una vez** y, al final, evalúa si la condición es verdadera para decidir si repite el ciclo. Es la estructura estándar para la validación perimetral de datos.

* **Pseudocódigo:**
    ```text
    Hacer
        instrucción_1
        instrucción_2
        // Entrada o modificación de datos
    Mientras Que (condicion_logica)
    ```
    ```
* **Diagrama de flujo**
<p align="center">
  <img src="https://www.tutorialesprogramacionya.com/javaya/imagentema/foto055.jpg" width="650" alt="Pseudocódigo Ahorro Anual">
</p>
    

---

#### 🔄3. Bucle Para (`for`)
Es un ciclo determinado ideal para cuando conocemos de antemano la **cantidad exacta de iteraciones** que se deben realizar. Compacta en una sola línea la inicialización, la condición de permanencia y el incremento/decremento.

* **Pseudocódigo:**
    ```text
    Para variable_control <- valor_inicial Hasta valor_final Con Paso incremento Hacer
        instrucción_1
        instrucción_2
    FinPara
    ```
    ```
* **Diagrama de flujo**
<p align="center">
  <img src="https://www2.eii.uva.es/fund_inf/cpp/_images/for.jpg" width="650" alt="Pseudocódigo Ahorro Anual">
</p>

  > ⚠️ **¡Cuidado con los bucles infinitos!** Un bucle debe tener siempre una condición de parada clara y una variable de control que se modifique en cada iteración.

</details>

---

### 💻 2. Caso Práctico: Sistema de Calificaciones de Computación



#### A. El Desafío (Planteamiento del Problema)
Diseñar un algoritmo bajo el lenguaje de programación C que procese de forma iterativa las calificaciones definitivas de un grupo de $n$ estudiantes. [cite_start]El sistema debe solicitar las notas, aplicar una **validación perimetral** (las notas deben estar estrictamente entre 0 y 10), calcular el promedio ponderado y categorizar el desempeño del alumno.

#### B. Panel de Análisis del Algoritmo

💡 *Usa esta tabla interactiva para mapear las variables y procesos esenciales del problema:*

| Componente | 📥 Datos de Entrada / Variables | ⚙️ Proceso / Fórmulas | 📤 Datos de Salida |
| :--- | :--- | :--- | :--- |
| **Descripción** | • Número de alumnos (`n`)<br>• Notas parciales: `APE`, `AA`, `ACD`, `ES`. | **1. Validación:** Ciclo `do-while`. <br>**2. Ponderación:** <br>$NF = (APE \times 0.25) + (AA \times 0.20) + (ACD \times 0.20) + (ES \times 0.35)$ | • Identificador del alumno.<br>• Nota Final (`NF`) formateada a 2 decimales.<br>• Nivel de rendimiento. |
| **Tipo de Dato**| `int` (enteros) y `float` (reales) | Operadores lógicos (`\|\|`) y aritméticos. | Mensajes de texto estructurados en consola. |

---

#### C. Código Fuente Animado y Comentado en C

> 🛠️ **Nota de Optimización:** Este código implementa un lazo `do-while` interno para filtrar datos erróneos y una escalera de `else if` que ahorra ciclos de reloj al procesador al detener las comprobaciones en cuanto halla la condición verdadera.

```c
#include <stdio.h>

int main() {
    int n, a;
    float APE, AA, ACD, ES, NF;

    printf("===============================================\n");
    printf("   SISTEMA DE CALIFICACIONES DE COMPUTACIÓN    \n");
    printf("===============================================\n");
    printf("Ingrese la cantidad de estudiantes a procesar: ");
    scanf("%d", &n);

    // [BUCLE EXTERNO]: Controla el recorrido de todos los estudiantes
    for(a = 1; a <= n; a++) {
        printf("\n🔹 Procesando datos del Estudiante Nro. %d:\n", a);

        // [BUCLE INTERNO]: Validación rigurosa de datos de entrada
        do {
            printf(" -> Nota APE (0-10): "); scanf("%f", &APE);
            printf(" -> Nota AA  (0-10): "); scanf("%f", &AA);
            printf(" -> Nota ACD (0-10): "); scanf("%f", &ACD);
            printf(" -> Nota ES  (0-10): "); scanf("%f", &ES);

            if(APE > 10 || AA > 10 || ACD > 10 || ES > 10 || APE < 0 || AA < 0 || ACD < 0 || ES < 0) {
                printf("\n❌ [ERROR] ¡Valores inválidos! Las notas deben estar entre 0 y 10. Reintente.\n");
            }
        } while(APE > 10 || AA > 10 || ACD > 10 || ES > 10 || APE < 0 || AA < 0 || ACD < 0 || ES < 0);

        // Operación matemática con los pesos oficiales de la UNL
        NF = (APE * 0.25) + (AA * 0.20) + (ACD * 0.20) + (ES * 0.35);

        printf("\n📊 Nota Final Calculada: %.2f", NF);

        // [ESTRUCTURA CONDICIONAL ANIDADA]: Clasificación de rendimiento
        if (NF >= 9.0 && NF <= 10.0) {
            printf("\n🏆 Nivel de Desempeño: EXCELENTE ✨\n");
        } else if (NF >= 7.0 && NF < 9.0) {
            printf("\n📈 Nivel de Desempeño: BUENO ✅\n");
        } else if (NF >= 5.0 && NF < 7.0) {
            printf("\n⚠️ Nivel de Desempeño: REGULAR 📝\n");
        } else {
            printf("\n🚨 Nivel de Desempeño: DEFICIENTE ❌\n");
        }
        printf("-----------------------------------------------");
    }

    printf("\n🎉 ¡Proceso finalizado con éxito para los %d alumnos!\n", n);
    return 0;
}





<p align="center">
**<strong><a href="Portafolio.md">**INICIO**</a></strong>**
</p>
