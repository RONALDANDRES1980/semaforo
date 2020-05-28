## <span style="color:blue; "> **PRACTICA 5: SEMÁFORO DE PEATONES** </span>

### **Objetivo:** 
Construir un semáforo para peatones utilizando dos LEDs y un zumbador.   

### **Descripción:** 
 1. Se conecta el LED rojo al pin digital 13 y el LED de color verde al pin digital 12 de la placa de Arduino 
2. La patilla larga del LED debe ser conectada al voltaje positivo (ánodo) y la corta al voltaje
negativo (cátodo) pasando por la resistencia. 
3. El zumbador se conecta debidamente polarizado al pin digital 11.

### **Materiales:**   
-	1 x Arduino UNO R3 
-	1 x Protoboard 
-	1 x Led Rojo 5mm 
-	1 x Led Verde 5mm 
-	1 zumbador 
-	2 x resistencias de 220Ω.
-	Cables de conexión. 

### **Montaje:**

![imagenmontaje](img/diseño_practica_5.png)



### **Código para Arduino:**  

define LedR 13  
define LedV 12   

**void setup** () {       
**pinMode** (LedR,OUTPUT);    
**pinMode** (LedV,OUTPUT);    
**pinMode** (Zum,OUTPUT);    

**digitalWrite**(LedR,LOW);   
**digitalWrite**(LedV,LOW);   
**digitalWrite**(Zum,LOW   
}    

**void loop** () {    
**digitalWrite**(LedR,HIGH);   
delay(5000);   
**digitalWrite**(LedR,LOW);    
  
**digitalWrite**(LedV,HIGH);    
for (int i=0; i&lt;10; i++){     
**digitalWrite**(Zum,HIGH);    
delay(200);    
**digitalWrite**(Zum,LOW);    
delay(500);    
}    
**digitalWrite**(LedV,LOW);    
} 

### **MAQUETA** 

![Imagenmontaje](img/Maqueta_5.png)


