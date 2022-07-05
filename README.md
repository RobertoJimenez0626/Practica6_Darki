### 【Requisito previo】
#### 〔Azure Sponsorships〕
Antes de empezar con cualquiera de las practicas mostradas por su servidor, es necesario verificar si contamos con la posibilidad de emplear las herramientas de Microsoft Azure.
Para ello, es necesario realizar la siguiente verificación:

1. Entrar al siguiente enlace: [**Microsoft Azure Sponsorships**](https://www.microsoftazuresponsorships.com/)
![Azure Sponsorships](https://i.imgur.com/OxY5WPf.png)
> Página de Microsoft Azure Sponsorships.

2. Después, hacemos clic en el apartado de **Check Your Balance**
![Azure Balance](https://i.imgur.com/e65k3qe.png)
> Balance de Azure.

3. En este apartado podemos **verificar** los siguientes datos:
- **Total de Crédito** de Azure: En este caso, tenemos un **total** de $100 USD.
- **Usado**: Crédito que hemos usado o **gastado** a lo largo del tiempo.
- **Restante**: Crédito con el cual **contamos** para su respectivo uso en la plataforma.
- **Suscripciones**: Cantidad de suscripciones que se encuentran **Activas** y que estan ligadas a nuestro Saldo/Crédito de Azure Sponsorships.
- Y por ultimo, la **dirección de correo** de nuestra cuenta de Azure.

Con esto, ya podemos saber si disponemos del uso de los servicios de Azure. Para una mayor comprobación, se puede intentar crear cualquier recurso de Azure, y si no existe restricción de algún tipo significaría que vamos por buen camino.

Una vez dicho todo esto, podemos empezar.

---

**Tabla de Contenidos**

 - [Introducción a Azure Functions](#introducción-a-azure-functions)
    - [Escenarios](#escenarios)
    - [Lenguajes admitidos](#lenguajes-admitidos)
    - [Detalles de la compatibilidad con lenguajes](#detalles-de-la-compatibilidad-con-lenguajes)
- [Practica 6](#practica-6-implementación-y-uso-de-azure-funtions)
    - []()
    - []()
    - []()
    - []()
    - []()

-------

# 【Introducción a Azure Functions】

![](https://www.vectorlogo.zone/logos/azurefunctions/azurefunctions-ar21.png)

*Azure Functions* es una solución sin servidor que le permite escribir menos código, mantener menos infraestructura y ahorrar costos. En lugar de preocuparse por implementar y mantener servidores, la infraestructura en la nube proporciona todos los recursos actualizados necesarios para mantener las aplicaciones en ejecución.

Usted se centra en los fragmentos de código que más le importan y Azure Functions se ocupa del resto.

A menudo, se crean sistemas para que reaccionen a una serie de eventos críticos. Independientemente de si compila una API web, responde a cambios en una base de datos, procesa flujos de datos de IoT o incluso si administra colas de mensajes, cada aplicación necesita una forma de ejecutar código a medida que se producen estos eventos.

Para ello, Azure Functions ofrece "proceso a petición" de dos maneras significativas.

En primer lugar, Azure Functions permite implementar la lógica del sistema en bloques de código fácilmente disponibles. Estos bloques de código se denominan "funciones". Se pueden ejecutar distintas funciones cada vez que necesite responder a eventos críticos.

En segundo lugar, a medida que aumentan las solicitudes, Azure Functions satisface la demanda con tantos recursos e instancias de función como se necesiten, pero solo cuando sea necesario. A medida que disminuyan las solicitudes, todos los recursos e instancias de la aplicación adicionales se descartarán automáticamente.

### 〔Escenarios〕

En muchos casos, una función se integra con una matriz de servicios en la nube para proporcionar implementaciones con numerosas características.

A continuación se incluye un conjunto de escenarios habituales de Azure Functions, si bien no están reflejadas todas las posibilidades.

| Si desea... | entonces... |
|:------------- | :------------- |
|**Crear una API web** | Implemente un punto de conexión para las aplicaciones web mediante el desencadenador HTTP|
|**Procesar cargas de archivos** | Ejecute código cuando se cargue o se cambie un archivo en el almacenamiento de blobs|
|**Compilar un flujo de trabajo sin servidor** | Encadene una serie de funciones mediante Durable Functions|
|**Responder a cambios en una base de datos** | Ejecute una lógica personalizada cuando se cree o actualice un documento en Cosmos DB|
|**Ejecutar tareas programadas** | Ejecución de código en intervalos de tiempo predefinidos|
|**Crear sistemas de cola de mensajes confiables** | Procese colas de mensajes mediante Queue Storage, Service Bus o Event Hubs|
|**Analizar flujos de datos de IoT** | Recopile y procese datos de dispositivos IoT|
|**Procesar datos en tiempo real** | Use Functions y SignalR para responder a los datos en el momento|

Al compilar las funciones, dispone de las siguientes opciones y recursos:

- Usar el lenguaje que prefiera: escriba funciones en C#, Java, JavaScript, PowerShell o Python, o use un controlador personalizado para usar prácticamente cualquier otro lenguaje.

- Automatizar la implementación: desde un enfoque basado en herramientas hasta el uso de canalizaciones externas, dispone de una enorme cantidad de opciones de implementación.

- Solucionar problemas de una función: use herramientas de supervisión y estrategias de pruebas para obtener información sobre las aplicaciones.

- Opciones de precios flexibles: con el plan de Consumo, solo pagará mientras se ejecuten las funciones, mientras que los planes Premium y App Service ofrecen características para necesidades especializadas.


### 〔Lenguajes admitidos〕

Hay dos niveles de compatibilidad:

- **Disponibilidad general (GA)** : totalmente compatible y aprobado para su uso en producción.
- **Versión preliminar**: todavía no se admite, pero se espera que llegue al estado de disponibilidad general en el futuro.

Hay disponibles varias versiones del entorno en tiempo de ejecución de Azure Functions. En la tabla siguiente se indica qué lenguajes se admiten en cada versión del sistema de tiempo de ejecución.

| Lenguaje | 1.x | 2.x | 3.x | 4.x |
| :------- | :-- | :-- | :-- | :-- |
| **C#** | Disponibilidad general (.NET Framework 4.8) | Disponibilidad general (.NET Core 2.11) | Disponibilidad general (.NET Core 3.1). Disponibilidad general (.NET 5.0) | Disponibilidad general (.NET 6.0). Versión preliminar (.NET Framework 4.8) |
| **JavaScript** | Disponibilidad general (Node.js 6) | Disponibilidad general (Node.js 10 & 8) | Disponibilidad general (Node.js 14, 12, & 10) | Disponibilidad general (Node.js 14). Disponibilidad general (Node.js 16) |
| **F#** | Disponibilidad general (.NET Framework 4.8) | Disponibilidad general (.NET Core 2.1) | Disponibilidad general (.NET Core 3.1) | Disponibilidad general (.NET 6.0) |
| **Java** | N/D | Disponibilidad general (Java 8) | Disponibilidad general (Java 11 & 8) | Disponibilidad general (Java 11 & 8) |
| **PowerShell** | N/D | Disponibilidad general (PowerShell Core 6) | Disponibilidad general (PowerShell 7.0 & Core 6) | Disponibilidad general (PowerShell 7.0). Versión preliminar (PowerShell 7.2) |
| **Python** | N/D | Disponibilidad general (Python 3.7 & 3.6) | Disponibilidad general (Python 3.9, 3.8, 3.7 & 3.6) | GA (Python 3.9, 3.8, 3.7) |
| **TypeScript&sup2;** | N/D | GA | Disponibilidad general | GA |

### 〔Detalles de la compatibilidad con lenguajes〕

En la tabla siguiente se muestran los idiomas admitidos por Functions que se pueden ejecutar en Linux o Windows. También indica si el idioma admite la edición en Azure Portal. El idioma se basa en la opción **Pila del entorno en tiempo de ejecución** que elija al crear la aplicación de función en Azure Portal. Esto es igual que la opción `--worker-runtime` cuando se usa el comando `func init` en Azure Functions Core Tools.

| Lenguaje | Pila en tiempo de ejecución | Linux | Windows | Edición en el portal |
| :------- | :-- | :--: | :--: | :--: |
| Biblioteca de clases C# | .NET | ✓ | ✓ |  |
| Script de C# | .NET | ✓ | ✓ | ✓ |
| JavaScript | Node.js | ✓ | ✓ | ✓ |
| Python | Python | ✓ |  | ✓ |
| Java | Java | ✓ | ✓ |  |
| PowerShell | PowerShell Core | ✓ | ✓ | ✓ |
| TypeScript | Node.js | ✓ | ✓ |  |
| Go/Rust/otro | Controladores personalizados | ✓ | ✓ |  |

--------------

# 【Practica 6: Implementación y uso de Azure Funtions】
### 〔〕

![]()

### 〔〕

![]()

### 〔〕

![]()

### 〔〕

![]()