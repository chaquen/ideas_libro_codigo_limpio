# Código limpio
Aquí encontraras agunas de las ideas del libro Código limpio, manual de estilo para el desarrollo de software

## Capítulo 1 
### La importancia del código
Primero te invito a que leas el primer capítulo el cual, es una perfecta introducción a la importancia de valorar como escribir código limpio, además de adentrarnos en los conceptos de diversos gurus de nuestra carrera, así que **no** te puedes saltar ese capítulo, es por tu bien.

## Capítulo 2 
### Nombres con sentido

El nombre de una función, variable, clase debe responder a una serie de cuestiones básicas

- ¿Porqué existe?
- ¿Qué hace?
- ¿Cómo se usa?

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

Debemos evitar dejar pistas falsas que dificulten el significado del código usando nombres que se alejen de lo que pretendemos por ejemplo hp que podrimos intrepretarlo en un contexto dado como hipotenusa, pero podria no serlo.
No utiice nombres que puedan tener na intepretación en el contexto como algo intrinseco pero que no lo es por ejemplo para un grupo de cuentas no use *accountList* al menos que realmente sea una lista de elementos ya que *List*
como bien sabemos tiene un significado propio como estructura de datos, en caso de no ser una lista podria usar *accountGroup*, *bounchOfAccounts*, o simplemente *accounts*
Evite nombres similares con variaciones mínimas  

### Realizar distinciones con sentido

Debemos buscar nombres claros que permitan distiguir cada variable, manteniendo un sentido claro que nos de a entender su significado, en ese caso debemos evitar usar nombres de variables como **var1**, **var2** o similares, de igual modo usar prefijos para diferencia una variable de la otra si no tiene sentido por ejemplo usar **zork** y **theZork** o **customer** y **theCustomer** ¿cúal seria la diferencia?,¿cúal realmenete represenat lo que queremos decir?, por eso debemos ser concretos a la hora de hacer distinciones entre variables.

### Usar nombres que se puedan usar 

Evitemos usar nombres de variables que no podamos pronunciar, evitando hacer acronimos o variantes de nombres que no podamos identificar a simple vista, para que reinventar el idioma, recuerda que programar es una actividad social.

### Usar nombres que se puedan buscar

Debemos usar nombres de variables o contantes que sean faciles de buscar, es mas fácil buscar **MAX_CLASS_PER_STUDENT** que el número **7**, evite usar numeros donde podria ir el nombre de una constante, evite nombres simples de una sola letra, al menos de que el contexto lo permita por ejemplo, en ciclos internos donde una simple **i** no representar mayor probabilidad de cambio, pero si dentro de este ciclo usted requiere una comparación o un cambio con respecto a **algo** debe procurar usar nombres que permitan saber a simple inspección que es ese **algo**


### Evitar codificaciones

Ya tenemos con aprender la codificación de cada lenguaje como para aprender una propia que usan nuestros programas, entonces evite usar palabras extrañas o "códificación" para que aprender otro lenguaje.

### Notación hungara

Aunque en muchos lenguajes, fue de gran utilidad, las herramientas y los lenguajes actuales, permiten identificar errores por el tipado de las variables, asi que hoy en dia es una forma de escritura que es inecesdario e irrelevante.

### Prefijos de miembros

Resulta innecesario usar prefijos para identificar miembros de clases, en muchas ocaciones son ignorados por los programadores y son un indicio de código antiguo.

### Interfaces e implementaciones

Existen casos espciales para codificar interfaces o clases abstractas, pór ejemplo intefaz que genere formas, en ese caso es preferible no usar adornos para dicha interfaz que implementaré mediante una clase, entonces para que usar **IShapeFactory** si puedo usar **ShapeFactory**, **I** es información innecesaria, a la hora de implementar puedo usar nombres como **ShapeFactoryImp** o **CShapeFactory**, en lugar de codificar la interfaz.

### Evitar asignaciones mentales

No hay jnada mejor que leer código claro y fácil de entender, por este motivo evite usar en bucles letras que puedan causar problemas a la hora de leer, y no solo menta allí para que intenar crear acronimos cuando puede ser claro, recuerde **la claridad es lo que importa**. 

### Nombres de clases

Las clases y objetos deben tener **nombres o frases de nombre** como *Customer, WikiPage, Account y AddressParser*
evite palabras como *Manager, Processor, Data o Info*, **el nombre de una clase NO debe ser un VERBO**.

### Nombre de métodos

**Los métodos DEBEN tener nombre de VERBOS**, así como los métodos de acceso, modificación deben tener su valor **get**, **set** 

### No exceda con el atractivo

Si los nombres tienden a usar terminos coloquiales, o jergas, por favor **evitelos**, opte por la mayor claridad antes que el entretenimiento.

### Una palabra por concepto


