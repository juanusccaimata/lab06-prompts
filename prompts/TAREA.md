# Tarea: Mi prompt profesional

**Estudiante:** Juan Jose Uscca Imata
**Herramienta de IA usada:** ChatGPT

## Funcionalidad elegida

La funcionalidad elegida es el **registro de productos** para una aplicación llamada **TiendaTec**, desarrollada en Java Swing.

El objetivo es crear un formulario que permita ingresar los datos de un producto y validar la información antes de registrarla.

## Version 1: prompt basico

```text
Crea un programa en Java para registrar productos de una tienda.
```

### Qué cambié

En esta primera versión hice un prompt corto y general. Solo indiqué que necesitaba un programa para registrar productos.

### Por qué

Quería ver qué respuesta me daba la IA sin darle muchos detalles.

### Qué mejoró en la respuesta

La respuesta fue muy general. No tenía una interfaz gráfica ni indicaba los campos que debía tener el producto.

## Version 2

```text
Actúa como desarrollador Java Senior. Diseña un formulario en Java Swing para registrar productos en la aplicación TiendaTec. El formulario debe permitir ingresar el código, nombre, precio y stock del producto. Separa el código en las clases Producto, ProductoDAO y ProductoFrame.
```

### Qué cambié

Agregué el rol de desarrollador Java y también indiqué que quería usar Java Swing. Además puse el nombre de la aplicación y algunos datos del producto.

### Por qué

La primera versión no tenía suficiente información. Quería que la IA entendiera mejor qué estaba haciendo.

### Qué mejoró en la respuesta

La respuesta fue más específica. Ya tenía una interfaz gráfica y una separación de las clases.

## Version 3: prompt final

```text
Actúa como desarrollador Java Senior con experiencia en Java Swing.

Diseña un formulario gráfico para registrar productos en la aplicación TiendaTec. El formulario debe solicitar código, nombre, precio, stock y categoría mediante un JComboBox.

Utiliza este estilo para el método de registro:

public boolean registrarProducto(Producto p)

Presenta la solución separada en tres clases: Producto.java, ProductoDAO.java y ProductoFrame.java.

La clase Producto debe contener los datos del producto. La clase ProductoDAO debe encargarse del registro y ProductoFrame debe contener la interfaz gráfica.

No utilices librerías externas. Valida que el precio y el stock sean mayores que cero usando JOptionPane y actualiza la tabla de productos después de guardar.
```

### Qué cambié

Agregué los datos que debe tener el formulario, las tres clases y las condiciones que debe cumplir el programa.

### Por qué

Quería que la IA tuviera más información para poder darme una respuesta más cercana a lo que necesito.

### Qué mejoró en la respuesta

La respuesta fue más completa y tuvo las validaciones que pedí. También siguió la estructura de las tres clases.

## Componentes del prompt final

| Componente      | Texto de mi prompt                                                                                  |
| --------------- | --------------------------------------------------------------------------------------------------- |
| **Rol**         | Actúa como desarrollador Java Senior con experiencia en Java Swing.                                 |
| **Instrucción** | Diseña un formulario gráfico para registrar productos en la aplicación TiendaTec.                   |
| **Contexto**    | El formulario debe solicitar código, nombre, precio, stock y categoría.                             |
| **Ejemplo**     | `public boolean registrarProducto(Producto p)`                                                      |
| **Formato**     | Presenta la solución separada en tres clases: Producto.java, ProductoDAO.java y ProductoFrame.java. |

## Evaluacion del resultado

| Criterio                     | ¿Cumple? | Observación                                                      |
| ---------------------------- | -------- | ---------------------------------------------------------------- |
| Usa Java Swing               | Sí       | Se indicó Java Swing en el prompt.                               |
| Tiene los datos del producto | Sí       | Incluye código, nombre, precio, stock y categoría.               |
| Está separado en tres clases | Sí       | Se solicitaron las clases Producto, ProductoDAO y ProductoFrame. |
| Tiene una restricción        | Sí       | Se indicó que no se deben usar librerías externas.               |

## Errores que evite

### Ser demasiado general

En la primera versión solo indiqué que quería un programa para registrar productos. Después fui agregando más información sobre la aplicación y los datos necesarios.

### No indicar el formato

En las primeras versiones no indiqué cómo quería organizar el código. En la versión final pedí que estuviera separado en tres clases: Producto, ProductoDAO y ProductoFrame.
