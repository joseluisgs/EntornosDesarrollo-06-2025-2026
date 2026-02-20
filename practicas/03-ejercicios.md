- [Parte 1: Ejercicios de Documentación XMLDoc](#parte-1-ejercicios-de-documentación-xmldoc)
- [Parte 2: Ejercicios de Markdown](#parte-2-ejercicios-de-markdown)
- [Parte 3: Ejercicios de Refactorización](#parte-3-ejercicios-de-refactorización)
- [Parte 4: Ejercicios de Optimización](#parte-4-ejercicios-de-optimización)
- [Parte 5: Ejercicios de Clean Code](#parte-5-ejercicios-de-clean-code)

---

# Parte 1: Ejercicios de Documentación XMLDoc

*Instrucciones:* Para los siguientes fragmentos de código, añade la documentación XMLDoc completa usando los tags apropiados.

### Ejercicio 1: Interfaz de Servicio

```csharp
public interface IGestorProductos
{
    List<Producto> ObtenerTodos();
    Producto ObtenerPorId(int id);
    void Guardar(Producto producto);
    bool Eliminar(int id);
    int ContarProductos();
}
```

### Ejercicio 2: Clase de Excepciones Personalizada

```csharp
public class ExcepcionUsuario : Exception
{
    public ExcepcionUsuario(string mensaje) : base(mensaje) { }
    public class UsuarioNoEncontrado : ExcepcionUsuario { }
    public class DatosInvalidos : ExcepcionUsuario { }
    public class UsuarioDuplicado : ExcepcionUsuario { }
}
```

### Ejercicio 3: Método con Parámetros y Excepciones

```csharp
public decimal CalcularDescuento(decimal precioBase, string tipoCliente, int cantidad)
{
    if (precioBase <= 0)
        throw new ArgumentException("El precio debe ser mayor que cero");
    
    // Cálculo del descuento...
    return precioFinal;
}
```

---

# Parte 2: Ejercicios de Markdown

*Instrucciones:* Crea documentación técnica en Markdown para los siguientes escenarios.

### Ejercicio 4: README.md para un Proyecto

Crea un README.md completo para una biblioteca de clases llamada "CalculadoraFinanceira" que incluya:
- Descripción del proyecto
- Cómo instalarla (NuGet)
- Ejemplo de uso básico
- Métodos disponibles en una tabla
- Licencia

### Ejercicio 5: Documentación de API

Crea la documentación en Markdown para un endpoint de API REST que gestione usuarios:
- Descripción del endpoint
- Parámetros
- Respuestas posibles (200, 400, 404, 500)
- Ejemplo de solicitud y respuesta JSON

### Ejercicio 6: Changelog

Crea un archivo CHANGELOG.md siguiendo el formato Keep a Changelog para una aplicación que pasa de la versión 1.0.0 a 1.1.0.

---

# Parte 3: Ejercicios de Refactorización

*Instrucciones:* Identifica los code smells y refactoriza el código.

### Ejercicio 7: Código Duplicado

**Código original:**
```csharp
public void GuardarEstudiante(Estudiante e)
{
    if (e == null) throw new ArgumentNullException();
    ValidarEstudiante(e);
    _context.Estudiantes.Add(e);
    _context.SaveChanges();
    Log("Estudiante guardado");
}

public void GuardarProfesor(Profesor p)
{
    if (p == null) throw new ArgumentNullException();
    ValidarProfesor(p);
    _context.Profesores.Add(p);
    _context.SaveChanges();
    Log("Profesor guardado");
}
```

**Refactorízalo** para eliminar la duplicación.

### Ejercicio 8: Método Largo

**Código original:**
```csharp
public void ProcesarPedido(Pedido pedido)
{
    // Validar cliente
    if (pedido.Cliente == null)
    {
        _logger.LogError("Cliente nulo");
        return;
    }
    
    // Validar dirección
    if (string.IsNullOrEmpty(pedido.Direccion))
    {
        _logger.LogError("Dirección vacía");
        return;
    }
    
    // Calcular totales
    decimal subtotal = 0;
    foreach (var item in pedido.Items)
    {
        subtotal += item.Cantidad * item.Precio;
    }
    
    // Aplicar descuento
    decimal descuento = 0;
    if (pedido.Cliente.TieneDescuento)
    {
        descuento = subtotal * 0.10m;
    }
    
    // Calcular IVA
    decimal iva = (subtotal - descuento) * 0.21m;
    decimal total = subtotal - descuento + iva;
    
    // Guardar pedido
    _repository.Guardar(pedido);
    
    // Enviar email
    _emailService.Enviar(pedido.Cliente.Email, "Pedido procesado");
}
```

**Refactorízalo** en métodos pequeños.

### Ejercicio 9: Magic Numbers

**Código original:**
```csharp
public class Calculadora
{
    public decimal CalcularImpuesto(decimal monto)
    {
        return monto * 0.21m; // Magic number!
    }
    
    public bool EsMayorDeEdad(int edad)
    {
        return edad >= 18;
    }
    
    public int ObtenerDiasPlazo(string tipo)
    {
        switch (tipo)
        {
            case "normal": return 30;
            case "urgente": return 7;
            case "express": return 1;
            default: return 30;
        }
    }
}
```

**Refactorízalo** usando constantes y enums.

### Ejercicio 10: Nombres Pobres

**Código original:**
```csharp
public class c
{
    public int p(int a, int b)
    {
        var x = a + b;
        var y = a - b;
        return x * y;
    }
}
```

**Refactorízalo** con nombres descriptivos.

---

# Parte 4: Ejercicios de Optimización

*Instrucciones:* Optimiza el código manteniendo su comportamiento.

### Ejercicio 11: Switch vs Pattern Matching

**Código original:**
```csharp
public string GetTipo(Usuario u)
{
    switch (u.Tipo)
    {
        case 1: return "Admin";
        case 2: return "Gestor";
        case 3: return "Usuario";
        case 4: return "Invitado";
        default: return "Desconocido";
    }
}
```

**Optimízalo** usando Pattern Matching.

### Ejercicio 12: Bucles vs LINQ

**Código original:**
```csharp
public List<int> GetPares(List<int> numeros)
{
    var resultado = new List<int>();
    for (int i = 0; i < numeros.Count; i++)
    {
        if (numeros[i] % 2 == 0)
        {
            resultado.Add(numeros[i]);
        }
    }
    return resultado;
}
```

**Optimízalo** usando LINQ.

### Ejercicio 13: Dictionary vs Switch

**Código original:**
```csharp
public int GetPrecioEnvio(string pais)
{
    switch (pais.ToLower())
    {
        case "espana": return 5;
        case "francia": return 8;
        case "alemania": return 10;
        case "italia": return 7;
        case "portugal": return 4;
        case "reino unidos": return 12;
        case "belgica": return 9;
        case "paises bajos": return 11;
        default: return 15;
    }
}
```

**Optimízalo** usando Dictionary.

### Ejercicio 14: Null Checking

**Código original:**
```csharp
public string GetNombre(Usuario u)
{
    if (u == null)
    {
        return "Anónimo";
    }
    
    if (u.Nombre == null)
    {
        return "Sin nombre";
    }
    
    return u.Nombre;
}
```

**Optimízalo** usando Null Coalescing Operator.

### Ejercicio 15: Interpolación de Strings

**Código original:**
```csharp
var mensaje = "El usuario " + usuario.Nombre + " con ID " + usuario.Id + " ha realizado " + 
              pedido.Cantidad + " compras por un total de " + pedido.Total + " euros.";
```

**Optimízalo** usando interpolación de strings.

---

# Parte 5: Ejercicios de Clean Code

*Instrucciones:* Aplica los principios de Clean Code.

### Ejercicio 16: Principios SOLID

Analiza el siguiente código y explica qué principios SOLID está violando:

```csharp
public class Gestor : IDisposable
{
    private SqlConnection _conn;
    private FileWriter _log;
    private EmailSender _email;
    
    public void ProcesarTodo(string datos)
    {
        // Conexión a BD
        _conn = new SqlConnection("connstring");
        _conn.Open();
        
        // Lógica de negocio
        var resultado = Procesar(datos);
        
        // Logging
        _log = new FileWriter("log.txt");
        _log.WriteLine(resultado);
        
        // Enviar email
        _email = new EmailSender();
        _email.Enviar("admin@empresa.com", resultado);
        
        // Y mucho más...
    }
    
    private string Procesar(string d) { /* ... */ return ""; }
    
    public void Dispose() { /* cleanup */ }
}
```

### Ejercicio 17: Estructura de Clase

Organiza el siguiente código siguiendo las convenciones de C#:

```csharp
using System;
using System.Collections.Generic;

namespace MiApp.Models
{
    public class Producto
    {
        public int Id { get; set; }
        public string nombre { get; set; }
        private decimal _precio;
        
        public void setPrecio(decimal p) { _precio = p; }
        public decimal getPrecio() { return _precio; }
        
        private string _categoria;
        
        public string CATEGORIA { get { return _categoria; } set { _categoria = value; } }
    }
}
```

### Ejercicio 18: Crea una Clase Bien Estructurada

Crea una clase "CalculadoraEstadistica" siguiendo todos los principios de Clean Code aprendidos:
- Nombres descriptivos
- Métodos pequeños
- Documentación XMLDoc
- Sin magic numbers
- Una responsabilidad clara
- Propiedades auto-implementadas

La clase debe poder:
- Calcular media de una lista de números
- Calcular mediana
- Calcular desviación estándar

### Ejercicio 19: Mejora el Código

Mejora el siguiente código aplicando todos los conceptos de Clean Code:

```csharp
public static class Utils
{
    public static object Get(object o, string tipo)
    {
        if (tipo == "int")
            return Convert.ToInt32(o);
        else if (tipo == "string")
            return o.ToString();
        else if (tipo == "decimal")
            return Convert.ToDecimal(o);
        else if (tipo == "date")
            return DateTime.Parse(o.ToString());
        else
            return null;
    }
}
```

### Ejercicio 20: Crea Documentación Completa

Para la clase del Ejercicio 18, crea:
1. Documentación XMLDoc completa
2. Un README.md en Markdown con ejemplos de uso
3. Un diagrama de clases en Mermaid

---

> **Nota del Profesor:** Estos ejercicios practican los conceptos vistos en la teoría. Recordad que la práctica hace al maestro. Intentad hacer los ejercicios primero sin mirar las soluciones y luego comparad.
