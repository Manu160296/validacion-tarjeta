# "Validación de tarjeta"

##### En este archivo encontraremos:
##### 1.-Breve descripción acerca del proyecto.
##### 2.-Pseudocódigo.
##### 3.-Diagrama de flujo.
***
#### 1.-Breve descripción del proyecto :
###### Este proyecto tiene como principal finalidad la validación de una tarjeta ; la web pedirá al usuario el numero de su tarjeta y esta mandará un mensaje "TARJETA VÁLIDA",en caso de que lo sea y "TARJETA INVÁLIDA",en caso contrario.

***
#### 2.- Pseudocódigo:
###### A continuación voy a presentar el pseudocódigo de mi proyecto , esperando como siempre que cumpla la finalidad de su creación :"Que todos puedan entenderlo"


  ***NOMBRE DEL PROCESO: isValidCard***

***VARIABLES : newArray,lastNumber,number,secondDigit,firstDigit,totalSum***

  ***función*** isValidCard (number)  
  newArray= vacío;  
  ***para*** cada elemento del número proporcionado ***hacer:***  
  * lastNumber = number%10;
  * number = valor absoluto(number/10);  
  ***agregar*** lastNumber a newArray;  **fin**

  ***para*** las posiciones pares de los elementos de newArray ***hacer:***
  * newArray[contador] = newArray[contador] \* 2;  
  * secondDigit=0;  
  * firstDigit=0;  
  ***si*** (newArray[contador] >=10) ***entonces***
  * secondDigit = newArray[contador] % 10;
  * firstDigit =valor absoluto (newArray[contador]/10);  
  ***reemplazando*** newArray[contador] ***por***  
  firstDigit + secondDigit; **fin**  
  totalSum=0;  
  ***para*** todos los elementos de newArray ***hacer***
  totalSum += newArray[contador];  
  ***si*** (totalSum%10)  
  ***retornar*** "TARJETA VÁLIDA";  
  ***si no***  
  ***retornar***  "TARJETA INVÁLIDA";  
  **fin**;    
  ***hacer:***  
  number = valor absoluto ( (***pedir:*** "Ingrese el número de su tarjeta para confirmar validez") );  
  ***mientras*** (number sea falso)
  ***llamar*** isValidCard(number);  
  **fin**

  ***
  #### 3.-Diagramas de flujo:

  ![diagrama tarjeta 1][1]  ![diagrama tarjeta 2][2]

   [1]: assets/docs/diagrama_tarjeta.png
   [2]: assets/docs/diagrama-tarjeta1.png
