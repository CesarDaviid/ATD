
# Get Logs for Mail Server Customer Support System v2

La organizacion tiene la necesidad de consultar logs a los servidores de correo de una forma segura y de rapida implementacion, estos servidores son en plataforma Linux.


## Decision

![image](https://github.com/CesarDaviid/ATD/assets/4713423/eae6513a-78ba-4e69-8dbc-a3494c8f0752)

### Tipo Conexion:

Se determino que el producto logstash recopile, parse y transforme los logs,los cuales seran enviados a Elasticsearch que es un motor de búsqueda y analítica distribuido, gratuito y abierto para todos los tipos de datos, incluidos textuales, numéricos, geoespaciales, estructurados y no estructurados y con Kibana que es una aplicación de frontend gratuita y abierta que se encuentra sobre el Elastic Stack y proporciona capacidades de visualización de datos y de búsqueda para los datos indexados en Elasticsearch se podran visualizar todos los logs.

### Forma de Consulta

Se debe realizar consultas por consola para realizar busquedas por la utilidad grep para buscar un patrón específico en un archivo o grupo de archivos



## Status = Aprovado




## Context

El sistema Customer Support Portal (CSP) es un proveedor de servicios de hosting para emails, en el cual los usuarios pueden alquilar servidores de email. Cuando un usuario tiene un problema (por ej., no recibe emails), puede llamar al área de Atención al Cliente para que lo ayude a diagnosticar el problema. Uno de los puntos de venta de la empresa son los Representantes de Servicio al Cliente (CSR), que son personal técnico abocado a realizar soporte al cliente.

Se debe habilitar una forma de poder consultar estos logs para que los CSR puedan solucionar o atender los diferentes issues reportados por los clientes.
Web / http No agrega valor a la solución
Motor DB SQL Sin afectacioón de los servicios transaccionales


## Consequences
### Positive

*Performance
las consultas se realizan en tiempo real. 
el tiempo de respuesta de la utilidad grep en grandes archivos es muy buena. 
*Seguridad
*Usabilidad
*Escalabilidad


### Negatives

El equipo CSR tendra accesos a los servidores de Correo
El equipo CSR 
*Performance
*Seguridad se debe aumentar los protocolos web
*Usabilidad no tiene afectación 
*Escalabilidad
  Dependencia a modor de DB
  Asociado a la demanda del negocio
