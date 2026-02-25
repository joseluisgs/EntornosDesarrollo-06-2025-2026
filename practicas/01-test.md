### Cuestionario de Clean Code - Documentación, Refactorización y Optimización

**1. ¿Qué es la refactorización de código?**
A) Añadir nuevas funcionalidades al código.
B) Modificar la estructura interna sin cambiar el comportamiento externo.
C) Corregir errores de compilación.
D) Eliminar comentarios del código.

**2. ¿Cuál es el principal objetivo de la refactorización?**
A) Hacer el código más rápido.
B) Mejorar la legibilidad y mantenibilidad del código.
C) Reducir el tamaño del archivo.
D) Eliminar los tests unitarios.

**3. ¿Qué son los "Code Smells" o "malos olores" del código?**
A) Errores de compilación que huelen mal.
B) Indicadores de posibles problemas en el diseño del código.
C) Comentarios obsoletos en el código.
D) Nombres de variables incorrectos.

**4. ¿Cuál de los siguientes es un Code Smell típico?**
A) Código bien indentado.
B) Métodos muy largos.
C) Nombres descriptivos.
D) Clases pequeñas con una responsabilidad.

**5. ¿Qué es un "Magic Number" en programación?**
A) Un número que aparece en un comentario.
B) Un valor literal sin explicación alguna en el código.
C) Una constante bien nombrada.
D) Un número que se usa en un test.

**6. ¿Cómo se deben tratar los "Magic Numbers"?**
A) Dejarlos como están para mantener el código simple.
B) Sustituirlos por constantes con nombres descriptivos.
C) Comentarlos para explicar qué significan.
D) Eliminarlos del código.

**7. ¿Cuál es una buena práctica para nombrar variables en C#?**
A) Usar letras simples como a, b, c.
B) Usar nombres como variable1, variable2.
C) Usar camelCase para variables locales.
D) Usar PascalCase para variables locales.

**8. ¿Qué convención de nombres se usa para las clases en C#?**
A) camelCase
B) snake_case
C) PascalCase
D) kebab-case

**9. ¿Qué convención de nombres se usa para las propiedades en C#?**
A) camelCase
B) PascalCase
C) snake_case
D) UPPER_CASE

**10. ¿Qué es la documentación XMLDoc en C#?**
A) Un formato para crear páginas web.
B) Un sistema de comentarios especial que genera documentación.
C) Un tipo de archivo XML.
D) Un lenguaje de programación.

**11. ¿Qué tag XMLDoc se usa para describir el propósito de un método?**
A) `<param>`
B) `<returns>`
C) `<summary>`
D) `<exception>`

**12. ¿Qué tag XMLDoc se usa para documentar los parámetros de un método?**
A) `<summary>`
B) `<param>`
C) `<returns>`
D) `<value>`

**13. ¿Qué tag XMLDoc se usa para documentar el valor de retorno de un método?**
A) `<summary>`
B) `<param>`
C) `<returns>`
D) `<exception>`

**14. ¿Qué tag XMLDoc se usa para documentar las excepciones que puede lanzar un método?**
A) `<summary>`
B) `<param>`
C) `<returns>`
D) `<exception>`

**15. ¿Qué significa documentar el código "durante" el desarrollo?**
A) Escribir la documentación después de terminar el proyecto.
B) Escribir la documentación mientras se escribe el código.
C) No escribir documentación.
D) Escribir documentación solo cuando hay errores.

**16. ¿Qué es Markdown?**
A) Un lenguaje de programación.
B) Un lenguaje de marcado ligero para documentación.
C) Un sistema de base de datos.
D) Un framework de desarrollo web.

**17. ¿Cuál de las siguientes NO es una ventaja de Markdown?**
A) Legibilidad del código fuente.
B) Conversión a HTML, PDF y otros formatos.
C) Requiere un compilador especial.
D) Funciona con control de versiones.

**18. ¿Qué símbolo se usa para crear un encabezado nivel 1 en Markdown?**
A) ##
B) ###
C) #
D) =====

**19. ¿Cómo se crea una lista con viñetas en Markdown?**
A) 1. 2. 3.
B) - Elemento
C) * Elemento
D) B y C son correctas

**20. ¿Qué es la optimización de código?**
A) Añadir más código para mejorar el programa.
B) Mejorar el rendimiento sin cambiar el comportamiento.
C) Eliminar todos los comentarios.
D) Renombrar todas las variables.

**21. ¿Cuál es la regla de oro antes de optimizar código?**
A) Optimizar siempre, sin importar nada.
B) Tener tests que pasen antes y después de la optimización.
C) Eliminar todos los comentarios.
D) Cambiar el nombre de todas las variables.

**22. ¿Qué es Pattern Matching en C#?**
A) Una técnica para buscar patrones en texto.
B) Una forma de evaluar expresiones contra patrones específicos.
C) Un tipo de expresión regular.
D) Un algoritmo de ordenación.

**23. ¿Cuál es la ventaja de usar LINQ frente a bucles tradicionales?**
A) El código es más lento.
B) El código es más declarativo y legible.
C) Requiere más líneas de código.
D) No funciona con colecciones.

**24. ¿Qué es mejor para buscar un elemento en una colección grande?**
A) Un switch con muchos casos.
B) Un Dictionary para búsqueda O(1).
C) Un bucle for tradicional.
D) Un if anidado.

**25. ¿Qué son las clases estáticas en C#?**
A) Clases que no se pueden instanciar y no tienen estado.
B) Clases que heredan de otras.
C) Clases con métodos privados.
D) Clases que solo tienen propiedades.

**26. ¿Qué son los Enums con métodos de extensión en C#?**
A) Enums que ya no se usan.
B) Enums que tienen métodos propios asociados.
C) Enums con errores de compilación.
D) Enums que contienen clases.

**27. ¿Qué significa DRY en Clean Code?**
A) Don't Repeat Yourself.
B) Do Repeat Yourself.
C) Data Repeat Yaml.
D) Don't Refactor Yet.

**28. ¿Qué significa KISS en Clean Code?**
A) Keep It Simple, Stupid.
B) Keep It Secure, Safe.
C) Know It Stay Safe.
D) Keep It Standard, Simple.

**29. ¿Cuál de los siguientes NO es un principio SOLID?**
A) Single Responsibility.
B) Open/Closed.
C) Lazy Loading.
D) Interface Segregation.

**30. ¿Qué significa "Single Responsibility" (S de SOLID)?**
A) Cada clase debe tener una única responsabilidad.
B) Los métodos deben ser muy largos.
C) Las variables deben ser globales.
D) Solo debe haber una clase por archivo.

**31. ¿Qué es un "código duplicado"?**
A) Código que está en un archivo de backup.
B) Código idéntico o muy similar en varios lugares.
C) Código que no compila.
D) Código que está comentado.

**32. ¿Cómo se resuelve el código duplicado?**
A) Dejándolo como está.
B) Extraer el código común a un método.
C) Añadir más código duplicado.
D) Eliminar el código.

**33. ¿Qué es el principio de "una responsabilidad" en métodos?**
A) Un método debe hacer varias cosas a la vez.
B) Un método debe hacer solo una cosa y hacerla bien.
C) Los métodos deben ser lo más largos posibles.
D) Los métodos no necesitan documentarse.

**34. ¿Cuál es el orden correcto de una clase en C# (convenciones)?**
A) Campos, Propiedades, Constructores, Métodos.
B) Using statements, Namespace, Clase.
C) Métodos, Propiedades, Campos, Constructores.
D) No hay un orden específico.

**35. ¿Qué son las constantes en C#?**
A) Variables que pueden cambiar de valor.
B) Valores inmutables con nombre descriptivo.
C) Variables locales.
D) Parámetros de métodos.

**36. ¿Qué diferencia hay entre refactorización y optimización?**
A) Son lo mismo.
B) Refactorización = estructura, Optimización = rendimiento.
C) Refactorización = velocidad, Optimización = legibilidad.
D) No están relacionadas.

**37. ¿Qué herramienta de JetBrains permite hacer refactorizaciones automáticamente?**
A) IntelliJ IDEA
B) Rider
C) PyCharm
D) WebStorm

**38. ¿Cuál es el atajo en Rider para la refactorización "Rename"?**
A) Ctrl+R
B) Shift+F6
C) Ctrl+Alt+M
D) F5

**39. ¿Cuál es el atajo en Rider para "Extract Method"?**
A) Ctrl+R
B) Shift+F6
C) Ctrl+Alt+M
D) F6

**40. ¿Qué refactorización permite cambiar el nombre de cualquier símbolo en toda la solución?**
A) Move
B) Rename
C) Extract Method
D) Inline

**41. ¿Qué es una refactorización "in-place"?**
A) Una refactorización que no requiere IDE.
B) Una refactorización aplicada directamente en el editor.
C) Una refactorización que elimina código.
D) Una refactorización que solo funciona en una línea.

**42. ¿Qué son los "flujos paralelos" en un diagrama de actividad?**
A) Flechas que van hacia atrás.
B) Operaciones que se ejecutan simultáneamente.
C) Líneas horizontales.
D) Comentarios en el código.

**43. ¿Qué son las particiones o "swimlanes" en un diagrama de actividad?**
A) Tipos de datos.
B) Carriles que dividen por responsabilidades.
C) Nodos de decisión.
D) Variables locales.

**44. ¿Qué herramienta genera documentación desde Markdown automáticamente?**
A) Docsify
B) Photoshop
C) Excel
D) Word

**45. ¿Qué es StringBuilder y cuándo debe usarse?**
A) Una clase para leer archivos.
B) Una clase eficiente para concatenar muchas cadenas.
C) Un tipo de dato.
D) Un IDE.

**46. ¿Qué es el operador null-coalescing (??) en C#?**
A) Un operador para sumar nulls.
B) Un operador que proporciona un valor por defecto si es null.
C) Un operador de comparación.
D) Un operador de asignación.

**47. ¿Qué son las propiedades auto-implementadas en C#?**
A) Propiedades que no tienen getter/setter.
B) Propiedades que generan un campo automáticamente.
C) Propiedades obsoletas.
D) Propiedades estáticas.

**48. ¿Qué significa "código expresivo"?**
A) Código que speak en voz alta.
B) Código que se lee como prosa y se explica solo.
C) Código muy complejo.
D) Código con muchos comentarios.

**49. ¿Cuál es el enfoque correcto ante código que necesita ser refactorizado?**
A) Reescribirlo desde cero siempre.
B) Hacer pequeños cambios incrementales y verificar con tests.
C) No tocarlo si funciona.
D) Añadir más código encima.

**50. ¿Por qué es importante mantener la documentación actualizada?**
A) No es importante.
B) Para que los desarrolladores entiendan el código y no introduzcan errores.
C) Solo importa al principio del proyecto.
D) La documentación obsoleta es peor que no tener documentación.
