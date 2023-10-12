# ARQUITECTURA DE SOFTWARE

# ¿ Que es la Arquitectura de Software ?

La arquitectura de software es el proceso de diseñar y estructurar un sistema de software. Consiste en organizar los requisitos funcionales y no funcionales.

Proporciona una base sólida para el desarrollo y evolución del software, permitiendo la adaptabilidad y el crecimiento a largo plazo.

la arquitectura de software permite que el sistema sea escalable, flexible, confiable y seguro, lo que permite también la reutilización de componentes y promueve la modularidad y la eficiencia.

existen diversidad de definiciones de arquitectura de software, no podríamos darle una definición en especifico ya que esto abarca el inicio y el final de un software a desarrollar.

![diagram.jpg](/img/diagram.jpg)

**algunos puntos clave al momento de desarrollar la arquitectura de software son:  Patrones de diseño, Patrones Arquitectónicos, Componentes, Conexiones, Ciclo de Vida**

# ¿ Que son los patrones de diseño ?

Básicamente es la solución a un problema de diseño.

conceptos clave de los patrones de diseño: 

| Reutilización de diseño | Usar una solución que ya ha resultado exitosa en otros proyectos. |
| --- | --- |
| Abstracción | facilita la comunicación entre  los miembros y mejor la comprensión del diseño, es como si todos los miembros de un equipo hablaran el mismo lenguaje. |
| Flexibilidad | permite aplicar patrones de diseño modificables , es decir, un código accesible y adaptable a cambios. |
| Estandarización | el paso a paso de un software, lo que permite que cualquier desarrollador se familiarice con el código y entiendan lo que se quiere alcanzar. |
| Categorías de patrones | Herramientas  que se agrupan en categorías según el trabajo o la función que cumplen, hay patrones creacionales (crear), estructurales (organizar el código) y de comportamiento (como funciona toda la relación) |

> El objetivo principal de un patrón de diseño es proporcionar soluciones a problemas específicos en el diseño de un software, como la creación, composición de objetos y la definición de comportamiento entre objetos.
> 

## 🎨**Patrones de diseños Creacionales:**

Se centran en la creación de objetos, proporcionando mecanismos para la creación de instancias de clases de manera flexible y eficiente con enfoques para manejar la creación de objetos en situaciones específicas, proporcionando flexibilidad y extensibilidad al diseño del sistema.

| Patron de Diseño | Propósito | Uso |
| --- | --- | --- |
| Singleton | Garantiza que una sola clase tenga una sola instancia y proporciona un punto de acceso global a esa instancia. | cuando solo se permite una única instancia de una clase debe haber un constructor privado y un método estático  ‘ObtenerInstancia()’ es el método estático que se utiliza para obtener la única instancia de la clase |
| Factory Method | Define una interfaz para crear un objeto, pero deja que las subclases alteren el tipo de objetos que se crearan. | se utiliza cuando una clase no puede anticipar la clase de objetos que debe crear, pero la clase delega la creación de estos objetos a sus subclases, como implementaciones concretas o anticipadas para saber el tipo de dato que queremos obtener. |
| Abstract Factory | Define una interfaz para crear grupos de objetos relacionados o independientes sin especificar sus clases concretas. | Cuando un sistema debe ser independiente de cómo se crean, componen y representan sus objetos. un ejemplo seria, personajes de un juego, mago, guerrero, ellos pertenecen a una clase que seria personaje |
| Builder | obtiene la construcción de un objeto complejo permitiendo la creación paso a paso del mismo. | Cuando un objeto debe ser construido con diferentes configuraciones o cuando la creación del objeto es demasiado compleja para un único constructor. |
| Prototype | Crea nuevos objetos duplicando un objeto existente, conocido como prototipo | Cuando la creación de un objeto consume mas recursos que la copia un un objeto existente |

## 🛠️Patrones de diseños Estructurales:

estos se centran en como las clases y objetos de componen para formar estructuras más grandes y como se pueden organizar para lograr un diseño mas flexible. buscan desacoplar componentes, simplificar interfaces o mejorar la eficiencia en la utilización de recursos.

| Patron de diseño | Definición | Propósito | uso |
| --- | --- | --- | --- |
| Adapter (adaptador) | Permite que la interfaz de una clase existente se utilice como interfaz para otra interfaz | facilita la operabilidad entre clases | cuando necesita que una clase existente funcione con una nueva interfaz sin modificar el código fuente |
| Bridge(Puente) | Desacopla una abstracción de su implementación, permite que ambas puedan variar de forma independiente | permite que una abstracción y su implementación evolucionen por separado | cuando quieres evitar un vinculo permanente entre una abstracción y su implementación |
| Composite(Compuesto) | compone objetos en forma de árbol para representar jerarquías parte-todo | permite tratar de manera uniforme a objetos individuales y composiciones de objetos | Cuando quieres tratar tanto a objetos individuales como a composiciones de objetos de manera uniforme. |
| Decorator(Decorador) | añade funcionalidades a un objeto sin modificar su estructura. | extiende la funcionalidad de un objeto sin modificar su estructura. | cuando se necesita agregar o modificar funcionalidades de objetos de forma individual y dinámica |
| Facade(Fachada) | Proporciona una interfaz  simplificada a un conjunto de interfaces más grandes y complejas | oculta la complejidad de un sistema y proporciona una interfaz mas fácil de usar. | cuando se necesita proporcionar una interfaz unificada para un conjunto de interfaces existentes y complejas. |
| Flyweigth(Peso Ligero) | reduce la redundancia cuando se tienen muchas instancias pequeñas de una clase | comparte eficientemente instancias comunes entre múltiples contextos para reducir el espacio utilizado. | Cuando tienes muchas instancias similares y deseas reducir el consumo de memoria. |
| Proxy | proporciona un sustituto o marcador de posición para otro objeto para controlar el acceso a él | controla el acceso y añade funcionalidad adicional a un objeto sin modificar su código | cuando necesitas controlar el acceso a un objeto, añadir funcionalidad adicional o retrasar la creación de un objeto hasta que sea necesario. |

## 🤖Patrones de diseños de Comportamiento:

Se centran en como  los objetos interactuan y se comunican entre sí, definiendo el comportamiento de un sistema permitiendo que los objetos cambien su comportamiento de manera dinámica y se coordinen eficientemente.

estos comportamientos proporcionan soluciones a problemas comunes en el diseño de software relacionados con la asignación de responsabilidades entre objetos y la coordinación de las interacciones.

| Patrón de diseño | Propósito | uso |
| --- | --- | --- |
| Chain of Responsibility (cadena de responsabilidad) | Desacoplar remitentes y destinatarios de solicitudes, permitiendo a varios objetos procesar la solicitud de manera independiente. | Cuando tienes múltiples objetos que pueden manejar una solicitud y quieres evitar acoplamientos fuertes. |
| Command(Comando) | Desacoplar el remitente de la acción que se ejecutará, permitiendo la parametrización y la manipulación de comandos. | Cuando necesitas parametrizar objetos con operaciones, poner operaciones en una cola o permitir operaciones deshacer. |
| Interpreter(Interprete) | Interpretar expresiones de un lenguaje específico y ejecutar acciones correspondientes. | Cuando necesitas interpretar y ejecutar expresiones definidas en un lenguaje específico. |
| Iterator(Iterador) | Desacoplar algoritmos de iteración de la estructura de la colección. | Cuando quieres proporcionar un acceso uniforme a los elementos de una colección sin exponer su implementación interna. |
| Mediator(Mediador) | Centralizar la comunicación y reducir las dependencias directas entre los componentes de un sistema. | Cuando hay muchas interacciones entre objetos y quieres evitar un acoplamiento excesivo. |
| Memento(Recuerdo) | Permite que un objeto vuelva a su estado anterior sin revelar los detalles de su implementación interna. | Cuando necesitas guardar y restaurar el estado interno de un objeto. |
| Observer(Observador) | Permite que múltiples objetos se actualicen de manera automática cuando cambie el estado de uno de ellos. | Cuando un objeto necesita notificar a otros objetos sobre cambios en su estado. |
| State(Estado) | Permite que un objeto cambie su comportamiento en tiempo de ejecución en función de su estado interno. | Cuando un objeto debe cambiar su comportamiento en función de cambios en su estado. |
| Strategy(Estrategia) | Permite que un algoritmo varíe independientemente de los clientes que lo utilizan. | Cuando necesitas definir una familia de algoritmos, encapsular cada uno y hacer que sean intercambiables. |
| Template Methos(Método plantilla) | Permite que las subclases extiendan o modifiquen partes de un algoritmo sin cambiar su estructura general. | Cuando quieres definir un algoritmo pero permitir que las subclases proporcionen implementaciones específicas para ciertos pasos. |
| Visitor(Visitante) | Permite agregar nuevas operaciones sin modificar las clases de los elementos sobre los que opera. | Cuando tienes una estructura de objetos y quieres realizar diferentes operaciones en estos objetos sin modificar sus clases. |

# ¿ Que son los patrones arquitectónicos?

proporcionan un enfoque estructurado para diseñar sistemas que pueden mejorar la eficiencia, la flexibilidad y la escalabilidad del software.

aquí algunos patrones arquitectónicos comunes:

| Arquitectura | Descripción |
| --- | --- |
| Modelo Vista Controlador (MVC) | Divide una aplicación en tres componentes principales: Modelo (lógica de la aplicación), Vista (interfaz de usuario) y Controlador (maneja la interacción entre el Modelo y la Vista). |
| Modelo Vista Vista-Modelo (MVVM) | Utiliza un componente adicional llamado ViewModel para manejar la lógica de presentación y mantener el estado del modelo. |
| Arquitectura de Microservicios | Divide una aplicación en servicios pequeños e independientes, cada uno ejecutándose en su propio proceso y comunicándose a través de interfaces bien definidas.
Uso típico: Sistemas distribuidos y escalables. |
| Arquitectura de Capas | Organiza el código en capas lógicas, como la interfaz de usuario, la lógica de negocio y la capa de datos. Cada capa tiene una responsabilidad específica. |
| Arquitectura Hexagonal(Puertos y adaptadores) | Separa la lógica de la aplicación del entorno externo utilizando "puertos" y "adaptadores". Los puertos definen interfaces a través de las cuales la aplicación se comunica con el exterior, mientras que los adaptadores implementan esas interfaces. |
| Publicador-Subscriptor(Observer) | Define una dependencia uno a muchos entre objetos para que cuando un objeto cambie su estado, todos sus dependientes sean notificados y actualizados automáticamente |
| Patrón de Repositorio | Abstrae la capa de acceso a datos proporcionando una interfaz para trabajar con datos. Permite desacoplar la lógica de negocio de la implementación específica de almacenamiento de datos. |
| Middleware | Introduce una capa de software entre el sistema operativo y las aplicaciones para facilitar la comunicación y el intercambio de datos. |
| Arquitectura Monolítica | Consiste en un solo bloque de código fuente donde todos los componentes del sistema están interconectados y desplegados como una única unidad. |
| Arquitectura basada en eventos | Utiliza eventos y mensajes para lograr la comunicación entre componentes. Los componentes pueden reaccionar y responder a eventos. |
| En tres capas | tiene la finalidad de separar la aplicación por capas, con la finalidad de que cada capa realiza una tarea específica. |

> La elección del patrón adecuado depende de los requisitos y las características especificas de la aplicación que estés desarrollando.
> 

# Diferencia entre patrones de diseño y patrones arquitectónicos

![diferencia.png](/img/diferencia.png)

> mientras que los patrones de diseño se enfocan en problemas específicos en el diseño detallado de clases y objetos, los patrones arquitectónicos se ocupan de cuestiones más amplias relacionadas con la organización y la estructura general de sistemas de software. Ambos tipos de patrones son valiosos en el desarrollo de software y se utilizan en diferentes etapas del proceso de diseño y desarrollo.
> 

|  | Patrones de diseño | Patrones Arquitectónicos |
| --- | --- | --- |
| Alcance | Los patrones de diseño se centran en la resolución de problemas específicos a nivel de diseño de clases y objetos. | Los patrones arquitectónicos se centran en la organización general y la estructura de sistemas de software completos. |
| Propósito | Estos patrones proporcionan soluciones para problemas comunes en el diseño de software, como la creación de objetos, la gestión de la estructura de clases, la composición de objetos y más. | Estos patrones proporcionan soluciones a nivel de arquitectura para problemas comunes en el diseño y la estructura de sistemas grandes y complejos. Se preocupan por la disposición de componentes a gran escala, la interconexión de módulos, la escalabilidad entre otros. |
| Nivel de abstracción | Son más detallados y específicos. Se centran en cuestiones más pequeñas y específicas dentro de un sistema. | Son más generales y de alto nivel. Tratan con la organización general de sistemas, su comportamiento y su interacción. |

# ¿ Qué son los estilos arquitectónicos?

> son patrones de diseño de alto nivel que definen la estructura y organización de un sistema de software. Estos estilos proporcionan un conjunto de reglas o pautas para organizar los componentes y subcomponentes de un sistema, así como las relaciones y las interacciones entre ellos. Los estilos arquitectónicos ofrecen una forma de abordar los desafíos comunes en el diseño de software y ayudan a los arquitectos de software a tomar decisiones fundamentales sobre la estructura de un sistema.
> 

Estos estilos arquitectónicos son herramientas conceptuales que los arquitectos de software utilizan para abordar diferentes desafíos en el diseño de sistemas, seleccionando el estilo que mejor se adapte a los requisitos y objetivos específicos del proyecto. La elección de un estilo arquitectónico puede tener un impacto significativo en aspectos como el rendimiento, la escalabilidad, el mantenimiento y la flexibilidad del sistema resultante.

**Arquitectura en Capas (Layered Architecture):**

- **Descripción:** Organiza el sistema en capas o niveles, donde cada capa proporciona servicios a la capa superior y utiliza servicios de la capa inferior.
- **Propósito:** Separar las preocupaciones y proporcionar una estructura modular y fácil de entender.
- **Uso Típico:** Aplicaciones empresariales, sistemas web.

**Arquitectura Cliente-Servidor (Client-Server Architecture):**

- **Descripción:** Divide el sistema en dos partes principales: un cliente, que solicita servicios, y un servidor, que proporciona servicios.
- **Propósito:** Distribuir la carga de trabajo entre clientes y servidores, facilitar la escalabilidad y la gestión centralizada.
- **Uso Típico:** Aplicaciones web, sistemas distribuidos.

**Arquitectura Orientada a Servicios (Service-Oriented Architecture - SOA):**

- **Descripción:** Organiza el sistema en servicios independientes que se comunican a través de interfaces bien definidas.
- **Propósito:** Facilitar la interoperabilidad, reutilización de servicios y adaptabilidad a cambios en los requisitos.
- **Uso Típico:** Sistemas empresariales, aplicaciones distribuidas.

**Arquitectura basada en Eventos (Event-Driven Architecture):**

- **Descripción:** Los componentes del sistema se comunican mediante eventos, donde un evento desencadena una acción en otros componentes.
- **Propósito:** Desacoplar componentes, permitir la extensibilidad y la reactividad.
- **Uso Típico:** Sistemas en tiempo real, sistemas que requieren manejo de eventos.

**Arquitectura basada en Microservicios (Microservices Architecture):**

- **Descripción:** Divide la aplicación en servicios independientes, cada uno ejecutándose en su propio proceso y comunicándose a través de API bien definidas.
- **Propósito:** Escalabilidad, despliegue independiente, mantenimiento y evolución más fácil.
- **Uso Típico:** Aplicaciones empresariales, sistemas distribuidos.

**Arquitectura en Pipelining:**

- **Descripción:** Divide el procesamiento en etapas secuenciales, donde cada etapa realiza una parte específica de la tarea y pasa el resultado a la siguiente etapa.
- **Propósito:** Mejorar la eficiencia al permitir que varias etapas del proceso se ejecuten simultáneamente.
- **Uso Típico:** Sistemas de procesamiento de datos, compiladores.

**Arquitectura Monolítica:**

- **Descripción:** La aplicación se desarrolla como una única unidad, donde todas las funcionalidades se implementan en un solo código base.
- **Propósito:** Simplicidad, facilidad de desarrollo y despliegue.
- **Uso Típico:** Aplicaciones pequeñas a medianas, prototipos.

**Arquitectura Peer-to-Peer (P2P):**

- **Descripción:** Todos los nodos en el sistema son iguales y colaboran para proporcionar un servicio o recurso.
- **Propósito:** Distribuir la carga de trabajo, mejorar la escalabilidad y la redundancia.
- **Uso Típico:** Redes de intercambio de archivos, sistemas de mensajería P2P.

![estilo arq.png](/img/estilo_arq.png)

# [Relación entre los patrones de diseño arquitectónicos y estilos arquitectónicos.](https://www.notion.so/ARQUITECTURA-DE-SOFTWARE-bcf2e8acc5b8467e90b72315a3252212?pvs=21)

![relacion entre los tres.png](/img/relacion_entre_los_tres.png)

tenemos que los patrones de diseño son el tipo de patrón más específico y que centra en resolver como las clases se crean, estructura, relacionan y se comportan en tiempo de ejecución, por otra parte, los patrones arquitectónicos se enfocan en los componentes y como se relacionan entre sí, finalmente, los estilos arquitectónicos son marcos de referencia mediante los cuales es posible basarse para crear aplicaciones que compartan ciertas características.

# Conceptos de Ingeniería de Software

desarrollo, mantenimiento y evolución de sistemas de software.

# Atributos de Calidad de software:

Los atributos son esenciales para evaluar y mejorar la calidad de un sistema de software a lo largo de su ciclo de vida. Dependiendo del contexto y los requisitos específicos del proyecto, algunos atributos pueden ser más críticos que otros, y la atención adecuada a estos atributos contribuye al éxito y la satisfacción de los usuarios finales.

algunos atributos esenciales son los siguientes: 

1. **Funcionalidad:**
    - *Definición:* Capacidad del software para proporcionar funciones que satisfacen las necesidades especificadas.
    - *Ejemplos:* Cumplimiento de requisitos, precisión en la ejecución de funciones.
2. **Fiabilidad:**
    - *Definición:* Habilidad del software para realizar sus funciones de manera confiable y predecible.
    - *Ejemplos:* Tolerancia a fallos, capacidad de recuperación.
3. **Usabilidad:**
    - *Definición:* Grado de facilidad con el cual los usuarios pueden utilizar el software.
    - *Ejemplos:* Diseño intuitivo, eficiencia en la interacción usuario-sistema.
4. **Eficiencia:**
    - *Definición:* Uso eficiente de los recursos del sistema, como memoria y procesamiento.
    - *Ejemplos:* Rendimiento rápido, bajo consumo de recursos.
5. **Mantenibilidad:**
    - *Definición:* Facilidad con la cual el software puede ser modificado o mejorado.
    - *Ejemplos:* Legibilidad del código, modularidad, facilidad de corrección de errores.
6. **Portabilidad:**
    - *Definición:* Capacidad del software para funcionar en diferentes entornos y plataformas.
    - *Ejemplos:* Adaptabilidad a sistemas operativos, independencia de hardware.
7. **Adaptabilidad:**
    - *Definición:* Capacidad del software para adaptarse a cambios en los requisitos y el entorno.
    - *Ejemplos:* Flexibilidad en la incorporación de nuevas funciones, ajuste a cambios de hardware o software.
8. **Seguridad:**
    - *Definición:* Protección contra acceso no autorizado y manejo seguro de datos sensibles.
    - *Ejemplos:* Autenticación, autorización, cifrado de datos.
9. **Cumplimiento:**
    - *Definición:* Conformidad con estándares y regulaciones predefinidos.
    - *Ejemplos:* Cumplimiento de normativas de privacidad, estándares de codificación.
10. **Interoperabilidad:**
    - *Definición:* Capacidad del software para interactuar y operar con otros sistemas.
    - *Ejemplos:* Compatibilidad con estándares de comunicación, integración con sistemas externos.
11. **Escalabilidad:**
    - *Definición:* Capacidad del software para manejar un aumento en la carga o el tamaño del sistema.
    - *Ejemplos:* Escalabilidad horizontal, escalabilidad vertical.
12. **Testabilidad:**
    - *Definición:* Facilidad con la cual el software puede ser probado para verificar su correcto funcionamiento.
    - *Ejemplos:* Diseño para pruebas unitarias, disponibilidad de herramientas de prueba.

## Principios de Ingeniería de Software:

### Acoplamiento:

Es una característica muy importante cuando estamos diseñando y desarrollando un componente, hace referencia a que tanto un componente sabe o requiere de otro componente.

**Acoplamiento eferente:** por que A depende de B y de C parta poder realizar su labor, hay una relación entre ellas, puede ser que herede datos, colecciones, clases o métodos.

![eferente.png](/img/eferente.png)

**Acoplamiento Aferente:** por que D y E depende de A para poder ejecutar su trabajo, ver en mi componente quienes más dependen de él.

![aferente.png](/img/aferente.png)

| Tipos de Acoplamiento | Definición | Observaciones |
| --- | --- | --- |
| Acoplamiento de contenido(acoplamiento patológico) | que el modulo depende de cosas que son privadas o internas de otro modulo o componente | Por buenas practicas no es recomendado hacer ya que intenta acceder a datos privados. |
| Acoplamiento común | tienes dos componentes que dependen de una variable global | este tipo de acoplamiento hay que evitarlo ya que solo con el hecho de depender de una variable global significa que alguien la puede tocar, a no ser que esa variable global sea una constante o sea un valor que no se pueda modificar |
| Acoplamiento sellado | hay dos componentes que dependen de una estructura de datos común, como una serie de objetos y uno de los componentes depende  de una parte de esos objetos y la otra parte depende de otro componente de otra parte. |  |
| Acoplamiento por datos | similar al acoplamiento sellado con la diferencia que aquí estamos hablando de tipos de datos primitivos , es decir, enteros, numero reales, booleanos, lo que se hace es , ejemplo,  un componente se comunica con un método y ese le pasa valores primitivos. |  |
| Acoplamiento de mensajes | lo que sucede es que hay una comunicación entre componentes pero no se cambian datos, ejemplo, un método de un componente llame a un método en otro componente, pero solamente lo llama, lo único que va a conocer es el nombre del método y no le manda ningún parámetro adicional del cual se genere mayor acoplamiento |  |

> **Lo recomendado es NO utilizar ningún tipo de acoplamiento, es decir, que los componentes sean totalmente independientes el uno del otro, que se puedan modificar en distintos momentos sin que se vean afectados.**
> 

pocas relaciones entre si para que cada uno se pueda modificar de forma independiente y no existan dependencias que hagan mas difícil mantener el código.

### Cohesión:

Es una característica muy importante en todas las aplicaciones a diseñar y desarrollar. En términos generales cohesión es, que tan relacionadas están las operaciones, métodos o funciones de un modulo o componente.

![cohesion.png](/img/cohesion.png)

podemos ver una imagen una clase llamada Service y ella tiene cuatro métodos

en términos de cohesión, el método CalculateProductTax, es diferente a los otros métodos por que si los comparamos tiene una función totalmente diferente, los otros métodos estén pensados para interactuar con la base de datos, pero éste tiene una funcionalidad totalmente distinta, este seria un problema de Cohesión.

**¿Cómo se soluciona esto?:** crear clases o separar los atributos muchos mas especificados, buscando siempre tener una alta cohesión, que cada componente tengan funciones que estén entre sí lo más relacionadas.

**Tipos de Cohesión:**

1. Cohesión Causal (cohesión por que sí): Cuando un modulo tiene muchas operaciones, sin ninguna relación entre sí. **EVITAR ESTE TIPO DE COHESION.**
2. Cohesión Lógica: donde los procedimientos o métodos comparten algo en común pero al final hace cosas muy diferentes.
3. Cohesión por Procedimientos:  donde el modulo opera bajo el mismo conjunto de datos.
4. Cohesión Funcional: donde se trata que las operaciones en el modulo estén altamente relacionadas y contribuyan a realizar una única tarea especifica. como la separación de responsabilidades. siempre tener en cuenta, que tan relacionados están las funciones o las tareas que hacen los módulos .

### Solid:

**• S: Single responsibility principle (SRP):** Este principio establece que cada clase debe tener una única responsabilidad dentro de nuestro software, y esta responsabilidad debe estar definida y ser concreta. Todos los métodos deben estar alineados con la finalidad de la clase.

• **O: Open/closed principle (OCP):**  La idea de este principio es que las clases están abiertas a la extensión pero cerradas a la modificación, lo que significa que ante peticiones de cambio en nuestro programa, hay que ser capaces de añadir funcionalidad sin modificar la existente.

• **L: Liskov substitution principle (LSP):** hace referencia a cómo usamos la herencia de forma adecuada. El principio dice algo como lo siguiente si S es un subtipo de T , T puede ser reemplazado con objetos de tipo S sin alterar el comportamiento esperado en el programa.

• **I: Interface segregation principle (ISP):** es preferible separar elementos que requieren ser utilizados por distintos clientes, cuando un cliente depende de una clase que implementa una interfaz cuya funcionalidad este cliente no usa, pero que otros clientes si usan, este cliente estará siendo afectado por los cambios que fuercen otros clientes en la clase en cuestión.

• **D: Dependency inversion principle (DIP):**  programar contra la abstracción, podemos hacer que el código que es el núcleo de nuestra aplicación no dependa de los detalles de implementación, como pueden ser el framework que utilices, la base de datos, cómo te conectes a tu servidor. Todos estos aspectos se especificarán mediante interfaces, y el núcleo no tendrá que conocer cuál es la implementación real para funcionar.

La definición que se suele dar es:

A. Las clases de alto nivel no deberían depender de las clases de bajo nivel. Ambas deberían depender de las abstracciones.

B. Las abstracciones no deberían depender de los detalles. Los detalles deberían depender de las abstracciones.