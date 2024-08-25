---
publishedAt: 2023-07-12 17:15:00
---

# La IA como multiplicador de productividad en el Quality Assurance.

## Introducción

Estamos en 2024 y desde el «boom» de finales de 2022 ya hace más de un año que la inteligencia artificial aparece por todas partes, la tenemos hasta en la sopa. Está claro que esta tecnología está aquí para quedarse y hacernos mucho más productivos en muchísimos ámbitos de nuestras vidas.

A lo largo de este tiempo he usado esta tecnología -la IA- en diferentes ámbitos y con multitud de propósitos distintos, ya sea para la generación de imágenes -con Midjourney- para crear fotografía de stock original para utilizar en el diseño de una página web como para aumentar mi productividad como consultor experto en calidad de software en Sngular.

Es en este segundo punto donde me gustaría hacer especial hincapié en este post compartiéndote los usos principales que le he encontrado en mi día a día como QE (Quality Engineer) y mostrándote como puede ayudarte a hacer más, mejor y en menos tiempo una buena parte de tu trabajo, yo uso ChatGPT y Github Copilot como mis asistentes personales en los que confío y sé que siempre puedo delegar en ellos las tareas más repetitivas y aburridas de mi trabajo, eso si, supervisando siempre -y mejorando si en necesario- los resultados que me devuelven para hacer siempre mi trabajo de la mejor forma posible.

## **Evolución y contexto actual del rol del QA**

El rol del QA ha ido evolucionando con los años, pasando de un mero ejecutor de pruebas en el pasado a un perfil mucho más transversal y que se involucra en todo el ciclo de desarrollo de software en la actualidad. Esto ha ocurrido en paralelo a una evolución del sector impulsado por la adopción de las metodologías ágiles y la cultura «DevOps» durante la última década buscando formas más eficientes de desarrollar y lanzar productos de software al mercado.

> “Hablo de poder dedicar más tiempo a entender que necesidad estamos satisfaciendo al usuario con la funcionalidad, de dar un paso atrás y ver la foto completa de la funcionalidad para tomar mejores decisiones de calidad”

Un ingeniero de calidad ya no solo ha de limitarse a definir un plan de pruebas que se ejecuta de forma manual tras el desarrollo, si no que ahora ha de ampliar sus miras definiendo una estrategia de pruebas y asegurando la calidad en todo el proceso: desde la definición de las historias de usuario (HU) por parte del «Product Owner (PO)» hasta la automatización y mantenimiento de los test automatizados tras el despliegue en producción del software.

Es en este entorno actual y complejo donde la IA puede ser nuestro mejor aliado para aliviar carga de trabajo que resulta pesada y repetitiva permitiéndonos centrar nuestros esfuerzos donde podamos aportar mayor valor, ahí donde la IA -al menos todavía- no puede llegar y el enfoque humano y la experiencia profesional es esencial.

Hablo de dedicar más tiempo a entender que necesidad estamos satisfaciendo al usuario con la funcionalidad, de dar un paso atrás y ver la foto completa de la funcionalidad para tomar mejores decisiones de calidad, hablo de poder dedicar más tiempo a pruebas exploratorias o a pruebas de experiencia de usuario si tenemos el conocimiento para ello, en definitiva a aquellas evaluaciones subjetivas guiados por nuestra experiencia como profesionales y expertos en calidad.

## IA Generativa para generar un plan de pruebas (con ChatGPT)

A continuación os voy a mostrar mediante un ejemplo como podemos utilizar ChatGPT -yo uso el modelo gratuito- para generar un plan de pruebas completo y como generar los escenarios a posteriori para llevárnoslo a nuestro IDE e integrarlo en nuestro framework de pruebas, yo le pediré que me los genere utilizando Gherkin para el framework de Cucumber.

### Parte 1: Generar plan de pruebas y darle formato con ChatGPT

Tenemos una aplicación web que es una calculadora científica y tiene todas las características de una calculadora de este tipo, le pediremos a ChatGPT que nos genere un plan de pruebas para esta funcionalidad, además veremos como le daremos formato al resultado obtenido.

**🎬 DemoPlanDePruebasChatGPT.mp4**

**Prompt (Yo):**

Generame un plan de pruebas completo en formato de tabla y usando Gherkin para una calculadora científica

**ChatGPT:**

Aquí tienes un ejemplo de un plan de pruebas completo utilizando Gherkin para una calculadora científica:

| **Funcionalidad**         | **Escenario**                                       | **Paso**                                                    | **Resultado esperado** | **Estado**                                                                            |
| ------------------------- | --------------------------------------------------- | ----------------------------------------------------------- | ---------------------- | ------------------------------------------------------------------------------------- |
| Suma                      | Sumar dos números positivos                         | Dado que tengo dos números positivos 5 y 3                  | 5 + 3                  | Se muestra el resultado correcto 8                                                    |
|                           | Sumar un número positivo y un número negativo       | Dado que tengo un número positivo 5 y un número negativo -3 | 5 + (-3)               | Se muestra el resultado correcto 2                                                    |
| Resta                     | Restar dos números positivos                        | Dado que tengo dos números positivos 8 y 3                  | 8 - 3                  | Se muestra el resultado correcto 5                                                    |
|                           | Restar un número negativo de un número positivo     | Dado que tengo un número positivo 8 y un número negativo -3 | 8 - (-3)               | Se muestra el resultado correcto 11                                                   |
| Multiplicación            | Multiplicar dos números positivos                   | Dado que tengo dos números positivos 4 y 3                  | 4 \* 3                 | Se muestra el resultado correcto 12                                                   |
|                           | Multiplicar un número negativo y un número positivo | Dado que tengo un número positivo 4 y un número negativo -3 | 4 \* (-3)              | Se muestra el resultado correcto -12                                                  |
| División                  | Dividir dos números positivos                       | Dado que tengo dos números positivos 8 y 2                  | 8 / 2                  | Se muestra el resultado correcto 4                                                    |
|                           | Dividir un número positivo entre cero               | Dado que tengo un número positivo 8 y el número cero        | 8 / 0                  | Se muestra un mensaje de error indicando que la división entre cero no está permitida |
| Funciones trigonométricas | Calcular el seno de un ángulo en radianes           | Dado que tengo un ángulo de 45 grados convertido a radianes | sen(45°)               | Se muestra el resultado correcto 0.7071                                               |
|                           | Calcular el coseno de un ángulo en radianes         | Dado que tengo un ángulo de 60 grados convertido a radianes | cos(60°)               | Se muestra el resultado correcto 0.5                                                  |
|                           | Calcular la tangente de un ángulo en radianes       | Dado que tengo un ángulo de 30 grados convertido a radianes | tan(30°)               | Se muestra el resultado correcto 0.5773                                               |

Este es un plan de pruebas básico que puede ser ampliado según los requisitos específicos de la calculadora científica y las funcionalidades adicionales que pueda tener. Cada escenario describe una situación de prueba específica y los pasos que se deben seguir para verificar que la calculadora esté funcionando correctamente. El estado de cada prueba puede ser actualizado a medida que se ejecutan y se obtienen los resultados reales.

**Prompt (Yo):**

Añádeme una primera columna a la izquierda del todo que me numere los casos de prueba

**ChatGPT:**

Por supuesto, aquí tienes el plan de pruebas con una columna adicional que numerará los casos de prueba:

| **Caso de Prueba** | **Funcionalidad**         | **Escenario**                                       | **Paso**                                                    | **Resultado esperado** | **Estado**                                                                            |
| ------------------ | ------------------------- | --------------------------------------------------- | ----------------------------------------------------------- | ---------------------- | ------------------------------------------------------------------------------------- |
| 1                  | Suma                      | Sumar dos números positivos                         | Dado que tengo dos números positivos 5 y 3                  | 5 + 3                  | Se muestra el resultado correcto 8                                                    |
| 2                  |                           | Sumar un número positivo y un número negativo       | Dado que tengo un número positivo 5 y un número negativo -3 | 5 + (-3)               | Se muestra el resultado correcto 2                                                    |
| 3                  | Resta                     | Restar dos números positivos                        | Dado que tengo dos números positivos 8 y 3                  | 8 - 3                  | Se muestra el resultado correcto 5                                                    |
| 4                  |                           | Restar un número negativo de un número positivo     | Dado que tengo un número positivo 8 y un número negativo -3 | 8 - (-3)               | Se muestra el resultado correcto 11                                                   |
| 5                  | Multiplicación            | Multiplicar dos números positivos                   | Dado que tengo dos números positivos 4 y 3                  | 4 \* 3                 | Se muestra el resultado correcto 12                                                   |
| 6                  |                           | Multiplicar un número negativo y un número positivo | Dado que tengo un número positivo 4 y un número negativo -3 | 4 \* (-3)              | Se muestra el resultado correcto -12                                                  |
| 7                  | División                  | Dividir dos números positivos                       | Dado que tengo dos números positivos 8 y 2                  | 8 / 2                  | Se muestra el resultado correcto 4                                                    |
| 8                  |                           | Dividir un número positivo entre cero               | Dado que tengo un número positivo 8 y el número cero        | 8 / 0                  | Se muestra un mensaje de error indicando que la división entre cero no está permitida |
| 9                  | Funciones trigonométricas | Calcular el seno de un ángulo en radianes           | Dado que tengo un ángulo de 45 grados convertido a radianes | sen(45°)               | Se muestra el resultado correcto 0.7071                                               |
| 10                 |                           | Calcular el coseno de un ángulo en radianes         | Dado que tengo un ángulo de 60 grados convertido a radianes | cos(60°)               | Se muestra el resultado correcto 0.5                                                  |
| 11                 |                           | Calcular la tangente de un ángulo en radianes       | Dado que tengo un ángulo de 30 grados convertido a radianes | tan(30°)               | Se muestra el resultado correcto 0.5773                                               |

Esta numeración proporciona una identificación única para cada caso de prueba, lo que facilita la referencia y el seguimiento del progreso durante la ejecución de las pruebas

**Prompt (Yo):**

Añádeme dos columnas a la tabla a la derecha , la primera será 'Evidencias' y la segunda 'Pass/Fail’

**ChatGPT:**

Claro, aquí está la tabla actualizada con las columnas adicionales de "Evidencias" y "Pass/Fail":

| **Caso de Prueba** | **Funcionalidad**         | **Escenario**                                       | **Paso**                                                    | **Resultado esperado** | **Estado**                                                                            | **Evidencias** | **Pass/Fail** |
| ------------------ | ------------------------- | --------------------------------------------------- | ----------------------------------------------------------- | ---------------------- | ------------------------------------------------------------------------------------- | -------------- | ------------- |
| 1                  | Suma                      | Sumar dos números positivos                         | Dado que tengo dos números positivos 5 y 3                  | 5 + 3                  | Se muestra el resultado correcto 8                                                    | Pendiente      |               |
| 2                  |                           | Sumar un número positivo y un número negativo       | Dado que tengo un número positivo 5 y un número negativo -3 | 5 + (-3)               | Se muestra el resultado correcto 2                                                    | Pendiente      |               |
| 3                  | Resta                     | Restar dos números positivos                        | Dado que tengo dos números positivos 8 y 3                  | 8 - 3                  | Se muestra el resultado correcto 5                                                    | Pendiente      |               |
| 4                  |                           | Restar un número negativo de un número positivo     | Dado que tengo un número positivo 8 y un número negativo -3 | 8 - (-3)               | Se muestra el resultado correcto 11                                                   | Pendiente      |               |
| 5                  | Multiplicación            | Multiplicar dos números positivos                   | Dado que tengo dos números positivos 4 y 3                  | 4 \* 3                 | Se muestra el resultado correcto 12                                                   | Pendiente      |               |
| 6                  |                           | Multiplicar un número negativo y un número positivo | Dado que tengo un número positivo 4 y un número negativo -3 | 4 \* (-3)              | Se muestra el resultado correcto -12                                                  | Pendiente      |               |
| 7                  | División                  | Dividir dos números positivos                       | Dado que tengo dos números positivos 8 y 2                  | 8 / 2                  | Se muestra el resultado correcto 4                                                    | Pendiente      |               |
| 8                  |                           | Dividir un número positivo entre cero               | Dado que tengo un número positivo 8 y el número cero        | 8 / 0                  | Se muestra un mensaje de error indicando que la división entre cero no está permitida | Pendiente      |               |
| 9                  | Funciones trigonométricas | Calcular el seno de un ángulo en radianes           | Dado que tengo un ángulo de 45 grados convertido a radianes | sen(45°)               | Se muestra el resultado correcto 0.7071                                               | Pendiente      |               |
| 10                 |                           | Calcular el coseno de un ángulo en radianes         | Dado que tengo un ángulo de 60 grados convertido a radianes | cos(60°)               | Se muestra el resultado correcto 0.5                                                  | Pendiente      |               |
| 11                 |                           | Calcular la tangente de un ángulo en radianes       | Dado que tengo un ángulo de 30 grados convertido a radianes | tan(30°)               | Se muestra el resultado correcto 0.5773                                               | Pendiente      |               |

Estas columnas adicionales te permitirán registrar las evidencias de la ejecución de cada paso del caso de prueba y marcar si el resultado esperado coincide (Pass) o no (Fail).

### Parte 2: Pasar del plan de pruebas en formato tabla a escenarios en lenguaje Gherkin para el framework de Cucumber con ChatGPT

**🎬 DemoScenariosGherkinCucumberChatGPT.mp4**

**Prompt (Yo):**

Con este plan de pruebas que hemos generado escribeme los Scenarios en Gherking para el framework de cucumber

**ChatGPT:**

Claro, aquí tienes los escenarios en formato Gherkin para el framework de Cucumber, basados en el plan de pruebas que hemos creado:

```gherkin
Feature: Calculadora Científica

  Scenario: Suma de dos números positivos
    Given tengo dos números positivos 5 y 3
    When sumo los números
    Then el resultado debe ser 8

  Scenario: Suma de un número positivo y un número negativo
    Given tengo un número positivo 5 y un número negativo -3
    When sumo los números
    Then el resultado debe ser 2

  Scenario: Resta de dos números positivos
    Given tengo dos números positivos 8 y 3
    When resto los números
    Then el resultado debe ser 5

  Scenario: Restar un número negativo de un número positivo
    Given tengo un número positivo 8 y un número negativo -3
    When resto los números
    Then el resultado debe ser 11

  Scenario: Multiplicación de dos números positivos
    Given tengo dos números positivos 4 y 3
    When multiplico los números
    Then el resultado debe ser 12

  Scenario: Multiplicar un número negativo y un número positivo
    Given tengo un número positivo 4 y un número negativo -3
    When multiplico los números
    Then el resultado debe ser -12

  Scenario: Dividir dos números positivos
    Given tengo dos números positivos 8 y 2
    When divido los números
    Then el resultado debe ser 4

  Scenario: Dividir un número positivo entre cero
    Given tengo un número positivo 8 y el número cero
    When intento dividir los números
    Then se muestra un mensaje de error indicando que la división entre cero no está permitida

  Scenario: Calcular el seno de un ángulo en radianes
    Given tengo un ángulo de 45 grados convertido a radianes
    When calculo el seno del ángulo
    Then el resultado debe ser 0.7071

  Scenario: Calcular el coseno de un ángulo en radianes
    Given tengo un ángulo de 60 grados convertido a radianes
    When calculo el coseno del ángulo
    Then el resultado debe ser 0.5

  Scenario: Calcular la tangente de un ángulo en radianes
    Given tengo un ángulo de 30 grados convertido a radianes
    When calculo la tangente del ángulo
    Then el resultado debe ser 0.5773

```

Estos escenarios están escritos de acuerdo con la sintaxis de Gherkin y pueden ser utilizados directamente en tus archivos de características para ejecutar pruebas utilizando Cucumber.

### Conclusiones

El correcto uso de la IA nos ahorra mucho tiempo que nos llevaría escribir caso a caso de forma manual y todo ello sin renunciar a nada al ser supervisada por un especialista QE.

Podemos personalizar y extender el plan de pruebas añadiendo casos de prueba a nuestro antojo, solo tienes que pedirle que te añada lo que necesites y lo hará como mucho en la mitad de tiempo que tu.

También podemos apoyarnos en ella para pasar nuestro plan de pruebas a lenguaje Gherkin para ahorrarnos este primer paso en la automatización de pruebas.

### 💡 Ideas

Una vez tengamos las «Features» y «Scenarios» en nuestro IDE y empecemos a desarrollar el código de automatización de los test funcionales podemos apoyarnos en otras herramientas de IA generativa especializada como Github Copilot que harán que el tiempo de automatización de pruebas (de desarrollo de estos test en código) se reduzca al máximo y a la vez se minimicen errores humanos.

## El futuro del «quality assurance»

La búsqueda de calidad del desarrollo de software cada vez está más presente y cobra más relevancia en las empresas. Si bien, la evidencia ha demostrado con el tiempo el ahorro de costes que supone detectar defectos en etapas tempranas del desarrollo y las bondades de la automatización de pruebas, cada vez la exigencia es mayor en este ámbito de especialidad y un bajo «time to market» es algo irrenunciable en muchos casos.

Es en este contexto de alta calidad y entregas continuas de valor al usuario dónde la IA se posiciona como un aliado clave en nuestro rol de ingenieros de calidad, aportando eficiencia en nuestro trabajo diario tanto en la definición de pruebas como en la automatización, dejando más tiempo para el análisis estratégico y otro tipo de tareas que aportan mayor valor y calidad al proceso de desarrollo de software donde la percepción humana y nuestra experiencia no pueden ser sustituidas por la inteligencia artificial, al menos todavía, veremos en unos años que nos depara esta apasionante época que nos ha tocado vivir de la inteligencia artificial.

> “Adaptarse o morir”

**Gonzalo Encinar**

Senior Quality Engineer at Sngular
