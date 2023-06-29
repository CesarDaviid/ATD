
# Get Logs for Mail Server Customer Support System v2

La organizacion tiene la necesidad de consultar logs a los servidores de correo de una forma segura y de rapida implementacion, estos servidores son en plataforma Linux.


## Decision


![image](https://github.com/CesarDaviid/ATD/assets/4713423/97e34820-0ea8-425f-882b-6a0683d643ab)

### Tipo Conexion:

Se determino que los servidores enviaran cada 10 minutos los logs del servidor de correo por medio del protocolo scp a un servidor central que tomara aquellos logs y los insertara en una base de datos relacional "MySQL".

### Forma de Consulta

Se podran enviar consultas a la base de datos por sql mediante una aplicacion web.



## Status = Vigente




## Context

El sistema Customer Support Portal (CSP) es un proveedor de servicios de hosting para emails, en el cual los usuarios pueden alquilar servidores de email. Cuando un usuario tiene un problema (por ej., no recibe emails), puede llamar al área de Atención al Cliente para que lo ayude a diagnosticar el problema. Uno de los puntos de venta de la empresa son los Representantes de Servicio al Cliente (CSR), que son personal técnico abocado a realizar soporte al cliente.

Se debe habilitar una forma de poder consultar estos logs para que los CSR puedan solucionar o atender los diferentes issues reportados por los clientes.
Web / http 
Motor DB SQL


## Consequences
### Positive

* Performance
Las consultas en SQL si se encuentran bien optimizadas asi mismo como su estructural relacional, los tiempos de respuesta son muy buenos.
* Seguridad
** De forma predeterminada el envio de los logs al servidor central mejora el atributo de seguridad.
** El motor de base de datos permite segmente usuarios y roles que tengan acceso a la informacion.



### Negatives

* Usabilidad
** El equipo CSR tendra que entender y realizar consultas en SQL en profundidad.
* Escalabilidad
** Dependencia del performance del motor de base de datos.
** Problemas de escabilidad al aumentar la cantidad de servidores que atiende el servicio de correos.
** Al aumentar la cantidad de logs almacenados en una bd relacional los recursos de esta base tambien deben crecer.
  
