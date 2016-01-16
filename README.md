[TOC]

# Getting Ready to Code
## Course Overview 
 * Lo da un instructor que no habia visto antes.
 * Es bastante Completo.
## What's a Programming Language?
* binary es lo que lee el procesador, despues hicieron asembly pero este fue reemplado por Fortran y Cobol
* C y C++ son Compiled Languages mientras que Ruby, php, javascript son Scripting languages
* Existen 2 styles de Programar o la manera de organizarse el codigo 
	- Procedular es similar a los script corren desde el comienzo al final 
	- Object Oriented; son objetos se definen maneras de manipularlo
* Ruby pertenece a los 2 estilos pero es facil de leer,
* Uno de los framework mas famosos de ruby es ruby on rails
* El curso esta enfocado en scripting task.
## Installing Ruby 
* Existen 2 maneras de instalar ruby 
	- Packages managers 
		- **Centos**  `yum install ruby irb rubygems`
		- **Ubuntu** `apt-get install ruby`
	- RVM 
		- el cual es un proceso manual pero con mas opciones.
		- Para instalar RVM buscamos en su pagina [rvm.io](rvm.io) y lo descargamos luego lanzamos; `rvm install ruby`
## The Ruby Environment
* Los  archivos de scripts son .rb
* Usaremos 3 programas con ruby 
	- ruby: compilador 
	- irb: shell  
	- gem: instalador de extensiones y plugins.
* puts == echo e igual es recomendable usar el shibang para evitar usar el `ruby example.rb`
* IRB es una shell como la que tiene python donde todos los comandos se comunican con el compilador.
* cuando sale => nill es totalmente normal.
* gems es util para instalar librerias, y muchas funcionalidades extras.
# Learning Basic Ruby Syntax
## Hello World! 
*  puts es un method y el Hello word es un argumento
*  Methods= encapsulate code can use arguments
* Para multiples arguments separarlos con ","
* Otra forma es usando **();** example; `puts("Hello World")`
## Variables 
* Crear las variables es muy similar a otros lenguajes pero añade nuevas clasificaciones.
* Existen varias variables que pueden empezar con @ o @@ incluso $
* Las vaiables pueden ser; locales, instance, certain places,
* ademas de variables existen constantes que no pueden cambiar y empiezAN con MAYUSCULA.
* esta manera de declarar variables solo funciona para numeros. a no ser que usemos ' ' para string.
## Types of Variables
* Existen 2 varios tipos de variables 
	- Litterals = le damos valores explicitamente 
	- Variables= los cuales son link a valores.
* Los mas famosos son:  
	- **numbers:** en los numbers existen integers y floats, dentro de Integers existe bignum o fixnum
	- **booleans:** son los tipicos true o false.
	- **strings:** son los textos 
	- **arrays:** su caracteristica es que son filas y estas pueden ser acumuladas pero colocadas al final si no se quiere reemplazar al anterior.
		- ex: `array = [1,2,3]`
		- en caso de añadir otro mas usamos `array [3]= 4`
		- En algunos casos es necesario crear un array limpio primero.
		- todos los valores deben estar en el `[]` y separarse por `,`
	- **hashes:** similas al array pero en vez de listar por numeros listamos por keys
		- `my_hash = "string" => "my string", "my number" => 4` luego llamamos con `my_hast ["simple string"]`
* Podemos asignar un valor a un array o hash existente puede crearse vacio con `my array []`
## Basic Math
* las math son las nomales pero existe una % que es modulus no se que hace.
* si existe una variable podemos llamarla sin los `""` o `''`
* podemos convertir diferentes variables por ejemplo de numbers to string.
* `.to_s`  a String.
* `.to_i`  a entero o integer.
* `.to_f` to float o decimal 
	* ex: ```irb(main):001:0> 12.to_f
=> 12.0			```
## Conditionals
* Los conditionals son buenisimos.
ex:
```ruby  
 if my_variable > 10
puts my_variable
end
```
* los extended conditional es cuando añadimos un **else**, el cual corre si la condicion es falsa.
* tambien podemos usamos **elsif** que permite añadir otro if si la primera condicion es falsa.
* En ruby podemos usar conditionals en una sola linea por ejemplo
`puts "Big Number" if my_variable > 10`
`puts "Small Number" unless my_variable > 10`
* la condicion **unless** tambien podemos usarla y es una negacion hasta que ocurra.
```ruby
unless my_variable > 10
	puts my_variable
end 
```
* Otra forma de hacerlo en una linea es usando la **Ternary Statement**
	* Regular Statement.
```ruby 
if my_variable > 10
	puts "big"
else 
	puts "small" 
end 
```
	* Ternary Statement 
`my_variable > 10 ? puts("big") : puts("small")`
 **#donde el `?` seria un **if** y el `:` un **else**, es necesario usar parentesis.**
* tambien existen los comparison tests donde
	- a > b 
	- a < b
	- a >= b
	- a <= b 
	- a == b
* Un ex de un script con condiciones.
```ruby
puts "Input an integer"
user_input = gets.to_i
if user_input > 10
output = user_input * user_inpu
else
output = user_input * 2
end
puts output
```
## Conditionals Continued
* Un script puede tener varios elsif de ser necesario. 
* ![Puedes tener varios elsif](https://i.imgur.com/mwL2jhB.png)
* Pero es posible usar case que es mucho mas facil de leer.
![enter image description here](https://i.imgur.com/MhtxIPN.png)
* Es posible añadir multiples conditionals 
	* Boolean AND
   ` if my_var == 10 && your_var == 5` Aca se tienen que cumplir los 2 para que se pueda correr.
	* Boolean OR 
	`if my_var ==10 || your_var == 5` Aca si cualquier de los 2 es verdadero el statement se aplica.
	* Boolean NOT
	`if my_var != 10` Si no es igual se lanza el statement.
	* Ejemplo con condicionales. 
```ruby
!#/usr/bin/ruby

puts "En tu escritorio tienes un Telefono (Y/N)"
case gets
        when "Y\n"
                phone  = true
        when "N\n"
                phone = false
end
puts "En tu escritorio tienes un lapiz (Y/N)"
case gets
        when "Y\n"
                pencil  = true
        when "N\n"
                pencil = false
end
puts "You have a phone" if phone
puts "You have a pencil" if pencil
```
## Iterators 
 * Los iterators son ideales para operar cada miembro de una variable por ejemplo los array si quisieramos mostrar cada miembro de un array seria como: 
 
 **Whitout Iterators**
	 `puts first_five_integers [0]`
	 `puts first_five_integers [1]`
	 `puts first_five_integers [2]`
	 `puts first_five_integers [3]`
	 `puts first_five_integers [4]`
	 
 **Con Iterators seria mucha mas sencillo**
```ruby
first_five_integers.each do |my_integer| 
	puts my_integer 
end 
```
* Como each es considerado un Method puede usar arguments pero en este caso el puede usar un block como argument para que tome el block of code debemos colocarlo entre do y end 
*  Tambien es posible suplir una variable al block con each definiendola entre | | despues del do y tendra el valor de cada miembro del array.
*  Los iterators actuan como loops para collections.
* DRY = Do not Repeat Yourself 
* El earch puede ser usado en un hash y se pueden suplir 2 variables la key y el value.
```ruby
my_hash = {"orange" => true, "banana" => false}
my_hash.each do | key,value | 
...
end 
```
Ejemplo de una lista de Compras 
```ruby
#!/usr/bin/ruby                                                                                                                                       
# Declaramos el Hash con los Valores que queramos incluir.                                                                                            
grocery_items = { "oranges" => false, "bananas" => false}                                                                                             
#Preguntamos lo que necesitamos usando el Iterator y suplimos 2 variables item y need_for_item.                                                       
puts "Do you need:"                                                                                                                                   
grocery_items.each do | item, need_for_item | # Aqui solo declaramos y preparamos las variables.                                                      
  puts item + "? (Y/N)" #Aqui es donde preguntamos.                                                                                                   
  case gets                                                                                                                                           
    when "Y\n"                                                                                                                                        
      grocery_items [item] = true                                                                                                                     
    when "N\n"                                                                                                                                        
      grocery_items [item] = false                                                                                                                    
  end                                                                                                                                                 
end                                                                                                                                                   
puts "Here's your list:"                                                                                                                              
grocery_items.each do | item, need_for_item |                                                                                                         
  puts item if need_for_item #Aqui aun no entiendo pero supongo que si es true se cumple la sentencia.                                                
end    
```
## Arrays and Hashes
* Podemos usar nested arrays los cuales se llaman multi.dimensional arrays. 
`childhood_games_played  = [["make believe", true], ["tag", false]]`
* Luego para llamar a los juegos debemos usar 
```ruby
childhood_games_played [0][0]
	"make believe"
childhood_games_played [1][0]
	"tag"
childhood_games_played [0][1]
	"true"
childhood_games_played [1][1]
	"false"
```
* Los hashes tambien pueden ser nested.
`cocktails = {"martini" => {"vodka" => true, "gin" => false}}`
* Luego para llamarlos usamos 
```ruby 
cocktails["martini"]["vodka"]
	true
cocktails["martini"]["gin"]
	false 
```
* Podemos ordenar los array con el method **.sort**
`my_array.sort` devuelve un array ordenado.
* En caso de querer ordenar el array en uso usamos `mv_array.sort!`
* Es posible al igual que con each usarlo en block of codes 
```ruby
my_array.sort do |a,b| 

	a <=> b #Diferencia quien esta primero.
	
end 
```
* Para saber la longitud de un array es posible usar los method 
	**.count**
	**.length**
* Para revisar si en el array existe un valor es posible usar el method **.include**
`first_five_integers.include? 1` Es importante usar el ? 
* Es posible crear un array a partir de otro usando **.map** un buen ejemplo es para calcular si unos numeros de un array son pares o impares.
```ruby
my_array = [1,2,3]
odd_or_even = my_array.map do |element|
	element % 2 == 0 ? "even" : "odd"
	end  
```
## Strings 
* Se deben colocar las String en `""` para que ruby pueda identificarlas.
*  Llamar las variables es diferente que en bash para llamar una variable entre strings usamos #{variable}
`puts "Your have #{bank_account} dollars."`Sin necesita de cerrar los " podemos incluir la variable e imprimir en una sola linea.
* Podemos sumar operaciones matematicas dentro de lo {} 
`puts "Tiene en total #{banesco + bod}bs. entre todas sus cuentas."`
* Podemos sumar string con string en caso de ser string y integers daria error.
* En caso de querer cambiar el string a Capital usamos **.upcase** si fuera a lower seria **.downcase**
* En caso de dividir una string usamos **.split(" ")** donde el space es el delimitador luego se convertiria en un array.
* Un pequeño ejemplo
```ruby
puts "Insertar una frase"
palabra = gets
numero_palabras = palabra.split(" ").count
puts "Tu frase tiene #{numero_palabras} palabra#{numero_palabras == 1 ? "." : "s."}"
```
## While Loop
* Repite una seccion del codigo hasta que una condicion sea cierta, para evitar que sea un loop infinito la variable debe cambiar.
* La syntax seria while condition do y un end es bueno añadir un contador al final de la sentencia ex: my_integer += 1 
```ruby
my_var = 10

while my_var < 30 do 
	puts "my_var = #{my_var}"
	my_var += 1 
end 
```
* El program block va entre el do y el end. 
* Es importante saber que si usamos " " no podemos llamar una variable a no ser que usemos el #{}.
* loops and arrays: the perfect match.
* El until loop es totalmente inverso.
* Un ejemplo de ordenar los enteros.
```ruby
integers = []
current_integer = 0 
while current_integer < 10 do 
puts "Type an integer"
integers[current_integer] = gets.to_i
	current_integer+=1
end 

integers.sort.each do |this_int|
	puts this_int
end 
```
## For Loop
* El For loop es igual al method each. 
* un ejemplo practico seria.
```ruby 
bags = ["suitcase", "messenger bag", "satcher", "backpack"]
for bag_types in bags do
	puts bag_type
end
```
* los for loop no solo pueden usarse en una collection es posible usarse en rangos 
* Existen 2 tipos de rangos Inclusive y Exclusive la diferencia es que en Exclusive se excluye el ultimo valor del rango.

```ruby
#inclusive range:
	for variable in 1..4 do
		...
	end 
```
```ruby
#Exclusive range:
	for variable in 1...4 do
		...
	end 
```
* Es recomendable dejar de usar for loop y usar **.each** 
## Loop Control 
* Con el key **next** podemos saltar las demas interacciones del loop y saltar a la proxima iteracion.
```ruby
my_var = 0
while my_var < 10 do
	if my_var == 3 
		my_var += 1 
		next
	end 
	puts my_var
	my_var += 1
end
```
* Creo que salta a una proximo block.
* La key **redo** va al comienzo del codigo asi la condicion sea verdadera o falsa.
```ruby
my_var = 0
while my_var < 10 do
	puts my_var
	if my_var == 3 
		my_var = 10 
		redo
	end 
	my_var += 1
end
```
* Seria como un if exit en bash.
* Lo extraño es que el redo seguira corriendo asi el statement del while sea falso....
* El redo no le veo mucho sentido.
* El key **break** sale del loop inmediatamente y es uno de los mas importantes.
```ruby
puts "Type something to continue. Or nothing to quit"
while a = gets do

	if a =="\n" 
		break
	end 
	puts a #Imprime la misma linea vacia.
end 
```
* Ejemplo final
```ruby
total = 0 
puts "Input your numbers" 
while input = gets do #Declaramos 
	if input == "\n" 
		break 
	end 
	total = total + input.to_f 
	puts "running total = #{total}" 
end 

puts "Total: #{total}" 
```
## Methods 
* Los Methods son como funtions en otro lenguaje antiguo
![enter image description here](https://i.imgur.com/AipGJrz.png)
*  Method Example
```ruby
def hello_user 
	puts "Enter your Name" 
	username = gets
	puts "Hello " + username
end 

hello_user #Llamamos al metodo.
```
* Los methods devuelven objects.
* En el irb podemos definir los scripts tal cual y cuando cambiemos de 001:0 a 002:1 es porque estamos dentro de un statement.
* Por defecto un method puede arrojar un nil pero esto puede cambiar
```ruby
def hello_user 
	puts "Enter your Name" 
	username = gets
	"Hello #{username.chop}." 
end 
hello_user
```
* Esta vez debe arrojar el object del username.
* Es util cuando un method arroja un boolean.
```ruby
def hello_user 
	puts "Enter your Name" 
	username = gets
	if username != "\n" 
		"Hello #{username.chop}."
	else
		false 
end
```
Ejemplo de unas recetas de comida.
```ruby
def get_ingredient
	new_ingredient = gets
	if new_ingredient != "\n"
		new_ingredient 
	else 
		false
	end
end
ingredients = [] 
puts "Input your Ingredients"
while my_ingredient  = get_ingredient do  #Comparamos que sea una string.
	ingredients[ingredients.count] = my_ingredient
end 
puts "Input your instructions"
instructions = gets
puts "Ingredients:"
puts ingredients
puts "Instructions:"
puts instructions

```
## Methods Continued
* Es posible usar metodos en un argumento.
![enter image description here](https://i.imgur.com/G8BiPcK.png)
* Es recomendable declarar el method seguido de declarar la variable que se usara como argumento.
* Para doblar un numero seria my_var **  *=2**
* El yield seria como el punto de stdin en donde el method introduce su resultudado.
```ruby
def my_method 
        puts "executing your code..."
        yield
        puts "done"
end
my_method do  
        puts 2 + 2 
end 

######RESULTADO#########
executing your code...
4
done
```
* Ejercicio que multiplica 2 numeros.
```ruby
def multiply_this a. b
	total = a * b 
	if total < 0 
		false
	else
		total
	end
end

user_input = []
puts "Input two numbers" 
while user_number = gets do
	user_input[user_input.count] = user_number.to_f 
	if user_input.count == 2 
		break 
	end
end 
if result = multiply_this(user_input[0], user_input[1]) #Declara una variable en el mismo statement
														#Arroja los argumentos al method desde un array.
	puts result 
else 
	puts "Invalid Input"
end
```
## Using Classes
* Se podria definir a una clase con una descripcion de un objeto.
*
![enter image description here](https://i.imgur.com/lLDtoa4.png)
* En ruby todo es un object por tanto todo pertenece a una clase.
* Array, Hash, y todos los tipos de variables son clases.
* Podemos decir que **my_array = [ ] == my_array = Array.new** 
* Las clases pueden contener dos tipos de cosas; variables definitions y method definitiios por ejemplo la class array incluye el method each. 
* Las instances al parecer representan un objeto en especifico en vez de tipos de objetos.
* La mayor ventaja es que puedo tener multiples instancias de una misma clase.
`my_first_array = Array.new`
`my_second_array = Array.new`
* Las clases pueden incluir propiedades de otras clases.
* Si usamos **.class** revelara a que clase pertenece pero si usamos **.superclass** revelara la clase de quien hereda.
![enter image description here](https://i.imgur.com/IlDo4qI.png)
* Vemos que si usamos el 1.class.superclass.superclass.superclass vemos es un Object como todo en ruby.
## Creating Classes 
* Para crear una class la syntax seria
`class Class_name `
`...`
`end`
* Es importante que la clase este escrita en Mayuscula.
* Para inicializar un object es importante que la clase ya estre creada.
`my_object = Class_name.new`
* attr_accesor = attribute accesor el cual es un method para crear ins
* Ejemplo de como crear una tabla
```ruby
class Table 
	attr_accessor :height, :width, :length
end
```
* el attr_accesor crea method para acceder a la data que le damos como argumento 
* El accesor crea una instance variable que son las creadas con @variable
* Cada vez que creemos clases crearemos instance variable dentro de ellas.
* Es importante saber que crea method para acceder a esas instance variables donde ese method corresponde al nombre.
* Cada vez que usamos `:` se crea un **symbol** en ruby.
* Podemos crear una class en un archivo y luego llamarla desde irb con `irv -r ./table.rb`
* cuando usamos `t = Table.new` estamos creando una instancia de la clase.
* Luego podemos colocar datos en la instancia t siguiendo de la instance variable ex: `t.height = 5`
* Es posible extender una Class ya creada usando el class con el nombre de la class y añadiendo lo nuevo dentro.
* en este caso la extendemos para introducir un nuevo method.
```ruby
class Table
	def cost
		@length * @width * 5 + 4 * @height * 2 
	end
end
```
* Vemos como llamamos nuestras variables con @ al ser Instance variables.
* Luego podemos llamar a la instancia que llamamos que se llama con el method que definimos al final **t.cost** 
## Creating Classes Continued
* Es posible definir un initialize method cada vez que instanciamos o instanstiate una class y colocarles unos valores por defecto.
* Ejemplo
```ruby
class table 
	def initialize ilength = 3, iwidth = 3, iheight = 3
		@lenght = ilength
		@width = iwidth
		@height = iheight
	end
end
```
*  Es importante saber que estamos extendiendo la class Table de la antigua clase por eso existe @lenght y los otros.
* Despues cuando inicializamos la clase con .new tendremos los valores 3 o incluso podemos añadir nuevos valores manteniendo los ordenes.
![enter image description here](https://i.imgur.com/YPgV8g0.png)
* Si usamos el private dentro de un method solo sera accesible para la class code no fuera de ella.
* Luego si usaramos **my_table.table_top_area** nos daria error al llamar a un method privado.
* Por defecto todas las clases heredan de la clase object. en caso de querer heredar de otra usamos 
* `class LibraryTable  < Table` al momento de declarar la clase de esta manera podemos llamar a los private method.
* Al igual que el private existe el protected que es usado para comparar al asegurar que el method solo es acedido desde sibling object o child objects
* Ejercicio de Cuenta Bancaria.
```ruby
class AccountBook
	def initialize 
		@ledger = []
		@current_total = 0 
	end 
	def add_money amount, memo = ""
		@ledger[@ledger.count] = [amount, memo]
		@current_total += amount
	end
	def subtract_money amount, memo =""
		@ledger[@ledger.count] = [amount * -1, memo]
		@current_total -= amount
	end
	
	def printout 
		tab = 0
		puts "Amount:\tMemo:\tTotal:"
		@ledger.each do |line|
			tab += line[0]
			puts "#{line[0]}\t#{line[1]}\t#{tab}"
		end
	end
end
```
## Variable Scope Revisited
* Existen 4 tipos de Variable 
	- local: comienzan con una letra en minuscula, y es solo accesible en el method que la definio
	- instance: Comienzan con @ pueden accederse en cualquier method de una instancia de una clase
	- class: Empiezan con doble @@ estan disponible en cualquier instancia y method de la clase.
	- global: Comienzan con $ y pueden llamarse en cualquier parte del codigo, se usan en general para los settings.
* Un ejemplo de local Variables seria.
```ruby
class Square

	def initialize 
	 @length = 10 #Declaramos una instance variable 
	end

	def printout 
		length = @lenght * 2 #Declaramos una variable local que es *2 a la instance variable parecieran iguales pero son diferentes. 
		puts "Length = #{length}." 
	end  
end 
```
* Es importante diferencia que las local variables solo estan disponible entre method.
* Las global variables son buenas para settings globales.
##  Class Methods and Singletons 
* Recordemos que la instancia de una clase es para un objeto en especifico de una clase las Class Methods hacen referencia a toda la clase util para operar todos los miembros, variables, o database cleanup methods.
* Creamos una clase pero esta vez creamos un method llamado self.Nombre-del-metodo-que-queramos luego en cualquier lugar de la class podremos llamar al method. 
* Para llamar al class method usamos **Class_Name.method_name** ==> Tree.trim 
* Los Singleton Methods estan definidos para solo un objecto. 
*  Lo definimos luego de crear una variable || objeto luego definimos un metodo con el nombre de la variable seguido del nombre del methodo que creamos.
Ejemplo `abc = "abc" ---> def abc.twice` 
* Tambien es posible usar una Singleton Class util si solo queremos crear una class importante pero unica.
* Existen 2 maneras de crear una Singleton Classes 
	- Crear una blank class y operar en ella.
```ruby
####Creamos una blank class.
class TableCorporation
end 
##Listo sin nada dentro.
class << TableCorporation 
#Todo lo que este dentro sera una singletons class.
end 
# -OR-
class TableCorporation
	class << self 
	....##todo lo que este dentro sera una singletons class.
	end
end
```
	- Crear una instancia de una clase y extenderla.
```ruby
####Creamos una class.
TableCorporation = Object.new
class << TableCorporation
....
end 

```
* Vemos que estamos operandolos methods en una clase porque todo en ruby es un object.
* Los attritubes y methods se crear igual que en cualquier otra clase.
* Crear una class para envio de paquetes
```ruby
class Box
	attr_accessor :length, :width, :height, :weight, :distance
	def initialize
	@@materials_cost = 0.01 #1 cent per square inch
	@@rate = 00.1 # 1 cent per pount per mile
	end 
	def self.rate= rate
	@@rate = rate
	end
	def self.materials_cost= cost
	@@materials_cost = cost
	end
	def package_cost
	(@length * @width * 2 + @length * @height * 2 + @width * height * 2) * @@materials_cost + @weight * @distance * @@rate 
	end
end
```
* Crear una instancia de una clase y extenderla.
```ruby
####Creamos una class.
TableCorporation = Object.new
class << TableCorporation
....
end 
```

