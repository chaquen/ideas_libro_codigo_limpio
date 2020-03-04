# Codigo limpio
Aquí encontraras agunas de las ideas del libro Código limpio, manual de estilo para el desarrollo de software

## Capítulo 1 
### La importancia del código
Primero te invito a que leas el primer capítulo el cual, es una perfecta introducción a la importancia de valorar como escribir código limpio, además de adentranos en los conceptos de diversos gurus de nuestra carrera, así que no te puedes saltar ese capítulo, es por tu bien.

## Capítulo 2 
### Nombres con sentido

El nombre de una función, variable, clase debe responder a una serie de cuestiones básicas

-¿Porqué existe?
-¿Qué hace?
-¿Cómo se usa?

Asi que si un nombre requiere un comentario, significa que no esta revelando su cometido
	
	int d; // tiempo transcurrido en días

Debes elegir un nombre que **especifique** lo que mide y la unidad de dicha medida.

	int elapsedTimeDays;
	int daysSinceCreation;
	int daysSinceModification;
	int file AgeInDays;

La elección de nombres debe revelar la intención, facilita considerablemente la comprensión y la modificación del código.

***Lo invito a leer el ejemplo de la página 46,47 donde vera la magia de elegir nombres adecuados ***	
