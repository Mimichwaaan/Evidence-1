# Evidence-1
## METODOLOGIA
*Para abordar el proyecto de la distribuidora **HALCON** será necesario una metodología que me permita gestionar eficientemente todo el desarrollo del software, sin dejar de lado ninguno de los requerimientos del cliente pues estos son primordales para el proyecto pues sin esto no tendríamos dicho proyecto. Como necesitamos construir una app con diferentes funcionalidades yo optaria por usar la metodología **SCRUM**, optaria por dicha metodología agil porque se centra el la entrega del proyecto en sprints e incremental de dicho software, con esta metodología podemos dividir el proyecto en sprits cortos que estos son generalmente de 2 a 4 semanas y en estos podremos implementar las funcionalidades prioritarias del producto, al final de cada uno de los sprints haremos un incremento del producto que podra y debera ser revisado y probado por el cliente esto para poder tener una retroalimentación temprana por parte del cliente para poder hacer los ajustes necesarios al proyecto según las necesidades del cliente*

## EXPLICACIÓN DIAGRMA BPMN
1. *CLIENTE: El proceso comienza cuando el cliente realiza la llamada para hacer un pedido a la distribuidora **HALCON***
2. *PEDIDOS: El vendedor registrara el pedido con los datos necesarios como #de factura, datos del cliente y la dirección de entrega, al hacer esto inmediatamente el pedido pasara a un estatus de **ORDENADO***
3. *En caso de tener todos los materiales el pedido pasara a un estatus de **EN RUTA**, si falta alguno o varios de los materiales se pasara al área de compras para que realice el pedido de los materiales faltantes, una vez que el pedido se encuentre completo finalmente pasara al estatus de **EN RUTA***
4. *Se asigna un transportista y se cargan los materiales para el traslado del pedido*
5. *Se hace entrega del pedido al cliente en la dirección acordada antes, el trasportista toma una foto del camión con el pedido aún cargado y la ube al sistema como evidencia de la entrega del pedido, una vez hecho esto se cambia el estatus del pedido a **Entregado**, y asi se finaliza con el proceso.*

## EXPLICACIÓN DEL DIAGRAMA DE CLASES
1. *USUARIO: Representa a los usuarios del sistema, que incluyen empleados y administradores, cada **USUARIO** tiene un nombre, email y contraseña*
2. *PEDIDO: Representa un pedido realizado por el cliente , contiene información como el número de factura, fecha, dirección de entrega, estado y notas adicionales**
3. *PRODUCTO: Representa los producos disponibles del sistema, cada producto tiene nombre, descripción y precio.*
4. *CLIENTE: Representa a los clientes de la empresa, contiene información como nombre, y los datos fiscales, en este caso el rfc*
5. *ESTADO: Define los diferentes estados que puede tener un pedido, **EN PROCESO**, **EN RUTA** y **ENTREGADO***

## EXPLICACIÓN DEL DIAGRAMA DE ACTIVIDADES
*En el diagrma se muestra la forma secuencial en la que las actividades ocrren desde que el **CLIENTE** realiza un pedido hasta que se hace la entrega del mismo y los procesos que se llevan a cabo en el intermedio de estas acciones*

## EXPLICACIÓN DEL DIAGRAMA DE CASOS
1. *CLIENTE: Puede ver el estado de sus pedidos*
2. *USUARIO: Puede iniciar sesión, registrar nuevos usuarios y asignar roles a los usuarios*
3. *ADMINISTRADOS: Tiene acceso al **DASHBOARD ADMINISTRATIVO** donde puede listar todos los pedidos, buscar pedidos por diferentes criterios, modificar o eliminar pedidos asi como ver los pedidos eliminados y poder restaurarlos de ser necesario*
4. *DEPARTAMENTOS: Aqui se incluyen los que es tomar pedidos por parte del **DEPARTAMENTO DE VENTAS**, gestionar las comprar por parte del **DEPARTAMENTO DE COMPRAS**, poder gestionar el almacen asi como preparar los pedidos por parte del **DEPARTAMENTO DE ALMACEN** y la supervision de la distribución de los pedidos por parte del **DEPARTAMENTO DE RUTAS***
