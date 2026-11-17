# **Taller 3 Investigación y Práctica: Análisis, Validación y Selección de Modelos de Proceso de Software**

# **1\. Encabezado Institucional y Metadatos del Taller**

* **Programa:** Análisis y Desarrollo de Software (ADSO) .
* **Referencia Bibliográfica Base:** Pressman, R. S. (*Ingeniería de Software: Un Enfoque Práctico*, 7.ª/8.ª Edición, Capítulos 2 y 3\) y marcos contemporáneos de entrega continua e ingeniería de confiabilidad (DevOps / DevSecOps).
* **Modalidad:** Investigación aplicada, análisis comparativo y arquitectura de procesos de software.
* **Entregables Finales:**
  1. Matriz Maestro de Validación Comparativa de Modelos de Proceso.
  2. Documento Técnico de Arquitectura de Procesos y Ciclo de Vida del Software (Formato estándar IEEE / Informe de Arquitectura de Procesos).

# **2\. Objetivo General y Objetivos Específicos**

## **Objetivo General**

Evaluar integralmente los modelos prescriptivos, evolutivos, ágiles y de entrega continua del ciclo de vida del software para validar, comparar y formular la estrategia metodológica óptima (pura, híbrida o personalizada) adaptada a las restricciones técnicas, funcionales y de riesgo de un proyecto de software real.

## **Objetivos Específicos**

* **Investigar** detalladamente los fundamentos, fases, actividades sombrilla (*umbrella activities*) y limitaciones de los modelos de proceso propuestos en la literatura clásica y moderna: Cascada, Modelo en V, Incremental, Construcción de Prototipos, Espiral de Boehm / WINWIN, Desarrollo Concurrente, Proceso Unificado (UP/RUP), Desarrollo Ágil (Scrum, XP, FDD, DSDM, ASD, Crystal) y DevOps.
* **Diligenciar** una matriz comparativa rigurosa evaluando criterios técnicos, gestión de riesgos, costo del cambio, participación del cliente, visibilidad del proyecto y entregables clave.
* **Validar** la viabilidad operativa y técnica de cada modelo frente a los Requerimientos Funcionales (RF) y No Funcionales (RNF) de un caso de estudio real o proyecto formativo asignado.
* **Proponer y Sustentar** mediante un Documento Técnico formal la selección de un modelo puro, una arquitectura híbrida o una adaptación a la medida, detallando sus fases, hitos de control, roles, artefactos y estrategia de mitigación de riesgos.

# **3\. Marco de Investigación: Taxonomía Completa de Modelos de Proceso**

Los equipos de trabajo deben investigar, analizar y documentar cada uno de los bloques metodológicos descritos a continuación, considerando las actividades estructurales (*comunicación, planeación, modelado, construcción, despliegue*) y las actividades sombrilla (*seguimiento y control de proyectos, gestión de riesgos, aseguramiento de la calidad de software \[SQA\], gestión de configuración \[SCM\], revisiones técnicas formalizadas y gestión de reusabilidad*).

## **3.1. Modelos Prescriptivos Tradicionales**

Son enfoques estructurados que imponen un orden secuencial o semi-secuencial estricto en el desarrollo de software.

* **Modelo en Cascada (Ciclo de Vida Clásico):**
  * *Mecanismo:* Flujo de ejecución lineal (Comunicación \$\\rightarrow\$ Planeación \$\\rightarrow\$ Modelado \$\\rightarrow\$ Construcción \$\\rightarrow\$ Despliegue).
  * *Fortalezas y Debilidades:* Alta predictibilidad y documentación exhaustiva; no obstante, presenta parálisis por análisis, alta rigidez ante cambios de requerimientos y generación diferida de código ejecutable (bloqueo al final del ciclo).
* **Modelo en V:**
  * *Mecanismo:* Asociación explícita entre cada fase del desarrollo (parte izquierda de la V) y su correspondiente nivel de prueba y validación (parte derecha de la V).
  * *Niveles de Prueba:* Requerimientos \$\\leftrightarrow\$ Pruebas de Aceptación; Diseño de Arquitectura \$\\leftrightarrow\$ Pruebas de Sistema; Diseño de Componentes \$\\leftrightarrow\$ Pruebas de Integración; Codificación \$\\leftrightarrow\$ Pruebas Unitarias.
* **Modelos de Proceso Incremental:**
  * *Mecanismo:* Combina elementos del flujo en cascada administrados de forma escalonada. Produce liberaciones funcionales parciales (incrementos), donde el primer incremento es el "núcleo" (*core*) del sistema.
  * *Aplicabilidad:* Proyectos donde el tiempo de salida al mercado (*Time-to-Market*) es crítico y se requieren capacidades básicas operativas desde etapas tempranas.

## **3.2. Modelos de Proceso Evolutivo**

Reconocen la naturaleza cambiante del software y permiten iterar hacia sistemas cada vez más complejos.

* **Construcción de Prototipos:**
  * *Mecanismo:* Flujo iterativo rápido (Comunicación \$\\rightarrow\$ Plan Rápido \$\\rightarrow\$ Modelado Rápido \$\\rightarrow\$ Construcción de Prototipo \$\\rightarrow\$ Despliegue, Entrega y Retroalimentación).
  * *Modalidades:* Prototipos Desechables (*Throwaway Prototypes* para esclarecer requerimientos oscuros) vs. Prototipos Evolutivos (que se pulen progresivamente hasta convertirse en el sistema final).
  * *Riesgos:* Tendencia del cliente a confundir un prototipo visual con el sistema de producción definitivo; deuda técnica precipitada.
* **Modelo en Espiral de Boehm y Variante WINWIN:**
  * *Mecanismo:* Proceso guiado por la evaluación de riesgos. Combina la naturaleza iterativa de la construcción de prototipos con los aspectos controlados y sistemáticos del modelo en cascada.
  * *Dimensiones:* Dimensión Radial (Costo acumulado) y Dimensión Angular (Progreso a través de las fases).
  * *Regiones de Tareas:* Comunicación con el cliente, Planeación, Análisis de riesgos, Ingeniería, Construcción y Entrega, Evaluación del cliente.
  * *Hitos de Fijación de Objetivos (Anchor Points):* Objetivos del Ciclo de Vida (LHO \- *Life Cycle Objectives*), Arquitectura del Ciclo de Vida (LCA \- *Life Cycle Architecture*) y Capacidad Operativa Inicial (IOC \- *Initial Operational Capability*).
  * *Variante WINWIN:* Enfocada en la negociación formal donde el equipo directivo/desarrollador gana satisfaciendo objetivos de costo y tiempo, y el cliente gana obteniendo las capacidades requeridas.
* **Modelo de Desarrollo Concurrente:**
  * *Mecanismo:* Representa el proceso como una red de actividades de ingeniería concurrentes. Cada actividad puede estar en estados como: *Inactiva, En Desarrollo, En Revisión, En Espera, En Modificación* o *Completada*.
  * *Aplicabilidad:* Adecuado para proyectos complejos donde múltiples equipos multidisciplinarios trabajan simultáneamente en módulos interdependientes.

## **3.3. Modelos Especializados y Proceso Unificado**

* **Desarrollo Basado en Componentes (CBD):** Reutilización sistemática de piezas de software preexistentes (componentes COTS o microservicios), priorizando la integración sobre la codificación desde cero.
* **Métodos Formales:** Especificación matemática rigurosa de sintaxis y semántica del software. Garantiza ausencia de defectos pero requiere alta especialización y genera elevados costos.
* **Desarrollo de Software Orientado a Aspectos (DSOA):** Aislamiento de incumbencias transversales (*Cross-Cutting Concerns*) como seguridad, auditoría y trazado (*logging*).
* **El Proceso Unificado (UP / RUP):**
  * *Mecanismo:* Proceso iterativo e incremental, dirigido por casos de uso, centrado en la arquitectura y enfocado en la mitigación de riesgos.
  * *Fases:*
    1. *Concepción:* Definición del alcance del proyecto, visión y modelo de negocio inicial.
    2. *Elaboración:* Análisis del dominio del problema, arquitectura base y mitigación de riesgos mayores.
    3. *Construcción:* Desarrollo iterativo del software ejecutable.
    4. *Transición:* Pruebas de aceptación, despliegue y capacitación a usuarios finales.
    5. *Producción:* Operación del sistema y monitoreo continuo.

## **3.4. Desarrollo Ágil (Manifiesto Ágil y Marcos Prescriptivos)**

Basado en las directrices del Manifiesto Ágil (Capítulo 3 de Pressman). Prioriza a los individuos e interacciones, el software funcionando, la colaboración con el cliente y la respuesta ante el cambio.

* **Aplanamiento de la Curva del Costo del Cambio:** La agilidad busca reducir la penalización financiera y temporal que implica modificar el software en etapas avanzadas mediante refactorización, automatización de pruebas y retroalimentación continua.
* **Marcos de Trabajo:**
  * *Extreme Programming (XP):* Enfoque centrado en la calidad del código, programación en parejas, desarrollo guiado por pruebas (TDD), integración continua y diseño simple.
  * *Scrum:* Marco iterativo estructurado en *Sprints*, fundamentado en eventos (Planificación, *Daily*, Revisión, Retrospectiva) y roles (Product Owner, Scrum Master, Developers).
  * *Desarrollo Adaptativo de Software (ASD):* Ciclo Especular \$\\rightarrow\$ Colaborar \$\\rightarrow\$ Aprender.
  * *Método de Desarrollo de Sistemas Dinámicos (DSDM):* Proporciona un marco formal para entregas a tiempo bajo el principio de que el 80% del sistema puede entregarse con el 20% del esfuerzo (Principio de Pareto).
  * *Crystal:* Familia de metodologías adaptables según la cantidad de personas en el equipo y la criticidad del sistema (Clear, Yellow, Orange, Red).
  * *Feature-Driven Development (FDD):* Proceso práctico iterativo centrado en la entrega de funcionalidades con valor para el cliente.

## **3.5. Cultura y Entrega Continua (DevOps)**

* **Sistemas de Registro (SoR) vs. Sistemas de Participación (SoE):** Transición de aplicaciones monolíticas tradicionales (SoR) a ecosistemas distribuidos, altamente dinámicos y orientados a la experiencia del usuario (SoE).
* **Shift Left (Mover a la Izquierda):** Integración temprana de la calidad, las pruebas automatizadas y la seguridad (DevSecOps) desde las primeras etapas del ciclo de vida.
* **Las 4 Rutas de Adopción de DevOps:**
  1. *DevOps orientado a la infraestructura* (Automatización de entornos).
  2. *DevOps centrado en la arquitectura* (Descomposición en microservicios).
  3. *DevOps impulsado por la integración continua* (CI/CD pipelines).
  4. *DevOps basado en la cultura* (Colaboración y responsabilidad compartida).
* **CI/CD e Infraestructura como Código (IaC):** Automatización del empaquetado, ejecución de suite de pruebas, provisioning de infraestructura declarativa y despliegues sin interrupción del servicio (*Zero-Downtime Deployments*).

# **4\. Guía Paso a Paso de Ejecución del Taller**

El taller se ejecutará secuencialmente mediante las siguientes 4 fases operativas:

## **Fase 1: Selección y Diagnóstico del Caso de Estudio**

Cada equipo elegirá o se le asignará uno de los siguientes proyectos de referencia (o su proyecto formativo institucional ADSO/Ingeniería):

1. *Sistema de Parqueadero Inteligente con Visión por Computadora (IA).*
2. *Sistema de Inventario POS y Facturación Electrónica en Tiempo Real.*
3. *Plataforma de PQRS con Chatbot Basado en Modelos LLM.*
4. *Control de Asistencia a Eventos Masivos mediante Reconocimiento Facial.*
5. *Sistema de Evaluación Agrícola y Diagnóstico de Cultivos por Imagen (IA Móvil).*
6. *Proyecto Formativo Integrador de la Titulación.*

**Entregables de la Fase 1:** El equipo debe documentar la volatilidad de requisitos, criticidad de los RNF (latencia, tolerancia a fallas, operación offline, cumplimiento normativo) y matriz inicial de riesgos del dominio.

## **Fase 2: Validación Exhaustiva y Cuadro Comparativo Maestro**

Los equipos deben analizar el comportamiento de cada modelo de proceso frente al caso de estudio seleccionado y completar la **Matriz Maestro de Validación Comparativa**.

### **Instrucciones para el llenado de la Matriz:**

* Evalúe rigurosamente cómo respondería cada modelo ante las características del proyecto.
* En la columna **Veredicto de Viabilidad**, marque una de las opciones: `Apto`, `Parcialmente Apto` o `No Apto`, adjuntando su correspondiente justificación técnica.

## **Plantilla de la Matriz Maestro de Validación Comparativa**

| Modelo de Proceso                     | Naturaleza y Enfoque                                   | Fases y Estructura Principal                                                                    | Manejo de Requisitos y Cambios                                 | Gestión de Riesgos                                                   | Rol del Cliente                                                     | Entregables Clave                                                  | Escenario Ideal                                                           | Limitaciones Críticas                                      | Veredicto de Viabilidad para el Proyecto                       |
| :------------------------------------ | :----------------------------------------------------- | :---------------------------------------------------------------------------------------------- | :------------------------------------------------------------- | :-------------------------------------------------------------------- | :------------------------------------------------------------------ | :----------------------------------------------------------------- | :------------------------------------------------------------------------ | :---------------------------------------------------------- | :------------------------------------------------------------- |
| **Cascada**                     | Prescriptivo, secuencial y determinista.               | Comunicación, Planeación, Modelado, Construcción, Despliegue.                                | Inflexible; requiere requisitos congelados al inicio.          | Reactiva; los riesgos se detectan en la fase de pruebas al final.     | Exclusivo al inicio (definición) y al final (entrega).             | Documentación exhaustiva, código fuente al final.                | Sistemas con requisitos fijos y normativas estrictas.                     | Parálisis por análisis, costo de cambio prohibitivo.      | *\[ Apto / Parcialmente Apto / No Apto \+ Justificación \]* |
| **Modelo en V**                 | Prescriptivo, enfocado en Verificación y Validación. | Fases de diseño mapeadas 1:1 con niveles de prueba.                                            | Riguroso; los cambios requieren re-evaluar todo el diagrama V. | Moderada; centrada en la eliminación de defectos de diseño.         | Definición de pruebas de aceptación en fases iniciales.           | Especificaciones de prueba formalizadas por nivel.                 | Sistemas críticos donde los fallos representan alto riesgo.              | Rigidez estructural similar a la Cascada.                   | *\[ Apto / Parcialmente Apto / No Apto \+ Justificación \]* |
| **Incremental**                 | Iterativo y escalonado.                                | Ciclos repetitivos en cascada para cada incremento.                                             | Flexible entre incrementos; congelado durante la entrega.      | Moderada; los riesgos se dividen por módulo.                         | Continuo al final de la entrega de cada incremento funcional.       | Incrementos operativos del sistema (*Core* \+ Funcionales).      | Proyectos con necesidad de salir al mercado rápidamente.                 | Puede sufrir de degradación de la arquitectura base.       | *\[ Apto / Parcialmente Apto / No Apto \+ Justificación \]* |
| **Construcción de Prototipos** | Evolutivo y experimental.                              | Plan Rápido \$\\rightarrow\$ Modelado \$\\rightarrow\$ Prototipo \$\\rightarrow\$ Evaluación. | Altamente adaptable; los requisitos se descubren al evaluar.   | Implícita; reduce el riesgo de inconsistencia de requisitos.         | Activo y colaborativo; evalúa constantemente las maquetas.         | Prototipos navegables, reporte de usabilidad.                      | Interfaces complejas o requisitos altamente inciertos.                    | Deuda técnica; el cliente exige liberar el prototipo.      | *\[ Apto / Parcialmente Apto / No Apto \+ Justificación \]* |
| **Espiral de Boehm / WINWIN**   | Evolutivo, guiado explícitamente por riesgos.         | 6 Regiones de tareas en ciclos radiales contiguos.                                              | Adaptable en cada iteración según el análisis de riesgo.    | Rigurosa y cuantitativa; corazón de la metodología.                 | Crítico en los puntos de fijación (LHO, LCA, IOC) y negociación. | Análisis de riesgos, prototipos, especificación formal.          | Sistemas de alta complejidad, alto costo e incertidumbre.                 | Requiere alta pericia en gestión de riesgos; costoso.      | *\[ Apto / Parcialmente Apto / No Apto \+ Justificación \]* |
| **Desarrollo Concurrente**      | Red de actividades simultáneas.                       | Estados de actividad (*Inactiva, En Cambio, Completada*).                                     | Gestionado mediante eventos que activan transiciones.          | Continua sobre las dependencias entre actividades.                    | Requerido en la validación de transiciones clave.                  | Redes de estados de actividades, componentes probados.             | Equipos multidisciplinarios trabajando en paralelo.                       | Dificultad para mantener la visibilidad de gestión.        | *\[ Apto / Parcialmente Apto / No Apto \+ Justificación \]* |
| **Proceso Unificado (UP/RUP)**  | Iterativo, centrado en arquitectura y Casos de Uso.    | Concepción, Elaboración, Construcción, Transición.                                          | Gestionado por priorización de Casos de Uso en iteraciones.   | Mitigación sistemática de riesgos arquitectónicos en Elaboración. | Involucrado en Concepción y Pruebas de Aceptación (Transición).  | Baseline de Arquitectura, Modelos UML, Incrementos de Software.    | Sistemas orientados a objetos de escala empresarial.                      | Sobrecarga documental y complejidad metodológica.          | *\[ Apto / Parcialmente Apto / No Apto \+ Justificación \]* |
| **Scrum / XP (Ágil)**          | Iterativo, incremental y altamente adaptativo.         | Sprints (Planificación, Daily, Review, Retrospectiva).                                         | Dinámico; gestionado mediante el Product Backlog.             | Empírica; identificación de impedimentos en la daily.               | Propietario del producto (*PO*) integrado diariamente.            | User Stories, Incrementos de Software Potencialmente Desplegables. | Requisitos cambiantes y equipos altamente capacitados.                    | Falta de visibilidad a largo plazo sin gobernanza.          | *\[ Apto / Parcialmente Apto / No Apto \+ Justificación \]* |
| **DevOps / Entrega Continua**   | Orientado a la cultura, automatización y operaciones. | CI/CD, IaC, Monitoreo, DevSecOps en loop continuo.                                              | Cambio dinámico con despliegues directos a producción.       | Automatizada; monitoreo continuo y pruebas en pipeline.               | Retroalimentación en tiempo real a través de telemetría.         | Pipelines automatizados, infraestructura declarativa.              | Sistemas cloud-native, microservicios, alta frecuencia de actualización. | Requiere madurez tecnológica e inversión en herramientas. | *\[ Apto / Parcialmente Apto / No Apto \+ Justificación \]* |

## **Fase 3: Matriz de Descarte y Selección / Diseño del Modelo Propuesto**

Los equipos deben analizar los resultados del cuadro comparativo y descartar aquellos modelos no viables mediante evidencia técnica explícita. Posteriormente, deben estructurar la propuesta final seleccionando una de las siguientes tres vías:

* **Opción A (Modelo Puro):** Aplicación estricta de una sola metodología (ej. Scrum puro) cuando el contexto del proyecto sea homogéneo y sin restricciones contradictorias.
* **Opción B (Arquitectura Híbrida):** Combinación estructurada de marcos de trabajo. Ejemplos comunes:
  * *Espiral \+ Scrum \+ DevOps:* Utilizar el marco estratégico del Espiral de Boehm para la fase de Concepción y Análisis de Riesgos de Inteligencia Artificial; Scrum para el desarrollo iterativo de funcionalidades de software; y DevOps para la automatización de la integración y el despliegue continuo (CI/CD).
  * *Proceso Unificado \+ XP:* Utilizar la fase de Elaboración de RUP para estabilizar la arquitectura del sistema y XP para la disciplina de desarrollo del código (Pair Programming, TDD).
* **Opción C (Modelo Personalizado a la Medida):** Construcción de un ciclo de vida propio detallando la secuencia exacta de etapas, puertas de decisión (*stage-gates*), actividades sombrilla e hitos adaptados al negocio.

## **Fase 4: Elaboración del Documento Técnico Resultante**

Sintetizar la propuesta técnica en el informe estructurado que se define a continuación.

# **5\. Estructura Obligatoria del Entregable: "Documento Técnico de Arquitectura de Procesos y Ciclo de Vida del Software"**

El documento resultante debe ser redactado con tono profesional, lenguaje técnico formal, rigor científico y presentado bajo la siguiente plantilla de contenidos:

## **Plantilla del Entregable Final**

```
================================================================================
DOCUMENTO TÉCNICO DE ARQUITECTURA DE PROCESOS Y CICLO DE VIDA DEL SOFTWARE
================================================================================
PROYECTO: [Nombre del Sistema Evaluado]
PROGRAMA: Análisis y Desarrollo de Software (ADSO) / Ingeniería de Software
EQUIPO EVALUADOR: [Nombres de los Integrantes]
FECHA DE REVISIÓN: [Fecha]
VERSIÓN DEL DOCUMENTO: 1.0.0
================================================================================

1. RESUMEN EJECUTIVO Y CONTEXTO DEL PROYECTO
   1.1. Descripción General del Problema y Dominio del Negocio.
   1.2. Alcance Técnico del Sistema.
   1.3. Matriz de Requerimientos Funcionales (RF) Críticos.
   1.4. Matriz de Requerimientos No Funcionales (RNF) Críticos (Rendimiento, Latencia, Seguridad, Concurrencia, Operación Offline).

2. ANÁLISIS DE RIESGOS TÉCNICOS, OPERATIVOS Y REGULATORIOS
   2.1. Identificación y Categorización de Riesgos del Proyecto (Matriz Impacto vs. Probabilidad).
   2.2. Mapeo de Riesgos derivados del Incumplimiento de RNF.
   2.3. Estrategias Preventivas y Contingencias Técnicas.

3. ESTUDIO COMPARATIVO Y VALIDACIÓN DE MODELOS DE PROCESO
   3.1. Matriz Maestro de Validación Comparativa (Tabla Completa según Fase 2).
   3.2. Matriz de Evaluación Ponderada (Puntuación de Modelos según los Criterios del Proyecto).
   3.3. Sustentación de Modelos Descartados (Evidencia técnica del por qué fallan ante el proyecto).

4. PROPUESTA METODOLÓGICA SELECCIONADA O DISEÑADA (PURO / HÍBRIDO / PERSONALIZADO)
   4.1. Justificación Técnica de la Elección Metodológica.
   4.2. Diagrama de Flujo del Ciclo de Vida Adoptado (Fases, Puertas de Control o Stage-Gates).
   4.3. Definición de Hitos de Control (LHO, LCA, IOC, Sprint Reviews, etc.).
   4.4. Estructura de Roles y Responsabilidades del Equipo.
   4.5. Operacionalización de las Actividades Sombrilla (SQA, SCM, Revisiones Técnicas, Gestión de Riesgos).

5. PLAN DE ARTEFACTOS, ENTREGABLES Y ESTRATEGIA DE VERIFICACIÓN / DESPLIEGUE
   5.1. Matriz de Artefactos por Fase (Documentos, Código, Modelos, Suites de Prueba).
   5.2. Estrategia de Verificación y Validación (Niveles de Prueba y Criterios de Aceptación).
   5.3. Estrategia DevOps y Pipeline CI/CD (Automatización, Ambientes y Seguridad DevSecOps).

6. DECLARACIÓN DE USO ÉTICO DE HERRAMIENTAS Y REFERENCIAS BIBLIOGRÁFICAS
   6.1. Declaración de Transparencia y Uso Ético de Inteligencia Artificial Generativa / Herramientas de Apoyo.
   6.2. Referencias Bibliográficas (Formato IEEE o APA 7.ª Edición, citando explícitamente Pressman Cap. 2 y 3).
================================================================================
```

# **6\. Rúbrica de Evaluación del Taller y del Documento Técnico**

| Criterio de Evaluación                                             | Peso (%)      | Excelente (90-100%)                                                                                                                                       | Sobresaliente (75-89%)                                                                                                               | Aceptable (60-74%)                                                                                                                         | Insuficiente (0-59%)                                                                                                                  |
| :------------------------------------------------------------------ | :------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------ |
| **Rigor Investigativo (Pressman Cap. 2-3 & DevOps)**          | **20%** | Demuestra un dominio excepcional de todas las familias de modelos, fases, actividades sombrilla y conceptos modernos de DevOps/DevSecOps.                 | Explica con claridad la mayoría de modelos y conceptos de Pressman y DevOps, con mínimas omisiones teóricas.                      | Muestra una comprensión básica de los modelos tradicionales y ágiles, pero carece de profundidad en actividades sombrilla o DevOps.     | Presenta confusiones teóricas graves o vacíos conceptuales sobre los modelos de proceso explicados en la bibliografía base.        |
| **Profundidad del Cuadro Comparativo y Validación**          | **25%** | Diligencia la matriz maestro en su totalidad con análisis técnico exhaustivo, justificaciones sólidas y un análisis impecable del impacto en los RNF. | Completa la matriz maestro evaluando todos los modelos; las justificaciones son pertinentes pero podrían profundizar en los RNF.    | El cuadro comparativo está incompleto en algunas columnas o presenta justificaciones superficiales para la asignación de viabilidad.     | La matriz comparativa carece de rigor, omitió modelos clave o los veredictos no tienen sustento técnico.                            |
| **Coherencia Técnica en la Selección / Diseño del Modelo** | **30%** | Defiende la elección (pura, híbrida o personalizada) con argumentos de arquitectura impecables, justificando descartes y detallando roles e hitos.      | Selecciona una alternativa metodológica coherente con el caso de estudio; define adecuadamente fases, hitos de control y roles.     | Propone una opción metodológica utilizable pero la justificación de descartes o el flujo de fases presenta incoherencias operativas.    | La elección del modelo es contradictoria con los riesgos y RNF del proyecto, o no se presenta un flujo de trabajo claro.             |
| **Calidad del Documento Técnico Resultante**                 | **25%** | El entregable sigue estrictamente la plantilla formal, presenta excelente redacción técnica, diagramas claros y citas bibliográficas correctas.        | Cumple con la estructura formal requerida; la redacción y organización son buenas con detalles menores a pulir en formato o citas. | Cumple de forma parcial con la estructura del documento técnico; redacción informal o inconsistencias en la presentación de artefactos. | Documento incompleto, no sigue la estructura formal estipulada, carece de lenguaje técnico o no incluye referencias bibliográficas. |
