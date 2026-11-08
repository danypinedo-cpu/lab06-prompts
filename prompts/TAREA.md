# Tarea: Mi prompt profesional
 
## Funcionalidad elegida
 Elegimos construir un gestor de productos e inventario (CRUD con control de stock) en Python.

¿Por qué? Porque es el corazón de cualquier tienda virtual: necesitas registrar productos, ver qué hay en almacén, cambiar precios, descontar existencias cuando se vende algo y avisar si queda poco stock.
## Version 1: prompt basico
 "Crea un CRUD de productos para una tienda en Python."

Qué pasó: Es como decir "hazme algo de comer". La IA te hace un script desordenado, mezclando preguntas por pantalla (input), variables sueltas y sin validar si un precio es negativo. Funciona a medias, pero no sirve para un sistema real.
## Version 2
 "Actúa como desarrollador backend. Crea clases Producto e Inventario en memoria con id, nombre, precio, stock y categoría. Valida precio > 0 y stock no negativo."

Qué mejoró: Ahora le dijimos qué plato cocinar y con qué ingredientes. La IA usó Programación Orientada a Objetos (POO) y validó precios y stock.

Qué faltaba aún: Todavía no sabía para qué proyecto era, usaba errores genéricos, no tenía ejemplos de prueba y no tenía límites técnicos claros.
## Version 3: prompt final
### Prompt utilizado
```text
Actúa como un programador de Python.

Contexto: Necesito un sistema sencillo para registrar productos de una tienda pequeña en memoria.

Instrucción: Crea una clase Producto (con id, nombre, precio, stock) y una clase Tienda que permita:
- Agregar un producto (validando que el precio sea mayor a 0).
- Listar todos los productos.
- Buscar un producto por su id.

Restricción: No uses librerías externas, solo Python básico.

Ejemplo:
tienda.agregar(Producto(1, "Cuaderno", 5.0, 10))
tienda.buscar(1) -> muestra el cuaderno.

Formato: Entrega solo el código en Python con ejemplos de prueba al final.
 ```
## Evaluacion del resultado
 ## Evaluacion del resultado

A continuación se evalúa el código obtenido con el prompt final (Versión 3) frente a los requisitos técnicos solicitados:

| Criterio de evaluación | Cumple (Sí / No) | ¿Por qué cumple? (Explicación simple) |
| :--- | :---: | :--- |
| **1. Compleitud de la funcionalidad** | **Sí** | Creó todas las operaciones del CRUD (crear, buscar, modificar stock, actualizar precio, eliminar y listar con filtros) sin dejar nada a medias. |
| **2. Respeto de restricciones técnicas** | **Sí** | Usó exclusivamente herramientas nativas de Python (`dataclasses` y `typing`), sin instalar paquetes externos raros ni ensuciar el código con `input()` o variables globales. |
| **3. Manejo de errores y casos límite** | **Sí** | Definó y disparó sus propias excepciones claras (`ProductoNoEncontradoError`, `ProductoDuplicadoError`, `ValorInvalidoError`) cuando se ingresa un precio negativo o un ID inexistente. |
| **4. Estilo y buenas prácticas (Clean Code)** | **Sí** | El código viene ordenado, con tipos de datos claros para cada variable, comentarios explicativos según el estándar formal de Google y una sección de pruebas al final. |
| **5. Ejecución autónoma directa** | **Sí** | Puedes copiar el código, pegarlo en cualquier intérprete moderno de Python 3 y corre al instante sin configuraciones extra. |
## Errores que evite
1. Ser demasiado general: Si dices "haz un inventario", la IA inventa los campos que quiere. Lo evitamos listando con nombre y tipo cada dato (id, nombre, precio, stock, categoria).

2. No definir el formato: Si no pides un formato estricto, la IA te llena la pantalla de explicaciones teóricas innecesarias. Lo evitamos exigiendo únicamente código ejecutable y tipado.