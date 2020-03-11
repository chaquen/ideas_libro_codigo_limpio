# [Código limpio](https://github.com/chaquen/ideas_libro_codigo_limpio/blob/master/Codigo%20LImpio.pdf)
Aquí encontraras agunas de las ideas del libro Código limpio, manual de estilo para el desarrollo de software


## Capítulo 1 
### La importancia del código
Primero te invito a que leas el primer capítulo el cual, es una perfecta introducción a la importancia de valorar como escribir código limpio, además de adentrarnos en los conceptos de diversos gurus de nuestra carrera, así que **no** te puedes saltar ese capítulo, es por tu bien.

## Capítulo 2 
### Nombres con sentido

El nombre de una función, variable, clase debe responder a una serie de cuestiones básicas

- **¿Porqué existe?**
- **¿Qué hace?**
- **¿Cómo se usa?**

Asi que si un nombre requiere un comentario, significa que no esta revelando su cometido
	
	int d; // tiempo transcurrido en días

Debes elegir un nombre que **especifique** lo que mide y la unidad de dicha medida.

	int elapsedTimeDays;
	int daysSinceCreation;
	int daysSinceModification;
	int file AgeInDays;

La elección de nombres debe revelar la intención, facilita considerablemente la comprensión y la modificación del código.

**Lo invito a leer el ejemplo de la página 46,47 donde vera la magia de elegir nombres adecuados**	

### Evitemos la desinformación

Debemos evitar dejar pistas falsas que dificulten el significado del código usando nombres que se alejen de lo que pretendemos por ejemplo *hp* que podrimos intrepretarlo en un contexto dado como *hipotenusa*, pero podria no serlo.
No utiice nombres que puedan tener na interpretación en el contexto como algo intrinseco pero que no lo es, por ejemplo para un grupo de cuentas no use *accountList* al menos que realmente sea una **lista** de elementos ya que *List* como bien sabemos tiene un significado propio como estructura de datos, en caso de no ser una lista podria usar *accountGroup*, *bounchOfAccounts*, o simplemente *accounts*.
Evite nombres similares con variaciones mínimas  

### Realizar distinciones con sentido

Debemos buscar nombres claros que permitan distiguir cada variable, manteniendo un sentido claro que nos de a entender su significado, en ese caso debemos evitar usar nombres de variables como **var1**, **var2** o similares, de igual modo usar prefijos para diferencia una variable de la otra si no tiene sentido por ejemplo usar **zork** y **theZork** o **customer** y **theCustomer** *¿cúal seria la diferencia?*, *¿cúal realmenete representa lo que queremos decir?*, por eso debemos ser concretos a la hora de hacer distinciones entre variables.

### Usar nombres que se puedan usar 

Evitemos usar nombres de variables que no podamos pronunciar, evitando hacer acrónimos o variantes de nombres que no podamos identificar a simple vista, para que reinventar el idioma, recuerda que programar es una actividad social.

### Usar nombres que se puedan buscar

Debemos usar nombres de variables o contantes que sean faciles de buscar, es mas fácil buscar **MAX_CLASS_PER_STUDENT** que el número **7**, evite usar numeros donde podria ir el nombre de una constante, evite nombres simples de una sola letra, al menos de que el contexto lo permita por ejemplo, en ciclos internos donde una simple **i** no representar mayor probabilidad de cambio, pero si dentro de este ciclo usted requiere una comparación o un cambio con respecto a **algo** debe procurar usar nombres que permitan saber a simple inspección que es ese **algo**


### Evitar codificaciones

Ya tenemos con aprender la codificación de cada lenguaje como para aprender una propia que usan nuestros programas, entonces evite usar palabras extrañas o "códificación" para que aprender otro lenguaje.

### Notación hungara

Aunque en muchos lenguajes, fue de gran utilidad, las herramientas y los lenguajes actuales, permiten identificar errores por el tipado de las variables, asi que hoy en dia es una forma de escritura que es innecesaria e irrelevante.

### Prefijos de miembros

Resulta inútil usar prefijos para identificar miembros de clases, en muchas ocaciones son ignorados por los programadores y son un indicio de código antiguo.

### Interfaces e implementaciones

Existen casos especiales para codificar interfaces o clases abstractas, pór ejemplo intefaz que genere formas, en ese caso es preferible no usar adornos para dicha interfaz que implementaré mediante una clase, entonces para que usar **IShapeFactory** si puedo usar **ShapeFactory**, **I** es información innecesaria, a la hora de implementar puedo usar nombres como **ShapeFactoryImp** o **CShapeFactory**, en lugar de codificar la interfaz.

### Evitar asignaciones mentales

No hay nada mejor que leer código claro y fácil de entender, por este motivo evite usar en bucles letras que puedan causar problemas a la hora de leer, y no solomente allí para que intentar crear acrónimos cuando puede ser claro, recuerde **la claridad es lo que importa**. 

### Nombres de clases

Las clases y objetos deben tener **nombres o frases de nombre** como *Customer, WikiPage, Account y AddressParser*
evite palabras como *Manager, Processor, Data o Info*, **el nombre de una clase NO debe ser un VERBO**.

### Nombre de métodos

**Los métodos DEBEN tener nombre de VERBOS**, así como los métodos de acceso, modificación deben tener su valor **get**, **set** 

### No exceda con el atractivo

Si los nombres tienden a usar términos coloquiales, o jergas, por favor **evítelos**, opte por la mayor claridad antes que el entretenimiento.

### Una palabra por concepto

Elija *una* palabra por cada concepto abstracto y *manténgala*, por ejemplo, es confuso usar *fetch*, *retrieve*, *get* como métodos equivalentes en clases distintas, un léxico coherente es una gran ventaja para los programadores que quieran usar su código.

### No haga juego de palabras

No use palabras que puedan tomar un concepto distinto, por ejemplo en lugar de usar la palabra *add* que se puede interpretar como sumar o agregar dependiendo del contexto, en reemplazo puede usar *insert* o *append* que tienen un significado similar pero que no podrá tener un significado distindo al de add que se puede interpretar de otra forma, con esto facilitas la comprensión del código, **queremos que el autor sea el responsable de transmitir el significado, no un módelo académico que exija investigar el significado mostrado**

### Usar nombres der dominios de soluciones

Recuerda que los lectores de tu código son programadores, asi que puedes usar términos informaticos, algoritmos, nombres de patrones, términos matemáticos, no es necesario extraer todos los nombres del dominio del problema, evita que el colega tenga que preguntar el significado de cada nombre cuando lo que aplica es un concepto que ya conoce.

### Añadir contextos con sentido

Para entender esta premisa lo invito a leer la pagina 56, con los ejemplos *Listado 2.1 y 2.2*, donde se muestra la imporancia del contexto de una variable y como al reorganizar el código es mas sencillo dar un contextoe identificar mas fácil el mismo, con lo que nos evitamos usar prefijos, aunque si es necesario no esta mal, pero debemos recordar que la organización de nuestro código es de vital importancia para entenderlo a la hora de leerlo.

### No añadir contextos innecesarios

Para que usar prefijos inutiles, que requerira recordar y usar en cualquier instancia, los nombres simples, crotos cuando lo ameritan y precisos son el objetivo de cualquier nombre.

## Funciones

Lo invito a leer los ejemplos mostrados en *Listado 3.1*, *Listado 3.2* y *Listado 3.3*, vera una fomar elegante de escribir funciones y le dara una noción de la importancia de escribir funciones breves, concisas y que permitan una rapida lectura, exiten dos reglas a la hora de escribir funciones

1.	Las funciones deben ser de tamaño reducido.
2.	Deben ser todavía mas reducidas

### Bloques y sangrado

Evite bloques *if,else,while* que impliquen un tamaño *excesivo*  y que albergue estructuras anidadas, resultara mas fácil que el bloque invoque una función, lo cual le dara un valor documental mas fácil de interpretación, remitase a los ejemplos del *Listado 3.1*, *Listado 3.2* y *Listado 3.3*.

### Hacer una cosa

***LAS FUNCIONES SOLO DEBEN HACER UNA COSA, DEBEN HACERLO BIEN Y DEBE SER LO ÚNICO QUE HAGAN***

Creamos funciones para descompones conceptos más amplios en un conjunto de pasos en el siguienet nivel de abstracción.


### Un nivel de abstracción por función

Procure que las instrucciones de la función se encuentren en el mismo nivel de abstracción.

### Leer código de arriba hacia abajo: la regla descendente










