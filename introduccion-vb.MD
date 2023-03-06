# **Introducción a Visual Basic**

## **Manejo de la consola:**
Se refiere a la gestión de entradas y salidas de texto del sistema. 
### **Salida:**
Utilizamos las sentencias:
```vbnet
Console.Write(texto)
Console.WriteLine(texto)
```
La diferencia sustancial entre el *Write* y el *Writeline*  es que la primera instrucción escribe en pantalla sin agregar un salto de línea, la segunda sin embargo agrega automáticamente el salto. 
Nota: El salto de línea se puede agregar manualmente en cualquier parte de una cadena de texto con el comando **vbCrLf**

Las sentencias:
```vbnet
Console.Write("Hola Mundo")
Console.Write("Buenas tardes")
```
devuelven una salida: 
```console
Hola MundoBuenas tardes
```
Mientras que las sentencias:
```vbnet
Console.WriteLine("Hola Mundo")
Console.WriteLine("Buenas tardes")
```
devuelven la salida:
```console
Hola Mundo
Buenas tardes
```
Por lo tanto también puedo igualar la salida usando el *Write* mientras le concateno con & el **vbCrLf** 

Las sentencias:
```vbnet
Console.Write("Hola Mundo" & vbCrLf)
Console.Write("Buenas tardes" & vbCrLf)
```
devuelven una salida: 
```console
Hola Mundo
Buenas tardes
```

La sentencia: 
```vbnet
Console.Write("Hola Mundo" & vbCrLf & "Buenas tardes")
```
devuelven una salida: 
```console
Hola Mundo
Buenas tardes
```

### **Entrada:**

Existen 3 métodos para la entrada de información en consola, los cuales son: 
```vbnet
Console.Read()
Console.ReadKey()
Console.Readline()
```
* **Console.Read():** Lee el caracter presionado, si no se ha presionado nada, devuelve un -1 
* **Console.ReadKey():** Lee la tecla presionada, puede ser una tecla de caracter o bien una tecla de función. 
* **Console.ReadLine():** lee la línea completa introducida por el usuario, en caso no haya ingresado nada devuelve un <span style="color:#CF8604">**null** </span>

## **Variables:**
Una variable en programación es un espacio de memoria con un tipo de dato asignado desde su creación y que tendrá un valor que puede cambiar a lo largo de la ejecución del programa.
### **Instrucciones para crear variables:**

Toda variable inicia con la palabra reservada **Dim** seguido de un nombre el cual no debe contener espacios en blanco y caracteres especiales que no sean (_) o (-) ni iniciar con un número. El nombre puede ser cualquier cosa, sin embargo para propósitos prácticos sería bueno utilizar cualquier nombre que se relacione con el contenido de la misma. Posteriormente se le agrega la palabra reservada **As** y el Tipo de variable que va a utilizar
Ejemplo: 
```vbnet
Dim direccion As String
Dim fecha_nac As Date
Dim nombres, apellidos As String 
Dim sueldo As Double
```
### **Asignando Valores a las variables:**
Para asignar un valor a una variable se usa el signo de igualación (=) **Nota:** En algunos lenguajes de programación esto es una igualación/asignación (=) y esto es una comparación (==). Éstas son algunas de las formas en las que podemos asignar datos. 

```vbnet
Dim apellido as String
Dim salario as Double
apellido = "Juárez"
salario = 12000
Dim n1 = 7
Dim nombre = "Santiago"
Dim suma As Integer
Dim n2 = 14
suma = n1 + n2
Dim clase As String
clase = Console.ReadLine()
```
Aquí creamos un ejemplo de como asignando variables y concatenando datos obtenemos una salida de información:
```vbnet
Dim nombre, apellidos, direccion As String
Dim edad As Integer
nombre = "Guillermo"
apellidos = "Galindo"
direccion = "Quetzaltenango"
edad = 27

Console.WriteLine("Nombre: " & nombre)
Console.WriteLine("Apellidos: " & apellidos)
Console.WriteLine("Dirección: " & direccion)
Console.WriteLine("Edad: " & edad & " años.")
```
Lo que nos dá una salida: 
```console
Nombre: Guillermo
Apellidos: Galindo
Dirección: Quetzaltenango
Edad: 27 años.
```

Ahora le haremos un ligero cambio, permitiendo que el usuario final del programa pueda hacer uso de el como le plazca.
```vbnet
Dim nombre, apellidos, direccion As String
Dim edad As Integer
Console.Write("Ingresa tu nombre: ")
nombre = Console.ReadLine()
Console.Write("Ingresa tu apellido: ")
apellidos = Console.ReadLine()
Console.Write("Ingresa tu dirección: ")
direccion = Console.ReadLine()
Console.Write("Ingresa tu edad: ")
edad = Console.ReadLine()

Console.WriteLine("Nombre: " & nombre)
Console.WriteLine("Apellidos: " & apellidos)
Console.WriteLine("Dirección: " & direccion)
Console.WriteLine("Edad: " & edad & " años.")
```
Observe como utilizamos un Console.Write(texto) antes de cada asignación de datos, esto con el objetivo de que el usuario final sepa que debe ingresar, esta es la primera barrera de protección ante una falla de capa 8. 


