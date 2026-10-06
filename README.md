Hugo Gavilán, Juanjo Prades e Ingrid Albert
Lenguaje: Go
Reto B: bucles


1. ¿Cómo se declara la variable o el contador? 

En Go, a diferencia de lenguajes más dinámicos como Python, el lenguaje es de tipado estático (necesita saber qué tipo de dato es cada variable). Sin embargo, Go ofrece varias formas de declarar un contador, siendo una de ellas muy ágil: 

En el código que vemos (for i := 1; i <= 5; i++), usamos el operador de declaración corta: :=. 

Cómo se escribe: i := 1 

Qué significa: Este operador especial hace dos cosas a la vez: crea la variable i y le asigna el valor 1. 

Inferencia de tipos: Aunque Go necesita saber el tipo de dato, al usar := el compilador es inteligente (infiere el tipo). Al ver que le asignas un 1, Go decide automáticamente que i será de tipo entero (int). Restricción: Este operador := solo se puede usar dentro de funciones. 

2. ¿Cómo se muestra información por consola? 

Usando un paquete de la librería estándar  fmt (que es la abreviatura de format). 

Primero importamos el paquete con: import fmt.  

Luego ya podemos usar la funcion fmt.Println(), y en nuestro caso usamos: fmt.Println(i). 

 

3. ¿Cómo se delimitan los bloques de código? Comparadlo con la indentación de Python. 

En Go, los bloques se delimitan con llaves {}, mientras que en Python se delimitan mediante la indentación. 

Go: usa {} obligatoriamente y la llave de apertura debe estar en la misma línea.  
Python: usa : e indentación para definir los bloques.  
En Go, la indentación solo facilita la lectura y gofmt la organiza automáticamente. 
 

4.⁠ ⁠¿Qué símbolos o palabras cambian respecto al ejemplo en Python?  

Al comparar la impresión de los números del 1 al 5, encontramos cambios significativos en el vocabulario y los símbolos que usa cada lenguaje: Desaparece while e in range: En Python, podrías usar while i <= 5: o for i in range(1, 6):. En Go, la palabra while no existe; todo se hace con for. Tampoco existe una función como range() para generar la secuencia de números; en su lugar, Go especifica mecánicamente desde dónde empezar, hasta dónde llegar y cómo avanzar. El separador punto y coma (;): En la misma línea del bucle, Go utiliza ; para separar las tres fases del ciclo (inicialización i := 1, condición i <= 5, e incremento i++). En Python, esto no se usa en absoluto en las estructuras de control. El operador de declaración corta (:=): Para crear el contador dentro del bucle, Go introduce este símbolo combinado de dos puntos e igual. En Python, la creación de la variable en el for es implícita o se usa un simple =. El operador de incremento (++): Para sumar uno al contador en cada vuelta, Go utiliza ++ (que significa "suma 1 a la variable"). Este símbolo no existe en Python; si usaras un bucle while en Python, tendrías que escribir explícitamente i += 1 o i = i + 1. Apertura de bloque (: vs {): Como comentamos antes, Python anuncia lo que va dentro del bucle con dos puntos :. Go los sustituye por la apertura de llaves {. La función de imprimir (print vs fmt.Println): La palabra clave print de Python se transforma en la llamada completa a la librería de formato: fmt.Println. 

 

5. ¿Qué decisiones o repeticiones se mantienen? Explicad el algoritmo en castellano, sin usar código. 

La lógica se mantiene: un contador, una condición que se comprueba antes de cada vuelta y un incremento. El algoritmo es este: empezar con un contador que vale 1; mientras el contador sea menor o igual que 5, mostrar su valor por pantalla y sumarle 1; cuando el contador pase de 5, dejar de repetir. 