<div class="toc"><ul><li><a href="#getting-ready-to-code">Getting Ready to Code</a><ul><li><a href="#course-overview">Course Overview</a></li><li><a href="#whats-a-programming-language">What's a Programming Language?</a></li><li><a href="#installing-ruby">Installing Ruby</a></li><li><a href="#the-ruby-environment">The Ruby Environment</a></li></ul></li><li><a href="#learning-basic-ruby-syntax">Learning Basic Ruby Syntax</a><ul><li><a href="#hello-world">Hello World!</a></li><li><a href="#variables">Variables</a></li><li><a href="#types-of-variables">Types of Variables</a></li><li><a href="#basic-math">Basic Math</a></li><li><a href="#conditionals">Conditionals</a></li><li><a href="#conditionals-continued">Conditionals Continued</a></li><li><a href="#iterators">Iterators</a></li><li><a href="#arrays-and-hashes">Arrays and Hashes</a></li><li><a href="#strings">Strings</a></li><li><a href="#while-loop">While Loop</a></li><li><a href="#for-loop">For Loop</a></li><li><a href="#loop-control">Loop Control</a></li><li><a href="#methods">Methods</a></li><li><a href="#methods-continued">Methods Continued</a></li><li><a href="#using-classes">Using Classes</a></li><li><a href="#creating-classes">Creating Classes</a></li><li><a href="#creating-classes-continued">Creating Classes Continued</a></li><li><a href="#variable-scope-revisited">Variable Scope Revisited</a></li><li><a href="#class-methods-and-singletons">Class Methods and Singletons</a></li></ul></li></ul></div><h1 id="getting-ready-to-code">Getting Ready to Code</h1>
<h2 id="course-overview">Course Overview</h2>
<ul>
<li>Lo da un instructor que no habia visto antes.</li>
<li>Es bastante Completo.</li>
</ul>
<h2 id="whats-a-programming-language">What’s a Programming Language?</h2>
<ul>
<li>binary es lo que lee el procesador, despues hicieron asembly pero este fue reemplado por Fortran y Cobol</li>
<li>C y C++ son Compiled Languages mientras que Ruby, php, javascript son Scripting languages</li>
<li>Existen 2 styles de Programar o la manera de organizarse el codigo
<ul>
<li>Procedular es similar a los script corren desde el comienzo al final</li>
<li>Object Oriented; son objetos se definen maneras de manipularlo</li>
</ul>
</li>
<li>Ruby pertenece a los 2 estilos pero es facil de leer,</li>
<li>Uno de los framework mas famosos de ruby es ruby on rails</li>
<li>El curso esta enfocado en scripting task.</li>
</ul>
<h2 id="installing-ruby">Installing Ruby</h2>
<ul>
<li>Existen 2 maneras de instalar ruby
<ul>
<li>Packages managers
<ul>
<li><strong>Centos</strong>  <code>yum install ruby irb rubygems</code></li>
<li><strong>Ubuntu</strong> <code>apt-get install ruby</code></li>
</ul>
</li>
<li>RVM
<ul>
<li>el cual es un proceso manual pero con mas opciones.</li>
<li>Para instalar RVM buscamos en su pagina <a href="rvm.io">rvm.io</a> y lo descargamos luego lanzamos; <code>rvm install ruby</code></li>
</ul>
</li>
</ul>
</li>
</ul>
<h2 id="the-ruby-environment">The Ruby Environment</h2>
<ul>
<li>Los  archivos de scripts son .rb</li>
<li>Usaremos 3 programas con ruby
<ul>
<li>ruby: compilador</li>
<li>irb: shell</li>
<li>gem: instalador de extensiones y plugins.</li>
</ul>
</li>
<li>puts == echo e igual es recomendable usar el shibang para evitar usar el <code>ruby example.rb</code></li>
<li>IRB es una shell como la que tiene python donde todos los comandos se comunican con el compilador.</li>
<li>cuando sale =&gt; nill es totalmente normal.</li>
<li>gems es util para instalar librerias, y muchas funcionalidades extras.</li>
</ul>
<h1 id="learning-basic-ruby-syntax">Learning Basic Ruby Syntax</h1>
<h2 id="hello-world">Hello World!</h2>
<ul>
<li>puts es un method y el Hello word es un argumento</li>
<li>Methods= encapsulate code can use arguments</li>
<li>Para multiples arguments separarlos con “,”</li>
<li>Otra forma es usando <strong>();</strong> example; <code>puts("Hello World")</code></li>
</ul>
<h2 id="variables">Variables</h2>
<ul>
<li>Crear las variables es muy similar a otros lenguajes pero añade nuevas clasificaciones.</li>
<li>Existen varias variables que pueden empezar con @ o @@ incluso $</li>
<li>Las vaiables pueden ser; locales, instance, certain places,</li>
<li>ademas de variables existen constantes que no pueden cambiar y empiezAN con MAYUSCULA.</li>
<li>esta manera de declarar variables solo funciona para numeros. a no ser que usemos ’ ’ para string.</li>
</ul>
<h2 id="types-of-variables">Types of Variables</h2>
<ul>
<li>Existen 2 varios tipos de variables
<ul>
<li>Litterals = le damos valores explicitamente</li>
<li>Variables= los cuales son link a valores.</li>
</ul>
</li>
<li>Los mas famosos son:
<ul>
<li><strong>numbers:</strong> en los numbers existen integers y floats, dentro de Integers existe bignum o fixnum</li>
<li><strong>booleans:</strong> son los tipicos true o false.</li>
<li><strong>strings:</strong> son los textos</li>
<li><strong>arrays:</strong> su caracteristica es que son filas y estas pueden ser acumuladas pero colocadas al final si no se quiere reemplazar al anterior.
<ul>
<li>ex: <code>array = [1,2,3]</code></li>
<li>en caso de añadir otro mas usamos <code>array [3]= 4</code></li>
<li>En algunos casos es necesario crear un array limpio primero.</li>
<li>todos los valores deben estar en el <code>[]</code> y separarse por <code>,</code></li>
</ul>
</li>
<li><strong>hashes:</strong> similas al array pero en vez de listar por numeros listamos por keys
<ul>
<li><code>my_hash = "string" =&gt; "my string", "my number" =&gt; 4</code> luego llamamos con <code>my_hast ["simple string"]</code></li>
</ul>
</li>
</ul>
</li>
<li>Podemos asignar un valor a un array o hash existente puede crearse vacio con <code>my array []</code></li>
</ul>
<h2 id="basic-math">Basic Math</h2>
<ul>
<li>las math son las nomales pero existe una % que es modulus no se que hace.</li>
<li>si existe una variable podemos llamarla sin los <code>""</code> o <code>''</code></li>
<li>podemos convertir diferentes variables por ejemplo de numbers to string.</li>
<li><code>.to_s</code>  a String.</li>
<li><code>.to_i</code>  a entero o integer.</li>
<li><code>.to_f</code> to float o decimal
<ul>
<li>ex: <code>irb(main):001:0&gt; 12.to_f =&gt; 12.0</code></li>
</ul>
</li>
</ul>
<h2 id="conditionals">Conditionals</h2>
<ul>
<li>Los conditionals son buenisimos.<br>
ex:</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"> <span class="token keyword">if</span> my_variable <span class="token operator">&gt;</span> <span class="token number">10</span>
puts my_variable
<span class="token keyword">end</span>
</code></pre>
<ul>
<li>los extended conditional es cuando añadimos un <strong>else</strong>, el cual corre si la condicion es falsa.</li>
<li>tambien podemos usamos <strong>elsif</strong> que permite añadir otro if si la primera condicion es falsa.</li>
<li>En ruby podemos usar conditionals en una sola linea por ejemplo<br>
<code>puts "Big Number" if my_variable &gt; 10</code><br>
<code>puts "Small Number" unless my_variable &gt; 10</code></li>
<li>la condicion <strong>unless</strong> tambien podemos usarla y es una negacion hasta que ocurra.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">unless</span> my_variable <span class="token operator">&gt;</span> <span class="token number">10</span>
	puts my_variable
<span class="token keyword">end</span> 
</code></pre>
<ul>
<li>Otra forma de hacerlo en una linea es usando la <strong>Ternary Statement</strong>
<ul>
<li>Regular Statement.</li>
</ul>
</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">if</span> my_variable <span class="token operator">&gt;</span> <span class="token number">10</span>
	puts <span class="token string">"big"</span>
<span class="token keyword">else</span> 
	puts <span class="token string">"small"</span> 
<span class="token keyword">end</span> 
</code></pre>
<pre><code>* Ternary Statement 
</code></pre>
<p><code>my_variable &gt; 10 ? puts("big") : puts("small")</code><br>
<strong>#donde el <code>?</code> seria un <strong>if</strong> y el <code>:</code> un <strong>else</strong>, es necesario usar parentesis.</strong></p>
<ul>
<li>tambien existen los comparison tests donde
<ul>
<li>a &gt; b</li>
<li>a &lt; b</li>
<li>a &gt;= b</li>
<li>a &lt;= b</li>
<li>a == b</li>
</ul>
</li>
<li>Un ex de un script con condiciones.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">puts <span class="token string">"Input an integer"</span>
user_input <span class="token operator">=</span> gets<span class="token punctuation">.</span>to_i
<span class="token keyword">if</span> user_input <span class="token operator">&gt;</span> <span class="token number">10</span>
output <span class="token operator">=</span> user_input <span class="token operator">*</span> user_inpu
<span class="token keyword">else</span>
output <span class="token operator">=</span> user_input <span class="token operator">*</span> <span class="token number">2</span>
<span class="token keyword">end</span>
puts output
</code></pre>
<h2 id="conditionals-continued">Conditionals Continued</h2>
<ul>
<li>Un script puede tener varios elsif de ser necesario.</li>
<li><img src="https://i.imgur.com/mwL2jhB.png" alt="Puedes tener varios elsif"></li>
<li>Pero es posible usar case que es mucho mas facil de leer.<br>
<img src="https://i.imgur.com/MhtxIPN.png" alt="enter image description here"></li>
<li>Es posible añadir multiples conditionals
<ul>
<li>Boolean AND<br>
<code>if my_var == 10 &amp;&amp; your_var == 5</code> Aca se tienen que cumplir los 2 para que se pueda correr.</li>
<li>Boolean OR<br>
<code>if my_var ==10 || your_var == 5</code> Aca si cualquier de los 2 es verdadero el statement se aplica.</li>
<li>Boolean NOT<br>
<code>if my_var != 10</code> Si no es igual se lanza el statement.</li>
<li>Ejemplo con condicionales.</li>
</ul>
</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token operator">!</span><span class="token comment" spellcheck="true">#/usr/bin/ruby
</span>
puts <span class="token string">"En tu escritorio tienes un Telefono (Y/N)"</span>
<span class="token keyword">case</span> gets
        <span class="token keyword">when</span> <span class="token string">"Y\n"</span>
                phone  <span class="token operator">=</span> <span class="token keyword">true</span>
        <span class="token keyword">when</span> <span class="token string">"N\n"</span>
                phone <span class="token operator">=</span> <span class="token keyword">false</span>
<span class="token keyword">end</span>
puts <span class="token string">"En tu escritorio tienes un lapiz (Y/N)"</span>
<span class="token keyword">case</span> gets
        <span class="token keyword">when</span> <span class="token string">"Y\n"</span>
                pencil  <span class="token operator">=</span> <span class="token keyword">true</span>
        <span class="token keyword">when</span> <span class="token string">"N\n"</span>
                pencil <span class="token operator">=</span> <span class="token keyword">false</span>
<span class="token keyword">end</span>
puts <span class="token string">"You have a phone"</span> <span class="token keyword">if</span> phone
puts <span class="token string">"You have a pencil"</span> <span class="token keyword">if</span> pencil
</code></pre>
<h2 id="iterators">Iterators</h2>
<ul>
<li>Los iterators son ideales para operar cada miembro de una variable por ejemplo los array si quisieramos mostrar cada miembro de un array seria como:</li>
</ul>
<p><strong>Whitout Iterators</strong><br>
	 <code>puts first_five_integers [0]</code><br>
	 <code>puts first_five_integers [1]</code><br>
	 <code>puts first_five_integers [2]</code><br>
	 <code>puts first_five_integers [3]</code><br>
	 <code>puts first_five_integers [4]</code></p>
<p><strong>Con Iterators seria mucha mas sencillo</strong></p>
<pre class=" language-ruby"><code class="prism  language-ruby">first_five_integers<span class="token punctuation">.</span><span class="token keyword">each</span> <span class="token keyword">do</span> <span class="token operator">|</span>my_integer<span class="token operator">|</span> 
	puts my_integer 
<span class="token keyword">end</span> 
</code></pre>
<ul>
<li>Como each es considerado un Method puede usar arguments pero en este caso el puede usar un block como argument para que tome el block of code debemos colocarlo entre do y end</li>
<li>Tambien es posible suplir una variable al block con each definiendola entre | | despues del do y tendra el valor de cada miembro del array.</li>
<li>Los iterators actuan como loops para collections.</li>
<li>DRY = Do not Repeat Yourself</li>
<li>El earch puede ser usado en un hash y se pueden suplir 2 variables la key y el value.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">my_hash <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token string">"orange"</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token keyword">true</span><span class="token punctuation">,</span> <span class="token string">"banana"</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token keyword">false</span><span class="token punctuation">}</span>
my_hash<span class="token punctuation">.</span><span class="token keyword">each</span> <span class="token keyword">do</span> <span class="token operator">|</span> key<span class="token punctuation">,</span>value <span class="token operator">|</span> 
<span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span>
<span class="token keyword">end</span> 
</code></pre>
<p>Ejemplo de una lista de Compras</p>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token comment" spellcheck="true">#!/usr/bin/ruby                                                                                                                                       
</span><span class="token comment" spellcheck="true"># Declaramos el Hash con los Valores que queramos incluir.                                                                                            
</span>grocery_items <span class="token operator">=</span> <span class="token punctuation">{</span> <span class="token string">"oranges"</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token keyword">false</span><span class="token punctuation">,</span> <span class="token string">"bananas"</span> <span class="token operator">=</span><span class="token operator">&gt;</span> <span class="token keyword">false</span><span class="token punctuation">}</span>                                                                                             
<span class="token comment" spellcheck="true">#Preguntamos lo que necesitamos usando el Iterator y suplimos 2 variables item y need_for_item.                                                       
</span>puts <span class="token string">"Do you need:"</span>                                                                                                                                   
grocery_items<span class="token punctuation">.</span><span class="token keyword">each</span> <span class="token keyword">do</span> <span class="token operator">|</span> item<span class="token punctuation">,</span> need_for_item <span class="token operator">|</span> <span class="token comment" spellcheck="true"># Aqui solo declaramos y preparamos las variables.                                                      
</span>  puts item <span class="token operator">+</span> <span class="token string">"? (Y/N)"</span> <span class="token comment" spellcheck="true">#Aqui es donde preguntamos.                                                                                                   
</span>  <span class="token keyword">case</span> gets                                                                                                                                           
    <span class="token keyword">when</span> <span class="token string">"Y\n"</span>                                                                                                                                        
      grocery_items <span class="token punctuation">[</span>item<span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token keyword">true</span>                                                                                                                     
    <span class="token keyword">when</span> <span class="token string">"N\n"</span>                                                                                                                                        
      grocery_items <span class="token punctuation">[</span>item<span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token keyword">false</span>                                                                                                                    
  <span class="token keyword">end</span>                                                                                                                                                 
<span class="token keyword">end</span>                                                                                                                                                   
puts <span class="token string">"Here's your list:"</span>                                                                                                                              
grocery_items<span class="token punctuation">.</span><span class="token keyword">each</span> <span class="token keyword">do</span> <span class="token operator">|</span> item<span class="token punctuation">,</span> need_for_item <span class="token operator">|</span>                                                                                                         
  puts item <span class="token keyword">if</span> need_for_item <span class="token comment" spellcheck="true">#Aqui aun no entiendo pero supongo que si es true se cumple la sentencia.                                                
</span><span class="token keyword">end</span>    
</code></pre>
<h2 id="arrays-and-hashes">Arrays and Hashes</h2>
<ul>
<li>Podemos usar nested arrays los cuales se llaman multi.dimensional arrays.<br>
<code>childhood_games_played = [["make believe", true], ["tag", false]]</code></li>
<li>Luego para llamar a los juegos debemos usar</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">childhood_games_played <span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span><span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span>
	<span class="token string">"make believe"</span>
childhood_games_played <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span>
	<span class="token string">"tag"</span>
childhood_games_played <span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">]</span>
	<span class="token string">"true"</span>
childhood_games_played <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">]</span>
	<span class="token string">"false"</span>
</code></pre>
<ul>
<li>Los hashes tambien pueden ser nested.<br>
<code>cocktails = {"martini" =&gt; {"vodka" =&gt; true, "gin" =&gt; false}}</code></li>
<li>Luego para llamarlos usamos</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">cocktails<span class="token punctuation">[</span><span class="token string">"martini"</span><span class="token punctuation">]</span><span class="token punctuation">[</span><span class="token string">"vodka"</span><span class="token punctuation">]</span>
	<span class="token keyword">true</span>
cocktails<span class="token punctuation">[</span><span class="token string">"martini"</span><span class="token punctuation">]</span><span class="token punctuation">[</span><span class="token string">"gin"</span><span class="token punctuation">]</span>
	<span class="token keyword">false</span> 
</code></pre>
<ul>
<li>Podemos ordenar los array con el method <strong>.sort</strong><br>
<code>my_array.sort</code> devuelve un array ordenado.</li>
<li>En caso de querer ordenar el array en uso usamos <code>mv_array.sort!</code></li>
<li>Es posible al igual que con each usarlo en block of codes</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">my_array<span class="token punctuation">.</span>sort <span class="token keyword">do</span> <span class="token operator">|</span>a<span class="token punctuation">,</span>b<span class="token operator">|</span> 

	a <span class="token operator">&lt;=</span><span class="token operator">&gt;</span> b <span class="token comment" spellcheck="true">#Diferencia quien esta primero.
</span>	
<span class="token keyword">end</span> 
</code></pre>
<ul>
<li>Para saber la longitud de un array es posible usar los method<br>
<strong>.count</strong><br>
<strong>.length</strong></li>
<li>Para revisar si en el array existe un valor es posible usar el method <strong>.include</strong><br>
<code>first_five_integers.include? 1</code> Es importante usar el ?</li>
<li>Es posible crear un array a partir de otro usando <strong>.map</strong> un buen ejemplo es para calcular si unos numeros de un array son pares o impares.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">my_array <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">2</span><span class="token punctuation">,</span><span class="token number">3</span><span class="token punctuation">]</span>
odd_or_even <span class="token operator">=</span> my_array<span class="token punctuation">.</span>map <span class="token keyword">do</span> <span class="token operator">|</span>element<span class="token operator">|</span>
	element <span class="token operator">%</span> <span class="token number">2</span> <span class="token operator">==</span> <span class="token number">0</span> <span class="token operator">?</span> <span class="token string">"even"</span> <span class="token punctuation">:</span> <span class="token string">"odd"</span>
	<span class="token keyword">end</span>  
</code></pre>
<h2 id="strings">Strings</h2>
<ul>
<li>Se deben colocar las String en <code>""</code> para que ruby pueda identificarlas.</li>
<li>Llamar las variables es diferente que en bash para llamar una variable entre strings usamos #{variable}<br>
<code>puts "Your have #{bank_account} dollars."</code>Sin necesita de cerrar los " podemos incluir la variable e imprimir en una sola linea.</li>
<li>Podemos sumar operaciones matematicas dentro de lo {}<br>
<code>puts "Tiene en total #{banesco + bod}bs. entre todas sus cuentas."</code></li>
<li>Podemos sumar string con string en caso de ser string y integers daria error.</li>
<li>En caso de querer cambiar el string a Capital usamos <strong>.upcase</strong> si fuera a lower seria <strong>.downcase</strong></li>
<li>En caso de dividir una string usamos <strong>.split(" ")</strong> donde el space es el delimitador luego se convertiria en un array.</li>
<li>Un pequeño ejemplo</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">puts <span class="token string">"Insertar una frase"</span>
palabra <span class="token operator">=</span> gets
numero_palabras <span class="token operator">=</span> palabra<span class="token punctuation">.</span><span class="token function">split<span class="token punctuation">(</span></span><span class="token string">" "</span><span class="token punctuation">)</span><span class="token punctuation">.</span>count
puts "<span class="token constant">Tu</span> frase tiene <span class="token comment" spellcheck="true">#{numero_palabras} palabra#{numero_palabras == 1 ? "." : "s."}"
</span></code></pre>
<h2 id="while-loop">While Loop</h2>
<ul>
<li>Repite una seccion del codigo hasta que una condicion sea cierta, para evitar que sea un loop infinito la variable debe cambiar.</li>
<li>La syntax seria while condition do y un end es bueno añadir un contador al final de la sentencia ex: my_integer += 1</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">my_var <span class="token operator">=</span> <span class="token number">10</span>

<span class="token keyword">while</span> my_var <span class="token operator">&lt;</span> <span class="token number">30</span> <span class="token keyword">do</span> 
	puts "my_var <span class="token operator">=</span> <span class="token comment" spellcheck="true">#{my_var}"
</span>	my_var <span class="token operator">+</span><span class="token operator">=</span> <span class="token number">1</span> 
<span class="token keyword">end</span> 
</code></pre>
<ul>
<li>El program block va entre el do y el end.</li>
<li>Es importante saber que si usamos " " no podemos llamar una variable a no ser que usemos el #{}.</li>
<li>loops and arrays: the perfect match.</li>
<li>El until loop es totalmente inverso.</li>
<li>Un ejemplo de ordenar los enteros.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">integers <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>
current_integer <span class="token operator">=</span> <span class="token number">0</span> 
<span class="token keyword">while</span> current_integer <span class="token operator">&lt;</span> <span class="token number">10</span> <span class="token keyword">do</span> 
puts <span class="token string">"Type an integer"</span>
integers<span class="token punctuation">[</span>current_integer<span class="token punctuation">]</span> <span class="token operator">=</span> gets<span class="token punctuation">.</span>to_i
	current_integer<span class="token operator">+</span><span class="token operator">=</span><span class="token number">1</span>
<span class="token keyword">end</span> 

integers<span class="token punctuation">.</span>sort<span class="token punctuation">.</span><span class="token keyword">each</span> <span class="token keyword">do</span> <span class="token operator">|</span>this_int<span class="token operator">|</span>
	puts this_int
<span class="token keyword">end</span> 
</code></pre>
<h2 id="for-loop">For Loop</h2>
<ul>
<li>El For loop es igual al method each.</li>
<li>un ejemplo practico seria.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">bags <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token string">"suitcase"</span><span class="token punctuation">,</span> <span class="token string">"messenger bag"</span><span class="token punctuation">,</span> <span class="token string">"satcher"</span><span class="token punctuation">,</span> <span class="token string">"backpack"</span><span class="token punctuation">]</span>
<span class="token keyword">for</span> bag_types <span class="token keyword">in</span> bags <span class="token keyword">do</span>
	puts bag_type
<span class="token keyword">end</span>
</code></pre>
<ul>
<li>los for loop no solo pueden usarse en una collection es posible usarse en rangos</li>
<li>Existen 2 tipos de rangos Inclusive y Exclusive la diferencia es que en Exclusive se excluye el ultimo valor del rango.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token comment" spellcheck="true">#inclusive range:
</span>	<span class="token keyword">for</span> variable <span class="token keyword">in</span> <span class="token number">1</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token number">4</span> <span class="token keyword">do</span>
		<span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span>
	<span class="token keyword">end</span> 
</code></pre>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token comment" spellcheck="true">#Exclusive range:
</span>	<span class="token keyword">for</span> variable <span class="token keyword">in</span> <span class="token number">1</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token number">4</span> <span class="token keyword">do</span>
		<span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span>
	<span class="token keyword">end</span> 
</code></pre>
<ul>
<li>Es recomendable dejar de usar for loop y usar <strong>.each</strong></li>
</ul>
<h2 id="loop-control">Loop Control</h2>
<ul>
<li>Con el key <strong>next</strong> podemos saltar las demas interacciones del loop y saltar a la proxima iteracion.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">my_var <span class="token operator">=</span> <span class="token number">0</span>
<span class="token keyword">while</span> my_var <span class="token operator">&lt;</span> <span class="token number">10</span> <span class="token keyword">do</span>
	<span class="token keyword">if</span> my_var <span class="token operator">==</span> <span class="token number">3</span> 
		my_var <span class="token operator">+</span><span class="token operator">=</span> <span class="token number">1</span> 
		<span class="token keyword">next</span>
	<span class="token keyword">end</span> 
	puts my_var
	my_var <span class="token operator">+</span><span class="token operator">=</span> <span class="token number">1</span>
<span class="token keyword">end</span>
</code></pre>
<ul>
<li>Creo que salta a una proximo block.</li>
<li>La key <strong>redo</strong> va al comienzo del codigo asi la condicion sea verdadera o falsa.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">my_var <span class="token operator">=</span> <span class="token number">0</span>
<span class="token keyword">while</span> my_var <span class="token operator">&lt;</span> <span class="token number">10</span> <span class="token keyword">do</span>
	puts my_var
	<span class="token keyword">if</span> my_var <span class="token operator">==</span> <span class="token number">3</span> 
		my_var <span class="token operator">=</span> <span class="token number">10</span> 
		<span class="token keyword">redo</span>
	<span class="token keyword">end</span> 
	my_var <span class="token operator">+</span><span class="token operator">=</span> <span class="token number">1</span>
<span class="token keyword">end</span>
</code></pre>
<ul>
<li>Seria como un if exit en bash.</li>
<li>Lo extraño es que el redo seguira corriendo asi el statement del while sea falso…</li>
<li>El redo no le veo mucho sentido.</li>
<li>El key <strong>break</strong> sale del loop inmediatamente y es uno de los mas importantes.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">puts <span class="token string">"Type something to continue. Or nothing to quit"</span>
<span class="token keyword">while</span> a <span class="token operator">=</span> gets <span class="token keyword">do</span>

	<span class="token keyword">if</span> a <span class="token operator">==</span><span class="token string">"\n"</span> 
		<span class="token keyword">break</span>
	<span class="token keyword">end</span> 
	puts a <span class="token comment" spellcheck="true">#Imprime la misma linea vacia.
</span><span class="token keyword">end</span> 
</code></pre>
<ul>
<li>Ejemplo final</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby">total <span class="token operator">=</span> <span class="token number">0</span> 
puts <span class="token string">"Input your numbers"</span> 
<span class="token keyword">while</span> input <span class="token operator">=</span> gets <span class="token keyword">do</span> <span class="token comment" spellcheck="true">#Declaramos 
</span>	<span class="token keyword">if</span> input <span class="token operator">==</span> <span class="token string">"\n"</span> 
		<span class="token keyword">break</span> 
	<span class="token keyword">end</span> 
	total <span class="token operator">=</span> total <span class="token operator">+</span> input<span class="token punctuation">.</span>to_f 
	puts "running total <span class="token operator">=</span> <span class="token comment" spellcheck="true">#{total}" 
</span><span class="token keyword">end</span> 

puts "<span class="token constant">Total</span><span class="token punctuation">:</span> <span class="token comment" spellcheck="true">#{total}" 
</span></code></pre>
<h2 id="methods">Methods</h2>
<ul>
<li>Los Methods son como funtions en otro lenguaje antiguo<br>
<img src="https://i.imgur.com/AipGJrz.png" alt="enter image description here"></li>
<li>Method Example</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">def</span> hello_user 
	puts <span class="token string">"Enter your Name"</span> 
	username <span class="token operator">=</span> gets
	puts <span class="token string">"Hello "</span> <span class="token operator">+</span> username
<span class="token keyword">end</span> 

hello_user <span class="token comment" spellcheck="true">#Llamamos al metodo.
</span></code></pre>
<ul>
<li>Los methods devuelven objects.</li>
<li>En el irb podemos definir los scripts tal cual y cuando cambiemos de 001:0 a 002:1 es porque estamos dentro de un statement.</li>
<li>Por defecto un method puede arrojar un nil pero esto puede cambiar</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">def</span> hello_user 
	puts <span class="token string">"Enter your Name"</span> 
	username <span class="token operator">=</span> gets
	"<span class="token constant">Hello</span> <span class="token comment" spellcheck="true">#{username.chop}." 
</span><span class="token keyword">end</span> 
hello_user
</code></pre>
<ul>
<li>Esta vez debe arrojar el object del username.</li>
<li>Es util cuando un method arroja un boolean.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">def</span> hello_user 
	puts <span class="token string">"Enter your Name"</span> 
	username <span class="token operator">=</span> gets
	<span class="token keyword">if</span> username <span class="token operator">!</span><span class="token operator">=</span> <span class="token string">"\n"</span> 
		"<span class="token constant">Hello</span> <span class="token comment" spellcheck="true">#{username.chop}."
</span>	<span class="token keyword">else</span>
		<span class="token keyword">false</span> 
<span class="token keyword">end</span>
</code></pre>
<p>Ejemplo de unas recetas de comida.</p>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">def</span> get_ingredient
	new_ingredient <span class="token operator">=</span> gets
	<span class="token keyword">if</span> new_ingredient <span class="token operator">!</span><span class="token operator">=</span> <span class="token string">"\n"</span>
		new_ingredient 
	<span class="token keyword">else</span> 
		<span class="token keyword">false</span>
	<span class="token keyword">end</span>
<span class="token keyword">end</span>
ingredients <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span> 
puts <span class="token string">"Input your Ingredients"</span>
<span class="token keyword">while</span> my_ingredient  <span class="token operator">=</span> get_ingredient <span class="token keyword">do</span>  <span class="token comment" spellcheck="true">#Comparamos que sea una string.
</span>	ingredients<span class="token punctuation">[</span>ingredients<span class="token punctuation">.</span>count<span class="token punctuation">]</span> <span class="token operator">=</span> my_ingredient
<span class="token keyword">end</span> 
puts <span class="token string">"Input your instructions"</span>
instructions <span class="token operator">=</span> gets
puts <span class="token string">"Ingredients:"</span>
puts ingredients
puts <span class="token string">"Instructions:"</span>
puts instructions

</code></pre>
<h2 id="methods-continued">Methods Continued</h2>
<ul>
<li>Es posible usar metodos en un argumento.<br>
<img src="https://i.imgur.com/G8BiPcK.png" alt="enter image description here"></li>
<li>Es recomendable declarar el method seguido de declarar la variable que se usara como argumento.</li>
<li>Para doblar un numero seria my_var **  <em>=2</em>*</li>
<li>El yield seria como el punto de stdin en donde el method introduce su resultudado.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">def</span> my_method 
        puts <span class="token string">"executing your code..."</span>
        <span class="token keyword">yield</span>
        puts <span class="token string">"done"</span>
<span class="token keyword">end</span>
my_method <span class="token keyword">do</span>  
        puts <span class="token number">2</span> <span class="token operator">+</span> <span class="token number">2</span> 
<span class="token keyword">end</span> 

<span class="token comment" spellcheck="true">######RESULTADO#########
</span>executing your code<span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span>
<span class="token number">4</span>
done
</code></pre>
<ul>
<li>Ejercicio que multiplica 2 numeros.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">def</span> multiply_this a<span class="token punctuation">.</span> b
	total <span class="token operator">=</span> a <span class="token operator">*</span> b 
	<span class="token keyword">if</span> total <span class="token operator">&lt;</span> <span class="token number">0</span> 
		<span class="token keyword">false</span>
	<span class="token keyword">else</span>
		total
	<span class="token keyword">end</span>
<span class="token keyword">end</span>

user_input <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>
puts <span class="token string">"Input two numbers"</span> 
<span class="token keyword">while</span> user_number <span class="token operator">=</span> gets <span class="token keyword">do</span>
	user_input<span class="token punctuation">[</span>user_input<span class="token punctuation">.</span>count<span class="token punctuation">]</span> <span class="token operator">=</span> user_number<span class="token punctuation">.</span>to_f 
	<span class="token keyword">if</span> user_input<span class="token punctuation">.</span>count <span class="token operator">==</span> <span class="token number">2</span> 
		<span class="token keyword">break</span> 
	<span class="token keyword">end</span>
<span class="token keyword">end</span> 
<span class="token keyword">if</span> result <span class="token operator">=</span> <span class="token function">multiply_this<span class="token punctuation">(</span></span>user_input<span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span><span class="token punctuation">,</span> user_input<span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">)</span> <span class="token comment" spellcheck="true">#Declara una variable en el mismo statement
</span>														<span class="token comment" spellcheck="true">#Arroja los argumentos al method desde un array.
</span>	puts result 
<span class="token keyword">else</span> 
	puts <span class="token string">"Invalid Input"</span>
<span class="token keyword">end</span>
</code></pre>
<h2 id="using-classes">Using Classes</h2>
<ul>
<li>Se podria definir a una clase con una descripcion de un objeto.</li>
<li></li>
</ul>
<p><img src="https://i.imgur.com/lLDtoa4.png" alt="enter image description here"></p>
<ul>
<li>En ruby todo es un object por tanto todo pertenece a una clase.</li>
<li>Array, Hash, y todos los tipos de variables son clases.</li>
<li>Podemos decir que <strong>my_array = [ ] == my_array = Array.new</strong></li>
<li>Las clases pueden contener dos tipos de cosas; variables definitions y method definitiios por ejemplo la class array incluye el method each.</li>
<li>Las instances al parecer representan un objeto en especifico en vez de tipos de objetos.</li>
<li>La mayor ventaja es que puedo tener multiples instancias de una misma clase.<br>
<code>my_first_array = Array.new</code><br>
<code>my_second_array = Array.new</code></li>
<li>Las clases pueden incluir propiedades de otras clases.</li>
<li>Si usamos <strong>.class</strong> revelara a que clase pertenece pero si usamos <strong>.superclass</strong> revelara la clase de quien hereda.<br>
<img src="https://i.imgur.com/IlDo4qI.png" alt="enter image description here"></li>
<li>Vemos que si usamos el 1.class.superclass.superclass.superclass vemos es un Object como todo en ruby.</li>
</ul>
<h2 id="creating-classes">Creating Classes</h2>
<ul>
<li>Para crear una class la syntax seria<br>
<code>class Class_name</code><br>
<code>...</code><br>
<code>end</code></li>
<li>Es importante que la clase este escrita en Mayuscula.</li>
<li>Para inicializar un object es importante que la clase ya estre creada.<br>
<code>my_object = Class_name.new</code></li>
<li>attr_accesor = attribute accesor el cual es un method para crear ins</li>
<li>Ejemplo de como crear una tabla</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">class</span> <span class="token class-name">Table</span> 
	attr_accessor <span class="token symbol">:height</span><span class="token punctuation">,</span> <span class="token symbol">:width</span><span class="token punctuation">,</span> <span class="token symbol">:length</span>
<span class="token keyword">end</span>
</code></pre>
<ul>
<li>el attr_accesor crea method para acceder a la data que le damos como argumento</li>
<li>El accesor crea una instance variable que son las creadas con @variable</li>
<li>Cada vez que creemos clases crearemos instance variable dentro de ellas.</li>
<li>Es importante saber que crea method para acceder a esas instance variables donde ese method corresponde al nombre.</li>
<li>Cada vez que usamos <code>:</code> se crea un <strong>symbol</strong> en ruby.</li>
<li>Podemos crear una class en un archivo y luego llamarla desde irb con <code>irv -r ./table.rb</code></li>
<li>cuando usamos <code>t = Table.new</code> estamos creando una instancia de la clase.</li>
<li>Luego podemos colocar datos en la instancia t siguiendo de la instance variable ex: <code>t.height = 5</code></li>
<li>Es posible extender una Class ya creada usando el class con el nombre de la class y añadiendo lo nuevo dentro.</li>
<li>en este caso la extendemos para introducir un nuevo method.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">class</span> <span class="token class-name">Table</span>
	<span class="token keyword">def</span> cost
		<span class="token variable">@length</span> <span class="token operator">*</span> <span class="token variable">@width</span> <span class="token operator">*</span> <span class="token number">5</span> <span class="token operator">+</span> <span class="token number">4</span> <span class="token operator">*</span> <span class="token variable">@height</span> <span class="token operator">*</span> <span class="token number">2</span> 
	<span class="token keyword">end</span>
<span class="token keyword">end</span>
</code></pre>
<ul>
<li>Vemos como llamamos nuestras variables con @ al ser Instance variables.</li>
<li>Luego podemos llamar a la instancia que llamamos que se llama con el method que definimos al final <strong>t.cost</strong></li>
</ul>
<h2 id="creating-classes-continued">Creating Classes Continued</h2>
<ul>
<li>Es posible definir un initialize method cada vez que instanciamos o instanstiate una class y colocarles unos valores por defecto.</li>
<li>Ejemplo</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">class</span> <span class="token class-name">table</span> 
	<span class="token keyword">def</span> initialize ilength <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">,</span> iwidth <span class="token operator">=</span> <span class="token number">3</span><span class="token punctuation">,</span> iheight <span class="token operator">=</span> <span class="token number">3</span>
		<span class="token variable">@lenght</span> <span class="token operator">=</span> ilength
		<span class="token variable">@width</span> <span class="token operator">=</span> iwidth
		<span class="token variable">@height</span> <span class="token operator">=</span> iheight
	<span class="token keyword">end</span>
<span class="token keyword">end</span>
</code></pre>
<ul>
<li>Es importante saber que estamos extendiendo la class Table de la antigua clase por eso existe @lenght y los otros.</li>
<li>Despues cuando inicializamos la clase con .new tendremos los valores 3 o incluso podemos añadir nuevos valores manteniendo los ordenes.<br>
<img src="https://i.imgur.com/YPgV8g0.png" alt="enter image description here"></li>
<li>Si usamos el private dentro de un method solo sera accesible para la class code no fuera de ella.</li>
<li>Luego si usaramos <strong>my_table.table_top_area</strong> nos daria error al llamar a un method privado.</li>
<li>Por defecto todas las clases heredan de la clase object. en caso de querer heredar de otra usamos</li>
<li><code>class LibraryTable &lt; Table</code> al momento de declarar la clase de esta manera podemos llamar a los private method.</li>
<li>Al igual que el private existe el protected que es usado para comparar al asegurar que el method solo es acedido desde sibling object o child objects</li>
<li>Ejercicio de Cuenta Bancaria.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">class</span> <span class="token class-name">AccountBook</span>
	<span class="token keyword">def</span> initialize 
		<span class="token variable">@ledger</span> <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>
		<span class="token variable">@current_total</span> <span class="token operator">=</span> <span class="token number">0</span> 
	<span class="token keyword">end</span> 
	<span class="token keyword">def</span> add_money amount<span class="token punctuation">,</span> memo <span class="token operator">=</span> <span class="token string">""</span>
		<span class="token variable">@ledger</span><span class="token punctuation">[</span><span class="token variable">@ledger</span><span class="token punctuation">.</span>count<span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token punctuation">[</span>amount<span class="token punctuation">,</span> memo<span class="token punctuation">]</span>
		<span class="token variable">@current_total</span> <span class="token operator">+</span><span class="token operator">=</span> amount
	<span class="token keyword">end</span>
	<span class="token keyword">def</span> subtract_money amount<span class="token punctuation">,</span> memo <span class="token operator">=</span><span class="token string">""</span>
		<span class="token variable">@ledger</span><span class="token punctuation">[</span><span class="token variable">@ledger</span><span class="token punctuation">.</span>count<span class="token punctuation">]</span> <span class="token operator">=</span> <span class="token punctuation">[</span>amount <span class="token operator">*</span> <span class="token operator">-</span><span class="token number">1</span><span class="token punctuation">,</span> memo<span class="token punctuation">]</span>
		<span class="token variable">@current_total</span> <span class="token operator">-</span><span class="token operator">=</span> amount
	<span class="token keyword">end</span>
	
	<span class="token keyword">def</span> printout 
		tab <span class="token operator">=</span> <span class="token number">0</span>
		puts <span class="token string">"Amount:\tMemo:\tTotal:"</span>
		<span class="token variable">@ledger</span><span class="token punctuation">.</span><span class="token keyword">each</span> <span class="token keyword">do</span> <span class="token operator">|</span>line<span class="token operator">|</span>
			tab <span class="token operator">+</span><span class="token operator">=</span> line<span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span>
			puts "<span class="token comment" spellcheck="true">#{line[0]}\t#{line[1]}\t#{tab}"
</span>		<span class="token keyword">end</span>
	<span class="token keyword">end</span>
<span class="token keyword">end</span>
</code></pre>
<h2 id="variable-scope-revisited">Variable Scope Revisited</h2>
<ul>
<li>Existen 4 tipos de Variable
<ul>
<li>local: comienzan con una letra en minuscula, y es solo accesible en el method que la definio</li>
<li>instance: Comienzan con @ pueden accederse en cualquier method de una instancia de una clase</li>
<li>class: Empiezan con doble @@ estan disponible en cualquier instancia y method de la clase.</li>
<li>global: Comienzan con $ y pueden llamarse en cualquier parte del codigo, se usan en general para los settings.</li>
</ul>
</li>
<li>Un ejemplo de local Variables seria.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">class</span> <span class="token class-name">Square</span>

	<span class="token keyword">def</span> initialize 
	 <span class="token variable">@length</span> <span class="token operator">=</span> <span class="token number">10</span> <span class="token comment" spellcheck="true">#Declaramos una instance variable 
</span>	<span class="token keyword">end</span>

	<span class="token keyword">def</span> printout 
		length <span class="token operator">=</span> <span class="token variable">@lenght</span> <span class="token operator">*</span> <span class="token number">2</span> <span class="token comment" spellcheck="true">#Declaramos una variable local que es *2 a la instance variable parecieran iguales pero son diferentes. 
</span>		puts "<span class="token constant">Length</span> <span class="token operator">=</span> <span class="token comment" spellcheck="true">#{length}." 
</span>	<span class="token keyword">end</span>  
<span class="token keyword">end</span> 
</code></pre>
<ul>
<li>Es importante diferencia que las local variables solo estan disponible entre method.</li>
<li>Las global variables son buenas para settings globales.</li>
</ul>
<h2 id="class-methods-and-singletons">Class Methods and Singletons</h2>
<ul>
<li>Recordemos que la instancia de una clase es para un objeto en especifico de una clase las Class Methods hacen referencia a toda la clase util para operar todos los miembros, variables, o database cleanup methods.</li>
<li>Creamos una clase pero esta vez creamos un method llamado self.Nombre-del-metodo-que-queramos luego en cualquier lugar de la class podremos llamar al method.</li>
<li>Para llamar al class method usamos <strong>Class_Name.method_name</strong> ==&gt; Tree.trim</li>
<li>Los Singleton Methods estan definidos para solo un objecto.</li>
<li>Lo definimos luego de crear una variable || objeto luego definimos un metodo con el nombre de la variable seguido del nombre del methodo que creamos.<br>
Ejemplo <code>abc = "abc" ---&gt; def abc.twice</code></li>
<li>Tambien es posible usar una Singleton Class util si solo queremos crear una class importante pero unica.</li>
<li>Existen 2 maneras de crear una Singleton Classes
<ul>
<li>Crear una blank class y operar en ella.</li>
</ul>
</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token comment" spellcheck="true">####Creamos una blank class.
</span><span class="token keyword">class</span> <span class="token class-name">TableCorporation</span>
<span class="token keyword">end</span> 
<span class="token comment" spellcheck="true">##Listo sin nada dentro.
</span><span class="token keyword">class</span> <span class="token operator">&lt;</span><span class="token operator">&lt;</span> <span class="token constant">TableCorporation</span> 
<span class="token comment" spellcheck="true">#Todo lo que este dentro sera una singletons class.
</span><span class="token keyword">end</span> 
<span class="token comment" spellcheck="true"># -OR-
</span><span class="token keyword">class</span> <span class="token class-name">TableCorporation</span>
	<span class="token keyword">class</span> <span class="token operator">&lt;</span><span class="token operator">&lt;</span> <span class="token keyword">self</span> 
	<span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token comment" spellcheck="true">##todo lo que este dentro sera una singletons class.
</span>	<span class="token keyword">end</span>
<span class="token keyword">end</span>
</code></pre>
<pre><code>- Crear una instancia de una clase y extenderla.
</code></pre>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token comment" spellcheck="true">####Creamos una class.
</span><span class="token constant">TableCorporation</span> <span class="token operator">=</span> <span class="token builtin">Object</span><span class="token punctuation">.</span><span class="token keyword">new</span>
<span class="token class-name">class</span> <span class="token operator">&lt;</span><span class="token operator">&lt;</span> <span class="token constant">TableCorporation</span>
<span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span>
<span class="token keyword">end</span> 

</code></pre>
<ul>
<li>Vemos que estamos operandolos methods en una clase porque todo en ruby es un object.</li>
<li>Los attritubes y methods se crear igual que en cualquier otra clase.</li>
<li>Crear una class para envio de paquetes</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token keyword">class</span> <span class="token class-name">Box</span>
	attr_accessor <span class="token symbol">:length</span><span class="token punctuation">,</span> <span class="token symbol">:width</span><span class="token punctuation">,</span> <span class="token symbol">:height</span><span class="token punctuation">,</span> <span class="token symbol">:weight</span><span class="token punctuation">,</span> <span class="token symbol">:distance</span>
	<span class="token keyword">def</span> initialize
	<span class="token variable">@@materials_cost</span> <span class="token operator">=</span> <span class="token number">0.01</span> <span class="token comment" spellcheck="true">#1 cent per square inch
</span>	<span class="token variable">@@rate</span> <span class="token operator">=</span> <span class="token number">00.1</span> <span class="token comment" spellcheck="true"># 1 cent per pount per mile
</span>	<span class="token keyword">end</span> 
	<span class="token keyword">def</span> <span class="token keyword">self</span><span class="token punctuation">.</span>rate<span class="token operator">=</span> rate
	<span class="token variable">@@rate</span> <span class="token operator">=</span> rate
	<span class="token keyword">end</span>
	<span class="token keyword">def</span> <span class="token keyword">self</span><span class="token punctuation">.</span>materials_cost<span class="token operator">=</span> cost
	<span class="token variable">@@materials_cost</span> <span class="token operator">=</span> cost
	<span class="token keyword">end</span>
	<span class="token keyword">def</span> package_cost
	<span class="token punctuation">(</span><span class="token variable">@length</span> <span class="token operator">*</span> <span class="token variable">@width</span> <span class="token operator">*</span> <span class="token number">2</span> <span class="token operator">+</span> <span class="token variable">@length</span> <span class="token operator">*</span> <span class="token variable">@height</span> <span class="token operator">*</span> <span class="token number">2</span> <span class="token operator">+</span> <span class="token variable">@width</span> <span class="token operator">*</span> height <span class="token operator">*</span> <span class="token number">2</span><span class="token punctuation">)</span> <span class="token operator">*</span> <span class="token variable">@@materials_cost</span> <span class="token operator">+</span> <span class="token variable">@weight</span> <span class="token operator">*</span> <span class="token variable">@distance</span> <span class="token operator">*</span> <span class="token variable">@@rate</span> 
	<span class="token keyword">end</span>
<span class="token keyword">end</span>
</code></pre>
<ul>
<li>Crear una instancia de una clase y extenderla.</li>
</ul>
<pre class=" language-ruby"><code class="prism  language-ruby"><span class="token comment" spellcheck="true">####Creamos una class.
</span><span class="token constant">TableCorporation</span> <span class="token operator">=</span> <span class="token builtin">Object</span><span class="token punctuation">.</span><span class="token keyword">new</span>
<span class="token class-name">class</span> <span class="token operator">&lt;</span><span class="token operator">&lt;</span> <span class="token constant">TableCorporation</span>
<span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span><span class="token punctuation">.</span>
<span class="token keyword">end</span> 
</code></pre>