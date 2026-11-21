# 📝 Ejemplos de Ciclos, Condicionales y `Según` en PSeInt

**Asignatura:** Lógica de Programación
**Herramienta:** PSeInt
**Tema:** Estructuras de control (ciclos, condicionales y selección múltiple)

---

## 🎯 Objetivo

Presentar un ejemplo funcional de cada estructura de control en PSeInt (ciclos `Mientras`, `Para`, `Repetir`; condicionales `Si...Entonces...SiNo` y anidados; y `Según`), con su pseudocódigo y una breve explicación, para que sirvan de modelo en la resolución de los 25 ejercicios del taller integrador.

---

## 🔁 Parte 1: Ciclos

### 📌 Ejemplo 1: Ciclo `Mientras` (While)

**Enunciado:** Leer números enteros hasta que el usuario ingrese 0; sumar todos los valores y mostrar el total.

**Pseudocódigo:**

```text
Algoritmo Ejemplo_Mientras
    Definir num, suma Como Entero;
    suma <- 0;
    Escribir "Digite un número (0 para terminar):";
    Leer num;
    Mientras num <> 0 Hacer
        suma <- suma + num;
        Escribir "Digite otro número (0 para terminar):";
        Leer num;
    FinMientras
    Escribir "La suma total es: ", suma;
FinAlgoritmo
```

**Explicación:**
- La condición `num <> 0` se evalúa **antes** de entrar al ciclo. Si el primer número es 0, el ciclo no se ejecuta.
- Dentro del ciclo se acumula en `suma` y se vuelve a leer un número para actualizar la condición.
- Es ideal cuando **no se sabe cuántas iteraciones** se necesitan.

**Prueba rápida (num = 5, 3, 0):** suma = 5 + 3 = **8** ✅

---

### 📌 Ejemplo 2: Ciclo `Para` (For)

**Enunciado:** Mostrar los números del 1 al 20 y contar cuántos son múltiplos de 3.

**Pseudocódigo:**

```text
Algoritmo Ejemplo_Para
    Definir i, contador Como Entero;
    contador <- 0;
    Para i <- 1 Hasta 20 Con Paso 1 Hacer
        Escribir i;
        Si i mod 3 = 0 Entonces
            contador <- contador + 1;
        FinSi
    FinPara
    Escribir "Cantidad de múltiplos de 3 entre 1 y 20: ", contador;
FinAlgoritmo
```

**Explicación:**
- El ciclo `Para` recorre un rango **conocido** (del 1 al 20). El índice `i` se incrementa automáticamente.
- `i mod 3 = 0` verifica si el número es múltiplo de 3 (el operador `mod` da el residuo).
- Es ideal cuando **se conoce el número exacto de iteraciones**.

**Resultado esperado:** 3, 6, 9, 12, 15, 18 → **6 múltiplos** ✅

---

### 📌 Ejemplo 3: Ciclo `Repetir` (Do-While)

**Enunciado:** Mostrar un menú de opciones (1. Saludar, 2. Despedirse, 3. Salir) y repetirlo hasta que el usuario elija 3.

**Pseudocódigo:**

```text
Algoritmo Ejemplo_Repetir
    Definir opcion Como Entero;
    Repetir
        Escribir "===== MENÚ =====";
        Escribir "1. Saludar";
        Escribir "2. Despedirse";
        Escribir "3. Salir";
        Escribir "Elija una opción:";
        Leer opcion;
        Segun opcion Hacer
            1: Escribir "¡Hola! Bienvenido.";
            2: Escribir "¡Hasta luego!";
            3: Escribir "Saliendo del programa...";
            De Otro Modo: Escribir "Opción no válida.";
        FinSegun
    Hasta Que opcion = 3
    Escribir "Programa finalizado.";
FinAlgoritmo
```

**Explicación:**
- El ciclo `Repetir...Hasta Que` ejecuta el cuerpo **al menos una vez** y evalúa la condición **al final**.
- El menú se muestra siempre antes de pedir la opción, garantizando que el usuario vea las alternativas.
- Termina cuando `opcion = 3`.

**Prueba (opción = 1, 2, 3):** Muestra saludo, despedida y sale. ✅

---

## 🔀 Parte 2: Condicionales

### 📌 Ejemplo 1: Condicional simple/compuesto `Si...Entonces...SiNo` (equivalente a `if...else`)

**Enunciado:** Leer un número entero y determinar si es par o impar.

**Pseudocódigo:**

```text
Algoritmo Ejemplo_SiElse
    Definir num Como Entero;
    Escribir "Digite un número entero:";
    Leer num;
    Si num mod 2 = 0 Entonces
        Escribir "El número ", num, " es par.";
    SiNo
        Escribir "El número ", num, " es impar.";
    FinSi
FinAlgoritmo
```

**Explicación:**
- Solo hay dos caminos posibles: **verdadero** (par) o **falso** (impar).
- `num mod 2 = 0` es la condición; si se cumple, se ejecuta el bloque del `Entonces`; si no, el del `SiNo`.
- Es el equivalente directo de `if...else` en otros lenguajes.

**Prueba (num = 7):** 7 mod 2 = 1 ≠ 0 → "es impar" ✅

---

### 📌 Ejemplo 2: Condicional anidado `Si...Entonces...SiNo` (equivalente a `else if`)

**Enunciado:** Leer una nota (0.0 a 5.0) y clasificarla: "Excelente" (≥4.5), "Bueno" (≥4.0), "Aceptable" (≥3.0), "Reprobado" (<3.0).

**Pseudocódigo:**

```text
Algoritmo Ejemplo_ElseIf
    Definir nota Como Real;
    Escribir "Digite la nota (0.0 a 5.0):";
    Leer nota;
    Si nota >= 4.5 Entonces
        Escribir "Excelente";
    SiNo
        Si nota >= 4.0 Entonces
            Escribir "Bueno";
        SiNo
            Si nota >= 3.0 Entonces
                Escribir "Aceptable";
            SiNo
                Escribir "Reprobado";
            FinSi
        FinSi
    FinSi
FinAlgoritmo
```

**Explicación:**
- Se evalúan las condiciones **en cascada**: si la primera falla, se prueba la siguiente, y así sucesivamente.
- Solo se ejecuta **un** bloque (el de la primera condición que se cumpla).
- Es el equivalente a `if...else if...else` en otros lenguajes.

**Prueba (nota = 4.2):** No es ≥4.5 → no es "Excelente"; sí es ≥4.0 → **"Bueno"** ✅

---

### 📌 Ejemplo 3: Condicional con operadores lógicos `Si...Entonces...SiNo` (equivalente a `else` combinado)

**Enunciado:** Leer la edad de una persona y una autorización; determinar si puede ingresar al evento (mayor de edad **O** con autorización).

**Pseudocódigo:**

```text
Algoritmo Ejemplo_ElseLogico
    Definir edad Como Entero;
    Definir autorizacion, puede_ingresar Como Logico;
    Escribir "Digite su edad:";
    Leer edad;
    Escribir "¿Tiene autorización? (Verdadero/Falso):";
    Leer autorizacion;
    puede_ingresar <- (edad >= 18) O autorizacion;
    Si puede_ingresar Entonces
        Escribir "Puede ingresar al evento.";
    SiNo
        Escribir "No puede ingresar al evento.";
    FinSi
FinAlgoritmo
```

**Explicación:**
- Se usa una variable **Lógica** (`puede_ingresar`) para almacenar el resultado de la condición compuesta.
- El operador `O` (OR) devuelve Verdadero si **al menos una** de las dos condiciones se cumple.
- El `SiNo` cubre el caso en que **ninguna** se cumple (menor de edad y sin autorización).

**Prueba (edad = 16, autorizacion = Verdadero):** (16≥18) O Verdadero = Verdadero → **"Puede ingresar"** ✅

---

## 🔘 Parte 3: `Según` (Switch)

### 📌 Ejemplo 1: `Según` con casos numéricos — Días de la semana

**Enunciado:** Leer un número del 1 al 7 y mostrar el día de la semana correspondiente.

**Pseudocódigo:**

```text
Algoritmo Ejemplo_Segun_Dias
    Definir dia Como Entero;
    Escribir "Digite un número del 1 al 7:";
    Leer dia;
    Segun dia Hacer
        1: Escribir "Lunes";
        2: Escribir "Martes";
        3: Escribir "Miércoles";
        4: Escribir "Jueves";
        5: Escribir "Viernes";
        6: Escribir "Sábado";
        7: Escribir "Domingo";
        De Otro Modo: Escribir "Número no válido.";
    FinSegun
FinAlgoritmo
```

**Explicación:**
- `Según` evalúa el valor de `dia` y ejecuta **solo** el caso que coincida.
- `De Otro Modo` es el equivalente a `default` en otros lenguajes: captura valores no contemplados.
- Es más legible que una cadena larga de `Si...SiNo` cuando hay **muchas opciones discretas**.

**Prueba (dia = 6):** → **"Sábado"** ✅

---

### 📌 Ejemplo 2: `Según` con operaciones — Calculadora básica

**Enunciado:** Leer dos números y un operador (+, -, *, /); realizar la operación y mostrar el resultado.

**Pseudocódigo:**

```text
Algoritmo Ejemplo_Segun_Calculadora
    Definir a, b, resultado Como Real;
    Definir operador Como Caracter;
    Escribir "Digite el primer número:";
    Leer a;
    Escribir "Digite el segundo número:";
    Leer b;
    Escribir "Digite el operador (+, -, *, /):";
    Leer operador;
    Segun operador Hacer
        '+': resultado <- a + b;
        '-': resultado <- a - b;
        '*': resultado <- a * b;
        '/': Si b <> 0 Entonces
                 resultado <- a / b;
             SiNo
                 Escribir "Error: división por cero.";
             FinSi
        De Otro Modo: Escribir "Operador no válido.";
    FinSegun
    Si operador = '+' O operador = '-' O operador = '*' O (operador = '/' Y b <> 0) Entonces
        Escribir "El resultado es: ", resultado;
    FinSi
FinAlgoritmo
```

**Explicación:**
- `Según` puede evaluar **caracteres** (encerrados entre comillas simples).
- En el caso de la división se añade una validación interna para evitar división por cero.
- `De Otro Modo` captura operadores no reconocidos.

**Prueba (a=10, b=4, operador='*'):** → **40** ✅

---

### 📌 Ejemplo 3: `Según` con rangos — Estaciones del año

**Enunciado:** Leer un mes (1-12) y mostrar la estación del año correspondiente (hemisferio norte).

**Pseudocódigo:**

```text
Algoritmo Ejemplo_Segun_Estaciones
    Definir mes Como Entero;
    Escribir "Digite el número del mes (1-12):";
    Leer mes;
    Segun mes Hacer
        12, 1, 2: Escribir "Invierno";
        3, 4, 5:  Escribir "Primavera";
        6, 7, 8:  Escribir "Verano";
        9, 10, 11: Escribir "Otoño";
        De Otro Modo: Escribir "Mes no válido.";
    FinSegun
FinAlgoritmo
```

**Explicación:**
- PSeInt permite **agrupar varios valores** en un mismo caso separándolos por comas (`12, 1, 2:`).
- Así se evita repetir la misma instrucción para cada mes de la estación.
- `De Otro Modo` maneja valores fuera del rango 1-12.

**Prueba (mes = 7):** → **"Verano"** ✅

---

## 📋 Tabla Resumen de Estructuras

| Estructura | Sintaxis en PSeInt | Cuándo usarla | Ejemplo del taller |
|:---|:---|:---|:---|
| **Mientras** | `Mientras cond Hacer ... FinMientras` | N° de iteraciones desconocido; condición al inicio | Suma hasta ingresar 0 |
| **Para** | `Para i <- ini Hasta fin Con Paso p Hacer ... FinPara` | N° de iteraciones conocido | Contar múltiplos de 3 del 1 al 20 |
| **Repetir** | `Repetir ... Hasta Que cond` | Al menos una ejecución; condición al final | Menú de opciones |
| **Si...SiNo** | `Si cond Entonces ... SiNo ... FinSi` | Dos caminos posibles | Par o impar |
| **Si anidado** | `Si cond1 ... SiNo Si cond2 ... FinSi FinSi` | Múltiples rangos o condiciones en cascada | Clasificación de nota |
| **Si con lógicos** | `Si (cond1) O (cond2) Entonces ... FinSi` | Combinar condiciones con Y / O / NO | Acceso con edad y autorización |
| **Según** | `Segun var Hacer caso: ... De Otro Modo: ... FinSegun` | Muchas opciones discretas de una variable | Días, operadores, estaciones |

---

## 💡 Consejos

> *"Siempre que vaya a desarrollar un algoritmo, primero debe clarificar el objetivo para que sepa hacia dónde va y hasta dónde debe llegar."* — Omar Iván Trejos Buriticá

- Antes de codificar, **haz la prueba de escritorio** de cada ejemplo con valores concretos.
- Recuerda que en PSeInt los **caracteres** van entre comillas simples (`'A'`) y las **cadenas** entre comillas dobles (`"Hola"`).
- El operador `mod` devuelve el **residuo** de la división entera; es clave para pares/impares y múltiplos.

---

### 📌 Instrucciones para usar este archivo `.md`

1. Copia todo el contenido de este documento.
2. Abre un editor de texto plano (Bloc de notas, VS Code, Obsidian, Typora, etc.).
3. Pega el contenido.
4. Guarda el archivo con el nombre `Ejemplos_Ciclos_Condicionales_Segun.md`.
5. ¡Listo! Ya tienes los ejemplos en formato Markdown, listos para consultar o implementar en PSeInt.

Si necesitas que agregue más ejemplos, incluya las pruebas de escritorio completas de cada uno o adapte algún ejercicio a un caso específico, házmelo saber.