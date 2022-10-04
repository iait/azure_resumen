# Informática en la nube 

La informática en la nube es la prestación de servicios informáticos a través de Internet, lo que permite una innovación más rápida, recursos flexibles y precios regulables.

## Modelos de nubes

### Nube privada (*on-premise*)

**Mayor control**

* La organización crea un entorno de nube en su centro de datos (*data center*).
* La organización es responsable de operar los servicios que brinda.
* No proporciona acceso a usuarios ajenos a la organización.
* Debe adquirirse hardware para el inicio y el mantenimiento.
* La organización tiene control total de los recursos y la seguridad.
* La organización es responsable del mantenimiento y las actualizaciones del hardware.

### Nube pública

**Mayor agilidad**

* Es propiedad del Cloud Service provider o proveedor de hosting.
* Proporciona recursos y servicios a múltiples organizaciones y usuarios.
* Se accede a través de una conexión de red segura (generalmente a través de Internet).
* No hay gastos de capital para escalar verticalmente.
* Las aplicaciones pueden aprovisionarse y desaprovisionarse rápidamente.
* La organización solo paga por lo que usa.

### Nube híbrida

**Mayor flexibilidad**

Combinación de nubes públicas y privadas para permitir que las aplicaciones se ejecuten en la ubicación más adecuada.

## Gastos de capital (CapEx)

* El gasto inicial de dinero en infraestructura física.
* Los bienes derivados de CapEx tienen un valor que se reduce con el tiempo.

## Gastos de operación (OpEx)

* Gasto en productos y servicios según sea necesario, pago por uso.
* Gastos que generan una factura periódica por el uso.

## Modelo basado en el consumo

Los proveedores de servicios en la nube operan en un **modelo basado en el consumo**, lo que significa que los usuarios finales solo pagan por los recursos que usan.

* Se proporcionan precios para recursos y servicios individuales.
* La facturación se basa en el uso real.
* Mejor predicción de costos.

## Beneficios en la nube

* **Alta disponibilidad**. Tener los recursos funcionando la mayor cantidad de tiempo posible y con el menor número de fallos posibles.
* **Escalabilidad**. Escalado horizontal (agregar más recursos, por ejemplo VMs) y vertical (aumentar/reducir la capacidad de un recurso existente, por ejemplo más RAM).
* **Confiabilidad**. Mecanismos para evitar desastres. Aunque algún componente falle poder seguir operando.
* **Predicción** (del rendimiento y costo).
* **Seguridad**. Prevención de ataques. Protección de datos.
* **Gobernanza**. Garantizar que todos los recursos cumplan con estándares establecidos.
* **Facilidad de uso**. Se puede administrar mediante diferentes herramientas como el portal web, cliente de línea de comandos (CLI), etc.
* **Elasticidad**. Capacidad de incrementar o disminuir la cantidad de recursos demandados de forma automática.

## Tipos de servicios

### Infraestructura como Servicio (IaaS)

* Más flexible
* Permite configurar y administrar el hardware de la aplicación.

El proveedor proporciona:
* Servidores y almacenamiento
* Firewalls y seguridad de red
* Planta física o edificio del centro de datos (*data center*)

### Plataforma como Servicio (PaaS)

Además de lo ofrecido por IaaS el proveedor proporciona:
* Sistema Operativo, con actualizaciones y mantenimiento
* Herramientas de desarrollo, administración de bases de datos, análisis de datos

### Software como Servicio (SaaS)

* Los usuarios utilizan directamente un software desarrollado por el proveedor.
* La organización solo controla los datos y los accesos.

## Región

* Las regiones se componen de uno o más centros de datos próximos.
* Proporcionan flexibilidad y capacidad de adaptación para reducir la latencia de los clientes.

## Pares de regiones

* Deben estar separadas al menos 500km entre sí.
* Replicación automática para algunos servicios.
* Se prioriza la recuperación de una región en caso de interrupción.
* Las actualizaciones se implementan secuencialmente para minimizar el tiempo de inactividad.

## Zonas de disponibilidad

* Proporcionan protección contra el tiempo de inactividad debido a errores del centro de datos.
* Centros de datos separados físicamente dentro de la misma región.
* Cada centro tiene sus propias redes, alimentación, refrigeración, etc.
* Se interconectan mediante redes privadas de fibra óptica.

## Regiones soberanas

Cumplen con necesidades de seguridad y cumplimiento de agencias federales, gobiernos estatales y locales.
* Instancias separada de Azure.
* Físicamente aisladas.
* Accesible solo para personal autorizado.

## Azure Active Directory (AAD)

Es el servicio de administración de identidad y acceso basado en la nube de Azure.

**Tenant**: es la representación de la organización después de crear un compromiso con Azure.

Proporciona:
* Autenticación
* Inicio de sesión único (SSO)
* Administración de aplicaciones
* Negocio a negocio (B2B)
* Servicios de identidad de negocio a cliente (B2C)
* Administración de dispositivos

## Suscripciones

Proporciona acceso autenticado y autorizado a las cuentas de Azure.
* Facturación independiente
* Control de acceso

## Grupos de administración (*management groups*)

* Cada tenant tiene su **tenant root group**.
* Los grupos de administración pueden incluir varias suscripciones Azure.

## Recursos

VMs, almacenamientos, virtual networks, bases de datos, functions, etc.

* Los recursos pueden ser agrupados en grupos de recursos.
* Los recursos solo pueden estar presentes en un único grupo.
* Los recursos de un grupo pueden estar en diferentes regiones.
* Los grupos de recursos pueden contener distintos tipos de recursos.
* La mayoría de los recursos se pueden mover a otros grupos.

## Servicios computacionales (*Azure Compute*)

Son por ejemplo: VMs, App Services, Container Instances, Azure Kubernetes, Azure Virtual Desktop.

* **Máquinas Virtuales**. Pueden ser Windows o Linux. Útiles para migraciones mediante *lift-and-shift* a la nube.
* **Virtual Desktop**. Proporciona una experiencia de escritorio Windows basada en la nube. Aplicaciones dedicadas para conectarse o accesible mediante cualquier navegador web.
* **Contenedores**. Entorno ligero adecuado para la ejecución de microservicios. Diseñado para escalabilidad y resistencia a través de orquestación (kubernetes). Las aplicaciones se empaquetan en contenedores que se encuentran sobre el SO host. Múltiples contenedores pueden estar en el mismo SO.

### Maquinas virtuales

Conjuntos de Disponibilidad (*availability sets*)

* Para evitar puntos de fallo.
* Para que se actualicen en secuencia.
* Se pueden incluir balanceadores de carga.
* Fault domain (diferentes racks).
* Update domain.

Conjuntos de Escalabilidad (*scale sets*)

* Escalable horizontalmente.
* Escale verticalmente.

### Azure Virtual Desktop

* Virtualización de aplicaciones y escritorios que se ejecuta en la nube.
* Permite crear un entorno de virtualización de escritorio completo sin tener que ejecutar servidores de puerta de enlace adicionales.

### Azure container services

* Entorno virtualizado ligero que no requiere administración del SO y puede responder a los cambios bajo demanda.
* Azure Container Instances.
* Azure Kubernetes Service.

### Azure functions

* Serverless.
* No eres responsable del manejo de la infraestructura para manejar tu código.
* Código basado en eventos que ejecuta tu servicio y no la infraestructura subyacente.
* Existen diferentes formas de desencadenar el código que vive en la nube.

### Azure App Services

Plataforma para crear implementar y escalar rápidamente aplicaciones web y APIs.

## Servicios de redes de Azure

* Virtual Private Network Gateway (VPN). Tunneling a través de Internet. Se usa para enviar tráfico cifrado entre una Azure Virtual Network (VNet) y una ubicación local a través de Internet público.
* Azure Express Route. No van por el Internet público. Extiende las redes locales de Azure a través de una conexión privada que facilita un proveedor de conexión.

### Azure DNS

* Permite administrar recursos externos y de Azure con un único servidor de nombres de dominio.
* En redes virtuales se permite usar nombres de dominio privados y totalmente personalizables.

## Almacenamiento

* Acceso frecuente. Optimizado para almacenar datos a los que se accede con frecuencia.
* Acceso esporádico. Optimizado para almacenar datos a los que se accede con poca frecuencia y se almacenan durante al menos 30 días.
* Archivo. Optimizado para almacenar datos a los que rara vez se accede y se almacenan durante al menos 180 días con requisitos de latencia flexibles.

### Cuentas de almacenamiento (*storage accounts*)

* Debe poseer un nombre único
* Duradero y altamente disponible (gracias a la redundancia)

Redundancia:
* LRS. Tres veces en el mismo *data center*.
* ZRS. Tres veces en las zonas de disponibilidad de la región primaria.
* GRS. Tanto LRS para la región principal como para la secundaria. Se puede habilitar la lectura en la región secundaria.
* GZRS. Replicar como ZRS en la región principal y LRS en la región secundaria.

Tipos de almacenamiento:
* Blob Storage. Sin estructura jerárquica de directorios.
* Disk Storage
* Azure Files

### Aplicaciones externas para el manejo de almacenamiento

* AzCopy. Utilidad de línea de comandos. Copia de blobs o archivos desde y hacia la cuenta de almacenamiento de Azure. Sincronización unidireccional.
* Azure Storage Explorer. Interfaz gráfica similar al explorador de Windows. Compatible con Windows, MacOS y Linux. Usa AzCopy internamente.
* Azure File Sync. Sincronización bidireccional.

### Azure Data Box

* Se utiliza para transferir terabytes de datos desde y hacia Azure de manera rápida, confiable y barata, por medio del transporte de un dispositivo físico con una capacidad máxima de 80 TB.
* Ideal para migraciones, actualizaciones periódicas de más de 40 TB.

### Azure Migrate

Sirve para evaluar y planificar una migración a Azure.

## Identidad

* Autenticación. Identificar a la persona o servicio que intenta acceder a un recurso.
* Autorización. Determinar si la persona o servicio tiene acceso al recurso.

### Mutli-Factor Authentication

Proporciona seguridad adicional para sus identidades al requerir dos o más elementos para la autenticación completa.
* Algo que sabe. Contraseña.
* Algo que posee. Envío de Token virtual.
* Algo que es. Datos biométricos.

### Acceso condicional

Permitir o denegar acceso a partir de señales:
* Usuario o grupo
* Ubicación de la IP
* Dispositivo
* Aplicativo
* Detección de riesgos

### Control de acceso basado en roles (RBAC)

* Administración de acceso específico.
* Otorgar la cantidad mínima de acceso requerido.

### Defensa en profundidad

Proporciona múltiples niveles de protección:
* Data
* Application
* Compute
* Red
* Perímetro
* Identidad y acceso
* Seguridad física

### Zero trust

Verifica cada solicitud como si proviniera de una fuente no conocida.

## Microsoft Defender for Cloud

* Proporciona recomendaciones de seguridad
* Siempre está evaluando los entornos
* Analiza e identifica posibles ataques
* Detecta y bloquea malware

## Administración de costos

Factores que afectan los costos:
1. Tipo de recurso. Varia según capacidades, región y configuración.
2. Consumo. Modelo pago por el uso. Se puede reducir costos con un compromiso de utilización de recursos (reserva).
3. Mantenimiento. Apagar máquinas virtuales que no se usan. Asegurarse de no conservar recursos que no se necesitan.
4. Geografía. Ubicación de los recursos.
5. Tráfico de red. Afectado por la geografía. Generalmente el tráfico entrante es gratuito pero el saliente tiene costo.
6. Suscripción. Por ejemplo existe la suscripción de prueba gratuita.

## Azure Marketplace

Permite probar aplicaciones y servicios de proveedores externos validados por Azure.

## Calculadora de precios

* Ayuda a estimar el costo de los productos de Azure.
* No implica una cotización.

## Calculadora de costo total de propiedad

Compara on-prem vs Azure

## Azure cost management

* Creación de informes de facturación
* Enriquecimiento de datos
* Fijar presupuestos máximos
* Alerta si se exceden los límites de costos
* Recomendaciones sobre los costos

## Etiquetas (Tags)

* Proporciona metadatos para los recursos
* Organizar lógicamente los recursos
* Consiste en nombre-valor
* Útil para acumular información de facturación

## Gobernanza y cumplimiento

### Azure blueprints (planos)

* Permite que los equipos de desarrollo puedan construir y poner en marcha nuevos entornos rápidamente. 
* Implementar servicios o entornos de manera rápida y eficiente.
* Permite normalizar una implementación.
* Permite definir configuraciones repetibles.
* Plantillas (templates).

### Azure Policy

* Nos permite cumplir con reglas que tu organización establezca.
* Evalúa los recursos y resalta los que no cumplan con los requisitos o evita que se creen.
* Proporciona gobernanza y consistencia de recursos con cumplimiento normativo, seguridad, costos y administración.
* Por ejemplo, se puede crear una regla para que las nuevas VM se creen en una región específica.
* Iniciativa: grupo de reglas que se administra como una unidad.

### Bloqueos de recursos

* Proteja recursos de Azure de la eliminación o la modificación accidental.
* Administra bloqueos a nivel de suscripción, grupo de recursos o recursos individuales.
* Los bloqueos son hereditarios.

### Portal de confianza de servicios

Muestra los estándares y certificaciones que posee Azure tanto centrales como regionales.
Por ejemplo, certificaciones ISO.

## Herramientas de administración e implementación

* Azure Portal
* Azure Mobile App
* Azure PowerShell
* Azure Cloud Shell
* Interfaz de la línea de comandos (CLI)

## Azure Resource Manager (ARM)

Proporciona una capa de administración que le permite crear, actualizar y eliminar recursos en su suscripción Azure. Toda las herramientas anteriores realizan su administración a través de este componente.

### Plantillas de ARM

JSON que se pueden usar para crear e implementar la infraestructura de Azure sin tener que escribir comandos.
* Sintaxis declarativa
* Resultados repetibles 
* Orquestación 
* Archivos modulares
* Validación incorporada
* Código exportable

### Azure Arc

* Útil para entornos híbridos y multi-nubes
* Administrar todo el entorno de forma conjunta

## Herramientas de supervisión

* **Azure Monitor**. Para maximizar la disponibilidad y rendimiento de aplicaciones y servicios ya que recopila, analiza y actúa desde entornos nube y locales. Proporciona insights, logs y alertas inteligentes.
* **Azure Advisor**. Analiza los recursos y hace recomendaciones basadas en las mejores prácticas.
* **Azure Service Health**. Te mantiene informado del estado general de Azure y de los servicios o recursos que estén afectados. Es la salud del proveedor Azure. Por ejemplo, te va a avisar si se cae un data center o si hay alguna baja planificada por actualización u otro motivo.

## Examen

* 40-60 preguntas.
* No todas tienen el mismo puntaje.
* No se penaliza por respuestas incorrectas.
* 65 minutos: 45 para responder y 20 para otras actividades.
* Presentarse 30 minutos antes.
* Resultado inmediato.
* Preguntas pueden ser de selección múltiple, creación de listas, drag and drop, etc.
* Se presenta un caso de estudio del cual se deben responder varias preguntas.
