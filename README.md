## Módulo de Gestión de Pedidos -Restaurante
Este módulo forma parte del sistema de gestión de pedidos para un restaurante, diseñado para manejar eficientemente el ciclo de vida de los pedidos, desde su creación hasta su cierre. A continuación, se presenta una justificación detallada del diseño del diagrama UML y cómo satisface los requerimientos funcionales del sistema.
### Justificación del Diseño UML
#### 1. Gestión de Pedidos Asociados a Mesas o Reservaciones
El sistema permite la creación de nuevos pedidos asociados a una mesa o una reservación, reflejado en la clase `Pedido`, que está relacionada tanto con `Mesa` como con `Reservacion`. Esto garantiza que el sistema maneje adecuadamente la asignación de pedidos a mesas disponibles o previamente reservadas.
#### 2. Adición y Modificación de Productos en Pedidos
La relación entre `Pedido` y `ProductoPedido` permite agregar productos a un pedido, especificando cantidad y detalles. Además, el sistema permite modificar los productos en el pedido a través de métodos como `modificarProducto()` y `eliminarProducto()`. Esto asegura que los pedidos puedan ser ajustados antes de ser servidos.
#### 3. Cambio de Estado del Pedido
El `Estado` de los pedidos puede cambiarse mediante el uso de la enumeración Estado, que incluye los valores `PENDIENTE, EN_PREPARACION`, `SERVIDO` y `PAGADO`. El método modificarEstado() de la clase Pedido permite al personal del restaurante actualizar el estado conforme el pedido avanza en el proceso.
#### 4. Visualización de Pedidos en Cocina
La clase `Cocina` incluye un método `visualizarPedido()`, que permite al personal de cocina ver los detalles de los pedidos, como la mesa, los productos solicitados y su estado actual. Esto facilita la gestión eficiente del flujo de trabajo en la cocina.
#### 5. Historial de Pedidos
La clase `HistorialPedido` permite registrar y gestionar el historial de pedidos
realizados. A través de los métodos `agregarPedido()` y `generarHistorial()`, se puede almacenar la información de cada pedido, incluyendo fecha, mesa, cliente y monto total. Este registro permite consultas futuras y análisis h## Módulo de Gestión de Pedidos -Restaurante
Este módulo forma parte del sistema de gestión de pedidos para un restaurante, diseñado para manejar eficientemente el ciclo de vida de los pedidos, desde su creación hasta su cierre. A continuación, se presenta una justificación detallada del diseño del diagrama UML y cómo satisface los requerimientos funcionales del sistema.
### Justificación del Diseño UML
#### 1. Gestión de Pedidos Asociados a Mesas o Reservaciones
El sistema permite la creación de nuevos pedidos asociados a una mesa o una reservación, reflejado en la clase `Pedido`, que está relacionada tanto con `Mesa` como con `Reservacion`. Esto garantiza que el sistema maneje adecuadamente la asignación de pedidos a mesas disponibles o previamente reservadas.
#### 2. Adición y Modificación de Productos en Pedidos
La relación entre `Pedido` y `ProductoPedido` permite agregar productos a un pedido, especificando cantidad y detalles. Además, el sistema permite modificar los productos en el pedido a través de métodos como `modificarProducto()` y `eliminarProducto()`. Esto asegura que los pedidos puedan ser ajustados antes de ser servidos.
#### 3. Cambio de Estado del Pedido
El `Estado` de los pedidos puede cambiarse mediante el uso de la enumeración Estado, que incluye los valores `PENDIENTE, EN_PREPARACION`, `SERVIDO` y `PAGADO`. El método `modificarEstado()` de la clase Pedido permite al personal del restaurante actualizar el estado conforme el pedido avanza en el proceso.
#### 4. Visualización de Pedidos en Cocina
La clase `Cocina` incluye un método `visualizarPedido()`, que permite al personal de cocina ver los detalles de los pedidos, como la mesa, los productos solicitados y su estado actual. Esto facilita la gestión eficiente del flujo de trabajo en la cocina.
#### 5. Historial de Pedidos
La clase `HistorialPedido` permite registrar y gestionar el historial de pedidos
realizados. A través de los métodos `agregarPedido()` y `generarHistorial()`, se puede almacenar la información de cada pedido, incluyendo fecha, mesa, cliente y monto total. Este registro permite consultas futuras y análisis históricos.
#### 6. Generación de Resumen del Pedido
El sistema incluye un método en la clase `Pedido` llamado `generarResumen()`, que permite generar un resumen detallado del pedido para ser entregado a la cocina, mejorando la eficiencia en la preparación de los productos.
### Relaciones Utilizadas en el Diagrama UML
- Asociación: Entre` Pedido`, `Mesa`, `Reservacion`, y `ProductoPedido`, para reflejar la vinculación funcional entre estos elementos.
-  Agregación: Entre `Pedido` y `ProductoPedido`, para denotar que un pedido está compuesto por múltiples productos, pero estos pueden existir independientemente.
-  Dependencia: Entre `Cocina` y `Pedido`, ya que la cocina depende de la información del pedido para preparar los productos.istóricos.
#### 6. Generación de Resumen del Pedido
El sistema incluye un método en la clase `Pedido` llamado `generarResumen()`, que permite generar un resumen detallado del pedido para ser entregado a la cocina, mejorando la eficiencia en la preparación de los productos.
### Relaciones Utilizadas en el Diagrama UML
- Asociación: Entre` Pedido`, `Mesa`, `Reservacion`, y `ProductoPedido`, para reflejar la vinculación funcional entre estos elementos.
-  Agregación: Entre `Pedido` y `ProductoPedido`, para denotar que un pedido está compuesto por múltiples productos, pero estos pueden existir independientemente.
-  Dependencia: Entre `Cocina` y `Pedido`, ya que la cocina depende de la información del pedido para preparar los productos.
