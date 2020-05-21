## <span style="color:blue; font-family:Times New Roman; ">  **PRACTICA 6. SENSOR DE LUZ CON LDR** </span>

### **Objetivos:**
Aprender a usar una fotocelda LDR como sensor de luz para modificar el brillo de un LED de acuerdo a la intensidad lumínica del entorno.

Una **fotocelda o fotorresistor** es un dispositivo cuya resistencia varía de acuerdo a la luz del entorno. Su valor de resistencia es muy bajo cuando incide luz sobre su superficie y en la oscuridad su resistencia es alta. Como la resistencia varía de acuerdo a la intensidad de luz, la fotocelda se considera como un sensor de luz análogo, por lo tanto, se debe conectar a un pin para lectura análoga de la tarjeta Arduino.

### **Descripción:**
1.	Se conecta los leds intermitentes en los pines digitales 11, 12 y 13 de la placa de Arduino (utilizando su debida resistencia). 
2.	Conectar la fotocelda al pin análogo A0, tenga presente el esquema.

### **Materiales:**
-	1 x Arduino UNO R3
-	1 x Protoboard
-	1 x Led Rojo 5mm
-	4 x resistencia de 220Ω.
-	1 x resistencia de 10KΩ
-	Cables de conexión.
### **Montaje:**
![Imagen montaje]( https://www.geekfactory.mx/wp-content/uploads/2014/11/arduino_con_fotoresistencia_LDR.png)

### **Código para Arduino:**

define ldr A0   
define Led1 11    
define Led2 12    
define Led3 13      
Int Luminicencia;      

**void setup** () {   
Serial.begin(9600);   
  **pinMode** (ldr, INPUT);   
  **pinMode** (Led1, OUTPUT);   
  **pinMode** (Led2, OUTPUT);   
  **pinMode** (Led3, OUTPUT); }   

**void loop** () {   
 Luminicencia= analogRead(ldr);   
   Serial.println ("Lectura Luminicencia (0 a 1023):");   
  Serial.println (Luminicencia);   
  Serial.println ("\n");    
     
  if (Luminicencia < 840 )   {   
    **digitalWrite** (11, HIGH);  
  }   
  else    
  {   
    **digitalWrite** (11, LOW);   
  }   
    
  if (Luminicencia < 700 )  {   
    **digitalWrite** (12, HIGH);   
  }   
  else    
  {   
    **digitalWrite** (12, LOW); }   
  
  if ( Luminicencia < 500 )  {   
    **digitalWrite** (13, HIGH);   
  }    
  else     
  {   
    **digitalWrite** (13, LOW); }     
    delay (10);                  
}   
