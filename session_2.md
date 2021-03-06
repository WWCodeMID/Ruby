Los ingredientes para programar
===

Esta sesión esta dedicada para platicar sobre los elementos esenciales para programar.


Haz un programa en Ruby
---
Antes de comenzar tienes que saber como hacer un programa.

1. Abre tu editor de texto
2. Crea un nuevo archivo
3. Escribe: puts 1+2
4. Guarda el archivo como: elnombrequequieras.**rb**
5. Ejecuta tu programa desde consola ejecutando: **ruby** elnombrequequieras.**rb**

**No pierdas de vista**


Todos archivos que contengan código Ruby deben llevar como extensión **.rb** es súper importante que siempre tengas en cuenta esto porque sino no podremos ejecutar nuestro programa.

Igualmente recuerda que la computadora es súper tonta y que sino la colocas en el directorio donde se encuentra tu archivo (dentro de la terminal/consola) nunca lo va encontrar, entonces recuerda siempre el comando **cd** (change directory - cambia de directorio) agregando la ruta de tu archivo.

Números
---
Te preguntaras que hace **puts**, 1+2 sabemos que es 3. Entonces **puts** simplemente imprime el resultado de la operación que le estamos indicando, es este caso es una simple suma. Mas adelante veras que puede servir para muchas otras cosas.

**Aritmética simple**

Para realizar operaciones aritméticas simples en un programa usamos estos caracteres: +, -, *, /.

Vamos a jugar un poco, escribe en tu programa:

     puts 3 + 4
     puts 9 - 4
     puts 5 * 10
     puts 9 / 2
   
Guarda y corre tu programa ejecutando: ruby elnombrequequieras.**rb**
   
Debes ver como resultado:

     7
     5
     50
     4
   

**Tipos de números**

A pesar de que Ruby te ahorra el trabajo de definir los tipos de datos el identifica cada uno, por ejemplo escribe en tu programa:

     puts 3.0 + 4.0
     puts 9.0 - 4.0
     puts 5.0 * 10.0
     puts 9.0 / 2.0
   
Guarda y corre tu programa ejecutando: ruby elnombrequequieras.**rb**
   
Debes ver como resultado

     7.0
     5.0
     50.0
     4.5
   
Nota que el resultado de la división cuando lo escribimos sin decimales fue **4** pero cuando lo hicimos con decimales fue **4.5**, aquí Ruby esta identificando entre enteros y flotantes (decimales).

Conclusión si tu operación la estas realización con enteros el resultado será entero y si la estas haciendo con flotantes el resultado será flotante.

**Pregunta existencial:** que pasa si sumo un entero con un flotante? Intentalo ;)
   

Letras
---
Así como **puts** nos sirvió para imprimir los resultados de nuestras operaciones, nos servirá para imprimir nuestras letras. Ahora para imprimir una palabra simplemente tenemos que escribir:

     puts "Hola Rubyficadas"
   
Guarda y corre tu programa ejecutando: ruby elnombrequequieras.**rb**

Debes ver como resultado:

     Hola Rubyficadas
   
Todo lo que queramos definir como texto en nuestro programa lo tenemos que escribir entre comillas, pueden ser simples (') o dobles (").

En Ruby un grupo de letras, pueden ser palabras u oraciones completas hasta párrafos, le llamamos **String**.

**Aritmética con palabras**

Así como podemos hacer aritmética con números lo podemos hacer con palabras (Strings) es decir podemos agregar palabras a nuestras palabras o multiplicarlas, vamos a intentar.

Escribe en tu programa:

     puts "Me gusta " + "las zarzamoras"
     puts "Me gusta"+" las zarzamoras"
   
Guarda y corre tu programa ejecutando: ruby elnombrequequieras.**rb**

Debes ver como resultado:

     Me gusta las zarzamoras
     Me gusta las zarzamoras
   
La función del **+** es concatenar (unir) las dos palabras.

**OJO** fíjate como solo esta considerando los espacios dentro de las comillas y no los que están fuera de estas.

Sin embargo hay otra forma mas practica de concatenar palabras, la grandiosa **interpolación**. Para usarla necesitamos esta se representa de esta forma: "En un año hay #{4*12} semanas". Todo lo que se encuentre dentro de los corchetes ({}) tiene que ser código que Ruby pueda entender.

Por ejemplo, escribe en tu programa:
   
     puts "Un día tiene #{24*60} minutos"

Guarda y corre tu programa ejecutando: ruby elnombrequequieras.**rb**

Debes ver como resultado:
   
     Un día tiene 1440 minutos   


Ahora vamos hacer volar tu mente multiplicando Strings.

Escribe en tu programa:

     puts "Somos lo máximo! " * 3
   
Guarda y corre tu programa ejecutando: ruby elnombrequequieras.**rb**

Debes ver como resultado:
   
     Somos lo máximo! Somos lo máximo! Somos lo máximo!
   
Padrísimo! Cuantos ciclos nos podemos ahorrar con esto, no?

*Ten en mente que para multiplicar palabras, la operación debe de ir después del String que quieres multiplicar, es decir no puedes hacer:*

     puts 3 * "Somos lo máximo!"

**Dígitos y números**

Antes de continuar debemos saber la diferencia entre dígitos y números. **12** es un numero y **'12'** es un String de dos dígitos. Vamos a jugar para ver las diferencias.

Escribe en tu programa:
    
     puts  12  +  12
     puts '12' + '12'
     puts '12  +  12'

Guarda y corre tu programa ejecutando: ruby elnombrequequieras.**rb**

Debes ver como resultado:

     24
     1212
     12  +  12
    
Estos ejemplos son muy sencillos, pero sino tienes cuidado de no mezclar números con Strings puedes llegar a tener problemas.

Por ejemplo, escribe en tu programa:

     puts '12' + 12

Guarda y corre tu programa ejecutando: ruby elnombrequequieras.**rb**
    
Debes ver como resultado:

     #<TypeError: no implicit conversion of Fixnum into String>
    
Error! Porque no puedes sumar un numero a un String.

**Comillas**

Otra pregunta existencial, que pasa si dentro de mi String quiero usar carácter comillas? Si estas son las que me ayudan a definir mi String. Para solucionar esto necesitamos escapar caracteres, como? Simplemente agregando una diagonal invertida antes de nuestro carácter.

Por ejemplo, escribe en tu programa:

     puts 'You\'re so sexy ;)'

Guarda y corre tu programa ejecutando: ruby elnombrequequieras.**rb**
    
Debes ver como resultado:

     you're so sexy
    
Lo mismo para las comillas dobles.



Símbolos
---
Los símbolos son una cosa extraña que quizás y en un principio no les encuentres utilidad pero poco a poco veras para que sirve, mientras tanto solo nos interesa saber que existe y como funcionan.

Son como un String pero inmutables, es decir durante la vida de tu programa nunca van a cambiar. Estos se guardan en un lugar especial de la memoria donde el garbage collector (el recolector de basura, encargado de limpiar las cosas que no estas utilizando en tu programa) no puede borrarlas.

Vamos hacer una prueba para comprobar que son inmutables.

Sobre tu terminal/consola escribe el comando: **irb** (este comando nos sirve para poner a nuestra terminal/consola) en modo Ruby, es decir que podemos escribir código Ruby y nos va a entender).

Debes ver como resultado algo así:

     2.0.0-p481 :001 >
    
Ahora escribe:

     :hola_rubyficadas

Debes ver como resultado:

      => :hola_rubyficadas
    
Ahora escribe:
    
     "Hola Rubyficadas".object_id

Debes ver como resultado algo como:

     => 2156454360
    
Si lo volvemos a correr vamos a ver que el resultado es diferente.

Ahora escribe:

     :hola_rubyficadas.object_id
    

Debes ver como resultado algo como:

      => 538408
     
En cambio con un símbolo, si lo volvemos a correr el resultado será el mismo. Esto quiere decir que cada vez que creamos un String estamos ocupando un nuevo espacio en memoria pero cada vez que creamos un Symbol se esta usando el mismo espacio en memoria.     
Variables y asignaciones
---
Hasta ahora todo lo que ponemos para imprimir con puts no lo podemos re-utilizar y cada vez que queremos imprimir "Hola Rubyficadas" tenemos que escribir toda la oración de nuevo. Para no tener que estar escribiendo una y otra vez esto existen las **variables** donde podemos guardar el valor que queramos para usarlo posteriormente.

La forma para declarar una variable es:

     saludo = "Hola Rubyficadas"
    
En Ruby tan simple que solo se necesita definir el nombre de la variable, en este caso: **saludo** es el nombre de la variable y el valor es: "Hola Rubyficadas" que es un String.

A las variables les podemos asignar cualquier valor no solo Strings.

Escribe en tu programa:
    
     var = 'otro ' + 'string'
     puts var

     var = 5 * (1+2)
     puts var
    
Guarda y corre tu programa ejecutando: ruby elnombrequequieras.**rb**

Debes ver como resultado algo como:

     otro string
     15
    
Sin embargo a lo único que no pueden apuntar las variables son a otras variables.

Escribe en tu programa:

     var1 = 8
     var2 = var1
     puts var1
     puts var2

     puts ''

     var1 = 'eight'
     puts var1
     puts var2
    
Guarda y corre tu programa ejecutando: ruby elnombrequequieras.**rb**

Debes ver como resultado algo como:

     8
     8

     eight
     8
    
Lo que paso aquí fue que primero hicimos que var2 apuntara a var1 y realmente apuntaban al **8**. Luego var1 apuntaba a 'eight' pero como var2 realmente no apuntaba a var1, sino a 8 se quedo en 8.

**Constantes**

Las contantes son variables que no cambian su valor, es decir si tu necesitas que una variable siempre tenga el mismo valor a lo largo de la vida de tu programa la puedes definir como una constante:

     LIMITE_DE_CODIFICADAS = 15
    
Hay dos cosas que debemos notar aquí:

1. Necesariamente el nombre de la variable tiene que ir en mayúsculas
2. Le puedes cambiar al valor, aunque no deberías, ya que al final es un variable.

PUTS, GETS and CHOMP
---


**puts** significa *put string* que significa poner un string, no lo olviden.

**gets** significa *get string* que significa obtener un string. Sin embargo gets toma el ENTER que damos para terminar la instrucción. En cambio **chomp** no, este no toma el ENTER por lo que toma correctamente lo que ingresan.

Para usar chomp es necesario poner:

     gets.chomp


Ejercicios
---
1. Haz un programa que solicite el nombre, primer y segundo apellido e saluda al usuario con su nombre completo.
2. Escribe un programa que solicite el numero favorito del usuario. Luego haz que tu programar multiplique por 10 ese numero y finalmente imprime el resultado sugiriendo al usuario que el nuevo numero es mejor.