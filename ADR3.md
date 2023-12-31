# Get Logs for Mail Server Customer Support System v2

La organizacion tiene la necesidad de consultar logs a los servidores de correo de una forma segura y de rapida implementacion, estos servidores son en plataforma Linux.


## Decision

![image](https://github.com/CesarDaviid/ATD/assets/4713423/77453c86-a4bd-4b2c-9b64-5197b1495666)

### Tipo Conexion:

Se determino que el producto logstash recopile, parse y transforme los logs,los cuales seran enviados a Elasticsearch que es un motor de búsqueda y analítica distribuido, gratuito y abierto para todos los tipos de datos, incluidos textuales, numéricos, geoespaciales, estructurados y no estructurados y con Kibana que es una aplicación de frontend gratuita y abierta que se encuentra sobre el Elastic Stack y proporciona capacidades de visualización de datos y de búsqueda para los datos indexados en Elasticsearch se podran visualizar todos los logs.

### Forma de Consulta

Kibana permitira visualizar y explorar datos que se encuentran indexados en Elasticsearch.

![image](https://github.com/CesarDaviid/ATD/assets/4713423/0ba28ea4-95c5-4c3e-97dc-5e76cf0c9396)



## Status = To Be




## Context

El sistema Customer Support Portal (CSP) es un proveedor de servicios de hosting para emails, en el cual los usuarios pueden alquilar servidores de email. Cuando un usuario tiene un problema (por ej., no recibe emails), puede llamar al área de Atención al Cliente para que lo ayude a diagnosticar el problema. Uno de los puntos de venta de la empresa son los Representantes de Servicio al Cliente (CSR), que son personal técnico abocado a realizar soporte al cliente.

Se debe habilitar una forma de poder consultar estos logs para que los CSR puedan solucionar o atender los diferentes issues reportados por los clientes.


## Consequences
### Positive

* Performance
   * Alto rendimiento, todos los componentes son nativos en nube y proporcianan de forma nativa alta escalabilidad
* Seguridad
    * Todos los productos tienen multiples forma de abordad la seguridad de la informacion en transito y en reposo.
* Usabilidad
    * Los dashboard de Kibana son altamente configurables y se pueden personalizar a las necesidades puntuales del area.
* Escalabilidad
    * Al existir unn recopilacion, parseo y transformacion de los logs unica en cada servidor su escalabilidad es bastante alta.


### Negatives

* los costos de implementacion son muchos mas altos que una solucion on-premise.
