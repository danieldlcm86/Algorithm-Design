# Sistema de Control de Nómina y Envío de Productos para “Patito de Goma S.A. de C.V.”

La empresa **“Patito de Goma S.A. de C.V.”** ha experimentado un gran éxito en el último año gracias a la venta de dos de sus productos estrella: **“El Super Patito de Goma 3000”** y **“El Disfraz de Patito Programador”**. Debido a este éxito, han decidido expandir su operación contratando más personal y abriendo una nueva sucursal para satisfacer la demanda actual de sus productos.

Como parte de su expansión, la empresa ha contratado tus servicios para desarrollar un **sistema de control de pagos del personal** y el **control de producción y envío de productos**. El sistema debe garantizar el correcto manejo de las nóminas, bonos, horas extras y la logística de la distribución de productos.

### Requerimientos del Sistema

#### 1. **Módulo de Nómina** (Control del personal y pagos)
El sistema debe calcular lo siguiente para cada empleado:

- **Salario base**: Se calcula según los días trabajados en el mes (de lunes a sábado), con un salario diario de **$357**.
- **Vacaciones proporcionales**: Se calculan en función de la antigüedad del empleado. Un empleado tiene derecho a **6 días de vacaciones por año laborado**. Especificar si el cálculo se hará mensual o anual.
- **Prima dominical**: En caso de que el empleado labore en domingo, se deberá pagar un **25% adicional del salario diario**.
- **Horas extras**: Las horas extras se pagarán a razón de **$50 por hora extra**.
- **Bono de productividad**: Si el empleado trabaja más de **24 días en un mes**, recibirá un **bono de productividad del 18%** sobre su sueldo total **después de impuestos**.
- **Impuestos**: Se debe calcular una deducción de **16%** sobre el sueldo total (incluyendo salario base, horas extras y prima dominical).

El sistema debe generar los siguientes cálculos:

- **Sueldo total antes de impuestos**: De forma mensual y quincenal.
- **Sueldo total después de impuestos**: De forma mensual y quincenal.
- **Vacaciones proporcionales**: Según la antigüedad y el tiempo trabajado en el año.

##### Validaciones Importantes:
- El número de días trabajados no puede exceder los 30 o 31 días al mes.
- Se debe registrar el número de **horas extras** y días en los que el empleado haya trabajado **en domingo**.
- El cálculo del sueldo mensual debe tener en cuenta que la **jornada laboral es de lunes a sábado**.

#### 2. **Módulo de Producción y Envío** (Control de ventas y logística)

Este módulo se encargará del cálculo de los costos y logística de envío de productos. Los detalles a considerar son:

- El precio del **Super Patito de Goma 3000** es de **$84** y su peso es de **119 gramos**.
- El precio del **Disfraz de Patito Programador** es de **$43** y su peso es de **77 gramos**.
- El **peso máximo permitido** para enviar paquetes es de **1 kilogramo**.
- La paquetería ofrece un **13% de descuento** si el peso total del envío es de más de **3 kilogramos**.

El sistema debe permitir:

- **Registrar el pedido de productos**: Se debe ingresar la cantidad de productos vendidos para cada pedido (Super Patito de Goma 3000 y Disfraz de Patito Programador).
- **Calcular el costo total del pedido**: Basado en el número de productos vendidos.
- **Calcular el peso total del pedido**: Sumando el peso de todos los productos.
- **Calcular la cantidad de paquetes necesarios**: Según el peso total del pedido, asegurando que no se exceda el límite de **1 kg por paquete**.
- **Calcular el descuento de la paquetería**: Si el peso total del pedido es mayor a 3 kg, aplicar un **13% de descuento** sobre el costo total del envío.

##### Ejemplo:
Si el peso total del pedido supera los 3 kg, se debe aplicar el descuento antes de calcular el número de paquetes necesarios. El sistema debe distribuir los productos en paquetes de máximo 1 kg.

#### 3. **Requisitos Adicionales**:
- **Interfaz del sistema**: Se recomienda tener una interfaz donde el administrador pueda ingresar los datos de los empleados (días trabajados, horas extras, domingos trabajados) y otra donde se registren los pedidos de productos (cantidad de productos vendidos).
- **Reporte de nómina**: Generar un reporte mensual y quincenal para cada empleado, mostrando el desglose de salario, horas extras, prima dominical, impuestos y bono de productividad.
- **Informe de pedidos**: Mostrar un informe detallado de cada pedido, indicando el costo total, el peso total, el número de paquetes necesarios y cualquier descuento aplicado.

### Consideraciones Importantes:
- El sistema debe permitir registrar la **antigüedad** de cada empleado (fecha de ingreso) para el cálculo proporcional de vacaciones.
- Para las **horas extras** y la **prima dominical**, se deberá llevar un registro por cada empleado, donde se especifique cuántas horas trabajó fuera de horario y si laboró en domingo.
- El **descuento de la paquetería** debe aplicarse solo si el pedido total supera los 3 kg, considerando la distribución correcta de los productos en los paquetes.

### Flujo de Trabajo del Sistema:

1. **Módulo de Nómina**:
   - El empleado o administrador ingresa los datos de días trabajados, horas extras y domingos laborados.
   - El sistema calcula el salario base, prima dominical, horas extras, y aplica impuestos.
   - El sistema genera el sueldo quincenal y mensual, antes y después de impuestos.
   - Si el empleado tiene más de 24 días trabajados, el sistema aplica el bono de productividad.

2. **Módulo de Producción y Envío**:
   - El usuario ingresa el pedido de productos.
   - El sistema calcula el costo total y el peso del pedido.
   - Se determina la cantidad de paquetes necesarios para el envío.
   - Si corresponde, el sistema aplica el descuento de paquetería y genera un informe de envío.

### Desafíos Adicionales (Opcional):
- **Escalabilidad**: Considera cómo el sistema podría crecer en el futuro si se añaden más productos o más empleados.
- **Optimización de envíos**: Desarrolla un algoritmo que optimice el empaquetado para maximizar el uso del espacio disponible por paquete.
- **Manejo de base de datos**: Piensa en cómo podrías almacenar esta información de manera persistente usando una base de datos.

---
