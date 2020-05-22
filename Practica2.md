## <span style="color:blue; ">  **PRACTICA 2: ENCENDER Y APAGAR UN LED CON UN PULSADOR**</span>

### **Objetivos:**
Encender y apagar un LED utilizando un botón pulsador que envié una señal que Arduino registre y decida si enciende o apaga el LED.

### **Descripción:**
1.	Colocar el LED en el protoboard.
2.	Conectar una resistencia de 220ohms o 330ohms al lado plano del LED.
3.	En la parte del lado redondo del LED (Ánodo +) se conecta un cable que ira a un pin digital de la tarjeta Arduino, en nuestro caso el pin 4.
4.	Se coloca el botón en la protoboard.
5.	Al igual que con el LED se conecta una resistencia al botón, pero en este caso tienes que ser de 5K ohm o 10K ohm
6.	En el otro extremo del botón se conecta un cable que conecte a una línea horizontal de la protoboard, en nuestro caso la roja.
7.	Ahora se conectará un cable que vaya del pin 8 de la Arduino a la protoboard, se tiene que situar entre la conexión de la resistencia y el botón.
8.	Lo siguiente es hacer la conexión de alimentación y tierra del Arduino, para eso vamos a la sección de alimentación de nuestro Arduino, sacamos un cable que vaya de 5v hasta la línea roja de nuestro Arduino, donde anteriormente se había conectado un cable que provenía del botón, eso es para la alimentación.
9.	Por ultimo sacamos un cable de cualquiera de las dos tierras que trae Arduino para que vaya a la tierra (la línea azul donde conectamos la resistencia del LED).

### **Materiales:**
-	1 Tarjeta ARDUINO UNO
-	1 Cable USB para Arduino
-	1 Tarjeta Protoboard
-	1 Diodo LED común (cualquier color)
-	1 Pulsador
-	Cables de conexión. 
-	1 Resistencia de 220 ohms ó 330 ohms
-	1 Resistencia de 10K

### **Montaje:**
![Imagen montaje](img/diseño_practica_2.png)   
Montaje del circuito con el uso de botones para encender y apagar

### **Código para Arduino:**

define LedR 4   
define Boton 8    
Estado=0;    

**void setup** ()  {    
  **pinMode** (LedR, OUTPUT); //Led     
  **pinMode** (Boton, INPUT); // Botón  
  
**void loop** () {    
  Estado= digitalRead (Boton); // leer estado    
   If ((Boton==HIGH) {    
    **digitalWrite** (LedR, HIGH); //enciende Led    
  }   
else {   
    **digitalWrite** (LedR, LOW); //apaga el Led  }   
}    
