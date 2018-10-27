# devops-course

# Ejercicio 1

## 1. ¿Podrías contar qué prácticas y herramientas DevOps usas en tu trabajo? ¿Cuáles te gustaría introducir? ¿Por qué?

El proyecto actual en el que me desenvuelvo, es un proyecto de software bancario, hago desarrollo bajo la herramienta TIBCO BusinessWorks que es utilizada para crear procesos que cumplan determinados requerimientos bajo una arquitectura orientada a servicios; en el día a día el proceso que se hace consiste en: desarrollar, crear el ejecutable manualmente (.ear) y desplegar manualmente mediante comandos en el cmd dependiendo del entorno (dev, int, uat); directamente en mi proyecto, lo que se ha comenzado a implementar es la automatización de algunas fases usando comandos maven, pero aún no contamos con un orquestador, es decir, con maven se crea el deployable usando un .bat, y se despliega mediante otro .bat, pero la parte importante de la orquestación de estas fases, no sé tiene implementada. 

En este punto me gustaría implementar herramientas que hagan la orquestación de estas fases, es decir que hagan la parte de integración continua, que ejecuten el juego de pruebas automaticamente y arrojen métricas para saber hasta que punto esta funcionando el servicio completo antes de desplegarse, y también utilizar contenedores para ejecutar determinadas tareas, ya que, como trabajo para un banco, me conecto a un ordenador que ponen a dispocisión, pero los recursos que me brindan son muy limitados, en cuanto a capacidad de disco, RAM, entre otros; todo esto con el fin de agilizar tareas de pruebas, despliegues y pasos a producción.


## 2. Las prácticas y herramientas DevOps evolucionan año tras año. ¿Podrías indicar cuáles son las tendencias de estos últimos años, así como su objetivo/beneficio?

Una tendencia en cuanto a cómo implementar DevOps, es utilizar Gitlab Ci, hacer un pipeline basado en YAML, y utilizar un agente para la ejecución de dicho pipeline; el agente que se utilice se puede ejecutar en cloud o en infrastructura propia, es decir, que pueden usar shell o docker, shell quiere decir que lo que se ejecute en el agente deberá estar instalado en el agente, y docker indica que solo debe instalarse docker y el agente correrá sobre este. El beneficio de esta tendencia es la automatización de operaciones mediante el uso de diferentes herramientas. 

Por otro lado, tenemos el enfoque modular, que se refiere a la utilización de equipos pequeños y ágiles para gestionar aplicaciones individuales. 

>Consejo: la clave del éxito de DevOps está en separar las actividades en distintas partes. Para cualquier nuevo producto que lance una organización, los equipos de DevOps deberían hacer una aproximación teniendo un enfoque modular y tener un plan claro de cómo romper con los productos monolíticos.

La infraestructura programable es otra tendencia que se viene aplicando desde 2016 qie implica programar la infraestrctura de manera que los propios desarrolladores puedan desarrollar y programar su entorno de forma simultánea 

Otra de las tendencias más reconocidas es la reducción del tiempo de despliegue, que se da a partir del uso de metodologías ágiles a la hora de trabajar. Con esto también se busca hacer sistemas más tolerantes a riesgos con el fin de que los cambios realizados tengan impactos menos negativos en el sistema y el tiempo de producción se vea considerablemente reducido.

Y finalmente, en cuanto al papel de operaciones, Devops busca constantemente la eliminación del mismo, buscando tener sistemas heredados más fuertes y llegando a la disminución de operación o su eliminación por completo.

*FUENTE*
[Global Partner](https://globbpartner.com/cinco-tendencias-devops-3232/)

## 3. En la actualidad existen diferentes aproximaciones a DevOps como puede ser SysOps, BizDevOps, DataOps, GitOps etc. Podrías explicar en qué consisten estas y otras aproximaciones, y en qué se diferencian de DevOps?

### SysOps

Sysops se enfoca en ITIL, el cual normalmente tiende a favorecer una tasa de cambio de código y un despliegue coherente. Se basa en proporcionar un desarrollo continúo de servicios sin riesgos y no ser tan flexible al cambio; este se interesa en hacer que los procesos del sistema funcionen sin problemas en toda la empresa.

*FUENTE*
[Intellipaat](https://intellipaat.com/blog/sysops-vs-devops-whats-difference/)

SysOps es el término antiguo utilizado para referirse a la persona que administra un "sistema informático".

*FUENTE*
[Quora](https://www.quora.com/What-is-difference-between-DevOps-SysOps-and-WebOps)

### BizDevOps

Esta metodología se basa en la gestión y desarrollo de servicios, desde el punto de vista de la disponibilidad del usuario final, buscando mejorar la satisfacción del usuario final
Los tres grandes pilares en los que se enfoca esta metodología son:

BIZ: Necesidades de negocio. 

DEV: Entrada de los cambios, desarrollo. 

OPS: Entrada de incidencias y problemas.

*FUENTE*
[VASS](https://www.vass.es/tecnologia/bizdevops/)

### DataOps

Se refiere a la nueva forma de administrar datos, que busca la comunicación e integración de datos, equipos y sistemas que antes de encontraban aislados entre sí.

*FUENTE*
[DiscoverTheNew](https://discoverthenew.ituser.es/predictive-analytics/2018/03/que-es-dataops-y-como-puede-ofrecer-mejores-analisis-funcionales)

Es una metodología enfocada en la automatización del proceso de analítica de Macrodatos, con el fin de mejorar la calidad y reducir el tiempo de desarrollo de soluciones de analísis de datos. 

*FUENTE* 
[Wikipedia](https://es.wikipedia.org/wiki/DataOps)

### GitOps

Busca usar herramientas donde se facilite el uso de Git como fuente y de esta manera lograr hacer configuraciones por hechos y no por instrucciones, con esto se busca simplificar la operatividad de todo el sistema así como también su recuperabilidad, predecibilidad y observabilidad.

*FUENTE* 
[Meetup](https://www.meetup.com/es-ES/10x-Buenos-Aires/events/254479546/)

Otras

### ServiceOps

Se refiere a un grupo creado por DeutscheBank el cual se encargaba de la fase de despliegues, enfocado en realizar los despliegues de las operaciones, fue un grupo creado con el fin de quitarle la responsabilidad a los desarrolladores de realizar despliegues.

### WebOps
Otro término que se dedica a la administración de aplicaciones web. Como DevOps se ocupa también en gran parte de las aplicaciones web, son prácticamente lo mismo.
