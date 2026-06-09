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

### 💻 2. Ejercicio Practico Alternativo

<details>
<summary><b>💻 CLIC AQUÍ para explorar el caso práctico</b></summary>
</p>
  
> 💡Sistema de Evaluación de Becas Académicas
  
#### 📝 A. Planteamiento del Problema
La Universidad Nacional de Loja requiere un programa interactivo en lenguaje C para evaluar las solicitudes de un grupo de "n" estudiantes que postulan a las *Becas de Excelencia Académica y Apoyo Socioeconómico*. El algoritmo debe registrar de forma iterativa el promedio global del ciclo anterior del estudiante y su puntaje de vulnerabilidad socioeconómica (en una escala de 0 a 10). Se debe aplicar una **validación perimetral rigurosa** para asegurar que los datos no estén fuera de rango, calcular un índice de priorización y determinar el porcentaje de cobertura de beca adjudicado mediante una escalera condicional de toma de decisiones.

#### 📊 B. Panel de Análisis del Algoritmo (Estructura Vertical)

| Componente | 📥 Datos de Entrada |
| :-: | :-- |
| **Descripción** | • Cantidad de estudiantes postulantes a procesar (`n`).<br>• Promedio académico final del ciclo anterior (`promedio`).<br>• Puntaje de necesidad o vulnerabilidad económica (`socioeconomico`). |
| **Variables** | • `n` (entero para el control de iteraciones del bucle principal).<br>• `promedio`, `socioeconomico` (flotantes para almacenar datos de precisión con decimales). |

| Componente | ⚙️ Proceso |
| :-: | :-- |
| **Descripción** | **1. Control Iterativo:** Un ciclo `for` se encarga de segmentar el análisis individual de cada postulante.<br>**2. Validación de Datos:** Estructura de control `do-while` que atrapa y rechaza valores basuras (menores a 0 o mayores a 10).<br>**3. Cálculo del Índice:** Operación matemática lineal ponderando el rendimiento cognitivo al 60% y el factor socioeconómico al 40%:<br>&nbsp;&nbsp;&nbsp;&nbsp;• $IP = (promedio \times 0.60) + (socioeconomico \times 0.40)$<br>**4. Adjudicación Lógica:** Clasificación por rangos mediante bloques de bifurcación condicional anidada para determinar la cobertura del beneficio. |
| **Variables / Fórmulas**| • `i` (entero, contador incremental del bucle `for`).<br>• $IP = (promedio \times 0.60) + (socioeconomico \times 0.40)$ |

| Componente | 📤 Datos de Salida |
| :-: | :-- |
| **Descripción** | • Despliegue secuencial del identificador en orden correlativo del alumno evaluado.<br>• Impresión en consola del Índice de Priorización (`IP`) calculado con precisión a 2 decimales.<br>• Mensaje explícito con el dictamen final del beneficio adjudicado (Beca Completa, Media Beca, etc.). |
| **Variables** | • `i` (identificador numérico activo).<br>• `IP` (flotante con el índice definitivo). |

---

#### 🗺️ C. Diseño del Algoritmo (Diagramación Vertical)

<p align="center">
  <img src="https://raw.githubusercontent.com/alisonramivilla-arch/Imagenes/refs/heads/main/DIAGRAMA%20DE%20FLUJO....png" width="650" alt="Pseudocódigo Ahorro Anual">
</p>

---

#### 🛠️ D. Codificación (Código Fuente Optimizado en Lenguaje C)

```c
#include <stdio.h>

int main() {
    int n, i;
    float promedio, socioeconomico, IP;
    //Datos de Entrada
    printf("---SISTEMA DE ADJUDICACION DE BECAS - UNL---\n");
    printf("Ingrese la cantidad de postulantes a evaluar: \n");
    scanf("%d", &n);
    // BUCLE EXTERNO
    for(i = 1; i <= n; i++) {
        printf("\n Evaluando Postulante Nro. %d:\n", i);
        do {
            //Datos de Entrada
            printf(" -> Promedio Academico (0-10): "); 
            scanf("%f", &promedio);
            printf(" -> Puntaje Socioeconomico (0-10): "); 
            scanf("%f", &socioeconomico);
            // Condicionales
            if(promedio < 0 || promedio > 10 || socioeconomico < 0 || socioeconomico > 10) {
                //Datos de Salida
                printf("\n [ERROR] Datos fuera de rango. Los valores deben ser de 0 a 10.\n");
                printf("Ingrese nuevamente los datos del estudiante %i\n", i);
            }
        //Condicional
        } while(promedio < 0 || promedio > 10 || socioeconomico < 0 || socioeconomico > 10);
        // Proceso 
        IP = (promedio * 0.60) + (socioeconomico * 0.40);
        printf("\n Indice de Priorizacion Calculado: %.2f", IP);
        // Estrucutura condicional anidada
        //Datos de Salida y Proceso
        if (IP >= 9.0) {
            printf("\n Dictamen: ADJUDICADO - BECA COMPLETA (100%% Cobertura) \n");
        } else if (IP >= 7.5 && IP < 9.0) {
            printf("\n Dictamen: ADJUDICADO - MEDIA BECA (50%% Cobertura) \n");
        } else if (IP >= 6.0 && IP < 7.5) {
            printf("\n Dictamen: ADJUDICADO - AYUDA ECONOMICA (25%% Cobertura) \n");
        } else {
            printf("\n Dictamen: SOLICITUD RECHAZADA - No cumple con el puntaje mínimo \n");
        }
       
    }
    printf("----------------------------------------------------------------");
    printf("Evaluacion de asignacion finalizada para los %d estudiantes\n", n);
    return 0;
}
```
</details>

---

### 📈 4. Dificultades Encontradas 

<details>
<summary><b>💻 CLIC AQUÍ para explorar DIFICULTADES</b></summary>
</p>

#### ⚠️ A. Principales Obstáculos en el Aprendizaje

> [!CAUTION]
> Durante el desarrollo teórico y práctico de esta Unidad 2, se presentaron los siguientes desafíos técnico-cognitivos en el diseño de algoritmos:

* **Criterio de Selección de Estructuras:** Identificar con precisión matemática **cuándo aplicar una estructura condicional específica o una repetitiva** ante un problema abierto constituía un reto inicial complejo. Discernir si un escenario requería una escalera de `else if` o si era optimizable mediante un control por casos (`switch`), o evaluar la frontera entre un ciclo condicionado o secuencial, generaba confusión en la etapa de abstracción y modelado.
* **Dominio Coherente del Bucle `for`:** Comprender la sincronización interna del ciclo determinado `for` (su inicialización, la condición lógica de frontera y el incremento automático en una sola línea de control) requirió romper con la estructura lineal secuencial a la que venía acostumbrada en la Unidad 1. Visualizar de forma síncrona cómo el contador altera el flujo en cada ciclo demandó un cambio drástico en la lógica mental.
* **Sincronización e Inicialización de Variables:** Determinar el momento exacto y el ámbito (*scope*) de memoria donde se debe **inicializar una variable** (como poner los contadores en `1` o limpiar los acumuladores de sumas masivas en `0.0` antes de abrir las compuertas de un bucle) fue una dificultad persistente. Olvidar este paso causaba que el compilador arrastrara "valores basura" de la memoria RAM, alterando los resultados lógicos en las pruebas de escritorio.
</details>

---

### 🧠 5. Reflexión Crítica 

<details>
<summary><b>💻 CLIC AQUÍ para explorar REFLEXIÓN CRÍTICA</b></summary>
</p>
  
> [!IMPORTANT]
 ### 📑 Análisis Metacognitivo del Desarrollo Lógico

 El paso del paradigma puramente secuencial abordado en la Unidad 1 hacia el control de flujos dinámicos en esta Unidad 2 representa el verdadero nacimiento del pensamiento computacional y la ingeniería de software en mi formación. Estudiar las estructuras condicionales y repetitivas no se limitó a aprender reglas sintácticas en lenguaje C, sino a comprender cómo administrar el recurso más valioso de una computadora: **el tiempo de procesamiento de la CPU**.

 Al analizar retrospectivamente mi evolución, identifico un cambio cualitativo en la forma de resolver problemas. Al inicio de la unidad, mi enfoque metodológico era puramente reactivo; escribía líneas de código consecutivas esperando que la lógica se alineara por sí sola. Esto causaba fallos críticos como bucles infinitos por falta de variables de control o el acarreo de "datos basura" por una incorrecta inicialización en la memoria RAM.
 
 La introducción de herramientas rigurosas como las **Pruebas de Escritorio detalladas** y la **Diagramación Vertical** en Draw.io transformó mi perspectiva. Diseñar visualmente el filtro perimetral de un ciclo `do-while` o pulir las condiciones lógicas de una cascada de selección me obligó a actuar como el propio compilador. Aprendí que la elegancia de un algoritmo no radica en su extensión, sino en su optimización; por ejemplo, preferir una escalera estructurada de `else if` que aproveche el "cortocircuito lógico" del procesador en lugar de evaluaciones concurrentes aisladas.

En conclusión, esta unidad marca un hito en mi aprendizaje. He dejado de ver al código como un conjunto de instrucciones rígidas y he comenzado a entenderlo como una arquitectura maleable orientada a la eficiencia. La comprensión del anidamiento complejo, el control estricto de variables mutables (contadores y acumuladores) y la validación proactiva de datos me brindan las competencias lógicas necesarias para afrontar los desafíos algorítmicos avanzados que demandará el resto de mi carrera en Ciencias de la Computación.

<p align="center">
**<strong><a href="Portafolio.md">**INICIO**</a></strong>**
</p>
