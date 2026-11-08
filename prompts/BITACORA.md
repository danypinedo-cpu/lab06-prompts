# Bitacora de prompts
 
Laboratorio 06: Fundamentos de Ingenieria de Prompts.
 
Herramienta de IA usada: (escribe aqui cual usaste)
 
## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. | 35 | 7 |
| The students program in Java. | 30 | 6 |
| desafortunadamente | 18 | 4 |

Observacion: En mi caso, la IA guardo la conversacion, al abrir otro chat usando la misma IA me dio ma misma respuesta a la pregunta: 

**Tu aplicación se llama TiendaTec y está desarrollada utilizando Java Swing.**

## Ejercicio 3: Temperatura
| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 | 100%|BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 |65.3% |BiblioTec, BiblioTec, BiblioTec, BiblioTec, PrestaLibro|
| 1 |44.5% |BiblioTec, BiblioTec, PrestaLibro, BiblioTec, LibroYa |
| 1.8 |32.2% |PrestaLibro, LibroYa, LibroYa, PrestaLibro, BiblioTec |

## Ejercicio 4: Prompt vago vs estructurado
 | Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema |SI |SI |
| Menciona a los usuarios principales |NO |SI |
| Tiene exactamente 3 funcionalidades |NO |SI |
| Esta en 3 parrafos |NO |SI |
| Lo usaria en un informe real |NO |SI |

## Ejercicio 5: Anatomia de un prompt
 | Componente | Texto de mi prompt |
|------------|--------------------|
| Rol |Actua como desarrollador Java. Crea un programa en Java. |
| Instruccion |Producto con los atributos codigo, nombre, precio y stock. |
| Contexto |Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda. |
| Ejemplo |Usa este estilo para los metodos: getPrecio(), setPrecio(double precio). |
| Formato |Explica primero la estructura de la clase y luego presenta el codigo Java. |

