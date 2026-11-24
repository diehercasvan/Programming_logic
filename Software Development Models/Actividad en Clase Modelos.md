Actividad de Clase: "La Decisión del Arquitecto de Procesos"

### 1. Datos Generales

- **Tema:** Modelos de Proceso de Software (Prescriptivos, Evolutivos, Incrementales, Espiral, etc.).
- **Referencia Bibliográfica:** Pressman, R. S. *Ingeniería de Software: Un enfoque práctico*, 9ª edición. Capítulo 2 y 3.
- **Duración:** 60-90 minutos.
- **Modalidad:** Grupos de 4-5 estudiantes.
- **Materiales:** Pizarra o tablero (dividido en secciones), marcadores/notas adhesivas, proyector (opcional para mostrar el caso).

---

### 2. Objetivo de Aprendizaje

Que el estudiante sea capaz de **seleccionar críticamente** un modelo de proceso de software (o una combinación de flujos de proceso) adecuado para un contexto específico, y **justificar** la elección de sus actividades estructurales (comunicación, planeación, modelado, construcción y despliegue) basándose en los riesgos y características del proyecto.

---

### 3. Descripción del Caso Práctico (El Problema)

**Título del Proyecto:** *Sistema de Gestión de Turnos para una Red de Clínicas "SaludTotal"*

**Contexto:**
La red de clínicas "SaludTotal" necesita urgentemente un sistema para gestionar la asignación de turnos en sus 5 sedes. Actualmente lo hacen con papel, lo que genera caos y pérdida de pacientes.

**Características del Proyecto (Restricciones):**

1. **Requisitos:** El cliente (Gerente General) tiene una idea vaga de lo que quiere ("Quiero que los pacientes saquen turnos desde el celular y que los médicos vean su agenda"). Sin embargo, hay regulaciones de salud estrictas sobre la privacidad de los datos que **no son negociables** y deben cumplirse desde el primer día.
2. **Tiempo:** El cliente quiere ver "algo funcionando" en **3 semanas** para presentarlo a los inversionistas (se requiere una versión mínima operativa).
3. **Riesgo Técnico:** La integración con el sistema legacy (antiguo) de facturación es compleja y **nadie en el equipo sabe si funcionará** hasta que se pruebe.
4. **Equipo:** El equipo de desarrollo es pequeño (3 personas) y no tiene mucha experiencia en arquitecturas complejas, pero sí en prototipado rápido.

---

### 4. Dinámica de la Actividad (Paso a Paso)

#### Fase 1: Análisis del Caso (15 min)

Cada grupo lee el caso y debe identificar en una hoja:

- **Riesgo Principal:** ¿Qué es lo que más miedo da que falle?
- **Restricción Clave:** ¿Qué es lo que *sí o sí* debe estar listo al inicio?
- **Necesidad de Retroalimentación:** ¿El cliente necesita ver algo ya o puede esperar 6 meses?

#### Fase 2: Selección en el Tablero (20 min)

El profesor dibuja en el tablero (o proyecta) las **5 Actividades Estructurales** de Pressman (Comunicación, Planeación, Modelado, Construcción, Despliegue) y los **Modelos** (Cascada, Incremental, Prototipos, Espiral, Concurrente, Agil).

**Instrucción para los grupos:**

1. **Seleccionar el Modelo:** El grupo escribe en el tablero (o pega una nota) el nombre del modelo elegido.
2. **Mapear las Fases:** Deben colocar flechas o marcar en el tablero **cómo se ejecutarán esas 5 actividades** en su modelo elegido.
   - *Ejemplo:* Si eligen **Espiral**, deben dibujar el bucle e indicar dónde va el "Análisis de Riesgos" (fundamental para el problema del sistema legacy).
   - *Ejemplo:* Si eligen **Prototipos**, deben indicar que la "Construcción" se enfoca en un prototipo desechable o evolutivo para las 3 semanas.

#### Fase 3: Justificación y Defensa (25 min)

Cada grupo presenta su selección (3 minutos por grupo). Deben responder obligatoriamente:

1. **¿Por qué este modelo?** (Ej: "Elegimos Espiral porque el riesgo de integración es alto y necesitamos analizar riesgos en cada ciclo").
2. **¿Por qué esas fases?** (Ej: "En nuestro modelo, la Comunicación es intensiva al inicio porque los requisitos son vagos, pero la Construcción se retrasa hasta tener un prototipo validado").
3. **¿Qué pasa con la fecha de 3 semanas?** (Aquí se evalúa si el modelo permite entregas tempranas).

#### Fase 4: Cierre y Debate (15 min)

El profesor contrasta las respuestas. Puntos clave para guiar el debate:

- **Si eligieron Cascada:** Preguntar: *"¿Cómo manejan el cambio de requisitos si el cliente no sabe qué quiere?"* (Pressman indica que Cascada es para requisitos muy bien entendidos ).
- **Si eligieron Incremental:** Preguntar: *"¿Cómo garantizan la seguridad desde el primer incremento?"*
- **Si eligieron Espiral:** Destacar que es el único que maneja explícitamente el **riesgo** , lo cual es vital para el sistema legacy.
- **Modelo Híbrido:** Se puede premiar si un grupo propone usar **Prototipos** para la interfaz (3 semanas) y luego **Espiral** para la integración compleja.

---

### 5. Solución Esperada (Guía para el Profesor)

No hay una única respuesta correcta, pero las mejores justificaciones deberían alinearse con lo que Pressman denomina **"Flujos de Proceso"** y la naturaleza del problema:

| Elemento del Caso                  | Implicación en el Modelo                              | Justificación Esperada del Estudiante (basada en Pressman)                                                                                                                                                                             |
| :--------------------------------- | :----------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Requisitos vagos**         | Evitar **Cascada** puro.                         | "El modelo en Cascada requiere que los requisitos estén congelados; aquí no lo están" .                                                                                                                                              |
| **Muestra en 3 semanas**     | Requiere **Incremental** o **Prototipos**. | "Usamos Prototipos para la interfaz rápida y luego evolucionamos a un Incremental para las funciones internas".                                                                                                                        |
| **Riesgo técnico (Legacy)** | Requiere **Espiral**.                            | "El modelo Espiral es el único que obliga a hacer un **Análisis de Riesgos** antes de codificar. Si la integración falla, lo sabremos en el primer bucle, no al final" .                                                       |
| **Seguridad estricta**       | Requiere **Modelado** riguroso desde el inicio.  | "Aunque usemos prototipos para la UI, la fase de Modelado (arquitectura de seguridad) debe ser lineal y estricta, no podemos prototipar la seguridad" (Esto demuestra madurez: usar un **flujo de proceso paralelo** o híbrido). |

### 6. Variante de la Actividad (Para grupos avanzados)

Si el tiempo lo permite, se puede pedir a los grupos que **combinen modelos** (ej. "Modelo Concurrente").

- **Instrucción:** "Dibujen en el tablero cómo el equipo de seguridad trabaja en paralelo (modelando) mientras el equipo de UI hace un prototipo rápido (construcción)". Esto refuerza el concepto de **Flujo de Proceso Paralelo** mencionado en el libro .

---

### 7. Conclusión de la Actividad

*"No existe un modelo de proceso único que sea el correcto para todos los proyectos"*. La habilidad clave no es memorizar los modelos, sino saber **adaptar el flujo de trabajo** a las restricciones del problema (riesgo, tiempo, claridad de requisitos), tal como se practicó en el tablero.
