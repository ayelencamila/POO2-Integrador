# Documento de Diseño y Planificación

---

## Trabajo en equipo

> **Descripción de las tareas asignadas a cada miembro:**
>
> - **Leonardelli Lisandro:**
> - **Castillo Mazo Andrés Luciano:**
> - **Amarilla Espindola Aldo Wilfrido:**
> - **Gimenez Iván Benjamin:**
> - **Sosa Ayelén:**
> - **Albornoz Franco:**

---

## Diseño OO

> ### Diagrama UML de clases
>
> ![Diagrama UML de clases](../../out/docs/Iteracion1/DiagramaClases_V1/iteracion1_VentaProductosLinea.png)
>
> Descripción del diagrama UML y los componentes incluidos en esta iteración.

---

## Wireframe y caso de uso

> ### Bocetos de la interfaz de usuario
>
> ![Wireframe](ruta/al/wireframe.png)
>
> ### Casos de uso
>
> **Caso de uso 1:** Visualización de productos ecológicos disponibles.
>
> - **Actores:** Cliente
> - **Curso típico de eventos:**
>   1. El cliente accede a la página principal o sección de productos ecológicos.
>   2. El sistema muestra una lista de productos ecológicos disponibles, incluyendo nombre, precio y breve descripción.
>   3. El cliente puede navegar por la lista y seleccionar productos para ver más detalles.
> - **Curso alternativo:**
>   1. Si no hay productos disponibles, el sistema muestra un mensaje indicando que no hay productos en stock.
>
> ---
>
> **Caso de uso 2:** Búsqueda de productos por categoría o palabras clave.
>
> - **Actores:** Cliente
> - **Curso típico de eventos:**
>   1. El cliente accede a la barra de búsqueda en la página principal o en la sección de productos.
>   2. El cliente ingresa una categoría o palabras clave en la barra de búsqueda.
>   3. El sistema filtra los productos y muestra los resultados relevantes.
>   4. El cliente puede navegar por los resultados y seleccionar productos para ver más detalles.
> - **Curso alternativo:**
>   1. Si no se encuentran productos que coincidan con la búsqueda, el sistema sugiere productos relacionados.
>
> ---
>
> **Caso de uso 3:** Visualización del precio total incluyendo descuentos.
>
> - **Actores:** Cliente
> - **Curso típico de eventos:**
>   1. El cliente agrega productos al carrito de compras.
>   2. El sistema calcula el precio total de la compra, incluyendo todos los descuentos aplicables.
>   3. El sistema muestra el precio total y los descuentos aplicados en el resumen del carrito.
>   4. El cliente puede proceder al pago con el precio total actualizado.
> - **Curso alternativo:**
>   1. Si el cliente elimina productos del carrito, el sistema actualiza dinámicamente el precio total y los descuentos aplicados.
>
> ---
>
> **Caso de uso 4:** Selección de método de pago.
>
> - **Actores:** Cliente
> - **Curso típico de eventos:**
>   1. El cliente procede al pago desde el carrito de compras.
>   2. El sistema muestra las opciones de métodos de pago disponibles (tarjeta de crédito, tarjeta de débito, transferencia bancaria).
>   3. El cliente selecciona un método de pago.
>   4. El sistema procesa el pago de forma segura y notifica al cliente del éxito o fallo del procesamiento.
> - **Curso alternativo:**
>   1. Si el procesamiento del pago falla, el sistema muestra un mensaje de error y permite al cliente intentar nuevamente o seleccionar otro método de pago.
>
> ---
>
> **Caso de uso 5:** Agregar nuevos productos al inventario.
>
> - **Actores:** Administrador
> - **Curso típico de eventos:**
>   1. El administrador accede al panel de administración.
>   2. El administrador selecciona la opción para agregar un nuevo producto.
>   3. El administrador ingresa el nombre, descripción, precio y cantidad del producto.
>   4. El sistema verifica que el precio sea un valor positivo y la cantidad un número entero.
>   5. El sistema guarda el nuevo producto en el inventario y lo muestra en la lista de productos disponibles.
> - **Curso alternativo:**
>   1. Si los datos ingresados no son válidos, el sistema muestra un mensaje de error y solicita al administrador corregir los datos.
>
> ---
>
> **Caso de uso 6:** Modificación del inventario tras una venta.
>
> - **Actores:** Administrador
> - **Curso típico de eventos:**
>   1. El cliente completa una compra.
>   2. El sistema reduce automáticamente la cantidad de productos en el inventario según la venta realizada.
>   3. El sistema alerta al administrador si la cantidad de un producto es menor que el umbral de inventario mínimo.
>   4. El administrador puede ver un historial de ajustes de inventario para cada producto.
> - **Curso alternativo:**
>   1. Si el inventario no se puede actualizar automáticamente, el sistema notifica al administrador para que realice la actualización manualmente.
>
> ---
>
> **Caso de uso 7:** Aplicación de descuentos automáticos en productos.
>
> - **Actores:** Administrador
> - **Curso típico de eventos:**
>   1. El administrador accede al panel de administración.
>   2. El administrador selecciona la opción para configurar descuentos.
>   3. El administrador ingresa los detalles del descuento (porcentaje o valor fijo, condiciones de aplicación).
>   4. El sistema aplica automáticamente los descuentos configurados a los productos o paquetes elegidos.
>   5. Los productos con descuento muestran el precio original tachado y el precio con descuento visible.
> - **Curso alternativo:**
>   1. Si las condiciones del descuento no se cumplen, el sistema no aplica el descuento y notifica al administrador.
>
> ---
>
> **Caso de uso 8:** Confirmación de compra por correo electrónico.
>
> - **Actores:** Cliente
> - **Curso típico de eventos:**
>   1. El cliente completa una compra.
>   2. El sistema envía automáticamente un correo de confirmación al cliente.
>   3. El correo incluye los detalles del pedido (productos, cantidades, precios, y total).
>   4. El cliente recibe el correo de confirmación inmediatamente después de finalizar la compra.
> - **Curso alternativo:**
>   1. Si el correo no se puede enviar, el sistema notifica al cliente y al administrador para que tomen las medidas necesarias.
>
> ---
>
> **Caso de uso 9:** Acceso al historial de ventas y detalles de pedidos.
>
> - **Actores:** Administrador
> - **Curso típico de eventos:**
>   1. El administrador accede al panel de administración.
>   2. El administrador selecciona la opción para ver el historial de ventas.
>   3. El sistema muestra un historial de ventas ordenado por fecha, con filtros de búsqueda.
>   4. Cada venta en el historial incluye detalles como productos vendidos, cantidades, precios, y método de pago.
>   5. El administrador puede exportar el historial de ventas a un formato común, como CSV o Excel.
> - **Curso alternativo:**
>   1. Si no hay ventas registradas, el sistema muestra un mensaje indicando que no hay ventas en el historial.
>
> ---
>
> **Caso de uso 10:** Recomendaciones de productos basadas en compras anteriores.
>
> - **Actores:** Cliente
> - **Curso típico de eventos:**
>   1. El cliente accede a su cuenta o a la página principal.
>   2. El sistema muestra al menos tres productos recomendados en base a las compras anteriores del cliente.
>   3. Las recomendaciones se actualizan dinámicamente después de cada compra para reflejar las preferencias del cliente.
>   4. El cliente puede navegar por las recomendaciones y seleccionar productos para ver más detalles.
> - **Curso alternativo:**
>   1. Si el cliente no tiene compras anteriores, el sistema muestra productos populares o destacados como recomendaciones.

---

## Backlog de iteración

> ### Historias de usuario a implementar
>
> 1. **Historia de usuario 1:** Como cliente, quiero ver una lista de productos ecológicos disponibles para escoger los productos que quiero comprar.
> 2. **Historia de usuario 2:** Como cliente, quiero poder buscar productos por categoría o palabras clave para encontrar rápidamente los productos que necesito.
> 3. **Historia de usuario 3:** Como cliente, quiero ver el precio total de mi compra incluyendo descuentos aplicables para saber cuánto pagaré antes de realizar el pedido.
> 4. **Historia de usuario 4:** Como cliente, quiero seleccionar diferentes métodos de pago como tarjeta o transferencia bancaria para pagar de forma conveniente y segura.
> 5. **Historia de usuario 5:** Como administrador, quiero agregar nuevos productos al inventario con su descripción, precio y cantidad para mantener el catálogo actualizado.
> 6. **Historia de usuario 6:** Como administrador, quiero modificar la cantidad de productos en el inventario cuando se realiza una venta para mantener un control preciso del inventario.
> 7. **Historia de usuario 7:** Como administrador, quiero aplicar descuentos automáticos a ciertos productos o paquetes para ofrecer promociones atractivas a los clientes.
> 8. **Historia de usuario 8:** Como cliente, quiero recibir una confirmación de compra por correo electrónico con el detalle de mi pedido para tener un comprobante y detalle de mi compra.
> 9. **Historia de usuario 9:** Como administrador, quiero acceder a un historial de ventas y detalles de cada pedido para analizar el rendimiento de las ventas y tomar decisiones informadas.
> 10. **Historia de usuario 10:** Como cliente, quiero ver recomendaciones de productos basadas en mis compras anteriores para descubrir productos que puedan interesarme y mejorar mi experiencia de compra.

---

## Tareas

> ### Lista de tareas específicas
>
> - **Tarea 1:** Descripción de la tarea.
> - **Tarea 2:** Descripción de la tarea.
> - **Tarea 3:** Descripción de la tarea.
> - **Tarea 4:** Descripción de la tarea.

---
