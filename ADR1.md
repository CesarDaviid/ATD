# Get Logs for Mail Server Customer Support System v1

La organizacion tiene la necesidad de consultar logs a los servidores de correo de una forma segura y de rapida implementacion, estos servidores son en plataforma Linux.


## Decision


![image](https://github.com/CesarDaviid/ATD/assets/4713423/8b0707da-de97-4808-aa3a-dd2e7f53c9b2)

### Tipo Conexion:

Se determino que el tipo de acceso se realizaria de forma directa a los servidores mediante ssh.

### Forma de Consulta

Se debe realizar consultas por consola para realizar busquedas por la utilidad grep para buscar un patrón específico en un archivo o grupo de archivos



## Status = Depreciado




## Contexto

El sistema Customer Support Portal (CSP) es un proveedor de servicios de hosting para emails, en el cual los usuarios pueden alquilar servidores de email. Cuando un usuario tiene un problema (por ej., no recibe emails), puede llamar al área de Atención al Cliente para que lo ayude a diagnosticar el problema. Uno de los puntos de venta de la empresa son los Representantes de Servicio al Cliente (CSR), que son personal técnico abocado a realizar soporte al cliente.

Se debe habilitar una forma de poder consultar estos logs para que los CSR puedan solucionar o atender los diferentes issues reportados por los clientes.


## Consecuencias
### Positivas

* Rapida Implementacion
* Las consultas se realizan en tiempo real.
* El tiempo de respuesta de la utilidad grep en grandes archivos es muy buena.

### Negativas

* El equipo CSR tendra accesos a los servidores de Correo
* El equipo CSR tendra acceso a la informacion confidencial de los servidores de correo.
