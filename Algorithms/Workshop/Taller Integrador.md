# 📝 Taller Integrador de PSeInt – 25 Ejercicios

**Asignatura:** Lógica de Programación
**Herramienta:** PSeInt
**Modalidad:** Individual
**Fecha de entrega:** [Insertar fecha]

---

## 🎯 Objetivo

Aplicar de forma integrada los conceptos de la lógica de programación (ciclos, condicionales, estructuras de selección múltiple, vectores, matrices, tipos de datos y pruebas de escritorio) mediante el diseño e implementación de algoritmos en PSeInt, fortaleciendo la verificación de la lógica antes de codificar.

---

## 📋 Listado de Ejercicios (Tabla de Asignación)

| N° | Categoría                 | Documento           | Título del Ejercicio             | Descripción breve                                                                                                                                |
| :-- | :------------------------- | :------------------ | :-------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1   | Bucles                     | [Agregar Documento] | Suma de números con `Mientras` | Leer números hasta que el usuario ingrese 0; sumar los valores ingresados y mostrar el total.                                                    |
| 2   | Bucles                     | [Agregar Documento  | Conteo con `Para`               | Mostrar los números del 1 al 20 y contar cuántos son múltiplos de 3.                                                                           |
| 3   | Bucles                     | 1042253925          | Menú con `Repetir`             | Mostrar un menú de opciones (1. Saludar, 2. Despedirse, 3. Salir) y repetirlo hasta que el usuario elija 3.                                      |
| 4   | Condicional `Si-Escriba` | [Agregar Documento] | Par o impar                       | Leer un número entero y determinar si es par o impar usando solo `Si...Entonces...SiNo`.                                                       |
| 5   | Condicional `Si-Escriba` | [Agregar Documento] | Aprobado o reprobado              | Leer una nota (0.0 a 5.0) y mostrar "Aprobado" si es ≥ 3.0, "Reprobado" en caso contrario.                                                       |
| 6   | Condicional `Si-Escriba` | [Agregar Documento] | Descuento por edad                | Leer la edad de una persona y aplicar un descuento del 20% si es menor de 18 o mayor de 65; mostrar el descuento aplicado.                        |
| 7   | Condicional `Si-Escriba` | [Agregar Documento] | Mayor de tres números            | Leer tres números y determinar cuál es el mayor usando estructuras `Si...SiNo` anidadas.                                                      |
| 8   | Condicional `Si-Escriba` | [Agregar Documento] | Clasificación de nota            | Leer una nota y clasificarla: "Excelente" (≥4.5), "Bueno" (≥4.0 y <4.5), "Aceptable" (≥3.0 y <4.0), "Reprobado" (<3.0).                        |
| 9   | Condicional `Si-Escriba` | [Agregar Documento] | Año bisiesto                     | Leer un año y determinar si es bisiesto usando condiciones anidadas con `Si...SiNo`.                                                           |
| 10  | `Según` (Switch)        | [Agregar Documento] | Días de la semana                | Leer un número del 1 al 7 y mostrar el día de la semana correspondiente usando `Según`.                                                      |
| 11  | `Según` (Switch)        | [Agregar Documento] | Calculadora básica               | Leer dos números y un operador (+, -, *, /); usar `Según` para realizar la operación y mostrar el resultado.                                 |
| 12  | `Según` (Switch)        | [Agregar Documento] | Estaciones del año               | Leer un mes (1-12) y mostrar la estación del año correspondiente usando `Según`.                                                             |
| 13  | Vectores                   | [Agregar Documento] | Llenar y mostrar vector           | Leer 8 números enteros en un vector y mostrarlos en el mismo orden en que fueron ingresados.                                                     |
| 14  | Vectores                   | [Agregar Documento] | Promedio de notas                 | Leer 5 notas reales en un vector, calcular y mostrar el promedio, la nota mayor y la menor.                                                       |
| 15  | Vectores                   | [Agregar Documento] | Buscar en vector                  | Leer 10 números en un vector, luego leer un número adicional e indicar cuántas veces aparece y en qué posiciones.                             |
| 16  | Matrices                   | [Agregar Documento] | Llenar y mostrar matriz           | Leer una matriz de 3x3 y mostrarla en pantalla en forma de tabla.                                                                                 |
| 17  | Matrices                   | [Agregar Documento] | Suma de filas y columnas          | Leer una matriz de 4x4 y calcular la suma de cada fila y de cada columna, mostrando los resultados.                                               |
| 18  | Matrices                   | [Agregar Documento] | Diagonal principal                | Leer una matriz de 3x3 y calcular la suma de los elementos de su diagonal principal.                                                              |
| 19  | Tipos de datos             | [Agregar Documento] | Aritmética entera vs real        | Realizar `10/3` con variables enteras y `10.0/3.0` con variables reales; mostrar y explicar la diferencia.                                    |
| 20  | Tipos de datos             | [Agregar Documento] | Conversión ASCII                 | Leer una letra minúscula (tipo Carácter) y convertirla a mayúscula restando 32 (código ASCII).                                                |
| 21  | Tipos de datos             | 1042253925          | Concatenar cadenas                | Leer nombre y apellido (tipo Cadena) y mostrar el nombre completo concatenado con un espacio.                                                     |
| 22  | Tipos de datos             | [Agregar Documento] | Variable lógica                  | Leer la edad y una autorización (Verdadero/Falso); usar una variable Lógica para decidir si puede ingresar (mayor de edad O con autorización). |
| 23  | Tipos de datos             | [Agregar Documento] | Cálculo con reales               | Leer el precio de un producto y un porcentaje de descuento (Real); calcular y mostrar el precio final.                                            |
| 24  | Prueba de escritorio       | [Agregar Documento] | Suma de dos números              | Realizar la prueba de escritorio del algoritmo que suma dos números (a=5, b=3) y entregar la tabla de memoria y pantalla.                        |
| 25  | Prueba de escritorio       | [Agregar Documento] | Contar dígitos                   | Realizar la prueba de escritorio del algoritmo que cuenta dígitos de un número (num=523) y entregar la tabla paso a paso.                       |

> **Nota:** La columna **"Documento"** debe ser diligenciada por el docente o el estudiante con el número de documento de identidad de la persona asignada al ejercicio.

---

## 📌 Instrucciones por Categoría

### 🔁 Bucles (Ejercicios 1–3)

- **Ejercicio 1:** Usa `Mientras` (While). El ciclo debe terminar cuando se ingrese 0.
- **Ejercicio 2:** Usa `Para` (For). Recorre del 1 al 20 con paso 1.
- **Ejercicio 3:** Usa `Repetir` (Do-While). El menú debe mostrarse al menos una vez.

### 🔀 Condicionales (Ejercicios 4–9)

- **Ejercicios 4, 5 y 6:** Usa únicamente `Si...Entonces...SiNo` (sin anidar en exceso).
- **Ejercicios 7, 8 y 9:** Usa `Si...Entonces...SiNo` anidados (equivalente a `else if` en otros lenguajes).

### 🔘 `Según` (Ejercicios 10–12)

- Usa la estructura `Según <variable> Hacer` con sus respectivos casos y `De Otro Modo` para valores no válidos.

### 📊 Vectores (Ejercicios 13–15)

- Declara con `Dimension nombre(n)`.
- Recorre con ciclos `Para`.
- Para el ejercicio 15, lleva un contador y muestra las posiciones donde aparece el número buscado.

### 🧮 Matrices (Ejercicios 16–18)

- Declara con `Dimension nombre(filas, columnas)`.
- Usa ciclos anidados (`Para` dentro de `Para`) para llenar y recorrer.
- En el ejercicio 18, la diagonal principal se recorre con un solo índice: `matriz[i, i]`.

### 🔤 Tipos de datos (Ejercicios 19–23)

- **Ejercicio 19:** Declara una variable `Entero` y otra `Real`; compara los resultados.
- **Ejercicio 20:** Usa `Definir letra Como Caracter`; la conversión se hace con `letra <- letra - 32` (o `Mayusculas(letra)` si se permite).
- **Ejercicio 21:** Usa `Definir nombre, apellido, completo Como Cadena`; concatena con `+`.
- **Ejercicio 22:** Usa `Definir acceso Como Logico`; evalúa con `O` (OR).
- **Ejercicio 23:** Usa `Real` para precio y descuento.

### 🧪 Pruebas de escritorio (Ejercicios 24–25)

- Entrega la tabla con columnas: **Paso**, **Instrucción**, **Memoria (variables)** y **Pantalla**.
- Sigue el algoritmo paso a paso sin "razonar" como humano, tal como lo indica el autor.
- Concluye si el algoritmo cumple el objetivo.

---

## 📦 Entregables

1. **Portada** (nombre, fecha, título del taller, número de documento).
2. **Tabla de asignación** diligenciada con el número de documento.
3. **Los 25 ejercicios resueltos** en PSeInt (código fuente `.psc` o captura del pseudocódigo).
4. Para los ejercicios 24 y 25: **tabla de prueba de escritorio** completa.
5. **Reflexión final:** un párrafo sobre la importancia de la prueba de escritorio y de elegir correctamente los tipos de datos antes de programar.

---

## 📊 Rúbrica de Evaluación (Sugerida)

| Criterio                              | Excelente (5)                                               | Bueno (4)                                           | Regular (3)                                         | Insuficiente (2)                      |
| :------------------------------------ | :---------------------------------------------------------- | :-------------------------------------------------- | :-------------------------------------------------- | :------------------------------------ |
| **Uso correcto de estructuras** | Usa la estructura solicitada en cada ejercicio sin errores. | La mayoría son correctas con pequeños errores.    | Algunas son correctas pero con errores notorios.    | No usa la estructura solicitada.      |
| **Lógica del algoritmo**       | Todos los ejercicios resuelven el problema correctamente.   | La mayoría resuelve el problema.                   | Algunos resuelven el problema con errores lógicos. | No resuelven el problema.             |
| **Pruebas de escritorio**       | Las tablas están completas, correctas y bien concluidas.   | La mayoría están completas con pequeños errores. | Algunas están incompletas o con errores.           | No presenta tablas o son incorrectas. |
| **Presentación y orden**       | Documento impecable, bien redactado y organizado.           | Documento ordenado con pequeños errores.           | Documento desordenado pero legible.                 | Documento desordenado e ilegible.     |
| **Reflexión final**            | Reflexión profunda y personal.                             | Reflexión correcta pero superficial.               | Reflexión muy breve.                               | No presenta reflexión.               |

---

## 💡 Consejos del Autor

> *"No se olvide que lo único que necesita para realizar una buena prueba de escritorio es que usted, mientras la esté realizando, no 'razone', o sea, que actúe como si usted fuera un computador (que no piensa) y de manera autómata realice y obedezca una a una las órdenes establecidas en el algoritmo."*

> *"Las variables son como unas cajitas de diferentes tamaños y, por tal motivo, se deben declarar previamente para que el computador las dimensione de acuerdo a las necesidades."*

---

**Nota:** Si tienes dudas sobre la sintaxis de PSeInt, consulta los ejemplos resueltos de los talleres anteriores o la documentación oficial de PSeInt.

---

### 📌 Instrucciones para usar este archivo `.md`

1. Copia todo el contenido que está entre las tres comillas invertidas (``markdown` ... ``).
2. Abre un editor de texto plano (Bloc de notas, VS Code, Obsidian, Typora, etc.).
3. Pega el contenido.
4. Guarda el archivo con el nombre `Taller_Integrador_PSeInt_25_Ejercicios.md`.
5. ¡Listo! Ya tienes el taller en formato Markdown, con la tabla de asignación, instrucciones, entregables y rúbrica.

Si necesitas que ajuste algo (por ejemplo, agregar más detalle a algún ejercicio, cambiar la distribución de las categorías o incluir las soluciones), házmelo saber.
