## <span style="color:blue;">  **PRACTICA 4: CRUCE DE SEMAFOROS**</span>

### **Objetivos:**
Programar el circuto para el cruce de dos semaforos.

### **Descripción:**
1.	Se conecta los Leds rojo, amarillo y verde a los pines digitales 2,3 y 4 del primer semáforo de la placa de Arduino (utilizando su debida resistencia). 
2.	Se conecta los Leds rojo, amarillo y verde a los pines digitales 6,7 y 8 del primer semáforo de la placa de Arduino (utilizando su debida resistencia).
3.	La patilla larga del Led debe ser conectada al voltaje positivo (ánodo) y la corta al voltaje negativo (cátodo) pasando por la resistencia. 

### **Materiales:**
-	1 Tarjeta Arduino UNO R3 
-	1 Protoboard 3
-	2 Led Rojo 5mm 
-	2 Led Amarillo 5mm 
-	2 Led Verde 5mm 
-	1 Pulsador 
-	6 Resistencias de 330 ohms  
-	1 Cable USB para ARDUINO 

### **Montaje:**

![imagen montaje](img/diseño_cruce_N_practica_4.png)



### **Código para Arduino:**

define LedR 2	        define LedA 3	     define LedV 4    
define LR 6	        define LA 7	      define LV 8     

**void setup** () {   
  **pinMode** (LedR, OUTPUT);    
  **pinMode** (LedA, OUTPUT);     
  **pinMode** (LedV, OUTPUT);    
  **pinMode** (LR, OUTPUT);    
  **pinMode** (LA, OUTPUT);   
  **pinMode** (LV, OUTPUT);    
   
  **digitalWrite** (LedR, LOW); //Nos aseguramos que los LED inician apagados   
  **digitalWrite** (LedA, LOW);    
  **digitalWrite** (LedV, LOW);    
  **digitalWrite** (LR, LOW);    

  **digitalWrite** (LA, LOW);    
  **digitalWrite** (LV, LOW);}    

**void loop** (){    
  **digitalWrite** (LedR, HIGH);    
  **digitalWrite** (LV, HIGH);   
  delay (5000); // retardo de 5 s     
  
  **digitalWrite** (LedA, HIGH);     
  **digitalWrite** (LA, HIGH);    
  delay (2000); // retardo de 2s    
    
  **digitalWrite** (LedA, LOW);    
  **digitalWrite** (LedR, LOW);         
  **digitalWrite** (LA, LOW);    
  **digitalWrite** (LV, LOW);    
  
  **digitalWrite** (LedV, HIGH);    
  **digitalWrite** (LR, HIGH);    
  delay (5000); // retardo de 5s    
  
  **digitalWrite** (LedA, HIGH);    
  **digitalWrite** (LA, HIGH);    
  delay (2000); // retardo de 2s    

  **digitalWrite** (LedA, LOW);     
  **digitalWrite** (LedV, LOW);    
  **digitalWrite** (LA, LOW);    
  **digitalWrite** (LR, LOW); }   
  
## **Maqueta**

![imagen montaje](img/Maqueta_practica_4.jpeg)
