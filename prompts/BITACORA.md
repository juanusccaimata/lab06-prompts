Markdown
# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.

Herramienta de IA usada: ChatGPT

## Ejercicio 2: Tokens y ventana de contexto
| Texto | Caracteres | Tokens |
|---|---|---|
| Los estudiantes programan en Java. | 35 | 8 |
| The students program in Java. | 30 | 7 |
| desafortunadamente | 18 | 4 |

### Que paso con el contexto:
* **Mismo chat:** ChatGPT respondio bien porque recordo los datos que le acaba de dar en la misma charla.
* **Chat nuevo:** No supo responder porque al abrir un chat nuevo la memoria empieza desde cero.

## Ejercicio 3: Temperatura
| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|---|---|---|
| 0 | 100.0% | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 65.3% | BiblioTec, BiblioTec, LibroYa, BiblioTec, BiblioTec |
| 1 | 44.5% | BiblioTec, BiblioTec, PrestaLibro, PaginaLibre, LibroYa |
| 1.8 | 32.2% | LibroYa, NubeDeTinta, BiblioTec, PrestaLibro, BiblioTec |

### Que paso con la temperatura:
* **Con temperatura baja (0):** La IA siempre elige la opcion mas probable y repetitiva.
* **Con temperatura alta (1.8):** Las probabilidades se reparten y da respuestas mas variadas.
* **Sobre nuevos nombres:** Nunca inventa un nombre fuera de la lista porque la temperatura solo cambia que tan arriesgado es al elegir entre lo que ya conoce.

## Ejercicio 4: Prompt vago vs estructurado
| Criterio | Prompt vago | Prompt estructurado |
|---|---|---|
| Menciona el objetivo del sistema | No | Si |
| Menciona a los usuarios principales | No | Si |
| Tiene exactamente 3 funcionalidades | No | Si |
| Esta en 3 parrafos | No | Si |
| Lo usaria en un informe real | No | Si |

### Comparativa:
* **Prompt vago:** Entrega un texto genérico, desordenado y sin la estructura necesaria para un trabajo formal.
* **Prompt estructurado:** Al darle un rol, objetivo y formato exacto, la IA responde con precisión directa y lista para usar.

## Ejercicio 5: Anatomia de un prompt
| Componente | Texto de mi prompt |
|---|---|
| **Rol** | Actua como desarrollador Java. |
| **Instrucción** | Crea un programa en Java para gestionar los productos de una tienda. |
| **Contexto** | Usando una clase Producto con los atributos codigo, nombre, precio y stock. |
| **Ejemplo** | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio). |
| **Formato** | Explica primero la estructura de la clase y luego presenta el codigo Java. |

### Como fue mejorando la respuesta:
* **Nivel 1:** Solo dio un "Hola Mundo".
* **Nivel 2:** Ya le dio forma de codigo mas ordenado y con buenas practicas.
* **Nivel 3:** Se enfoco de una en el tema de la tienda de abarrote.
* **Nivel 4:** Creo exactamente la clase producto con las 4 variables que le pedi.
* **Nivel 5:** Separo la explicacion del codigo y dejo los metodos limpios como en el ejemplo.

## Ejercicio 6: Del prompt basico al profesional
### Evaluacion del resultado:
* **¿Usa Java y Swing?:** Si
* **¿Pide correo y contraseña?:** Si
* **¿Explica el codigo antes o despues?:** Si
* **¿Esta ordenado en clases?:** Si
* **¿Valida los datos ingresados?:** Si

### Prompts utilizados e iteracion:

**Prompt inicial:**

Actua como desarrollador Java. Crea un ejemplo de login para una aplicacion de escritorio utilizando Swing. El usuario debe ingresar correo y contrasena. Explica brevemente el funcionamiento y presenta el codigo organizado por clases.